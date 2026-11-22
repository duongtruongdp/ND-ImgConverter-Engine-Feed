# Integrity verification

The staging client verifies, in order:

1. HTTPS and the configured manifest host.
2. Manifest schema, staging channel, key ID and Ed25519 signature.
3. Publication and expiry window plus monotonic revision.
4. Engine package identity, target platform and architecture.
5. Artifact byte size and SHA-256.
6. Executable health using the engine-specific version command.

A manifest is published only after all referenced release assets return
anonymous HTTPS success. The feed repository stores the signed manifest and
non-sensitive metadata only; private keys never appear here.
