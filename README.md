# Ludus Community Source

Community-built [Ludus](https://ludus.cloud) content in one [source](https://docs.ludus.cloud/docs/using-ludus/sources); vendored here as git submodules pinned to their authors' releases.

```bash
ludus source add https://github.com/badsectorlabs/ludus-source-community
```

> [!IMPORTANT]
> Every entry remains its author's project: issues and PRs about their behavior belong upstream; this repo only aggregates and pins.

## Contributing

To add your role, collection, template, or blueprint, open a PR that adds it as a submodule:

```bash
# roles: the directory name IS the role name users reference in range configs.
# Use your Galaxy name (author.role) if published to Galaxy, else your repo name.
git submodule add https://github.com/<you>/<repo>.git ansible/roles/<role_name>

# collections: identity comes from galaxy.yml, the directory name is cosmetic
git submodule add https://github.com/<you>/<repo>.git ansible/collections/<repo>

# templates: one Packer template per repo, the directory name is cosmetic
git submodule add https://github.com/<you>/<repo>.git templates/<name>

# blueprints: identity is the id in blueprint.yml, the directory name is cosmetic
git submodule add https://github.com/<you>/<repo>.git blueprints/<id>
```

Requirements: the repo root must be the content itself — a single role (`tasks/` and `meta/main.yml` at the top level), a collection (`galaxy.yml` at the top level), a single Packer template, or a blueprint (`blueprint.yml`, `range-config.yml`, and `requirements.yml` at the top level). Tag releases (`v1.2.3` or `1.2.3`) and pins follow your latest tag; if you don't tag, pins track your default branch — so keep it deployable.

## Versioning

Each submodule pins a specific upstream commit, so a given commit of this repo is a reproducible snapshot. A [daily automation](.github/workflows/README.md) advances every pin — to the upstream's latest release tag, or to its default-branch HEAD when it doesn't tag releases — through a single human-reviewed PR. Re-running `ludus source add` (or `ludus source sync`) after this repo updates picks up the new pins.

## Licenses

Each vendored project remains under its own author's license — this repo holds pointers (submodules), not copies. The aggregation files themselves are MIT.
