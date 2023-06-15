# Addon Development Guidelines

We welcome any addon contributions into the Open Cluster Management (OCM) community!

This document outlines a structure for developing an addon in the OCM project.
This ensures a clear clarification of goals/non-goals of addons,
ensures the addon maintainers working with stable commitment, ensures a rapid response
to potential required fixes (e.g. critical security problems) and (most importantly)
it ensures that contributors and users receive quick feedback on their issues and contributions.

## Scope of an addon

- The addon must provide management capability over multiple Kubernetes clusters.
- It can be a brand new project or an integration with an existing project.
- The addon should adopt [addon APIs](https://open-cluster-management.io/concepts/addon/) for management.

## Rules for New Addons

* The name of an addon code repo in github.com/open-cluster-management-io must have `-addon` as the suffix
* The addon repo must adopt the OCM Code of Conduct.
* All addon projects must use the Apache License version 2.0.
* OWNERS of the addon project must also be active OCM members.
* Must be approved by the following process:
  1. It has been discussed and recognized in the community meeting with a publicly linkable written decision.
  2. It must have two sponsors, each of whom must be the maintainer of an existing sub-project.
  3. A repository onboarding issue is created under the community repo.

## Addon Release Cadence

The release of addon projects are not required to be aligned with OCM [release cadence](release.md)

Maintainers of an addon project can decide the release schedule of the addon, but should indicate the supported version
of OCM for each release of the addon.
