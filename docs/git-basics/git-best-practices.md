# Git Best Practices

Here's the rundown of some of widely recommended practices for using Git based on general expertise
and insights from the developer community.

1. Commit early and often (with meaningful messages).
2. Use branches strategically.
3. Pull and merge regularly.
4. Leverage `.gitignore`.
5. Review code before merging.
6. Tag releases
7. Backup and sync with remotes.
8. Use Git tools and aliases.
9. Keep history clean.
10. Document your workflow.

## Commit early and often

- Make small, focused commits that address one logical change at a time (e.g., fixing a bug, adding
  a feature, refactoring code, etc.)
- Write clear and concise commit messages that describe the changes made.
- Use the present tense in the commit message (e.g., "Add feature X" instead of "Added feature X").
- Use the imperative mood in the commit message (e.g., "Fix bug" instead of "Fixed bug").

A common format is:

```text
<type>(<scope (optional)>): <short  summary (50 chars or less)>
<blank line>
<detailed explanation (wrap at 72 characters), if needed>
```

Examples:

```text
feat(ui): add new button to toggle dark mode
```

```text
fix(api): fix bug in user authentication
```

```text
refactor(auth): improve user authentication code

Refactored user authentication code to use a more secure method.
```

See [Writing good commit messages](https://www.conventionalcommits.org/en/v1.0.0/#summary) to learn
how to write better commit messages.

## Use branches strategically

- Keep the `main` (or `master`) branch stable and production-ready.  Avoid committing directly to it.
- Create feature branches for new work (e.g., `feature/add-login-page`), bug fixes (e.g.,
  `fix/bugs-123`), or experiments.  Name them descriptively so that others (and your future self)
  can understand the purpose of the branch at a glance.
- Use a branching strategy like
  [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) or [GitHub
  Flow](https://docs.github.com/en/get-started/quickstart/github-flow) to manage branches.
- Delete branches after merging to keep the repository clean (`git branch -d <branch-name>`).  You
  can also delete branches in the GitHub web interface.

## Pull and merge regularly

- Pull updates from the remote repository (`git pull`) to your local branch regularly to avoid merge conflicts.
- Use `git rebase` to keep a cleaner history when working on your branch, but be cautious if others
  are collaborating on the same branch since rebasing rewrites the commit history.
- Resolve merge conflicts promptly and test thoroughly after merging.
- Merge branches back into the `main` (or `master`) branch regularly to keep the branch history
  clean and up to date.
- Use the squash merge option when merging branches to keep the commit history clean.

## Leverage `.gitignore`

- Exclude files that shouldn't be tracked (e.g., build artifacts, local config files, IDE settings,
  logs).  Use a `.gitignore` file trailored to your project.  There are templates available online,
  and GitHub offers a wide variety of templates for different languages and frameworks when you
  create a new repository.
- Use the `git add -f` command to force add files that are ignored by `.gitignore`.
- Example `.gitignore`:

```text
# Ignore all files in the build directory
build/

# Ignore all logs
*.log

# Igore node modules
node_modules/

# Ignore all files in the temp directory
temp/*
```

## Review code before merging

- Use GitHub pull requests (PRs).  This ensures code is reviewed by peers.
- Use branch protection rules to enforce code reviews and prevent direct merges into `main` (or
  `master`).
- Test your changes locally before submitting a PR.
- Keep PRs small and focused (e.g., one feature or bug fix).
- Write a detailed PR description that includes the changes made and the rationale behind them.
- Use the squash merge option when merging branches to keep the commit history clean.

## Tag releases

- Use annotated tags for releases or significant milestones (`git tag -a v1.0.0 -m "Release
  1.0.0"`).  This helps track stable versions for your project.
- Push tags to the remote repository (`git push origin v1.0.0`).
- Use the GitHub web interface to create releases from tags.  For more advanced users, [automate the
  release process](https://docs.github.com/en/repositories/releasing-projects-on-github/automating-releases-with-github-actions).

## Backup and sync with remotes

- Regularly push your local branch to the remote repository (`git push origin <branch-name>`).  This
  acts as a backup and enables collaboration.
- Avoid force-pushing (`git push --force`) to the remote repository unless absolutely necessary, as
  it overwrites history and can disrupt others.  You can prevent force-pushes with a branch
  protection rule or a pre-receive hook.
- Regularly pull updates from the remote repository (`git pull`).

## Use Git tools and aliases

- Learn commands like `git log`, `git blame`, and `git diff` to understand changes.
- Set up aliases for frequent commands in your `.gitconfig` file.  Example:

```text
[alias]
  co = checkout
  cm = commit
  st = status
```

- Use `git stash` to temporarily save uncommitted changes when switching branches.
- Familiarize yourself with `git reset`, `git revert`, and `git reflog`, to recover from errors.
- Use `git bisect` to find the commit that introduced a bug.
- Use `git cherry-pick` to apply specific commits from one branch to another.
- Use `git rebase` to keep a cleaner history when working on your branch.

## Keep history clean

- Squash unnecessary commits before merging  (`git rebase -i`) to maintain a readable history.
- Avoid committing sensitive data (e.g., API keys, passwords, etc.) in the repository.  Use
  environment variables or a secrets manager instead.  If it happens, use `git filter-branch` to
  remove the sensitive data.

## Document your workflow

- Agree on a team workflow (e.g., Git Flow) and document it in a `README.md` or wiki.
- Include setup instructions, branching rules, and contribution guidelines.
