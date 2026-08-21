# simple-agent-audit

Warn when agent/AI config files change in a pull request.

## Usage

```yaml
name: Simple Agent Audit
on:
  pull_request:

permissions:
  contents: read
  pull-requests: write

jobs:
  simple-agent-audit:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: dmytropaduchak/simple-agent-audit@v0.1.0
        with:
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

## Develop

```bash
npm install && npm run build
```
