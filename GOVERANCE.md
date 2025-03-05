# Open Cluster Management Project Governance

## Table of Contents

- [Values](#values)
- [Project Governance](#project-governance)
  - [Adding New Subprojects](#adding-new-subprojects)
  - [Removing Projects](#removing-projects)
- [Steering Committee](#steering-committee)
  - [Duties](#duties)
  - [Members](#members)
  - [Elections](#elections)
  - [Decision Making](#decision-making)
- [Code of Conduct](#code-of-conduct)

# Values

Open Cluster Management and its leadership embrace the following values:

- Openness: Open Cluster Management is an open source community driven project.
- Distributed design: Distributed asynchronous ownership, collaboration, communication and decision making are the cornerstones of our world-wide community.
- Fairness: Ideas and contributions are accepted according to their technical merit and alignment with project objectives, scope, and design principles.
- Diversity and inclusion: Everyone are welcome to participate in the Open Cluster Management project regardless of gender, gender identity, sexual orientation, disability, race, ethnicity, age, religion or economic status.

# Project Governance

The project consists of the following Subprojects:

- Registration
- Work
- Scheduling
- Install (operator and CLI)
- Addon Framework
- Extensions (including all developed addons and other extensions)

All active Maintainers of each Subproject, as defined in the Contributor Ladder, are
members of that project's Maintainer Committee, which governs that project. The
Subproject's Maintainer Committee is responsible for the following project governance
activities:

- Ensuring that the Subproject creates and publishes regular releases;
- Holding regular, Subproject-wide discussions on issues and planning;
- Monthly review of project contributors for advancement on the Contributor Ladder;
- Making final decisions on Subproject changes that involve controversial trade-offs;
- Responding to security compromise reports;
- Supporting the Code of Conduct within their Subproject and referring violations
  to the Code of Conduct Committee.

Additionally, the project's Maintainer Committee will select, by majority vote, one
representative to the Steering Committee. This representative need not
be a member of the Subproject's Maintainer Committee, and will be replaced or
renewed by the committee annually.

Should a member of the Maintainer Committee cease being active in the Subproject,
violate the Code Of Conduct, or need to be removed for some other reason, they
may be removed by a 2/3 majority vote of the other Committee members, or a
majority vote of the Steering Committee.

## Adding New Subprojects

During the monthly Steering meeting, any project member may recommend projects
to become part of Open Cluster Management. These projects should have the following
characteristics:

- Have a mission of Kubernetes cluster and multicluster management;
- Are appropriately licensed and governed or willing to become so;
- Are under active development;
- Consist of high quality code and designs.

Before submitting an application to the Steering Committee, the applying project
must hold an internal consensus vote of all major contributors to join
Open Cluster Management. The Steering Committee will then review the
application, and decide whether or not to accept it. If it is accepted, the Committee
will assign one person to assist the Subproject in their integration.

In some cases, promising but incomplete projects may be accepted as Experimental
Subprojects. Such Experimental Subprojects will be considered part of
Open Cluster Management, but will be marked as Experimental on the website and in code
repositories, in order to inform users. Experimental Subproject Members are considered
Members of Open Cluster Management, but the Subproject is not entitled to a representative on the
Steering Committee. Steering will review Experimental Subprojects at least twice
per year to determine if they have matured to full Subproject status.

New Subprojects will be initialized with a set of maintainers, reviewers,
contributors, and other roles assigned based on the people doing the work before
the Subproject was accepted. The appropriate contributors will be added as
Organization Members without the regular process.

## Removing Projects

In some cases, projects will become inactive or unmaintainable, or wish to separate
from Open Cluster Management. Any Steering Committee member may propose removal of a project on
these grounds, and Steering can confirm this with a majority vote. The CNCF will
determine which, if any, assets of those subprojects will be removable should a
project leave OCM.

Where possible, projects which still have contributors will then be moved to a
repository in their own namespace. Projects which have ceased all activity are
moved to an archive namespace.

# Steering Committee

The overall Open Cluster Management umbrella project is governed by a Steering Committee(SC).

## Duties

The Steering Committee is responsible for the following tasks, any of which may
be delegated to a person or group selected by the committee:

- Reviewing and deciding on new projects to add to Open Cluster Management.
- Arbitrating inter-project disagreements.
- Selecting the Code of Conduct Committee and ratifying CoC judgements.
- Removing projects which have become inactive.
- Acting on escalated security or code quality issues.
- Resolving issues that individual projects are unable to resolve.
- Administering project infrastructure, intellectual property, and resources.
- Determining overall direction for advocacy and marketing.
- Issuing statements on behalf of Open Cluster Management and its Subprojects.
- Reviewing and approving Contributor Ladder advancement for participants who
  work on the overall umbrella project.

In performance of these duties, the Steering Committee will hold a monthly meeting
that is open to all contributors. The Committee may hold additional, closed meetings
in order to discuss non-public issues such as security exploits, CoC enforcement,
and legal questions.

Steering Committee members are expected to advocate for all of Open Cluster Management, not just
certain projects or corporate sponsors, comply with and support the Code of
Conduct, and be professional and compassionate in all of their dealings with
project participants.

## Memebers

The Steering Committee is currently composed of the following members:

- TODO: Add more members

Emeritus members:

- TODO: Add emeritus members

## Elections

The Community Representative(s) will be elected by the collective Organization Members
of all Subprojects, as defined in the Contributor Ladder. They
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

# Code of Conduct

This project follows the [CNCF Code of Conduct](https://github.com/cncf/foundation/blob/main/code-of-conduct.md).
Any code of conduct violations should be reported to the org maintainers.

For violations involving an org maintainer, the accused maintainer will be recused from the investigation process.
These cases must be escalated to the appropriate CNCF contact, who may intervene as needed.
