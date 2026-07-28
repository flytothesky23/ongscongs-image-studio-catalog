# 옹스콩스 Image Studio public catalog

This repository publishes public, signed template data and thumbnails for the
옹스콩스 Image Studio Chrome extension.

- GitHub Pages content lives in `docs/`.
- `docs/v1/latest.json` is signed by `docs/v1/latest.sig`.
- Immutable releases live below `docs/v1/releases/<revision>/`.
- The extension bundles the matching P-256 public key.

This repository must never contain private signing keys, user reference images,
prompt drafts, Companion state, capabilities, Codex credentials, or local
filesystem paths.

The private signing key is held outside the repository by the local editorial
automation. A release is generated from the reviewed Open Image Studio source
catalog with:

```sh
node ../scripts/build-catalog-pages.mjs
```
