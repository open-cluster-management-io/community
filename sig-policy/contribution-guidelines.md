# Contribution Guidelines

## Code Changes

### Terms

All contributions to the repository must be submitted under the terms of the
[Apache Public License 2.0](https://www.apache.org/licenses/LICENSE-2.0).

### Certificate of Origin

By contributing to this project, you agree to the Developer Certificate of Origin (DCO). This document was created by
the Linux Kernel community and is a simple statement that you, as a contributor, have the legal right to make the
contribution. See the [DCO](https://github.com/open-cluster-management/community/blob/main/DCO) file for details.

### Code Formatting

All Go code is formatted with `go fmt` among other tools. In the root of the repository, you may run `make fmt` to
automatically run the formatting tools that are required.

Some formatting issues cannot be automatically fixed and these issues are flagged by various linters. You may run
`make lint` in the root of the repository to find any linting errors.

The linters are run on every pull-request.

### Tests

All new code must contain unit tests whenever possible. If the code change is not unit testable, an integration test
must be added. These live in the `test/e2e` directory of the repository and are executed against a running instance of
the component in a Kind cluster.

Both unit and integration tests are run on every pull-request.

### Commit Messages

All commit messages must conform to the standards in the
[Kubernetes commit message guidelines](https://github.com/kubernetes/community/blob/master/contributors/guide/pull-requests.md#commit-message-guidelines).

In addition, the GitHub issue that the issue relates to should be linked at the bottom of the commit message.

You must also sign off your commit to state that you certify the
[DCO](https://github.com/open-cluster-management/community/blob/main/DCO). To certify your commit for DCO, add a line
like the following at the end of your commit message:

```
Signed-off-by: John Smith <john@example.com>
```

This can be done with the `--signoff` option to `git commit`. See the
[Git documentation](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt--s) for details.

### Commit Structure

A commit must encompass only one "logical" change. For example, if a pull-request (PR) fixes a bug but also resolves an
unrelated CI failure, that PR should contain two commits. This is so that the Git history clearly describes what each
change is and why. Additionally, it makes it easier to revert changes since reverting a commit only would revert a
single "logical" change.

### Submitting a Change

Start by filing a GitHub issue describing the bug or feature if one doesn't already exist. If the change is a feature,
please also create a design document in the
[enhancements repository](https://github.com/open-cluster-management-io/enhancements) in the
[enhancements/sig-policy directory](https://github.com/open-cluster-management-io/enhancements/tree/main/enhancements/sig-policy).
One of the maintainers listed in the
[OWNERS file](https://github.com/open-cluster-management-io/enhancements/blob/main/enhancements/sig-policy/OWNERS) will
review the design document.

Then proceed by creating a pull-request (PR). Please make sure you follow the commit guidelines described in this
document. Once the PR is created, Prow (CI tool) will automatically prompt maintainers to review the PR based on the
list in the "OWNERS" file at the root of the repository.

Once the PR is approved, Prow will merge the PR.

For more details on how the code review process works with Prow, you may read the
[Kubernetes code review process](https://github.com/kubernetes/community/blob/master/contributors/guide/owners.md#the-code-review-process).
