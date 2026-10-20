# Security model (planned)

Third-party plugins are untrusted. GitHub hosting or inclusion in this registry does not establish trust.

The host should:
- Run executable plugin logic in a separately restricted process, not inside the main UI process.
- Expose only versioned, allowlisted IPC APIs with explicit permission checks.
- Default-deny arbitrary filesystem, network, process execution and original-photo modification.
- Ask the user before granting sensitive capabilities; use per-file access grants.
- Validate archive entries against path traversal, symlinks, decompression bombs and oversized payloads.
- Verify exact asset hashes and publisher authenticity where supported; treat hashes as integrity checks only.
- Enforce timeouts, memory budgets, crash isolation, safe mode and rollback.
- Keep `.lumixa` projects openable if a plugin is missing, with clear warnings for effects that cannot be recomputed.

JavaScriptCore alone is not a security sandbox. None of these protections are implemented merely by creating this repository.
