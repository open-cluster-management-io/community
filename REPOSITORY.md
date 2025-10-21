# Open Cluster Management Repositories Guidelines

This document attempts to outline a structure for creating GitHub repositories
with the Open-Cluster-Management project. It also describes how and when repositories
are removed. It is in the best interests of everyone involved in the 
Open-Cluster-Management community that our various projects and repositories are active
and healthy. This ensures a clear clarification of goal/non-goal of the repositories,
ensures the maintainers working with stable commitment, ensures a rapid response
to potential required fixes (e.g. critical security problems) and (most importantly)
it ensures that contributors and users receive quick feedback on their issues and contributions.

## Rules for New Repositories

* All repos will live in github.com/open-cluster-management-io/\<project-name\>.
* Have a mission of Kubernetes cluster and multicluster management;
* Must contain the topic for the sponsoring subprojects - e.g. application. (Added through the Manage topics link on the repo page.)
* Must adopt the Open-Cluster-Management Code of Conduct.
* All code projects use the Apache License version 2.0.
* All OWNERS of the project must also be active Open-Cluster-Management members.
* Must be approved by the following process.
  1. It has been discussed and recognized in the community meeting with a
   publicly linkable written decision.
  2. It must have two sponsors, each of whom must be the maintainer of a sub project.
  3. A repository onboarding issue is created under this repo.

## Review process

The Steering Committee together with project sponsors will then review the
application, and decide whether or not to accept it.  If it is accepted, the Committee
will assign one person to assist the Subproject in their integration.

In some cases, promising but incomplete projects may be accepted as Experimental
Subprojects.  Such Experimental Subprojects will be considered part of
Open Cluster Management, but will be marked as Experimental on the website and in code
repositories, in order to inform users.  Experimental Subproject Members are considered
Members of Open Cluster Management, but the Subproject is not entitled to a representative on the
Steering Committee.  Steering will review Experimental Subprojects at least twice
per year to determine if they have matured to full Subproject status.

## Removing Repositories

As important as it is to add new repositories, it is equally important to prune
old repositories that are no longer relevant or useful. 

### Grounds for removal

Repositories may be removed from the project if they
are deemed _inactive_. Inactive repositories are those that meet any of the
following criteria:

   * There are no longer any active maintainers for the project and no
     replacements can be found.
   * All PRs or Issues have gone un-addressed for longer than six months.
   * There have been no new commits or other changes in more than a year.
   * The contents have been folded into another actively maintained project.

Any Steering Committee member may propose removal of a project on
these grounds, and Steering can confirm this with a majority vote.

Projects which still have contributors will then be moved to a repository in their
own namespace.  Projects which have ceased all activity are moved to an archive namespace.