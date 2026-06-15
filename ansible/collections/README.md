# Collections

Each directory here is a community-built Ansible collection, vendored as a git submodule pinned to its author's repository. A collection's identity is the FQCN (`namespace.name`) from its `galaxy.yml` — the directory name is cosmetic. Reference a collection role in a range config's `roles:` list as `<namespace>.<collection>.<role>`.

| Collection | Description | Upstream |
|---|---|---|
| `bagelbyt3s.ludus_adfs` | An Ansible collection that installs an ADFS deployment with optional configurations. | [bagelByt3s/ludus_adfs](https://github.com/bagelByt3s/ludus_adfs) |
| `inf0junki3.ludus` | A collection of roles for your ludus cyber-range | [Inf0Junki3/inf0junki3.ludus](https://github.com/Inf0Junki3/inf0junki3.ludus) |
| `professor_moody.ludus_scorch` | An Ansible collection that installs a SCORCH (System Center Orchestrator) deployment with optional configurations for security testing with Ludus. | [professor-moody/ludus_scorch](https://github.com/professor-moody/ludus_scorch) |
| `synzack.ludus_sccm` | An Ansible collection that installs an SCCM deployment with optional configurations. | [Synzack/ludus_sccm](https://github.com/Synzack/ludus_sccm) |

## Build your own

Start from the annotated [collection starter in ludus-source-template](https://github.com/badsectorlabs/ludus-source-template/tree/main/ansible/collections), then open a PR to vendor it here — see [Contributing](../../README.md#contributing).

## Inspiration

Browse the official Bad Sector Labs collections in [ludus-source-bsl](https://github.com/badsectorlabs/ludus-source-bsl/tree/main/ansible/collections).
