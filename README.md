# principal-release-notes-action

GitHub action to update release notes in releases and CHANGELOG.md file via [github-release-notes] (https://github.com/github-tools/github-release-notes).

## Usage

```
on:
  release:
    types: [published]

name: Update release

jobs:
  update_release:
    name: Update release
    runs-on: ubuntu-latest
    steps:
      - name: Checkout code
        uses: actions/checkout@v2
      - name: Setup node/npm
        uses: actions/setup-node@v1
      - name: Setup node/npm
        uses: actions/principal-post-release-action@v1
        with:
          main-branch: master
```