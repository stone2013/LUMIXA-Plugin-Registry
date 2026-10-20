# Submit a plugin

1. Publish source code and a version-tagged GitHub Release in your own repository.
2. Attach a `.lumixaplugin` asset, describe its permissions and supported LUMIXA Plugin API version, and publish its SHA-256 digest.
3. Open a pull request adding an entry to `registry.json` with a link to the release, a changelog, screenshots and a reproducible test description.
4. Maintainers review metadata, permission scope, compatibility and package integrity before merging.
5. Updates require a new immutable release and a registry change.

Review and inclusion are not security guarantees. Never embed secrets or user data in plugin submissions.
