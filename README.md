# Hello World Website

A basic static Hello World website.

## Run locally

Open `index.html` in a browser, or serve the folder:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000.

## CI

GitHub Actions workflows in `.github/workflows/`:

- **Lint** (`lint.yml`) — runs HTMLHint and Stylelint on every push and PR.
- **Claude PR Review** (`claude-review.yml`) — posts an automated review on each PR. Requires a `CLAUDE_CODE_OAUTH_TOKEN` repository secret (create one with `claude setup-token`).
- **Claude Code** (`claude.yml`) — mention `@claude` in an issue, PR comment, or review to have Claude respond. Uses the same `CLAUDE_CODE_OAUTH_TOKEN` secret.
- **Assign Reviewer** (`assign-reviewer.yml`) — requests review from `razyogevus-rgb` on PRs opened by `razyogev`, and vice versa.
