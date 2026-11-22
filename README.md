# ND Image Converter Engine Feed

This public repository hosts **staging-only** Media Engine update metadata and
immutable, non-sensitive release assets for ND Image Converter.

It is not a production update channel. The staging manifest is available at:

`https://github.com/duongtruongdp/ND-ImgConverter-Engine-Feed/raw/refs/heads/main/manifests/staging/manifest.json`

The application retrieves engine artifacts anonymously from immutable GitHub
Release URLs. No GitHub login or token is required. Private signing material
and publisher controls remain in
[`ND-ImgConverter-Engines`](https://github.com/duongtruongdp/ND-ImgConverter-Engines).

## Release rules

- Every release tag is immutable and identifies one reviewed staging set.
- Artifacts are uploaded and publicly verified before the manifest is updated.
- The manifest is signed with the staging Ed25519 identity and published last.
- Manifest revisions are monotonic and expire after the documented validity window.
- Production keys, production manifests and application releases are never published here.

See `docs/staging-feed.md`, `docs/integrity-verification.md` and
`docs/third-party-notices.md`.
