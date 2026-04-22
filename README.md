<img src="https://wcm.io/images/favicon-16@2x.png"/> github-action-release-from-tag
======

Composite GitHub Action that creates a GitHub release from a tag.

Usage example:

```yaml
name: Release from Tag

on:
  push:
    tags:
      - '*'
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - name: Release from Tag
        uses: wcm-io-devops/github-action-release-from-tag@v1
        with:
          body: 'Changes: <url>'
          github-token: ${{ secrets.GITHUB_TOKEN }}
```

For all parameters, see [action.yml](action.yml).
