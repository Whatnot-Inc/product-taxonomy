# Whatnot Product Taxonomy

The public, machine-readable catalog of Whatnot's product taxonomy — the category tree that
organizes products across the Whatnot marketplace. It is published automatically from Whatnot's
internal source of truth; this repository is generated, not hand-edited.

## Table of Contents

- [Data](#data)
- [Versioning](#versioning)
- [Changelog](#changelog)
- [Contributing](#contributing)
- [License](#license)

## Data

The taxonomy is published in two equivalent formats under [`data/`](data):

- [`data/taxonomy.yml`](data/taxonomy.yml)
- [`data/taxonomy.json`](data/taxonomy.json)

Each entry describes a category:

| Field | Type | Description |
| --- | --- | --- |
| `id` | number | Stable category identifier. |
| `type` | string | Machine-readable category slug. |
| `label` | string | Human-readable display name. |
| `parent_id` | number \| null | Parent category `id`; `null` for top-level categories. |
| `allows_inventory` | boolean | Whether the category accepts inventory (present where applicable). |

The top-level `version` field is the published semantic version of the taxonomy.

## Versioning

The published `version` follows [semantic versioning](https://semver.org):

- **major** — a field was removed from the taxonomy shape.
- **minor** — a field was added to the taxonomy shape.
- **patch** — the data changed (categories added, removed, or edited).

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for the history of published versions.

## Contributing

Thanks for your interest! This repository is generated automatically from Whatnot's internal
taxonomy, so we are **not currently accepting external contributions** — please don't open issues
or pull requests against it. If something looks wrong, feel free to fork and explore.

## License

Released under the [MIT License](LICENSE).
