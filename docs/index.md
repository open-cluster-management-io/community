# Multicluster architecture

Open Cluster Management consists of several multicluster components, which are used to access and manage your clusters. Learn more about the architecture in the following sections, then follow the links to more detailed documentation.

The Open Cluster Management project was started to bring together the various aspects of managing Kubernetes clusters into an integrated solution comprised of loosely coupled building blocks. Here are some example Multicluster APIs that are part of the project today:

- Define API for cluster registration independent of cluster CRUD lifecycle.
- Define API for work distribution across multiple clusters.
- Define API for dynamic placement of content and behavior across multiple clusters.
- Define API for policy definition to ensure desired configuration and security settings are auditable or enforceable.
- Define API for distributed application delivery across many clusters and the ability to deliver ongoing updates.
- Define API to collect cluster and application health metrics and alerts across multiple clusters.


Learn more about the following components

* Hub cluster
* Managed cluster
* Cluster lifecycle
* Application lifecycle
* Governance and risk

## Hub cluster

The _hub_ cluster is the common term that is used to define the central controller that runs in a {product-title} cluster.
From the hub cluster, you can access the console and product components, as well as APIs such as the `rcm-api`, which handles API requests related to cluster lifecycle management, which is defined later in this topic.

The hub cluster aggregates information from multiple clusters by using an asynchronous work request model.
With a graph database, the hub cluster maintains the state of clusters and applications that run on it.
The hub cluster also uses `etcd`, a distributed key value store, to store the state of work requests and results from multiple clusters, and provides a set of REST APIs for the various functions that it supports.

## Managed cluster

The managed cluster is the term that is used to define additional clusters with the Klusterlet, which is the agent that initiates a connection to the {product-title} hub cluster.
The managed cluster receives and applies requests, then returns the results.


## Cluster lifecycle

_cluster lifecycle_ defines the process of creating, importing, and managing clusters across public and private clouds.
From the hub cluster console, you can view an aggregation of all cluster health statuses, or view individual health metrics.
You can upgrade managed Red Hat Openshift clusters individually or in bulk, as well as destroy any Red Hat Openshift clusters that you created from your hub cluster.

## Application lifecycle

_application lifecycle_ defines the processes that are used to manage application resources on your managed clusters.
A multi-cluster application uses a Kubernetes specification, but with additional automation of the deployment and lifecycle management of resources to individual clusters.
A multi-cluster application allows you to deploy resources on multiple clusters, while maintaining easy-to-reconcile service routes, as well as full control of Kubernetes resource updates for all aspects of the application.


## Governance and risk

Governance and risk is the term used to define the processes that are used to manage security and compliance from a central interface page.
After you configure a {product-title} hub cluster and a managed cluster, you can view and create policies with the Red Hat Advanced Cluster Management policy framework.