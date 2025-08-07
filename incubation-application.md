WORK IN PROGRESS | WORK IN PROGRESS | WORK IN PROGRESS

# Review Project Moving Level Evaluation
- [x] I have reviewed the TOC's [moving level readiness triage guide](https://github.com/cncf/toc/blob/main/operations/dd-toc-guide.md#initial-triageevaluation-prior-to-assignment), ensured the criteria for my project are met before opening this issue, and understand that unmet criteria will result in the project's application being closed.

# Open Cluster Management (OCM) Incubation Application
v1.6
This template provides the project with a framework to inform the TOC of their conformance to the Incubation Level Criteria. 

Project Repo(s): https://github.com/open-cluster-management-io/ocm/
Project Site:  https://open-cluster-management.io/
Sub-Projects:
 - https://github.com/open-cluster-management-io/api/
 - https://github.com/open-cluster-management-io/clusteradm/
 - For a full list of sub-projects see our [GOVERNANCE](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md#project-core) file

Communication: https://kubernetes.slack.com/channels/open-cluster-mgmt

Project points of contacts:
- [Qiu Jian](https://github.com/qiujian16), jqiu@redhat.com
- [Mike Ng](https://github.com/mikeshng), ming@redhat.com

- [ ] (Post Incubation only) [Book a meeting with CNCF staff](http://project-meetings.cncf.io) to understand project benefits and event resources. 

## Incubation Criteria Summary for Open Cluster Management (OCM)

### Application Level Assertion

- [x] This project is currently Sandbox, accepted on 20211109, and applying to Incubation.
- [ ] This project is applying to join the CNCF at the Incubation level.

### Adoption Assertion

_The project has been adopted by the following organizations in a testing and integration or production capacity:_
* Appscode
* eBay
* SpectroCloud
* Alibaba
* Red Hat

Please see our [ADOPTERS](https://github.com/augustrh/ocm/blob/main/ADOPTERS.md) file for full use cases and details
Additonal non-public adopters are available on request.

## Application Process Principles

### Suggested

N/A

### Required

- [x] **Engage with the domain specific TAG(s) to increase awareness through a presentation or completing a General Technical Review.**
  - This was completed and occurred on 20-JAN-2022 TAG-Runtime meeting, and can be discovered at https://www.youtube.com/watch?v=g6sWygYKuK8

<!-- (Project assertion goes here) --> 

- [x] **TAG provides insight/recommendation of the project in the context of the landscape**
  - This was done in the meeting above as well as in the more recent TAG-Runtime occurred on 06-MAR-2025: https://www.youtube.com/watch?v=ex3vdlCDPXw

<!-- (Project assertion goes here) --> 

- [x] **All project metadata and resources are [vendor-neutral](https://contribute.cncf.io/maintainers/community/vendor-neutrality/).**
  - Yes, OCM avoids vendor lock-in by using APIs that are not tied to any cloud providers or proprietary platforms.

<!-- (Project assertion goes here) --> 

- [x] **Review and acknowledgement of expectations for [Sandbox](https://sandbox.cncf.io) projects and requirements for moving forward through the CNCF Maturity levels.**        
  - Met during Project's application on 28-SEP-2023.
  - Onboarding Issue https://github.com/cncf/sandbox/issues/227/

<!-- (Project assertion goes here) --> 

- [ ] **Due Diligence Review.**

Completion of this due diligence document, resolution of concerns raised, and presented for public comment satisfies the Due Diligence Review criteria.

- [x] **Additional documentation as appropriate for project type, e.g.: installation documentation, end user documentation, reference implementation and/or code samples.**
  - OCM [documentation](https://open-cluster-management.io/docs/) covers the installation, user guide, developer guides, and user scenarios. It also has a list of blog posts https://open-cluster-management.io/blog/.
<!-- (Project assertion goes here) --> 

## Governance and Maintainers

Note: this section may be augmented by the completion of a Governance Review from the Project Reviews subproject.

### Suggested

- [x] **Governance has continuously been iterated upon by the project as a result of their experience applying it, with the governance history demonstrating evolution of maturity alongside the project's maturity evolution.**

Governance document is found [here](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md)

We have been following other successful CNCF projects models to lead us to the linked one. We will continuously update as we move ahead and adjust to ensure they remain clear and current. We've maintained additional information across our website and provide below some basic examples of those:

Examples of iterations:
- Updated the contributor ladder: https://github.com/open-cluster-management-io/community/pull/187
- Updated the meeting times: https://github.com/open-cluster-management-io/community/pull/188 

- [x] **Clear and discoverable project governance documentation.**

Found in our [GOVERNANCE](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md) document.

<!-- (Project assertion goes here) --> 

- [x] **Governance is up to date with actual project activities, including any meetings, elections, leadership, or approval processes.**

The governance document is current and recently updated. We also have a detailed [CONTRIBUTORS](https://github.com/open-cluster-management-io/ocm/blob/main/CONTRIBUTING.md) guide which covers specifics around contributing and approvals and processes for it. We have regular updates of new contributors and maintainers, for example: https://github.com/open-cluster-management-io/community/pull/190 

<!-- (Project assertion goes here) --> 

- [x] **Governance clearly documents [vendor-neutrality](https://contribute.cncf.io/maintainers/community/vendor-neutrality/) of project direction.**

We regularly review the CNCF vendor-neutrality documentation and ensure we match all the requirements. Additionally we align closely and contribute to the [SIG Multicluster APIs](https://multicluster.sigs.k8s.io/) to ensure we always remain vendor neutral and 100% based on community standards.

<!-- (Project assertion goes here) --> 

- [x] **Document how the project makes decisions on leadership, contribution acceptance, requests to the CNCF, and changes to governance or project goals.**

Documented in our [Governance](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md) document.

<!-- (Project assertion goes here) --> 

- [x] **Document how role, function-based members, or sub-teams are assigned, onboarded, and removed for specific teams (example: Security Response Committee).**

Documented in our [Governance](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md) document.

We also maintain and active [Slack channel](https://kubernetes.slack.com/channels/open-cluster-mgmt) where members can actively collaborate and ensure clarity for on-boarding and governance.

<!-- (Project assertion goes here) --> 

- [x] **Document a complete maintainer lifecycle process (including roles, onboarding, offboarding, and emeritus status).**

Defined in on [contributor ladder](https://github.com/open-cluster-management-io/community/blob/main/CONTRIBUTOR_LADDER.md)

<!-- (Project assertion goes here) --> 

- [x] **Demonstrate usage of the maintainer lifecycle with outcomes, either through the addition or replacement of maintainers as project events have required.**

All maintainer lifecycle is managed via PRs, discussed in Slack, and reviewed and discussed in project meetings.

Here is an example of a remove maintainer PR: https://github.com/open-cluster-management-io/community/pull/209 

<!-- (Project assertion goes here) --> 

- [x] **If the project has subprojects: subproject leadership, contribution, maturity status documented, including add/remove process.**

Documented in:
  - [GOVERNANCE.md](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md#default-subproject-governance) 
  - [Add-on contrib section of website](https://github.com/open-cluster-management-io/addon-contrib?tab=readme-ov-file#governance)


### Required

- [x] **Document complete list of current maintainers, including names, contact information, domain of responsibility, and affiliation.**

Fully documented and kept current in our [maintainers](https://github.com/open-cluster-management-io/community/blob/main/MAINTAINERS.md) document.

- [x] **A number of active maintainers which is appropriate to the size and scope of the project.**

OCM currently has a total of 22 maintainers from a variety of organizations. Full details are available in our [maintainers](https://github.com/open-cluster-management-io/community/blob/main/MAINTAINERS.md) file.

Full stats can be found at: https://openclustermanagement.devstats.cncf.io

Some highlights:

- We currently, as of this writing, have [77 contributors](https://landscape.cncf.io/?item=orchestration-management--scheduling-orchestration--open-cluster-management) and regularly see at least a minimum of [15 contributors per month on average](https://openclustermanagement.devstats.cncf.io/d/74/contributions-chart?orgId=1&var-period=m&var-metric=commits&var-repogroup_name=All&var-country_name=All&var-company_name=All&var-company=all) 
- In the last 12 months we’ve had contributions from [12 different companies](https://openclustermanagement.devstats.cncf.io/d/5/companies-table?orgId=1&var-period_name=Last%20year&var-metric=contributions) across a wide variety of industries.
- Our stars continue to climb! [![Star History Chart](https://api.star-history.com/svg?repos=open-cluster-management-io/ocm&type=Date)](https://www.star-history.com/#open-cluster-management-io/ocm&Date)

<!-- (Project assertion goes here) --> 

- [x] **Code and Doc ownership in Github and elsewhere matches documented governance roles.**

<!-- (Project assertion goes here) --> 

Our [GOVERNANCE](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md) and [MAINTAINERS](https://github.com/open-cluster-management-io/community/blob/main/MAINTAINERS.md) and [OWNERS](https://github.com/open-cluster-management-io/ocm/blob/main/OWNERS) files accurately reflect our actual Github code and doc ownership.

- [x] **Document adoption and adherence to the CNCF Code of Conduct or the project's CoC which is based off the CNCF CoC and not in conflict with it.**

Adopted during sandbox onboarding. https://github.com/open-cluster-management-io/community/blob/main/CODE_OF_CONDUCT.md 

<!-- (Project assertion goes here) --> 

- [x] **CNCF Code of Conduct is cross-linked from other governance documents.**

Yes, we link to the CNCF Code of Conduct directly from out [GOVERNANCE doc](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md#code-of-conduct)

<!-- (Project assertion goes here) --> 

- [x] **All subprojects, if any, are listed.**

Yes. See the top of this document or jump directly to a full list of sub-projects from our [GOVERNANCE](https://github.com/open-cluster-management-io/community/blob/main/GOVERNANCE.md#subprojects) file.

<!-- (Project assertion goes here) --> 

## Contributors and Community

Note: this section may be augmented by the completion of a Governance Review from the Project Reviews subproject.

### Suggested

- [x] **Contributor ladder with multiple roles for contributors.**

Please see our [ladder document](https://github.com/open-cluster-management-io/community/blob/main/CONTRIBUTOR_LADDER.md)

<!-- (Project assertion goes here) --> 

### Required

- [x] **Clearly defined and discoverable process to submit issues or changes.**

Detailed and clear steps for contributing and understanding the project can be found in our [README](https://github.com/open-cluster-management-io/ocm/blob/main/README.md), community [CONTRIBUTING](https://github.com/open-cluster-management-io/community/blob/main/CONTRIBUTING.md) and OCM [CONTRIBUTING](https://github.com/open-cluster-management-io/ocm/blob/main/CONTRIBUTING.md) documents.

<!-- (Project assertion goes here) --> 

- [x] **Project must have, and document, at least one public communications channel for users and/or contributors.**

Both our [README](https://github.com/open-cluster-management-io/ocm?tab=readme-ov-file#get-connected) and https://open-cluster-management.io/ have links to the community Slack and other communication channels.

<!-- (Project assertion goes here) --> 

- [x] **List and document all project communication channels, including subprojects (mail list/slack/etc.).  List any non-public communications channels and what their special purpose is.**

Project communication is done through Slack, GitHub, a weekly community meeting and office hours.

<!-- (Project assertion goes here) --> 

- [x] **Up-to-date public meeting schedulers and/or integration with CNCF calendar.**

## Community Meetings
We offer two meetings to accomodate timezones and interests. Both are available on the [OCM Calendar](https://calendar.google.com/calendar/u/0/embed?src=openclustermanagement@gmail.com) and **anyone is welcome to join them both**!
  - **Open Cluster Management Lunch Chat**: A bi-weekly (fortnightly) North America/Europe-centric timezone meeting. This is a more free-flowing "office hours" type of call. All questions, issues, interests, and comments are welcome!
  - **Open Cluster Management community meeting**: A bi-weekly (fortnightly) and aligned closer to an APAC timezone with a more formal discussion format with presentations.

As with any global community working with timezones all meetings are flexible and may vary in content and frequency. Recordings of meetings and additonal community communication can be found on the [Community](https://open-cluster-management.io/community/) page of the website.

<!-- (Project assertion goes here) --> 

- [x] **Documentation of how to contribute, with increasing detail as the project matures.**

We maintain detailed and up to date documents for community [CONTRIBUTING](https://github.com/open-cluster-management-io/community/blob/main/CONTRIBUTING.md) and OCM [CONTRIBUTING](https://github.com/open-cluster-management-io/ocm/blob/main/CONTRIBUTING.md) 

<!-- (Project assertion goes here) --> 

- [x] **Demonstrate contributor activity and recruitment.**

Github: https://github.com/open-cluster-management-io/community/issues/201 

We have a total of [42 contributors](https://openclustermanagement.devstats.cncf.io/d/66/developer-activity-counts-by-companies?orgId=1&var-period_name=Last%20decade&var-metric=contributions&var-repogroup_name=All&var-country_name=All&var-companies=All) to the project since conception and have a total of [28 contributors](https://openclustermanagement.devstats.cncf.io/d/66/developer-activity-counts-by-companies?orgId=1&var-period_name=Last%20year&var-metric=contributions&var-repogroup_name=All&var-country_name=All&var-companies=All) in the last year.
Over the last year, we have an average of 758 contributions and 30 contributors per month, and an average of 85 PRs merged per month.

<!-- (Project assertion goes here) --> 

## Engineering Principles

### Suggested

- [x] **Roadmap change process is documented.**

We maintain and active roadmap on [Github](https://github.com/orgs/open-cluster-management-io/projects/2/views/9) and are working with our maintainers and adopters to shape a longer term plan at on our [website](https://open-cluster-management.io/docs/roadmap/)

<!-- (Project assertion goes here) --> 

- [x] **History of regular, quality releases.**

We maintain a detailed history of [releases](https://open-cluster-management.io/docs/release/) as well as our [Github dashboard](https://github.com/orgs/open-cluster-management-io/projects/2) showing all issues for each release over the last few years! 

<!-- (Project assertion goes here) --> 

### Required 

- [x] **Document project goals and objectives that illustrate the project’s differentiation in the Cloud Native landscape as well as outlines how this project fulfills an outstanding need and/or solves a problem differently. _This can also be satisfied by completing a General Technical Review._**

At its core, Open Cluster Management (OCM) exists to make running, managing, and utilising heterogeneous, multicluster environments simpler. We believe that no one runs just one cluster and making multicluster as easy as possible encourages community growth across all projects, empowering our users and their customers.

We do this via a flexible, extensible, and open model that allows any software project to easily understand how to run in a multicluster way. Our core goal is to “multicluster everything.” To do this we align with, and contribute to, the SIG-Multicluster APIs for multicluster management. But we also have developed, and shared, a number of key concepts and components within OCM that makes it easier and more accessible for any project, large or small, to “do multicluster.” 

Two key components are documented below:

[The Placement API](https://open-cluster-management.io/docs/concepts/content-placement/placement/): The OCM Placement API is a very dynamic and sophisticated scheduler for multicluster environments. It operates on a Hub-Spoke model and is deeply integrated with our Work API, ManifestWork. The Placement API allows an administrator to use a vendor-neutral work selector to easily place resources across a fleet of clusters. Within the API the PlacementDecision resource provides a list of clusters that have been selected. We’ve successfully used this within OCM and are working closely to lead our extended community in the effort for its inclusion in SIG’s API specs.  By standardizing on a single PlacementDecision API, any scheduler can publish its choices and any consumer can subscribe to them, eliminating friction and enabling true "plug and play". For full details of this effort and how OCM is leading please see this [enhancement proposal](https://github.com/kubernetes/enhancements/issues/5313). 

[Add-ons](https://open-cluster-management.io/docs/concepts/add-on-extensibility/addon/): OCM utilises the concept of an add-on to clearly define a framework which allows developers to easily add their software to OCM and make it mlticluster aware. Add-ons are simple to write and are fully documented and maintained to the specifications in the [addon-framework](https://github.com/open-cluster-management-io/addon-framework) repo. Add-ons are used by multiple projects such as Argo, Submariner, Kubevela and more. Add-ons are also used extensively for internal components of OCM so the framework is actively developed and maintained. With add-ons any project can plug-in to OCM with minimal code and, almost instantaneously become multicluster aware.

We are also in the process of creating a goals and objectives page on our website to surface these ideas with even more visibility.

<!-- (Project assertion goes here) --> 

- [x] **Document what the project does, and why it does it - including viable cloud native use cases. This can also be satisfied by completing a General Technical Review.**

What OCM does is documented on our [website](https://open-cluster-management.io/), with detailed sections on the [key concepts](https://open-cluster-management.io/docs/concepts/) where it is outlined in great detail; however, below we provide some highlights for easy review:


Open Cluster Management is a community-driven project focused on multicluster and multicloud scenarios for Kubernetes apps. We offer both a reference implementation of the API’s put forward by SIG-Multicluster as well as extended capabilities to accentuate them for numerous additional use cases. We utilise open APIs and an easy to use add-on structure to allow projects to gain the benefits of simple, secure, and vendor-neutral multicloud management.
We do this because we believe that managing multiple clusters should be simple and easy. With the variety of both free and proprietary cloud and on-premises offerings it is important to us to help the community utilise these heterogeneous environments to their fullest potential. We want to ensure users can remain focused on their code and core business. With the growth and popularity of Kubernetes we know that no one can afford to run just one cluster, so we offer them the solution to keep pace and focus on innovation over infrastructure headaches. 
Everything OCM does is Cloud Native by definition. Our architecture is modular and extensible and built to always model Kubernetes principles. We utilize open declarative APIs and build code with DevOps and automation.  OCM runs on a hub-spoke model that can survive failure, and recovery, of components without interrupting workloads. It’s containerised, vendor-neutral, and focuses on declarative management style aligned with GitOps principles of development and automation. 


To dive into additional Cloud Native use cases review our comprehensive [User Scenarios](https://open-cluster-management.io/docs/scenarios/) section of our website.

<!-- (Project assertion goes here) --> 

- [x] **Document and maintain a public roadmap or other forward looking planning document or tracking mechanism.**

Our roadmap is maintained and documented on [GitHub](https://github.com/orgs/open-cluster-management-io/projects/2/views/9)

<!-- (Project assertion goes here) --> 

- [x] **Document overview of project architecture and software design that demonstrates viable cloud native use cases, as part of the project's documentation. _This can also be satisfied by completing a General Technical Review and capturing the output in the project's documentation._**

See the previous sections' dicussion of cloud native use cases and for a deep dive into the components please visit our [Architecture](https://open-cluster-management.io/docs/concepts/architecture/) page. 

<!-- (Project assertion goes here) --> 

- [x] **Document the project's release process.**

We have a [release runbook](https://github.com/open-cluster-management-io/community/blob/main/RELEASE.md)

<!-- (Project assertion goes here) --> 

## Security

### Suggested

N/A

### Required

Note: this section may be augmented by a joint-assessment performed by TAG Security and Compliance.

- [x] **Clearly defined and discoverable process to report security issues.**

This is described in our [SECURITY](https://github.com/open-cluster-management-io/community/blob/main/SECURITY.md) document. 

<!-- (Project assertion goes here) --> 

- [x] **Enforcing Access Control Rules to secure the code base against attacks (Example: two factor authentication enforcement, and/or use of ACL tools.)**

Code is maintained in GitHub so uses 2FA by default. We have a [dedicated contact]https://github.com/open-cluster-management-io/community/blob/main/SECURITY.md) documented for raising security issues directly with the project. Merge and commit access is managed by OWNERS file and prow CICD.

<!-- (Project assertion goes here) --> 

- [x] **Document assignment of security response roles and how reports are handled.**

This is detailed ono our [secuirty](https://open-cluster-management.io/docs/security/) page on the website.

<!-- (Project assertion goes here) --> 

- [x] **Document [Security Self-Assessment](https://tag-security.cncf.io/community/assessments/guide/self-assessment/).**

Available for review in out [SELF_ASSESSMENT](https://github.com/open-cluster-management-io/ocm/blob/main/SELF_ASSESSMENT.md) document.

<!-- (Project assertion goes here) --> 

- [x] **Achieve the Open Source Security Foundation (OpenSSF) Best Practices passing badge.**

Yes, we have achieved this badge: https://www.bestpractices.dev/en/projects/5376

<!-- (Project assertion goes here) --> 

## Ecosystem

### Suggested

N/A

### Required

- [x]  **Publicly documented list of adopters, which may indicate their adoption level (dev/trialing, prod, etc.)**

Our list of adopters can be found [here](https://github.com/open-cluster-management-io/ocm/blob/main/ADOPTERS.md). We have expanded this to include uses cases and additonal details. We have additonal adopters that can't be listed publically yet.

<!-- (Project assertion goes here) --> 

- [x] **Used in appropriate capacity by at least 3 independent + indirect/direct adopters, (these are not required to be in the publicly documented list of adopters)**

<!-- (Project assertion goes here) --> 
In addition to the adopters listed at the top of the document, we also have at least 2 other non-public adopters using it at large companies. As appropriate, we will update our list as we get permissions from those companies.

- [ ] **TOC verification of adopters.**

<!-- (Project assertion goes here) --> 

Refer to the Adoption portion of this document.

- [x] **Clearly documented integrations and/or compatibility with other CNCF projects as well as non-CNCF projects.**

 These integrations are documented on https://open-cluster-management.io/ and https://github.com/open-cluster-management-io/ocm/tree/main/solutions

 For reference, we either integrate with or build on top of the following projects:

 - [Kubernetes (CNCF)](https://kubernetes.io/) - OCM is built on top of Kubernetes, offering multicluster orchestration capabilities and a flexible extensibility framework for other projects in the Kubernetes ecosystem.
 - [Argo CD](https://argo-cd.readthedocs.io/en/stable/operator-manual/applicationset/Generators-Cluster-Decision-Resource/#how-it-works) (CNCF) - OCM supplies Argo  CD with ClusterDecision resources via Argo  CD’s Cluster Decision Resource Generator, enabling it to select target clusters for GitOps deployments.
 - [KubeVela](https://kubevela.io/docs/platform-engineers/system-operation/working-with-ocm/) (CNCF) KubeVela develops an integration addon to work with OCM supporting application deployment across multiple clusters.
 - [KubeStellar](https://docs.kubestellar.io/latest/direct/start-from-ocm/) (CNCF) KubeStellar uses OCM as the backend of multicluster management.
 - [Kueue](https://kueue.sigs.k8s.io/docs/tasks/manage/setup_multikueue/#optional-setup-multikueue-with-open-cluster-management) (Kubernetes SIGs)
OCM supplies Kueue with a streamlined MultiKueue setup process, automated generation of MultiKueue specific Kubeconfig, and enhanced multicluster scheduling capabilities.

<!-- (Project assertion goes here) --> 

## Additional Information

<!-- Provide any additional information you feel is relevant for the TOC in conducting due diligence on this project. -->
