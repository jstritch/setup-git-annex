# setup-git-annex

Installs git-annex on Linux, macOS, or Windows.
[git-annex](https://git-annex.branchable.com/) is an integrated alternative to storing large files in Git.

## Example

The workflow snippet shown below installs git-annex on Linux, macOS, and Windows.
Once installed, the help command is invoked to demonstrate git-annex is available from the command line.

```yaml
jobs:
  test:
    runs-on: ${{ matrix.os }}
    strategy:
      matrix:
        os:
          - ubuntu-latest
          - macos-latest
          - windows-latest
    steps:
      - uses: actions/checkout@v3
      - uses: jstritch/setup-git-annex@v1
      - run: git annex help
```
