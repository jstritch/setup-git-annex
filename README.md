# setup-git-annex

Installs git-annex on Linux, macOS, or Windows.
[git-annex](https://git-annex.branchable.com/) is an integrated alternative to storing large files in Git.

## Example

The workflow snippet shown below installs git-annex on Linux, macOS, and Windows.
Setting fail-fast to false allows other jobs in the matrix to continue if any job in the matrix fails.

Once installed, the help command is invoked to demonstrate git-annex is available from the command line.

```yaml
jobs:
  test:

    strategy:
      matrix:
        os:
          - ubuntu-latest
          - macos-latest
          - windows-latest
      fail-fast: false

    runs-on: ${{ matrix.os }}

    steps:
      - uses: actions/checkout@v3
      - uses: jstritch/setup-git-annex@v1
      - run: git annex help
```
