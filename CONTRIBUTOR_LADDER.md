# Contributor Ladder Template

* [Contributor Ladder](#contributor-ladder-template)
    * [Contributor](#contributor)
    * [Organization Member](#organization-member)
    * [Reviewer](#reviewer)
    * [Maintainer](#maintainer)
    * [Core Maintainer](#core-maintainer)
* [Inactivity](#inactivity)
* [Involuntary Removal](#involuntary-removal-or-demotion)
* [Stepping Down/Emeritus Process](#stepping-downemeritus-process)
* [Contact](#contact)


## Contributor Ladder

Hello! We are excited that you want to learn more about our project contributor ladder! This contributor ladder outlines the different contributor roles within the project, along with the responsibilities and privileges that come with them. Community members generally start at the first levels of the "ladder" and advance up it as their involvement in the project grows.  Our project members are happy to help you advance along the contributor ladder.

Each of the contributor roles below is organized into lists of three types of things. "Responsibilities" are things that contributor is expected to do. "Requirements" are qualifications a person needs to meet to be in that role, and "Privileges" are things contributors on that level are entitled to.

Open Cluster Management (OCM) is a project made up of several Subprojects, such as Foundation and Policy.  This contributor ladder applies to each Subproject.  As such, a contributor advances in each Subproject separately, and may be a Member in one Subproject while being a Maintainer in another.  For the Open Cluster Management project overall, the contributor is considered to be the highest level they have reached in any Subproject.  Thus, someone who is a Project Member in one Subproject is a Project Member of OCM overall.

| Role | Responsibilities | Requirements | Privileges |
| ---- | ---------------- | ------------ | ---------- |
| [Contributor](#contributor) | Casual contributor to the project | n/a | Invitations to contributor events, Eligible to become an Organization Member |
| [Organization Member](#organization-member) | Regular active contributor in the community | Has pushed at least one PR to an open-cluster-management-io repository | Can recommend a contributor to become a member |
| [Reviewer](#reviewer) | Hold expertise of a repo or a specific area | Need to review PRs | Can recommend a member to become a reviewer |
| [Maintainer](#maintainer) | Reviewing at least 20 PRs per year, especially PRs that involve multiple parts of the project, Participating in, and leading, community meetings | Experience as a Reviewer for at least 3 months, Can commit to spending at least 15 hours per month working on the project | Added to the OWNERs file in one or more Subprojects, and recommand a reviewer to become a maintainer |

### Contributor

Description: A Contributor contributes directly to the project and adds value to it. Contributions need not be code. People at the Contributor level may be new contributors, or they may only contribute occasionally.

* Responsibilities include:
    * Follow the CNCF CoC
    * Follow the project contributing guide
* Requirements (one or several of the below):
    * Sign the DCO for Open Cluster Management, either individually or through their employer
    * Report and sometimes resolve issues
    * Occasionally submit PRs
    * Contribute to the documentation
    * Show up at meetings, takes notes
    * Answer questions from other community members
    * Submit feedback on issues and PRs
    * Test releases and patches and submit reviews
    * Run or helps run events
    * Promote the project in public
    * Help run the project infrastructure
* Privileges:
    * Invitations to contributor events
    * Eligible to become an Organization Member


### Organization Member
Description: An Organization Member is an established contributor who regularly participates in the project. Organization Members have privileges in both project repositories and elections, and as such are expected to act in the interests of the whole project. While Organization Members are selected by individual subprojects, some of their requirements and privileges apply to the entire OCM project.

An Organization Member must meet the responsibilities and has the requirements of a Contributor, plus:

* Requirements:
    * Contribute at least 1 PR within the last 6 months
    * Attend to community meetings

* Privileges:
    * May be assigned Issues and Reviews
    * May give commands to CI/CD automation
    * Entitled to vote in the [TODO: appropriate election]
    * Can be added to GitHub teams in the Open Cluster Management org
    * Can recommend other contributors to become Org Members

The process for a Contributor to become an Organization Member is as follows:

1. The contributor or an Org Member may propose them for membership in an Issue in the relevant Subproject.  This issue will name at least two existing Org Members (sponsors) who can vouch for the contributor, and will list their existing contributions.
2. Both sponsors will +1 the request.
3. GitHub administrator will add the contributor to the GitHub organization, as well as to the relevant Subproject's general contributor Team.

### Reviewer
Description: A Reviewer has responsibility for specific code, documentation, test, or other project areas. They are collectively responsible, with other Reviewers, for reviewing all changes to those areas and indicating whether those changes are ready to merge. They have a track record of contribution and review in the project.

Reviewers are responsible for a "specific area." This can be a specific code directory, driver, chapter of the docs, test job, event, or other clearly-defined project component that is smaller than an entire repository or subproject. Most often it is one or a set of directories in one or more Git repositories. The "specific area" below refers to this area of responsibility.

Reviewers have all the rights and responsibilities of an Organization Member, plus:

* Responsibilities include:
    * Following the reviewing guide
    * Reviewing most Pull Requests against their specific areas of responsibility
    * Reviewing at least 10 PRs per year
    * Helping other contributors become reviewers
* Requirements:
    * Experience as a Contributor for at least 3 months
    * Is an Organization Member
    * Has reviewed, or helped review, at least 10 Pull Requests
    * Has analyzed and resolved test failures in their specific area
    * Has demonstrated an in-depth knowledge of the specific area
    * Commits to being responsible for that specific area
    * Is supportive of new and occasional contributors and helps get useful PRs in shape to commit
* Additional privileges:
    * Has GitHub or CI/CD rights to approve pull requests in specific directories
    * Can recommend and review other contributors to become Reviewers

The process of becoming a Reviewer is:
1. The contributor is nominated by opening a PR against the appropriate repository, which adds their GitHub username to the OWNERS file for one or more directories.
2. At least two members of the team that owns that repository or main directory, who are already Approvers, approve the PR.

### Maintainer
Description: Maintainers are very established contributors who are responsible for one or more Subprojects. As such, they have the ability to approve PRs against any area of that Subproject, and are expected to participate in making decisions about the strategy and priorities of that Subproject and Open Cluster Management as a whole.

A Maintainer must meet the responsibilities and requirements of a Reviewer, plus:

* Responsibilities include:
    * Reviewing at least 20 PRs per year, especially PRs that involve multiple parts of the project
    * Mentoring new Reviewers
    * Writing refactoring PRs
    * Participating in CNCF maintainer activities
    * Determining strategy and policy for the project
    * Participating in, and leading, community meetings
* Requirements
    * Experience as a Reviewer for at least 3 months
    * Demonstrates a broad knowledge of the project across multiple areas
    * Is able to exercise judgement for the good of the project, independent of their employer, friends, or team
    * Mentors other contributors
    * Can commit to spending at least 15 hours per month working on the project
* Additional privileges:
    * Added to root OWNERs file in one or more Subprojects
    * Approve PRs to any area of those Subprojects
    * Represent the project in public as a Maintainer
    * Communicate with the CNCF on behalf of the project
    * Have a vote in Maintainer decision-making meetings


Process of becoming a maintainer:
1. Any current Maintainer may nominate a current Reviewer to become a new Maintainer, by opening a PR against the root of the Subproject's primary repository, adding the nominee as an Approver in the OWNERS file.
2. The nominee will add a comment to the PR testifying that they agree to all requirements of becoming a Maintainer.
3. A majority of the current Maintainers of that Subproject must then approve the PR.

### Core Maintainer
Description: Core Maintainers are Maintainers of the Project (core) components with additional responsibilities for the overall stability and strategic direction of Open Cluster Management. They are responsible for maintaining the core foundation components that other projects depend on, and must commit to OCM's stability and compatibility guarantees.

A Core Maintainer must meet the responsibilities and requirements of a Maintainer, plus:

* Responsibilities include:
    * Maintaining core project components (OCM, API, Clusteradm, Addon Framework, SDK)
    * Ensuring version compatibility guarantees and migration paths
    * Making technical decisions on core project changes and implementations
    * Responding to security compromise reports according to OCM security procedures
    * Participating in cross-project coordination
    * Helping define overall project direction and strategy
    * Mentoring other maintainers and contributors across the project
* Requirements:
    * Experience as a Maintainer for at least 6 months
    * Demonstrated exceptional technical and leadership contributions to core functionality
    * Deep understanding of OCM architecture and core components
    * Commitment to OCM's stability and compatibility guarantees
    * Ability to make decisions for the good of the entire project ecosystem
    * Can commit to spending at least 20 hours per month working on core project activities
* Additional privileges:
    * Participate in core project governance decisions
    * Help define overall project direction and roadmap
    * Represent the project in strategic discussions
    * Vote on core project technical decisions
    * Mentor and guide the development of other maintainers

Process of becoming a Core Maintainer:
1. Any current Core Maintainer may nominate a current Maintainer to become a Core Maintainer.
2. The nomination should include evidence of exceptional contributions to core functionality and leadership within the project.
3. The nominee will add a comment testifying that they agree to all requirements of becoming a Core Maintainer.
4. A majority of the current Core Maintainers must approve the nomination.


## Inactivity
It is important for contributors to be and stay active to set an example and show commitment to the project. Inactivity is harmful to the project as it may lead to unexpected delays, contributor attrition, and a loss of trust in the project.

* Inactivity is measured by:
    * Periods of no contributions for longer than **18** months
    * Unannounced periods of no communication for longer than **4** months
* Consequences of being inactive include:
    * Involuntary removal or demotion
    * Being asked to move to Emeritus status

## Involuntary Removal or Demotion

Involuntary removal/demotion of a contributor happens when responsibilities and requirements aren't being met. This may include repeated patterns of inactivity, extended period of inactivity, a period of failing to meet the requirements of your role, and/or a violation of the Code of Conduct. This process is important because it protects the community and its deliverables while also opens up opportunities for new contributors to step in.

Involuntary removal or demotion is handled through a vote by a majority of the current Maintainers of the relevant Subproject, or in some cases a majority of all Maintainers for OCM.

## Stepping Down/Emeritus Process
If and when contributors' commitment levels change, contributors can consider stepping down (moving down the contributor ladder) vs moving to emeritus status (completely stepping away from the project).

Contact the Maintainers about changing to Emeritus status, or reducing your contributor level.
