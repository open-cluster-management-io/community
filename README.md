
## Open Cluster Management

Welcome! The open-cluster-management.io project is focused on enabling end-to-end visibility and control across your Kubernetes clusters.

Please read the [MISSION.md](MISSION.md) statement for more information.

The open-cluster-management architecture uses a hub - agent model. The hub centralizes control of all the managed clusters. An agent, which we call the klusterlet, resides on each managed cluster to manage registration to the hub and run instructions from the hub.


![image](assets/ocm-arch.png)

There are a number of key use cases that are enabled by this project.

### Cluster registration

The API and controllers provide the function for cluster registration and manifests delivery to clusters. Simple core functions connect clusters, such as the klusterlet, to the hub. Other components run on this base. The following repositories describe the API and controllers for registration:

* https://github.com/open-cluster-management/api
* https://github.com/open-cluster-management/registration
* https://github.com/open-cluster-management/work

### Delivery, upgrade, and configuration of applications on Kubernetes clusters

* Centrally create, update, and delete Kubernetes clusters across multiple private and public clouds.
* Automatically deploy applications to specific clusters by subscribing to different workload (resource) channels, such as GitHub, Helm repository, ObjectStore, and resource templates.

The application model defines a Kubernetes-first way of describing the application. Your existing Kubernetes apps or `kustomized` apps can be adapted with the addition of a few new objects: `Channel`, `Subscription`, and `PlacementRule`. Changes made to the app are then easily delivered to managed clusters based on the dynamic placement engine.

The following repositories describe the underlying API and controllers for the app model:

* https://github.com/open-cluster-management/multicloud-operators-subscription
* https://github.com/open-cluster-management/multicloud-operators-placementrule
* https://github.com/open-cluster-management/multicloud-operators-subscription-release
* https://github.com/open-cluster-management/multicloud-operators-channel

There are demonstrations available at https://github.com/open-cluster-management/demo-subscription-gitops .

### Governance, Risk and Compliance (GRC) across Kubernetes clusters

* Use prebuilt security and configuration controllers to enforce policy on Kubernetes configuration, identity and access management (IAM), Center for Internet Security (CIS), and certificate management across your clusters.
* Use the governance policy framework provides governance capability to gain visibility, and drive remediation for various security and configuration aspects to help meet such enterprise standards.

Policy controllers allow the declarative expression of a desired condition that can be audited or enforced against a set of managed clusters. `Policies` allow you to drive cross-cluster configuration or validate that certain configuration explicitly does not exist.

See [Governance Policy Framework](https://github.com/open-cluster-management/governance-policy-framework) for more details.

### Deployment images

The open-cluster-management project uses `quay.io` to host deployment images. These images might not contain the latest changes. Following a merged pull request, please wait up to an hour for the images to be updated.

### Community meetings

The community meets on a bi-weekly cadence on Thursday at 15:30 UTC.

Meeting Agenda and Topics can be found here: https://github.com/open-cluster-management/community/projects/1.
  
  Meeting dial-in details, meeting notes and agendas are announced and published to the [open-cluster-management mailing list on Google Groups](https://groups.google.com/g/open-cluster-management).

### Get connected

See the following options to connect with the community:

 - [Website](https://open-cluster-management.io)
 - [Slack](https://kubernetes.slack.com/archives/C01GE7YSUUF)
 - [Mailing group](https://groups.google.com/g/open-cluster-management)
 - [Community meetings](https://github.com/open-cluster-management/community#community-meetings)
 - [YouTube channel](https://www.youtube.com/channel/UC7xxOh2jBM5Jfwt3fsBzOZw)
