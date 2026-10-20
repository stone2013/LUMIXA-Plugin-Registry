# LUMIXA Plugin Registry

Community plugin index and developer resources for **LUMIXA Lite**.

> Status: planning / early development. No plugins are currently published in this registry. Listing a plugin does not automatically make it trusted.

## Goals
- Discover plugins in the LUMIXA Lite Plugin Hub.
- Download versioned `.lumixaplugin` assets from GitHub Releases.
- Check compatibility, integrity and declared permissions before installation.
- Support local offline installation without an account.

## Repository contents
- [registry.json](registry.json): machine-readable index (currently empty).
- [docs/registry-format.md](docs/registry-format.md): proposed index schema.
- [docs/submitting-a-plugin.md](docs/submitting-a-plugin.md): submission and review process.
- [docs/security.md](docs/security.md): security requirements and trust limitations.
- [examples/example-entry.json](examples/example-entry.json): illustrative metadata only, **not** an installable plugin.

## How it will work
The desktop app fetches the registry, filters compatible releases, presents permissions, downloads an exact GitHub Release asset, verifies its SHA-256 and (when supported) trusted publisher signature, then installs atomically with rollback. An HTTPS download and SHA-256 value alone do **not** prove publisher authenticity.

## Contributing
Open an issue or pull request with your plugin's GitHub repository and a tagged Release. See the submission guide. Do not submit unreviewed executable binaries directly to this registry.

## Licensing
No project-wide license has been selected yet. Do not assume that the code or documentation is licensed for reuse until a license is added.
