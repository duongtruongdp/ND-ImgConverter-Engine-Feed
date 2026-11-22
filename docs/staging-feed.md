# Staging feed contract

The current manifest endpoint is:

`https://github.com/duongtruongdp/ND-ImgConverter-Engine-Feed/raw/refs/heads/main/manifests/staging/manifest.json`

It contains the existing schema-2 manifest with a staging channel and a
monotonic `manifestRevision`. GitHub Release assets use immutable tags such as
`engine-staging-2026-11-22` and canonical artifact names that include engine,
version, platform and architecture.

Raw GitHub content is cached by the CDN for a bounded period. The `refs/heads`
raw URL is used to avoid the stale 404 observed for the legacy shorthand path.
The publisher verifies the final manifest from outside the publishing workflow
and checks that its revision is visible after publication. A new revision is
used for each manifest change.

This feed is for a staging-enabled test client only. The public v0.9.1 client
does not trust the staging key and is intentionally unchanged.
