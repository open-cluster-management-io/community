# Open Cluster Management Project Governance

## Table of Contents

- [Values](#values)
- [Project Governance](#project-governance)
  - [Project Structure](#project-structure)
    - [Project (Core)](#project-core)
    - [Subprojects](#subprojects)
  - [Core Project Governance](#core-project-governance)
    - [Core Project Maintainers](#core-project-maintainers)
    - [Becoming a Core Project Maintainer](#becoming-a-core-project-maintainer)
    - [Removing a Core Project Maintainer](#removing-a-core-project-maintainer)
    - [Decision Making and Voting](#decision-making-and-voting)
    - [Adding to Core Project](#adding-to-core-project)
    - [Removing from Core Project](#removing-from-core-project)
  - [Subproject Governance](#subproject-governance)
    - [Adding Subprojects](#adding-subprojects)
    - [Removing Subprojects](#removing-subprojects)
- [Contributor Ladder](#contributor-ladder)
- [Security](#security)
- [Release Process](#release-process)
- [Code of Conduct](#code-of-conduct)
- [Communication Channels](#communication-channels)
  - [Public Channels](#public-channels)
  - [Community Meetings](#community-meetings)
  - [Project-Specific Channels](#project-specific-channels)
  - [Private Channels](#private-channels)
- [Amendments](#amendments)

# Values

Open Cluster Management and its leadership embrace the following values:

- Openness: Open Cluster Management is an open source community driven project.
- Distributed design: Distributed asynchronous ownership, collaboration, communication and decision making are the cornerstones of our world-wide community.
- Fairness: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles.
- Diversity and inclusion: Everyone are welcome to participate in the Open Cluster Management project regardless of gender, gender identity, sexual orientation, disability, race, ethnicity, age, religion or economic status.

# Project Governance

Open Cluster Management follows a federated governance model with two distinct categories: the core project and subprojects, each with different governance requirements and expectations:

## Project Structure

### Project (Core)
The core project forms the foundation of Open Cluster Management and is maintained by the OCM core team with strict governance requirements:

- [OCM](https://github.com/open-cluster-management-io/ocm)
- [API](https://github.com/open-cluster-management-io/api)
- [Clusteradm](https://github.com/open-cluster-management-io/clusteradm)
- [Addon Framework](https://github.com/open-cluster-management-io/addon-framework)
- [SDK](https://github.com/open-cluster-management-io/sdk-go)

**Core Project Requirements:**
- Maintained by OCM core maintainers
- Follow strict release cycles and version compatibility guarantees
- Provide long-term support and stability commitments
- Must follow the governance rules defined in this document

### Subprojects
Subprojects are optional components that run on top of OCM core to support different use cases and extend OCM functionality:

- [Addon-Contrib](https://github.com/gopen-cluster-management-io/addon-contrib)
- [Argo Integration](https://github.com/open-cluster-management-io/argocd-pull-integration)
- [Cluster Proxy Addon](https://github.com/open-cluster-management-io/cluster-proxy)
- [Policy Addon](https://github.com/open-cluster-management-io/config-policy-controller)
- [Managed Service Account Addon](https://github.com/open-cluster-management-io/managed-serviceaccount)
- [Lab](https://github.com/open-cluster-management-io/lab)
- And others as they are added to the ecosystem

**Subproject Governance:**
- Project maintainers have autonomy over their governance model
- Each subproject MAY define its own governance in a `GOVERNANCE.md` file within the project directory
- If no custom governance document exists, the project follows the default governance rules defined in the "Subproject Governance" section below
- Release cycles, versioning, and quality standards are determined by project maintainers
- Project maintainers are responsible for maintenance, security responses, and community management

## Core Project Governance

Open Cluster Management Core Project is governed by the [Core Project Maintainers](https://github.com/open-cluster-management-io/community/blob/main/MAINTAINERS.md#the-maintainer-list-of-core-ocmnames-are-in-alphabetical-order), who collectively form the **Maintainer Council**. This council serves as the governing body for both technical and strategic decisions related to the core project.

### Core Project Maintainers

All active Maintainers of the Core Project, as defined in the Contributor Ladder, have write access to the core project repositories and are responsible for:

**Technical Responsibilities:**
- Creating and publishing regular, stable releases following OCM release cycles
- Maintaining version compatibility guarantees and migration paths
- Making technical decisions on core project changes and implementations
- Responding to security compromise reports according to OCM security procedures
- Ensuring comprehensive testing and code quality standards are maintained
- Reviewing and merging pull requests
- Maintaining project documentation and technical specifications

**Governance Responsibilities:**
- Strategic decisions and governance policies for the core project
- Cross-project coordination between core components
- Reviewing and deciding on new projects to add to the Core Project
- Removing projects which have become inactive or no longer align with project goals
- Administering core project infrastructure, intellectual property, and resources
- Arbitrating inter-project disagreements and conflicts within the core project
- Acting on escalated security or code quality issues that affect the core project

**Community Responsibilities:**
- Monthly review of core project contributors for advancement on the Contributor Ladder
- Resolving issues that individual core components are unable to resolve
- Representing the core project to CNCF and the broader community
- Ensuring compliance with the Code of Conduct within the core project

The collective team of all Core Project Maintainers is known as the **Maintainer Council**, which is the governing body for the core project. This privilege is granted with the expectation of responsibility: maintainers are people who care about the OCM project and want to help it grow and improve.

### Becoming a Core Project Maintainer

To become a Core Project Maintainer, candidates must demonstrate:

**Commitment to the project:**
- Participate in discussions, contributions, code and documentation reviews for 6+ months
- Perform reviews for 10+ non-trivial pull requests in core project repositories
- Contribute 5+ non-trivial pull requests to core project repositories and have them merged
- Demonstrate understanding of OCM's stability and compatibility guarantees

**Technical and leadership abilities:**
- Ability to write quality code and/or documentation
- Ability to collaborate with the team and mentor other contributors
- Understanding of how the team works (policies, processes for testing and code review, etc)
- Understanding of the core project's codebase and coding and documentation style
- Demonstrated commitment to OCM's long-term success and stability

A new Core Project Maintainer must be proposed by an existing Core Project Maintainer through a GitHub issue in the [community repository](https://github.com/open-cluster-management-io/community) or during a maintainer meeting. A simple majority vote of existing Core Project Maintainers approves the application. Maintainer nominations will be evaluated without prejudice to employer or demographics.

### Removing a Core Project Maintainer

Core Project Maintainers may resign at any time if they feel that they will not be able to continue fulfilling their project duties.

Core Project Maintainers may also be removed after being inactive, failure to fulfill their maintainer responsibilities, violating the Code of Conduct, or other reasons. Inactivity is defined as a period of very low or no activity in the core project for 18 months, with no definite schedule to return to full maintainer activity.

A Core Project Maintainer may be removed at any time by a 2/3 vote of the remaining Core Project Maintainers.

Depending on the reason for removal, a Core Project Maintainer may be converted to Emeritus status. Emeritus Maintainers will still be consulted on some project matters, and can be rapidly returned to Maintainer status if their availability changes.

### Decision Making and Voting

The Core Project Maintainer Council follows these decision-making principles for all governance and technical matters:

**Consensus-Driven Approach:**
- Primary focus is on reaching consensus through discussion and collaboration
- Multiple revision iterations are common and encouraged
- Goal is to minimize major objections rather than achieve unanimous agreement
- Decisions are made through "lazy consensus" where silence is considered agreement

**Voting Protocol:**
- Formal voting is considered a last resort when consensus cannot be reached
- Any Core Project Maintainer may call for a formal vote on any matter
- Most decisions require a simple majority of all Core Project Maintainers to succeed
- Certain critical decisions require a 2/3 majority vote:
  - Removing a Core Project Maintainer
  - Adding new components to the Core Project
  - Modifying this governance document
  - Major architectural changes that affect compatibility

**Meeting and Communication:**
- Core Project Maintainers are expected to participate in regular community meetings
- Decisions may be made asynchronously via GitHub issues or discussions
- Private meetings may be held for security reports or Code of Conduct violations
- All current Core Project Maintainers must be invited to such meetings, except for any maintainer who is accused of a CoC violation

**Community Participation:**
- Community members are welcome to provide feedback on all decisions
- Community feedback is considered valuable input but is non-binding
- Major decisions should be communicated to the community for comment before implementation

### Adding to Core Project

Adding components to the core project requires Core Project Maintainer Council approval due to their critical nature and long-term commitments. Any project member may recommend components to become part of the Core Project of Open Cluster Management through a GitHub issue or during a maintainer meeting. These components must meet strict requirements:

**Technical Requirements:**
- Have a mission directly aligned with core Kubernetes cluster and multicluster management functionality
- Demonstrate architectural integration with existing core components
- Consist of high quality, well-tested code and designs
- Provide clear value proposition that cannot be achieved through subprojects

**Governance Requirements:**
- Are appropriately licensed (Apache 2.0 or compatible)
- Have established maintainer team willing to commit to OCM governance standards
- Demonstrate ability to maintain stable release cycles and version compatibility
- Commit to long-term support and maintenance responsibilities

**Process:**
Before submitting an application to the Core Project Maintainer Council, the applying component must hold an internal consensus vote of all major contributors to join Open Cluster Management as part of the Core Project. The Maintainer Council will then review the application through discussion and consensus, and decide whether or not to accept it. If accepted, the Council will assign one or more maintainers to assist the component in their integration and ensure compliance with core governance requirements.

### Removing from Core Project

In some cases, core project components may become inactive, unmaintainable, or no longer align with the core project's mission. Any Core Project Maintainer may propose removal of a core component on these grounds, and the Core Project Maintainer Council can confirm this with a 2/3 majority vote due to the critical nature of core components.

**Removal Process:**
- Core Project Maintainer proposes removal through GitHub issue or maintainer meeting
- Discussion period of at least two weeks for community input
- 2/3 majority vote of Core Project Maintainer Council required for approval
- If approved, component may be transitioned to subproject status if maintainers are available
- Components with no active maintainers are moved to archive status

## Subproject Governance

Subprojects that do not have their own `GOVERNANCE.md` file follow these default governance rules:

**Project Maintainership:**
- Each subproject has designated project maintainers who have administrative rights
- Project maintainers are responsible for defining contribution processes, release schedules, and quality standards
- Project maintainers may delegate responsibilities to other contributors as they see fit

**Decision Making:**
- Project maintainers make final decisions on technical direction, feature acceptance, and releases
- For controversial decisions, project maintainers should seek input from active contributors
- Conflicts that cannot be resolved within the project may be escalated to the Core Project Maintainer Council for guidance

**Contributor Management:**
- Project maintainers determine how contributors are onboarded and what permissions they receive
- Project maintainers are responsible for maintaining a welcoming and inclusive environment
- All contributors must follow the OCM Code of Conduct

**Project Governance Participation:**
- Subprojects participate in overall project governance through community discussions and input
- Subproject maintainers can participate in community meetings and provide feedback on project-wide decisions
- Major subproject concerns can be escalated to the Core Project Maintainer Council for consideration

### Adding Subprojects

Subprojects have a more streamlined acceptance process to encourage ecosystem growth:

**Requirements:**
- Have a mission related to extending or enhancing OCM functionality for specific use cases
- Are appropriately licensed (Apache 2.0 or compatible preferred)
- Are under active development or have clear development plans
- Have designated project maintainers willing to maintain the project

**Process:**
- Project maintainers may request addition to the OCM ecosystem through a GitHub issue in the [community repository](https://github.com/open-cluster-management-io/community) or community meeting
- The Core Project Maintainer Council will review for basic compatibility and licensing requirements
- Acceptance is generally granted unless there are significant concerns about licensing, security, or conflicts with existing projects
- Projects may be marked as "Experimental" initially and graduate to full status based on adoption and maturity

**Experimental Status:**
Promising but incomplete projects may be accepted as Experimental Subprojects. Such projects will be marked as Experimental on the website and in code repositories to inform users. Experimental projects are considered part of the OCM ecosystem with limited governance expectations. The Core Project Maintainer Council will review Experimental projects at least twice per year to determine if they have matured to full status.

### Removing Subprojects

In some cases, subprojects will become inactive or unmaintainable, or wish to separate from Open Cluster Management. Any Core Project Maintainer may propose removal of a subproject on these grounds, and the Core Project Maintainer Council can confirm this with a simple majority vote.

**Removal Process:**
- Core Project Maintainer proposes removal through GitHub issue or community meeting
- Discussion period for community input
- Simple majority vote of Core Project Maintainer Council required for approval
- The CNCF will determine which, if any, assets of those subprojects will be removable should a project leave OCM

**Post-Removal:**
Where possible, projects which still have contributors will then be moved to a repository in their own namespace. Projects which have ceased all activity are moved to an archive namespace.

# Contributor Ladder

Open Cluster Management follows a contributor ladder that provides clear paths for community members to increase their involvement and responsibility within the project.

For detailed information about contributor roles, responsibilities, and advancement processes, please refer to the [CONTRIBUTOR_LADDER.md](CONTRIBUTOR_LADDER.md) file.


# Security

Open Cluster Management takes security seriously and maintains comprehensive security policies and procedures.

For detailed information about security reporting, response processes, and requirements, please refer to the [SECURITY.md](SECURITY.md) file.

# Release Process

Open Cluster Management follows structured release processes for both core project and subprojects to ensure quality and compatibility.

For detailed information about release schedules, requirements, and procedures, please refer to the [RELEASE.md](RELEASE.md) file.

# CNCF Resources

Any Maintainer may suggest a request for CNCF resources, either in the [mailing list](cncf-ocm-maintainers@lists.cncf.io), or during a meeting. A simple majority of Maintainers approves the request. The Maintainers may also choose to delegate working with the CNCF to non-Maintainer community members, who will then be added to the [CNCF's Maintainer List](https://github.com/cncf/foundation/blob/main/project-maintainers.csv) for that purpose.

# Code of Conduct

This project follows the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/main/code-of-conduct.md).
Any code of conduct violations should be reported to the org maintainers.

For violations involving an org maintainer, the accused maintainer will be recused from the investigation process.
These cases must be escalated to the appropriate CNCF contact, who may intervene as needed.

# Communication Channels

Open Cluster Management maintains several communication channels for different purposes:

## Public Channels

- **Slack #open-cluster-mgmt**: Real-time community chat - [START HERE!](https://kubernetes.slack.com/channels/open-cluster-mgmt) :)
- **Mailing List**: [OCM Mailing List at Google Groups](https://groups.google.com/g/open-cluster-management)

## Community Meetings
We offer two meetings to accomodate timezones and interests. Both are available on the [OCM Calendar](https://calendar.google.com/calendar/u/0/embed?src=openclustermanagement@gmail.com) and **anyone is welcome to join them both**!
  - **Open Cluster Management Lunch Chat**: A bi-weekly (fortnightly) North America/Europe-centric timezone meeting. This is a more free-flowing "office hours" type of call. All questions, issues, interests, and comments are welcome!
  - **Open Cluster Management community meeting**: A bi-weekly (fortnightly) and aligned closer to an APAC timezone with a more formal discussion format with presentations.

As with any global community working with timezones all meetings are flexible and may vary in content and frequency. Recordings of meetings and additonal community communication can be found on the [Community](https://open-cluster-management.io/community/) page of the website.

## Project-Specific Channels

Each subproject may maintain its own communication channels as documented in their respective repositories.

## Private Channels

- **Security Reports**: OCM-security@googlegroups.com
- **Code of Conduct Reports**: cncf-ocm-maintainers@lists.cncf.io

# Amendments

This governance document may be amended by a 2/3 majority vote of the Core Project Maintainer Council.

**Amendment Process:**
1. Proposed amendments must be circulated to the community for comment at least one week before voting
2. The Core Project Maintainer Council will consider community feedback before voting
3. Amendments take effect immediately upon approval unless otherwise specified
4. All amendments will be documented in the project's governance history

**Emergency Amendments:**
In cases where immediate action is required for legal, security, or CNCF compliance reasons, amendments may be made with a simple majority vote of available Core Project Maintainers, with community notification to follow within 48 hours.
