# General Technical Review - Open Cluster Management / Sandbox

- **Project:** Open Cluster Management
- **Project Version:** v1.0.0
- **Website:** https://open-cluster-management.io/
- **Date Updated:** 2025-8-7
- **Template Version:** v1.0
- **Description:** A lightweight and extensible multi-cluster Kubernetes management tool

## Day 0 - Planning Phase

### Scope

* Describe the roadmap process, how scope is determined for mid to long term features, as well
  as how the roadmap maps back to current contributions and maintainer ladder?

  The roadmap is managed in github projects https://github.com/orgs/open-cluster-management-io/projects/2.
  The issue will be at first tagged as enhancement, and put in the backlog. In the Bi-weekly community meeting,
  we will discuss the scope and the priority of the enhancement.  An enhancement will require an enhancement
  proposal in https://github.com/open-cluster-management-io/enhancements if it involves API update or changes
  of multiple components, in which the graduation plan for this enhancement needs to be identified. Commonly
  a contributor needs to own at least one feature or enhancement to become a maintainer. The details of contributor
  ladder is here https://github.com/open-cluster-management-io/community/blob/main/CONTRIBUTOR_LADDER.md

* Describe the target persona or user(s) for the project?

  The target users of the project are those who have multiple Kubernetes clusters and want to manage them easily,
  and also those who provide Kubernetes cluster management platforms

* Explain the primary use case for the project. What additional use cases are supported by the project?

  1. Administrators are able to manage and monitor multiple Kubernetes clusters in a centralized control plane
  2. Users are able to deploy their workload across multiple clusters.
  3. Users are able to define a cluster selection criteria to deploy different workloads.
  4. Users are able to easily extend the control plane by adding more management functionality across multiple clusters.

* Explain which use cases have been identified as unsupported by the project.

  Provisioning/lifecycle management of Kubernetes clusters is not the scope of this project.

* Describe the intended types of organizations who would benefit from adopting this project. (i.e. financial services, any software manufacturer, organizations providing platform engineering services)?  
  
  - Entities, e.g. financial institutions, internet companies, with many Kubernetes clusters.
  - Vendors that provide platform engineering services.

* Please describe any completed end user research and link to any reports.

  - AppsCode held a webinar on "Managing Many Clusters using Open Cluster Management" on 15th June 2023.
  https://appscode.com/blog/post/monthly-review-june-2023/#managing-many-clusters-using-open-cluster-management
  - Alibaba published a document on their user experience with kubefed and why they moved to OCM on Sep 22, 2021.
  https://cloudnativenow.com/features/the-next-kubernetes-frontier-multicluster-management/ 

### Usability

* How should the target personas interact with your project?

  - [CLI](https://github.com/open-cluster-management-io/clusteradm): For users who have multiple clusters to manage, they
  use the clusteradm CLI tool to interact with OCM.io for deploying resources and managing clusters.

  - [SDK-GO](https://github.com/open-cluster-management-io/sdk-go) and [Addon-Framework](https://github.com/open-cluster-management-io/addon-framework):
  For users who provide a cluster management platform, they use sdk-go and addon-framework to extend OCM.io’s capabilities.

* Describe the user experience (UX) and user interface (UI) of the project.

  OCM's UX is mainly built around `clusteradm` and a collection of CRDs. There is also a web UI in the [lab repo](https://github.com/open-cluster-management-io/lab/tree/main/dashboard), but it is in the alpha phase and not yet ready for production use.

* Describe how this project integrates with other projects in a production environment.

  - [ArgoCD](https://github.com/open-cluster-management-io/addon-contrib/tree/main/argocd-agent-addon): OCM integrates
  ArgoCD by deploying an agent addon to managed clusters, enabling automated GitOps-based application synchronization and management.
  - [Kueue](https://github.com/open-cluster-management-io/addon-contrib/tree/main/kueue-addon): OCM integrates Kueue by installing
  a scheduler addon on managed clusters, providing unified batch workload scheduling and resource management across clusters.
  - [Fluid](https://github.com/open-cluster-management-io/addon-contrib/tree/main/fluid-addon): OCM integrates Fluid by deploying
  its runtime via an addon, enabling distributed data caching and acceleration capabilities in managed clusters.
  - [Open-Telemetry](https://github.com/open-cluster-management-io/addon-contrib/tree/main/open-telemetry-addon): OCM
  integrates Open-Telemetry by deploying its operator through an addon, allowing centralized observability and telemetry data
  collection across clusters.

### Design

* Explain the design principles and best practices the project is following.

  - hub-spoke architecture: the hub component is lightweight to let users set instructions to the spoke via CRD mechanism,
  and the spoke agent acts based on the hub’s instructions.
  - Extensible: another design principle of the projects is to keep the core components as simple and lightweight as possible,
  but with extension points to easily add customized functionality.

* Outline or link to the project's architecture requirements? Describe how they differ for Proof of Concept, Development, Test and Production environments, as applicable.

  The OCM architecture consists of a hub-spoke model documented at https://open-cluster-management.io/docs/concepts/architecture/.

  For different environments:
  - **Proof of Concept**: Single hub cluster with 1-3 spoke clusters, minimal resource allocation (2 CPU, 4GB RAM per hub component)
  - **Development**: Similar to PoC but with additional development addons and potentially multiple hub clusters for testing
  - **Test**: Multi-hub setup with various addon configurations to test different scenarios and upgrade paths
  - **Production**: High availability hub clusters with proper resource allocation, backup/restore procedures, and monitoring across potentially hundreds of managed clusters

* Define any specific service dependencies the project relies on in the cluster. 

  OCM relies on kubernetes as the control plane, utilizing CRDs to host APIs.

* Describe how the project implements Identity and Access Management.  

  OCM does not implement an IAM component, it leverages IAM integrated with kubernetes.

* Describe how the project has addressed sovereignty.

  OCM leverages CRDs in the Kubernetes to store API resources. The hub clusters (kubernetes) can be deployed
  in different locations to address data sovereignty.

* Describe any compliance requirements addressed by the project.  

  OCM has a policy add-on component that can integrate with Open Policy Agent or Kyverno to manage compliance
  policies across multiple clusters. Details are documented here https://open-cluster-management.io/docs/getting-started/integration/policy-controllers/

* Describe the project’s High Availability requirements.  

  OCM control plane is based on the Kubernetes control plane. The controller of OCM hub and agent on the spoke cluster
  can run in multiple replicas with leader election.
  
  In addition, there is also a requirement that OCM hub clusters can be recovered upon disaster, which needs API
  backup/restore and agents’ connection switch among kubernetes clusters. How to meet this requirement is documented
  in https://github.com/open-cluster-management-io/ocm/tree/main/solutions/multiplehubs

* Describe the project’s resource requirements, including CPU, Network and Memory.  

  OCM has controllers on the hub cluster, and agents on spoke clusters. Each has its own CPU/memory requirements.
  The CPU/memory of the hub and agent can be set in ClusterManager/Klusterlet API or using clusteradm.
  OCM requires the spoke cluster to be able to reach the API server of the hub cluster directly or via HTTP proxy.

* Describe the project’s storage requirements, including its use of ephemeral and/or persistent storage.  

  OCM uses CRDs to store API resources, it leverages kubernetes and underlying kubernetes etcd for data storage.

* Please outline the project’s API Design:
    * Describe the project’s API topology and conventions
  
      OCM has mainly 4 aspects of APIs for 4 basic function areas in multicluster management:
      - Cluster related: managedcluster, managedclusterset etc
      - Manifest delivery: manifestwork
      - Scheduling: placement, placementscore
      - Addon related: managedclusteraddon, clustermanagementaddon, addontemplate.
      - And operator API (clustermanager and klusterlet) to manage components in OCM.

      The API design follows the API conventions defined at https://github.com/open-cluster-management-io/api/blob/main/docs/api-conventions.md

    * Describe the project defaults

      OCM defaults include secure hub-spoke communication via mTLS, least-privilege RBAC, and automatic certificate rotation with 24-hour expiry.
      Default resource limits are set conservatively for hub components (500m CPU, 2Gi memory) and can be customized via ClusterManager/Klusterlet APIs.

    * Outline any additional configurations from default to make reasonable use of the project

      For production use, administrators should:
      - Configure high availability with multiple replicas for hub components
      - Set up proper resource requests/limits based on cluster scale
      - Enable addon frameworks for policy management, observability, and application lifecycle management
      - Configure backup/restore procedures for disaster recovery scenarios

    * Describe any new or changed API types and calls \- including to cloud providers \- that will result from this project
    being enabled and used

      OCM introduces several CRDs in the cluster.open-cluster-management.io API group:
      - ManagedCluster, ManagedClusterSet for cluster lifecycle
      - ManifestWork for resource deployment to managed clusters
      - Placement, PlacementDecision for cluster selection and scheduling
      - ManagedClusterAddon, ClusterManagementAddon for addon lifecycle
      OCM does not make direct calls to cloud providers - it operates through standard Kubernetes APIs.

    * Describe compatibility of any new or changed APIs with API servers, including the Kubernetes API server

      All OCM APIs are implemented as standard Kubernetes CRDs, ensuring full compatibility with any conformant Kubernetes API server.
      We maintain compatibility with Kubernetes versions from 1.24+ and test against multiple Kubernetes distributions.

    * Describe versioning of any new or changed APIs, including how breaking changes are handled 

      A new or changed API would introduce an API version upgrade which would need API migration taking more than 1 release.
      The document https://github.com/open-cluster-management-io/api/blob/main/docs/development.md#api-upgrade-flow describes
      the general flow we follow for API upgrades.

    * Describe the project’s release processes, including major, minor and patch releases.

      The release process is defined here https://github.com/open-cluster-management-io/community/blob/main/RELEASE.md

### Installation

* Describe how the project is installed and initialized, e.g. a minimal install with a few lines of code or does it require more complex integration and configuration?  

  The project can be installed in minutes using a command-line tool for a minimal setup, while also offering more configurable installation methods for production environments.
  A minimal install, which sets up a hub cluster and registers a spoke cluster, is achieved with the clusteradm CLI tool. This provides a "few lines of code" experience:
  Initialize the Hub Cluster: On your designated hub cluster, run:
  ```
  clusteradm init
  ```
  Join the Spoke Cluster: On your spoke cluster, use the token from the previous step to install the agent and register:
  ```
  clusteradm join --hub-token <token-from-previous-command> --hub-apiserver <hub-server-url> --cluster-name <my-spoke-cluster>
  ```
  Accept the Spoke Cluster: On your hub cluster, accept the spoke cluster joining request:
  ```
  clusteradm accept --clusters <my-spoke-cluster>
  ```
  For more complex production integrations, we provide official Helm charts that allow for detailed configuration of
  ingress, high availability, resource requirements, and other enterprise-grade settings.
  ```
  helm repo add ocm https://open-cluster-management.io/helm-charts
  helm repo update
  helm search repo ocm
  helm install
  ```

  * Install cluster manager

    ```
    helm install cluster-manager  --version <version> ocm/cluster-manager --namespace=open-cluster-management --create-namespace
    ```

  * Install klusterlet

    ```
    helm install klusterlet --version <version> ocm/klusterlet \
    --set klusterlet.clusterName=<cluster name> \
    --set-file bootstrapHubKubeConfig=<the bootstrap kubeconfig file of hub cluster> \
    --namespace=open-cluster-management \
    --create-namespace
   ```

* How does an adopter test and validate the installation?

  An adopter can test and validate the installation through a series of checks and a simple end-to-end test:
  Verify Agent and Controller Status:
  On the hub cluster, check that the OCM controller pods are running:
  ```
  kubectl get pods -n open-cluster-management
  kubectl get pods -n open-cluster-management-hub
  ```
  On the spoke cluster, check that the Klusterlet agent pods are running:
  ```
  kubectl get pods -n open-cluster-management
  kubectl get pods -n open-cluster-management-agent
  ```

  Validate Cluster Registration: The most important validation is ensuring the spoke cluster has successfully
  registered with the hub.

  On the hub cluster, run the following command. The output should list your spoke cluster with a Managed status
  of true and an Available status that becomes true after a minute.
  ```
  kubectl get managedclusters
  ```

  Perform an End-to-End Workload Test: To confirm the entire system is working, deploy a simple application from
  the hub to the spoke:
  - Create a ManifestWork YAML file on the hub that defines a simple workload (e.g., an Nginx deployment) and targets
  your managed cluster.
  - Apply it to the hub: `kubectl apply -f my-manifest-work.yaml`
  - Check the status of the ManifestWork on the hub to ensure it was applied successfully.
  - Finally, connect to the spoke cluster and verify that the Nginx pod is running (kubectl get pods). This confirms
  that the hub can successfully dispatch work to the managed cluster.

### Security

* Please provide a link to the project’s cloud native [security self assessment](https://tag-security.cncf.io/community/assessments/).

Self-assessment: https://github.com/open-cluster-management-io/ocm/blob/main/SELF_ASSESSMENT.md

* Please review the [Cloud Native Security Tenets](https://github.com/cncf/tag-security/blob/main/community/resources/security-whitepaper/secure-defaults-cloud-native-8.md) from TAG Security.
    * How are you satisfying the tenets of cloud native security projects?
  
      - Managed clusters isolation: Components running on a managed cluster are restricted to accessing only their own resources on the hub, preventing
      unauthorized interactions between clusters.
      - Managed clusters credential free: The hub cluster does not need/store the managed clusters credentials.
      - Double Opt-In Handshake for Cluster Registration: A mutual authentication process during cluster registration, requiring explicit approval from
      both the hub and the managed cluster.

    * Describe how each of the cloud native principles apply to your project.  

      - Secure by Default: OCM establishes a secure communication channel between the hub and spoke clusters using mutual TLS (mTLS).
      The registration process ensures that only authenticated and authorized spoke clusters (via a bootstrap token and subsequent certificate signing)
      can connect to the hub. No insecure ports are exposed, and all API interactions are subject to Kubernetes RBAC.
      - Least Privilege: The principle of least privilege is deeply embedded in OCM's architecture. The agent running on
      a managed cluster, known as the Klusterlet, operates with the minimal set of permissions required for its core functions.
      It can apply most kubernetes resources as defined by ManifestWork objects dispatched from the hub, others CustomeResourceDefinition
      to be managed need the user to grant permission explicitly. And any additional permissions needed for add-on features, such as policy
      inspection or application monitoring, must be granted explicitly through separate, scoped ClusterRoleBindings. This prevents the agent
      from having overly broad permissions and limits the potential impact of a compromise.
      - Defense in Depth: OCM employs a multi-layered security model:
      - Network: mTLS encrypts and authenticates all hub-spoke traffic.
      - API: Kubernetes RBAC on both the hub and spoke clusters controls access to all OCM resources.
      - Workload: OCM agents and add-ons run in dedicated namespaces with scoped ServiceAccounts.
      - Never Trust, Always Verify (Zero Trust): The hub and spoke clusters operate on a zero-trust model. A spoke cluster must go
      through a secure registration and certificate approval process. Every API request from the Klusterlet to the hub is authenticated
      via its client certificate, and every dispatch of work from the hub to the spoke is verified and applied by the agent based on its specific permissions.
      - Security as Code: The entire desired state of the managed fleet—including workload deployments, configurations, and
      security RBAC resources(role, rolebinding)—is represented by declarative Kubernetes-style API objects (ManifestWork, Placement).
      This enables users to manage their fleet’s security posture through GitOps workflows, providing versioning, auditing, and automated control.

    * How do you recommend users alter security defaults in order to "loosen" the security of the project? Please link to any documentation the project has written concerning these use cases.  
  
      We do not recommend or document methods to "loosen" the security of the project, as our defaults are designed to be secure. However,
      OCM is highly configurable; in some cases, users need to grant Klusterlet agent permissions to manage their resources. We recommend users
      only grant permissions with the least privilege, referencing the documentation permission setting for work agent. For purposes like testing, users
      can grant sufficient privileges to the Klusterlet agent that could intentionally create a less secure configuration.

      These actions require deliberate and explicit configuration by a cluster administrator. Our documentation focuses on how to configure
      RBAC for specific use cases, not on how to weaken security.

* Security Hygiene
    * Please describe the frameworks, practices and procedures the project uses to maintain the basic health and security of the project.

      The OCM project maintains strong security hygiene through several automated and procedural safeguards:
      - Vulnerability Scanning: We enabled GitHub security scanning to scan our code for known vulnerabilities (CVEs) automatically.
      - Dependency Management: We use Dependabot to monitor our Go module and container base image dependencies, automatically
      creating pull requests for security updates.
      - Secure Coding Practices: All code submissions require pull requests with reviews from CODEOWNERS. Branch protection
      rules are enabled to enforce these reviews and require CI checks to pass before merging.
      - Private Vulnerability Reporting: We maintain a security page with a clear, private process for security researchers
      to report vulnerabilities to the project maintainers.

    * Describe how the project has evaluated which features will be a security risk to users if they are not maintained by the project?

    The ManifestWork API feature was designed to dispatch/manage Kubernetes resources on the managed cluster. Since it can dispatch/manage any resources,
    the work-agent might need wide permissions for the managed clusters. To mitigate the risk, we ensured that:
    - The agent on the spoke cluster to apply the manifests has admin permission, instead of cluster-admin, so that it can apply most Kubernetes resources.
    - For some specific resources, like some CustomResourceDefinitions, users need to explicitly grant permission to the work agent referencing the documentation permission setting for work agent
    - Users can delegate manifest application to a specific identity on the spoke cluster, further sandboxing the operation, see dynamic identity authorization.

* Cloud Native Threat Modeling
    * Explain the least minimal privileges required by the project and reasons for additional privileges. 
  
      OCM requires a minimal set of privileges on both the hub and the managed cluster to function.

      On the Hub Cluster (during registration):
      - Permission to create a Certificate Signing Request (CSR) to obtain a client certificate for secure communication.
      - Permission to read the secret containing the bootstrap credentials.

      On the Hub Cluster (post-registration):
      - Permission to watch ManifestWork objects within its dedicated cluster namespace.
      - Permission to create events and update its ManagedCluster status.
      - Permission to create/update leases for heartbeating.

      On the Managed Cluster:
      - Permission to apply/manage the resources specified in a ManifestWork. This is the most powerful permission and is the core of OCM's functionality.
      - Additional privileges are required only for OCM add-ons, which run as separate agents. For instance, the policy add-on needs permissions
      to inspect various resources on the managed cluster to check for compliance. These privileges are granted explicitly when the add-on is
      enabled and are scoped to the add-on's specific ServiceAccount.

    * Describe how the project is handling certificate rotation and mitigates any issues with certificates.
  
      OCM implements automatic, seamless certificate rotation for the Klusterlet agent and the addons’ agents.
      The client certificate used by the Klusterlet/addon to authenticate with the hub has a 24-hours expiry.

      The Klusterlet continuously monitors its own certificate. When a predefined threshold is met (e.g., 80% of its lifetime has passed), it will:
      - Generate a new private key on the managed cluster.
      - Create a new CSR on the hub cluster.
      - The hub’s registration controller automatically approves this CSR for a known and valid cluster.
      - The Klusterlet retrieves the newly signed certificate and begins using it for all communication.
      - This automated process mitigates the risk of cluster communication failure due to expired certificates and requires no manual intervention.

    * Describe how the project is following and implementing [secure software supply chain best practices](https://project.linuxfoundation.org/hubfs/CNCF\_SSCP\_v1.pdf)

      OCM is committed to securing its software supply chain and aligns with the best practices outlined by the CNCF.
      - Secure Source Code: We enforce DCO sign-offs on all commits and use protected branches with mandatory PR reviews from official maintainers in our GitHub organization.
      - Secure Builds: Our build pipelines run in isolated, ephemeral environments via GitHub Actions. All build and release processes are defined as code within the repository, ensuring they are transparent and auditable.
      - Secure Artifacts:
      - Digital Signatures: All official OCM container images are signed using Cosign and the Sigstore project. This allows users to verify that the images they deploy were created by our official build pipeline and have not been tampered with.
      - Software Bill of Materials (SBOM): We generate a SPDX-formatted SBOM for every container image we release. This SBOM is attached to the container image as a signed Cosign attestation, providing a verifiable inventory
      of all our software components and their dependencies.

      All official container images are uploaded to https://quay.io/organization/open-cluster-management with security scanning enabled.
      All charts are uploaded to https://artifacthub.io/packages/search?org=open-cluster-management&sort=relevance&page=1, which provides the community with a trusted, versioned, and verifiable source to deploy the OCM components,
      ensuring they are using official project artifacts.

## Day 1 - Installation and Deployment Phase

### Project Installation and Configuration

* Describe what project installation and configuration look like.
  - Install doc: https://open-cluster-management.io/docs/getting-started/installation/
  - Install cluster manager: https://github.com/open-cluster-management-io/ocm/tree/main/deploy/cluster-manager/chart/cluster-manager
  - Install klusterlet: https://github.com/open-cluster-management-io/ocm/blob/main/deploy/klusterlet/chart/klusterlet/README.md

### Project Enablement and Rollback

* How can this project be enabled or disabled in a live cluster? Please describe any downtime required of the control plane or nodes. 

  Open Cluster Management is a foundational component, and it cannot be enabled/disabled in a live cluster.
  Users can only cut off the connection between hub and spoke by following this doc
  https://open-cluster-management.io/docs/concepts/cluster-inventory/managedcluster/#cluster-removal. No downtime required.

* Describe how enabling the project changes any default behavior of the cluster or running workloads.  

  OCM does not change any behavior of the cluster or running workloads

* Describe how the project tests enablement and disablement.  

  OCM does not support being enabled/disabled in a live cluster.

* How does the project clean up any resources created, including CRDs?

  Open Cluster Management cleans up resources when the managed cluster is deleted.
  The process is described at: https://open-cluster-management.io/docs/getting-started/installation/register-a-cluster/#detach-the-cluster-from-hub

### Rollout, Upgrade and Rollback Planning

* How does the project intend to provide and maintain compatibility with infrastructure and orchestration management tools like Kubernetes and with what frequency?

  We upgrade the k8s.io dependencies to the latest version in each release, for example: https://github.com/open-cluster-management-io/ocm/blob/v1.0.0/go.mod#L30-L39

* Describe how the project handles rollback procedures. 

  OCM handles rollbacks the same as upgrades, but needs to specify a lower version: https://open-cluster-management.io/docs/getting-started/administration/upgrading/

* How can a rollout or rollback fail? Describe any impact to already running workloads.  

  If a rollout or rollback fails, the spoke cluster may lose connection with the hub and cannot be managed anymore. The already running
  workloads will keep running, but will not be managed by the hub and their status will not be reported back to the hub.

* Describe any specific metrics that should inform a rollback.  

  Clusteradm provides commands to check the cluster info after upgrade and rollback: https://open-cluster-management.io/docs/getting-started/administration/upgrading/
  The ManagedCluster status will also reflect whether a cluster is available or not after the upgrade.

* Explain how upgrades and rollbacks were tested and how the upgrade-\>downgrade-\>upgrade path was tested.  

  Users should run `clusteradm upgrade` on the test environment before upgrading in the production environment.

* Explain how the project informs users of deprecations and removals of features and APIs.  

  We will log issues in the community for features/API deprecations and removal plans, add them to the roadmap, and inform users in community meetings and Slack channels as well.

* Explain how the project permits utilization of alpha and beta capabilities as part of a rollout.

  The project follows the API upgrade flow https://github.com/open-cluster-management-io/api/blob/main/docs/development.md#api-upgrade-flow to rollout from alpha to beta.
  Feature gates from alpha to beta follow a standard lifecycle:
  https://open-cluster-management.io/docs/getting-started/administration/featuregates/ 
