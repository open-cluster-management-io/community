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
Additional non-public adopters are available on request.

## Application Process Principles

### Suggested

N/A

### Required

- [x] **Engage with the domain specific TAG(s) to increase awareness through a presentation or completing a General Technical Review.**
  - Please see our [General Technical Review](https://github.com/open-cluster-management-io/community/blob/main/cncf/GTR.md) for full details.

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

We follow the CNCF's vendor-neutrality requirements, and make sure that our project's governance clearly describes how people can become contributors or maintainers based on their community involvement, not their company affiliation. We also make sure that all project communications are community focused and vendor neutral, and open to everyone to participate. Additionally, we align closely and contribute to the [SIG Multicluster APIs](https://multicluster.sigs.k8s.io/) to ensure we always remain vendor neutral and 100% based on community standards.

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

Some examples of this process can be found below.

- A recent [Slack thread announcing new maintainers](https://kubernetes.slack.com/archives/C01GE7YSUUF/p1753726598660099)

- Example PR's adding and reviewing new maintainers:
-- https://github.com/open-cluster-management-io/community/pull/210
-- https://github.com/open-cluster-management-io/community/pull/214

Additionally, we review and adjust maintainer status periodically to ensure currency and accuracy. Here's an example of moving two maintainers to emeritus status reflecting their previous contributions but transparently acknowledging they are no longer active:
- https://github.com/open-cluster-management-io/community/pull/209

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

Both our [README](https://github.com/open-cluster-management-io/ocm?tab=readme-ov-file#community) and https://open-cluster-management.io/ have links to the community Slack and other communication channels.

<!-- (Project assertion goes here) --> 

- [x] **List and document all project communication channels, including subprojects (mail list/slack/etc.).  List any non-public communications channels and what their special purpose is.**

Project communication is done through Slack, GitHub, a weekly community meeting and office hours.
More information can be found on the [Community](https://open-cluster-management.io/community/) page of the website.

<!-- (Project assertion goes here) --> 

- [x] **Up-to-date public meeting schedulers and/or integration with CNCF calendar.**

## Community Meetings
We offer two meetings to accomodate timezones and interests. Both are available on the [OCM Calendar](https://calendar.google.com/calendar/u/0/embed?src=openclustermanagement@gmail.com) and **anyone is welcome to join them both**!
  - **Open Cluster Management Lunch Chat**: A bi-weekly (fortnightly) North America/Europe-centric timezone meeting. This is a more free-flowing "office hours" type of call. All questions, issues, interests, and comments are welcome!
  - **Open Cluster Management community meeting**: A bi-weekly (fortnightly) and aligned closer to an APAC timezone with a more formal discussion format with presentations.

As with any global community working with timezones all meetings are flexible and may vary in content and frequency. Recordings of meetings and additional community communication can be found on the [Community](https://open-cluster-management.io/community/) page of the website.

<!-- (Project assertion goes here) --> 

- [x] **Documentation of how to contribute, with increasing detail as the project matures.**

We maintain detailed and up to date documents for community [CONTRIBUTING](https://github.com/open-cluster-management-io/community/blob/main/CONTRIBUTING.md) and OCM [CONTRIBUTING](https://github.com/open-cluster-management-io/ocm/blob/main/CONTRIBUTING.md) 

<!-- (Project assertion goes here) --> 

- [x] **Demonstrate contributor activity and recruitment.**

Github: https://github.com/open-cluster-management-io/community/issues/201 

We have a total of [42 contributors](https://openclustermanagement.devstats.cncf.io/d/66/developer-activity-counts-by-companies?orgId=1&var-period_name=Last%20decade&var-metric=contributions&var-repogroup_name=All&var-country_name=All&var-companies=All) to the project since conception and have a total of [28 contributors](https://openclustermanagement.devstats.cncf.io/d/66/developer-activity-counts-by-companies?orgId=1&var-period_name=Last%20year&var-metric=contributions&var-repogroup_name=All&var-country_name=All&var-companies=All) in the last year.
Over the last year, we have an average of 758 contributions and 30 contributors per month, and an average of 85 PRs merged per month.

OCM has actively participated in KubeCons and other global CNCF events. Including Project Pavilion kiosks at KubeCon North America, China, Japan, Europe, as well as many speaking sessions. Some recent examples include:

- [ArgoCon EU 2025 - Scale GitOps With the Argo CD Agent and Open Cluster Management](https://www.youtube.com/watch?v=trR8OcmizXQ)
- [KubeCon EU 2025 - How the SIG-Multicluster API Specifications Are Used for Real World](https://www.youtube.com/watch?v=I9GV4N23dvE)
- [KCD China 2025 - AI-Driven Troubleshooting for Multi-Cluster Environments](https://github.com/cncf/presentations/blob/main/chinese/kcd-beijing/2025-03-15/AI/01-%E5%A4%9A%E9%9B%86%E7%BE%A4%E7%8E%AF%E5%A2%83%E4%B8%AD%20AI%20%E9%A9%B1%E5%8A%A8%E7%9A%84%E6%95%85%E9%9A%9C%E8%AF%8A%E6%96%AD%20-Meng%20Yan.pdf)
- [KCD China 2025 - Unlocking the Power of CEL for Advanced Multi-Cluster Scheduling](https://github.com/cncf/presentations/blob/main/chinese/kcd-beijing/2025-03-15/Cloud%20Native/04-%E9%87%8A%E6%94%BE%20CEL%20%E5%9C%A8%E9%AB%98%E7%BA%A7%E5%A4%9A%E9%9B%86%E7%BE%A4%E8%B0%83%E5%BA%A6%E4%B8%AD%E7%9A%84%E6%BD%9C%E5%8A%9B%20-Qing%20Hao.pdf)

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

Please see our [General Technical Review](https://github.com/open-cluster-management-io/community/blob/main/cncf/GTR.md) for full details.

<!-- (Project assertion goes here) --> 

- [x] **Document what the project does, and why it does it - including viable cloud native use cases. This can also be satisfied by completing a General Technical Review.**

What OCM does is documented in our [General Technical Review](https://github.com/open-cluster-management-io/community/blob/main/cncf/GTR.md) and on our [website](https://open-cluster-management.io/), with detailed sections on the [key concepts](https://open-cluster-management.io/docs/concepts/) where it is outlined in great detail; however, below we provide some highlights for easy review:

Open Cluster Management is a community-driven project focused on multicluster and multicloud scenarios for Kubernetes apps. We offer both a reference implementation of the API’s put forward by SIG-Multicluster as well as extended capabilities to accentuate them for numerous additional use cases. We utilise open APIs and an easy to use add-on structure to allow projects to gain the benefits of simple, secure, and vendor-neutral multicloud management.
We do this because we believe that managing multiple clusters should be simple and easy. With the variety of both free and proprietary cloud and on-premises offerings it is important to us to help the community utilise these heterogeneous environments to their fullest potential. We want to ensure users can remain focused on their code and core business. With the growth and popularity of Kubernetes we know that no one can afford to run just one cluster, so we offer them the solution to keep pace and focus on innovation over infrastructure headaches. 
Everything OCM does is Cloud Native by definition. Our architecture is modular and extensible and built to always model Kubernetes principles. We utilize open declarative APIs and build code with DevOps and automation.  OCM runs on a hub-spoke model that can survive failure, and recovery, of components without interrupting workloads. It’s containerised, vendor-neutral, and focuses on declarative management style aligned with GitOps principles of development and automation. 


To dive into additional Cloud Native use cases review our comprehensive [User Scenarios](https://open-cluster-management.io/docs/scenarios/) section of our website.

<!-- (Project assertion goes here) --> 

- [x] **Document and maintain a public roadmap or other forward looking planning document or tracking mechanism.**

Our roadmap is maintained and documented on [GitHub](https://github.com/orgs/open-cluster-management-io/projects/2/views/9)

<!-- (Project assertion goes here) --> 

- [x] **Document overview of project architecture and software design that demonstrates viable cloud native use cases, as part of the project's documentation. _This can also be satisfied by completing a General Technical Review and capturing the output in the project's documentation._**

We have a comprehensive [General Technical Review](https://github.com/open-cluster-management-io/community/blob/main/cncf/GTR.md) and maintain the information in our [project documentation](https://open-cluster-management.io/docs/concepts/).

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
