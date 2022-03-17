# SIG Policy charter

## Scope

The Policy SIG covers governance capability, security remediation, and configuration management for the Open Cluster
Management (OCM) project.

In particular, it currently includes the OCM Policy Framework, which is responsible for top-level `Policy` objects and
syncing those objects between the Hub and managed clusters. It additionally includes the controllers that process the
down-level policies such as `ConfigurationPolicy`.

### In scope

#### Code, Binaries and Services

- Review and approve policy related OCM enhancements.
- The APIs in the `policy.open-cluster-management.io` API group. The API versioning and deprecation strategy
  follows the OCM
  [graduation criteria](https://github.com/open-cluster-management-io/enhancements/tree/main/guidelines#graduation-criteria).
- Tools and documentation to aid in ecosystem tool interoperability around policy (e.g. Policy Generator).
- Enhancements that affect security and scalability will often be discussed at the OCM community level.

#### Cross-cutting and Externally Facing Processes

- A discussion platform for solving OCM policy related development and management problems.
- Represent the needs and persona of OCM policy developers and operators.

### Out of scope

SIG Policy scope does not include:

- Any non policy related OCM projects.
- Private vulnerability response (belongs to the PSC), including:
    - Embargoed vulnerability management
    - Bug bounty submission triage and management
    - Non-public vulnerability collection, triage, and disclosure
- Security audit for all other OCM components.

### Additional responsibilities of Chairs

- Report the Project status at events and community meetings, when possible.
- Actively promote diversity and inclusion in the Community.
- Uphold the Code of Conduct, especially in terms of personal behavior and responsibility.
