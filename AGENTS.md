# Agent instructions

Preset library for the SongWalker music engine (GitHub Pages + Relay catalog).

---

## Git and go-live

Catalog repo **`songwalker-library`** · branch **`main`** · publish origin **`iad1`**.

| Step | Action |
|------|--------|
| 1 | Checkout **`main`**. |
| 2 | **`git push iad1 HEAD:main`** first. |
| 3 | **`git push gitlab HEAD:main`**. |

**Structure:** root **`index.json`** lists libraries; each library has **`index.json`** + instrument **`preset.json`** trees. Status: [`docs/PLAN_STATUS.md`](docs/PLAN_STATUS.md).

*Last updated: 2026-08-23*
