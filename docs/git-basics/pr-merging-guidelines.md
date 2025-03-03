# Pull Request Merging Guidelines

Keeping a clean Git history is important for a number of reasons.  It makes it easier to
understand the history of the codebase, it makes it easier to revert changes if necessary, and it
makes it easier to cherry-pick changes onto other branches.

## Merge Requirements

In order to merge a pull request, the following requirements must be met:

- The pull request must be approved by at least one other developer.
- The pull request must pass all automated checks.
- When merging, the pull request must be squashed.

## Squashing Commits

When merging a pull request, the commits should be squashed into a single commit.  This makes the
Git history cleaner and easier to understand.  When squashing commits, the commit message should be
updated to reflect the changes made in the pull request, and should follow the [conventional
commits](https://www.conventionalcommits.org/) specification.  The commit message should be
descriptive and include the issue number if it is related to a specific issue.  Adding a description
of the changes made in the commit message body is optional.

## Examples

Here are some examples of commit messages that follow the conventional commits specification:

### With scope

```text
feat(feature-name): add feature description

- Add feature description
- Add feature description
- Add feature description
- Add feature description
- Add feature description
```

### Without scope

```text
feat: add feature description

- Add feature description
- Add feature description
```

### With issue number

```text
feat: add feature description

- Add feature description
- Add feature description
- Add feature description
- Add feature description
- Add feature description

Closes #123
```

### Commit with subject only

```text
feat: add feature description
```

