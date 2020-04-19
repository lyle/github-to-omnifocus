# Add GitHub Issues to Omnifocus

A script to add GitHub issues that are assigned to you to your
Omnifocus task list.

## Using

Create `~/.github-to-omnifocus.toml`. This must contain a value for `auth_token`
file in the `[github]` table.

The following values are the defaults; you can leave out these values if they
are correct for your use-case. As mentioned, the only value that must be
specified is `auth_token`.

```toml
[github]
api_url = "https://api.github.com"
auth_token = ""  # App will fail to launch if this isn't set

[omnifocus]
tag = "github"
issue_project = "GitHub Issues"
pr_project = "GitHub PRs"
```

- Auth token can be generated at https://github.com/settings/tokens. They
    should have `notifications`, `repo` and `user` scope. Strictly
    `notifications` is not required, but it's a feature I'd like to add.
- Using the same project name for `issue_project` and `pr_project` isn't supported
  right now.
- The `api_url` for a GitHub Enterprise install will look something like
  `https://github.mycompany.com/api/v3`.
