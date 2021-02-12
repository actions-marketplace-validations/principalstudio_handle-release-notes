# handle-release-notes

A very opiniated GitHub action to handle release notes and milestones via [github-release-notes](https://github.com/github-tools/github-release-notes).

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
      - name: checkout
        uses: actions/checkout@v2
      - name: setup-node
        uses: actions/setup-node@v1
      - name: handle-release-notes
        uses: principalstudio/handle-release-notes@v2
        with:
          main-branch: master
          token: ${{ secrets.GITHUB_TOKEN }}
```