# permissions-test-repo
GitHub permissions test

## Branches

### Branch protection

Unlike some other Git providers, GitHub does not permit branch protection rule `Require pull request reviews before merging` with the reviewer being the repo owner. Instead, this rule must be temporarily disabled, leaving a window where the protected branch isn't.

### master

Branch protection enabled for branches matching 'master'. Flags set:

- Require pull request reviews before merging
- Require signed commits
- Include administrators

All flags not mentioned are not set.

GitHub does not allow authors to approve their own pull requests (`PR`). If a merge is required, but no other person with appropriate permissions to your repo is available, edit the `Branch protection rule`, disable `Require pull request reviews before merging`, merge the PR, then re-enable `Require pull request reviews before merging`.

### develop

No branch protection rules match this branch name.

## Commit signing

Per [Managing commit signature verification](https://help.github.com/en/github/authenticating-to-github/managing-commit-signature-verification), all commits MUST be signed with a valid key associated with a verified email address.

### Commit signing troubleshooting

If you've added an identity [such as a new email address](https://help.github.com/en/github/authenticating-to-github/associating-an-email-with-your-gpg-key) to your GPG key, you MUST delete your key on GitHub and re-upload it. GitHub will not let you update your key with the new user ID details. GitHub does not have a [public issue tracker](https://github.com/holman/ama/issues/152), however, GitHub user `isaacs` has created one which tries to do the job [here](https://github.com/isaacs/github/issues).

