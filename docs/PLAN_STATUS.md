# SongWalker Library — Plan Status

> **Last updated:** 2025-03-13  
> **Role:** Preset repository — synths, samplers, effects  
> **Hosted:** [clevertree.github.io/songwalker-library](https://clevertree.github.io/songwalker-library)  
> **Presets:** ~1,108 across 16 libraries

---

## 1. Feature Completion Status

| Feature | Status | Notes |
|---------|--------|-------|
| **Preset format** | ✅ Complete | songwalker-preset v1, JSON schema |
| **Index generation** | ✅ Complete | generate-index.js |
| **SF2 conversion** | ✅ Complete | convert-webaudiofontdata.mjs |
| **SPC conversion** | ✅ Complete | convert-spc.py (experimental) |
| **Libraries** | ✅ Complete | _shared, FluidR3_GM, Aspirin, etc. |
| **GitHub Pages** | ✅ Complete | Served as static site |
| **CDN/mirror** | ⏳ Optional | Could add jsDelivr for faster fetch |

---

## 2. Recommendations

### Refactoring
- **Scripts:** Move to `scripts/`; add `package.json` with `npm run generate-index`.
- **Preset validation:** Schema validation (JSON Schema) before commit; CI check.
- **Conversion pipeline:** Document source → preset flow; add validation step.

### Cleanup
- **Duplicate presets:** Audit for near-duplicates across libraries.
- **Metadata:** Ensure `tags`, `metadata` populated consistently.
- **License files:** Per-library license for SF2-derived samples.

### Hardening
- **Sample integrity:** Checksums for zone sampleData; detect corruption.
- **Index consistency:** Assert all preset.json referenced in index exist.
- **Size limits:** Very large presets; consider splitting or compression.

### Organization
- **docs/:** Add CONTRIBUTING (how to add presets), schema reference.
- **CI:** GitHub Action to regenerate index on push; validate schema.

---

## 3. What Should Be Done Next

### Immediate
1. **CONTRIBUTING.md** — How to add a new preset, run conversion scripts.
2. **Schema doc** — Document preset.json format, zone structure.
3. **Index regeneration** — Document `npm run generate-index` or equivalent.

### Short-term
4. **Preset validation CI** — Validate all preset.json against schema.
5. **Retro presets** — Add NES/GB oscillator presets when songwalker-core retro_synth lands.
6. **Tag consistency** — Standardize tags (e.g. "piano", "acoustic", "keyboard").

### Medium-term
7. **CDN mirror** — jsDelivr or similar for faster global fetch.
8. **Preset versioning** — Version field; migration path for format changes.
9. **Search index** — Pre-built search index (tags, name) for faster client search.
