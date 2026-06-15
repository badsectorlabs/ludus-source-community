# Blueprints

Each `blueprints/<id>/` directory is one vendored blueprint — a named, versioned
range config plus its dependency manifest, applied as `<sourceID>/<id>`
(e.g. `ludus blueprint apply my-repo/example`).

## Available blueprints

No community blueprints are vendored yet. The format mirrors the other inventories:

| Blueprint | Description | Link |
|---|---|---|
| _your-blueprint-id_ | _One-line summary_ | _[author/repo](https://github.com/you/repo)_ |

## Build your own

Start from the annotated [blueprint starter in ludus-source-template](https://github.com/badsectorlabs/ludus-source-template/tree/main/blueprints) —
it documents `blueprint.yml`, `requirements.yml`, and versioning. Then open a PR
to vendor it here: see [Contributing](../README.md#contributing).

## Inspiration

Browse production blueprints (GOAD, AD + Elastic) in [ludus-source-bsl](https://github.com/badsectorlabs/ludus-source-bsl/tree/main/blueprints).

## Not vendored

Community range configs that aren't packaged as blueprints — copy and adapt directly:

- [jessefmoore/Ludus-Ranges](https://github.com/jessefmoore/Ludus-Ranges) — ready-made range configs to copy and adapt
