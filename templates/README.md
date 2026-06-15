# Packer templates

Each `templates/<name>/` directory is one vendored Packer template for building a VM image.

## Available templates

No community templates are vendored yet. The format mirrors the other inventories:

| Template | Description | Link |
|---|---|---|
| _your-template_ | _One-line summary_ | _[author/repo](https://github.com/you/repo)_ |

## Build your own

Start from the annotated [template starter in ludus-source-template](https://github.com/badsectorlabs/ludus-source-template/tree/main/templates), then open a PR
to vendor it here: see [Contributing](../README.md#contributing).

## Inspiration

Browse the official Bad Sector Labs templates in [ludus-source-bsl](https://github.com/badsectorlabs/ludus-source-bsl/tree/main/templates).

## Not vendored

These projects bundle several templates per repository, so they can't be vendored as single-template submodules — grab them directly:

- [Croko-fr/ludus-templates](https://github.com/Croko-fr/ludus-templates) — French-localized Packer templates (AlmaLinux, CentOS, Debian, Kali, Rocky, Ubuntu, Windows)
- [Patrick-DE/Ludus-TPM-Templates](https://github.com/Patrick-DE/Ludus-TPM-Templates) — TPM-enabled Packer templates (Win11 24H2, Server 2025)
