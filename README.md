
## Open Cluster Management

Welcome! The open-cluster-management.io project is focused on enabling end to end visiblity and control across your Kubernetes clusters.

Please read the [MISSION.md](MISSION.md) statement for more information.

![image](assets/acm-arch.jpg)

There are a number of key use cases that are enabled by this project.

### Cluster & Application visibility on Kubernetes.

* Search, find, and modify any Kubernetes resource across the set of managed clusters.

### Provisioning, configuration, upgrade and decommission lifecycle of Kubernetes clusters

* Use the graphical console to identify, isolate, and resolve issues
impacting distributed workloads using dynamic search.
* Quickly troubleshoot and resolve issues across the set of managed clusters.

Cluster management in the current versioin has largely relied on the Cluster Registry project from Kubernetes. There is work underway to define a more current/up to date API for Cluster inventory and registration. Jump in and get involved with this process in one of the following repositories:

* https://github.com/open-cluster-management/api
* https://github.com/open-cluster-management/registration
* https://github.com/open-cluster-management/work

### Delivery, upgrade and configuration of applications on Kubernetes clusters

* Centrally create, update, and delete Kubernetes clusters across multiple
private and public clouds
* Automatically deploy applications to specific clusters by subscribing
to different workload (resource) channels, such as GitHub, Helm
repository, ObjectStore, and resource templates.

The application model defines a Kubernetes-first way of describing the application. Your existing Kubernetes apps or `kustomized` apps can be adapted with the addition of a few new objects: `Channel`, `Subscription`, and `PlacementRule`. Changes made to the app are then easily delivered to managed clusters based on the dynamic placement engine.

The following repositories describe the underlying API and controllers for the app model:

* https://github.com/open-cluster-management/multicloud-operators-subscription
* https://github.com/open-cluster-management/multicloud-operators-placementrule
* https://github.com/open-cluster-management/multicloud-operators-subscription-release
* https://github.com/open-cluster-management/multicloud-operators-channel

There is also a demonstrations available at https://github.com/open-cluster-management/demo-subscription-gitops .

### Governance, Risk and Compliance (GRC) across Kubernetes clusters

* Use prebuilt security and configuration controllers to enforce policy
on Kubernetes configuration, identity and access management (IAM),
Center for Internet Security (CIS), and certificate management across
your clusters.
* Use the governance and risk dashboard to view and manage the
number of security risks and policy violations in all of your clusters
and applications.

Policy controllers allow the declarative expression of a desired condition that can be audited or enforced against a set of managed clusters. `Policies` allow you to drive cross-cluster configuration or validate that certain configuration explicitly does not exist.

Several example policies are available under https://github.com/open-cluster-management/deploy/tree/master/resources/policies

And you can define your own policy controller using the following example: https://github.com/open-cluster-management/multicloud-operators-policy-controller


## Getting Started

The open-cluster-management.io project has been productized in new product offering *Red Hat Advanced Cluster Management for Kubernetes* (see [product reference](https://www.redhat.com/en/technologies/management/advanced-cluster-management)).

Documentation is available under https://github.com/open-cluster-management/rhacm-docs/blob/doc_stage/summary.md

Take a look a few of the followiing videos to learn more:

*  **Red Hat Kubernetes Multicloud Management** on Tech Field Day's YouTube channel:  https://www.youtube.com/watch?v=Xo9FI8RdnBo