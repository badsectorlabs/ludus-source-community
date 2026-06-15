# Automated submodule updates

Everything this source ships (`ansible/roles/*`, `ansible/collections/*`) is
vendored as a git submodule pointing at the author's repository. The
[`bump-submodules.yml`](./bump-submodules.yml) workflow keeps those pins
current — every run sweeps all submodules and advances each one to its
upstream's **latest release tag**, falling back to the **default-branch HEAD**
for upstreams that don't tag releases:

- a daily `schedule` (08:17 UTC, ~3am US Eastern) picks up whatever upstreams
  have released or merged;
- it can also be run on demand from the Actions tab (`workflow_dispatch`), or:

      gh workflow run bump-submodules.yml -R badsectorlabs/ludus-source-community

The sweep opens (or updates) a single rolling PR on the fixed branch
`automation/bump-submodules`; merging it adopts the new pins. The PR body
lists every pin move — that review is the control point before anything
reaches `main`.
