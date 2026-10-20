# Registry format (proposal, schemaVersion 1)

`registry.json` is a UTF-8 JSON document with `schemaVersion`, `updatedAt` and `plugins`. Each entry identifies a plugin and one or more immutable releases.

Suggested plugin fields:
- `id`: globally unique reverse-domain identifier, e.g. `dev.example.colorlab`
- `name`, `summary`, `author`, `repository`, `category`
- `releases`: array of `version`, `apiVersion`, `minAppVersion`, `minMacOS`, `architectures`, `assetUrl`, `sha256`, `permissions`, and optional `signature`

`assetUrl` must point to a versioned `.lumixaplugin` file attached to a GitHub Release. Never use a moving branch archive as an executable plugin package. Registry clients must reject duplicate IDs, malformed URLs, unsupported versions, mismatched hashes and unauthorized redirects.

Example metadata lives in `examples/example-entry.json` and is **not** included in the live index. This format is a proposal, not yet an implemented or validated application API.
