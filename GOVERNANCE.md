# Open Cluster Management Project Governance

## Table of Contents

- [Values](#values)
- [Project Governance](#project-governance)
  - [Project Structure](#project-structure)
  - [Core Project Governance](#core-project-governance)
  - [Default Subproject Governance](#default-subproject-governance)
  - [Adding New Projects](#adding-new-projects)
  - [Removing Projects](#removing-projects)
- [Contributor Ladder](#contributor-ladder)
- [Steering Committee](#steering-committee)
  - [Duties](#duties)
  - [Members](#members)
  - [Elections](#elections)
  - [Decision Making](#decision-making)
- [Security](#security)
- [Release Process](#release-process)
- [Code of Conduct](#code-of-conduct)

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
- If no custom governance document exists, the project follows the default governance rules defined in the "Default Subproject Governance" section below
- Release cycles, versioning, and quality standards are determined by project maintainers
- Project maintainers are responsible for maintenance, security responses, and community management

## Core Project Governance

All active Maintainers of the Core Project, as defined in the Contributor Ladder, are
responsible for the technical aspects of the core project. The Core Project Maintainers are responsible
for the following activities:

- Creating and publishing regular, stable releases following OCM release cycles;
- Maintaining version compatibility guarantees and migration paths;
- Making technical decisions on core project changes and implementations;
- Responding to security compromise reports according to OCM security procedures;
- Ensuring comprehensive testing and code quality standards are maintained;
- Reviewing and merging pull requests;
- Maintaining project documentation and technical specifications.

Strategic decisions, governance policies, and cross-project coordination are handled by the Steering Committee as defined below.

Should a Core Project Maintainer cease being active in the core project,
violate the Code Of Conduct, or need to be removed for some other reason, they
may be removed by a 2/3 majority vote of the other Core Project Maintainers, or a
majority vote of the Steering Committee.

## Default Subproject Governance

Subprojects that do not have their own `GOVERNANCE.md` file follow these default governance rules:

**Project Maintainership:**
- Each subproject has designated project maintainers who have administrative rights
- Project maintainers are responsible for defining contribution processes, release schedules, and quality standards
- Project maintainers may delegate responsibilities to other contributors as they see fit

**Decision Making:**
- Project maintainers make final decisions on technical direction, feature acceptance, and releases
- For controversial decisions, project maintainers should seek input from active contributors
- Conflicts that cannot be resolved within the project may be escalated to the Steering Committee

**Contributor Management:**
- Project maintainers determine how contributors are onboarded and what permissions they receive
- Project maintainers are responsible for maintaining a welcoming and inclusive environment
- All contributors must follow the OCM Code of Conduct

**Project Governance Participation:**
- Subprojects participate in overall project governance through the established Steering Committee structure
- Subproject maintainers can participate in community discussions and provide input on project-wide decisions
- Major subproject concerns can be escalated to the Steering Committee for consideration

## Adding New Projects

### Adding to Core Project

Adding components to the core project requires Steering Committee approval due to their critical nature and long-term commitments. During the monthly Steering meeting, any project member may recommend components to become part of the Core Project of Open Cluster Management. These components must meet strict requirements:

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
Before submitting an application to the Steering Committee, the applying component must hold an internal consensus vote of all major contributors to join Open Cluster Management as part of the Core Project. The Steering Committee will then review the application, and decide whether or not to accept it. If accepted, the Committee will assign one person to assist the component in their integration and ensure compliance with core governance requirements.

### Adding Subprojects

Subprojects have a more streamlined acceptance process to encourage ecosystem growth:

**Requirements:**
- Have a mission related to extending or enhancing OCM functionality for specific use cases
- Are appropriately licensed (Apache 2.0 or compatible preferred)
- Are under active development or have clear development plans
- Have designated project maintainers willing to maintain the project

**Process:**
- Project maintainers may request addition to the OCM ecosystem through a GitHub issue or Steering Committee meeting
- The Steering Committee will review for basic compatibility and licensing requirements
- Acceptance is generally granted unless there are significant concerns about licensing, security, or conflicts with existing projects
- Projects may be marked as "Experimental" initially and graduate to full status based on adoption and maturity

**Experimental Status:**
Promising but incomplete projects may be accepted as Experimental Subprojects. Such projects will be marked as Experimental on the website and in code repositories to inform users. Experimental projects are considered part of the OCM ecosystem with limited governance expectations. The Steering Committee will review Experimental projects at least twice per year to determine if they have matured to full status.

## Removing Projects

In some cases, projects will become inactive or unmaintainable, or wish to separate
from Open Cluster Management. Any Steering Committee member may propose removal of a project on
these grounds, and Steering can confirm this with a majority vote. The CNCF will
determine which, if any, assets of those subprojects will be removable should a
project leave OCM.

Where possible, projects which still have contributors will then be moved to a
repository in their own namespace. Projects which have ceased all activity are
moved to an archive namespace.

# Contributor Ladder

Open Cluster Management follows a contributor ladder that provides clear paths for community members to increase their involvement and responsibility within the project. The complete contributor ladder is defined in the [CONTRIBUTOR_LADDER.md](CONTRIBUTOR_LADDER.md) file.

## Roles Overview

### Contributors
- Anyone who contributes to the project through code, documentation, issue reporting, or community participation
- No special permissions required
- Expected to follow the Code of Conduct

### Organization Members
- Contributors who have made sustained contributions to the project
- Have triage permissions on repositories
- Can be assigned to issues and pull requests
- Eligible to vote in community elections

### Reviewers
- Organization Members with expertise in specific areas
- Can review and approve pull requests in their areas of expertise
- Help mentor new contributors
- May be specific to individual subprojects

### Maintainers
- Reviewers with additional responsibilities and permissions
- Have write access to repositories
- Can merge pull requests and make releases
- Participate in subproject governance decisions
- Expected to be responsive to community needs

### Core Maintainers
- Maintainers of the Core Project with additional responsibilities
- Must commit to OCM's stability and compatibility guarantees
- Participate in cross-project coordination
- Help define overall project direction

## Advancement Process

Advancement through the contributor ladder is based on sustained contributions and community recognition:

1. **To Organization Member**: Demonstrated sustained contributions over 3+ months
2. **To Reviewer**: Technical expertise and history of quality reviews
3. **To Maintainer**: Leadership qualities, deep project knowledge, and community trust
4. **To Core Maintainer**: Exceptional technical and leadership contributions to core functionality

All advancement decisions are made by existing maintainers of the relevant subproject, with input from the broader community.

# Steering Committee

The overall Open Cluster Management umbrella project is governed by a Steering Committee(SC).

## Duties

The Steering Committee is responsible for the strategic governance of the entire Open Cluster Management project. Key responsibilities include:

**Strategic Direction:**
- Determining overall project direction and roadmap
- Setting project-wide policies and standards
- Coordinating between core project and subprojects

**Project Management:**
- Reviewing and deciding on new projects to add to Open Cluster Management
- Removing projects which have become inactive or no longer align with project goals
- Administering project infrastructure, intellectual property, and resources

**Community Governance:**
- Monthly review of project contributors for advancement on the Contributor Ladder
- Arbitrating inter-project disagreements and conflicts
- Resolving issues that individual projects are unable to resolve
- Selecting the Code of Conduct Committee and ratifying CoC judgements

**External Relations:**
- Determining overall direction for advocacy and marketing
- Issuing statements on behalf of Open Cluster Management and its subprojects
- Representing the project to CNCF and the broader community
- Acting on escalated security or code quality issues that affect the entire project

In performance of these duties, the Steering Committee will hold a monthly meeting
that is open to all contributors. The Committee may hold additional, closed meetings
in order to discuss non-public issues such as security exploits, CoC enforcement,
and legal questions.

Steering Committee members are expected to advocate for all of Open Cluster Management, not just
certain projects or corporate sponsors, comply with and support the Code of
Conduct, and be professional and compassionate in all of their dealings with
project participants.

## Members

The Steering Committee is composed of project maintainers and elected community representatives.

### Member Requirements

All Steering Committee members must:
- Be active contributors to the OCM ecosystem
- Commit to attending monthly Steering Committee meetings
- Represent the interests of the entire OCM community, not just their employer or subproject
- Follow the OCM Code of Conduct and maintain professional conduct
- Disclose any conflicts of interest

## Elections

Community representatives on the Steering Committee will be elected by the collective Organization Members
of the OCM project, as defined in the Contributor Ladder. They
will be elected annually.

Once per year, the Steering Committee will select between two and three Election
Officers to run the annual election and sets the dates for the election. Election
Officers should be project Members in good standing, not running for election
themselves, and represent more than one project employer.

These officers will update the list of eligible Members according to
project records, send out announcements, and conduct the election. The election
starts with a call for nominations, which lasts for at least one week, and will
include a period for project Members to request changes to their voting status.
Candidates may nominate themselves, or they may be nominated by other members of the community.

The election itself will last for at least one week, and is conducted as a
preference election online, using a method such as Condorcet or IRV. The
Election Officers will announce the selected candidates at the next regular
community meeting.

## Decision Making

The Steering Committee (SC) serves as a decision-making body for both technical and non-technical matters, often responding to requests from project Maintainers and Contributors.

The Steering Committee follows these decision-making principles:

**Consensus-Driven Approach**

- Primary focus is on reaching consensus through discussion.
- Multiple revision iterations are common and encouraged.
- Goal is to minimize major objections rather than achieve unanimous agreement.

**Voting Protocol**

- Voting is considered a last resort.
- Used only when consensus cannot be reached.
- Recognizes that voting may leave significant concerns unaddressed.

**Procedural Decisions**

- Some decisions can be approved asynchronously via GitHub.
- Requires approval from 2/3 of SC members.
- Any SC member can request a meeting for further discussion.
- When a meeting is called, standard consensus process applies.

**Community Participation**

- Non-SC members are welcome to provide feedback.
- Community feedback is considered non-binding but valuable.

# Security

## Security Response Team

Open Cluster Management maintains a Security Response Team responsible for coordinating security-related activities:

**Core Responsibilities:**
- Receive and triage security vulnerability reports
- Coordinate with maintainers to develop fixes
- Manage security advisory process
- Ensure timely communication to users about security issues

**Current Security Response Team Members:**
- TODO: Add security team members with contact information

## Reporting Security Issues

**For Core Project:**
Security vulnerabilities should be reported privately to the Security Response Team at: security@open-cluster-management.io

**For Subprojects:**
- If the subproject has defined its own security contact, report to that contact
- Otherwise, report to the main OCM Security Response Team who will coordinate with project maintainers

## Security Process

1. **Initial Report**: Security issues are reported privately to avoid public disclosure before fixes are available
2. **Acknowledgment**: The Security Response Team acknowledges receipt within 48 hours
3. **Assessment**: Team assesses the severity and impact of the reported issue
4. **Coordination**: Team works with relevant maintainers to develop and test fixes
5. **Disclosure**: Public disclosure follows responsible disclosure practices, typically after fixes are available
6. **Post-Incident**: Team conducts post-incident review to improve security processes

## Security Requirements

**For Core Project:**
- Must follow OCM security guidelines and processes
- Required to participate in security reviews and assessments
- Must implement security best practices in code and infrastructure
- Required to respond to security issues within defined SLAs

**For Subprojects:**
- Encouraged to follow OCM security guidelines
- Must report security issues that could affect the broader OCM ecosystem
- Responsible for their own security practices and incident response

# Release Process

## Core Project Releases

The core project follows coordinated release cycles to ensure compatibility and stability:

**Release Schedule:**
- Major releases: Every 6 months (aligned with Kubernetes release cycle)
- Minor releases: Monthly or as needed for important features
- Patch releases: As needed for bug fixes and security updates

**Release Requirements:**
- All releases must pass comprehensive test suites
- Breaking changes require migration guides and deprecation notices
- Security patches receive priority and expedited release process
- Release notes must document all changes and compatibility impacts

**Version Compatibility:**
- Core project components maintain API compatibility within major versions
- Deprecation policy provides at least one major version notice before removal
- Cross-component compatibility is tested and documented

## Subproject Releases

Subprojects manage their own release cycles:

**Flexibility:**
- Project maintainers determine release schedules and versioning schemes
- No requirement to coordinate with core OCM releases
- Encouraged to document compatibility with OCM versions

**Quality Standards:**
- Projects are encouraged to follow semantic versioning
- Should provide clear documentation of breaking changes
- Recommended to maintain some level of backward compatibility

# Code of Conduct

This project follows the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/main/code-of-conduct.md).
Any code of conduct violations should be reported to the org maintainers.

For violations involving an org maintainer, the accused maintainer will be recused from the investigation process.
These cases must be escalated to the appropriate CNCF contact, who may intervene as needed.

## Code of Conduct Committee

The Steering Committee appoints a Code of Conduct Committee (CoCC) to handle Code of Conduct violations:

**Responsibilities:**
- Receive and investigate Code of Conduct violation reports
- Determine appropriate responses to violations
- Maintain confidentiality of reports and investigations
- Provide recommendations to the Steering Committee for serious violations

**Current Code of Conduct Committee Members:**
- TODO: Add CoCC members with contact information

# Communication Channels

Open Cluster Management maintains several communication channels for different purposes:

## Public Channels

- **GitHub Discussions**: [OCM Community Discussions](https://github.com/open-cluster-management-io/community/discussions) - General community discussions
- **Slack**: [CNCF Slack #open-cluster-mgmt](https://cloud-native.slack.com/channels/open-cluster-mgmt) - Real-time community chat
- **Mailing List**: TODO: Add mailing list information
- **Community Meetings**: Monthly community meetings (calendar link: TODO)

## Project-Specific Channels

Each subproject may maintain its own communication channels as documented in their respective repositories.

## Private Channels

- **Security Reports**: security@open-cluster-management.io
- **Code of Conduct Reports**: conduct@open-cluster-management.io
- **Steering Committee**: steering@open-cluster-management.io

# Amendments

This governance document may be amended by a 2/3 majority vote of the Steering Committee.

**Amendment Process:**
1. Proposed amendments must be circulated to the community for comment at least one week before voting
2. The Steering Committee will consider community feedback before voting
3. Amendments take effect immediately upon approval unless otherwise specified
4. All amendments will be documented in the project's governance history

**Emergency Amendments:**
In cases where immediate action is required for legal, security, or CNCF compliance reasons, amendments may be made with a simple majority vote of available Steering Committee members, with community notification to follow within 48 hours.
