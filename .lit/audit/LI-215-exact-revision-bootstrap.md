# LI-215 Exact-Revision Bootstrap

- Predecessor `develop`: `1cf1fedb688af59d57637d9928869c66dde8ac6c`
- Shared-assets source: `da9d4a640a6d83097196a7e4a8e1b8b4f753427e`
- Superseded promotion PRs: `#528`, `#530`, `#531`
- Recovery: advance `develop` with this audit-only commit, then let the
  protected promotion controller create one fresh App-owned promotion and
  dispatch its Exact-Revision review.

This file changes no collection or workflow behavior. It records the bounded
bootstrap needed because the old `main`-side controller could not dispatch the
new Exact-Revision producer and the single human-owned Copilot request did not
return within the guarded observation window.
