

## 4. Multi‑QR Chunking & Reassembly for Large Binary Files

**Description:**
Allow uploading arbitrary binary files (images, ML models, binaries), optionally compressing them, chunking into multiple QR codes with sequence metadata, and exporting a multi‑QR package (ZIP/manifest) that can be reassembled by the scanner.

**Reproduction Steps:**
1. Attempt to generate a QR for a file larger than the current fixed payload — no chunking available.

**Acceptance Criteria:**
- File upload accepts binary files and optional compression (gzip).
- File split into sequential chunks with metadata headers (index, total, file-id/hash).
- Generator outputs multi‑QR package (images + manifest or ZIP).
- Scanner supports reassembly from multiple scans or bundle upload.

**Files to change:**
- [index.html](index.html)
- [js/script.js](js/script.js)

**Labels:** generator, feature, hard, backend-logic
**Difficulty:** hard
**First steps:** Design manifest/chunk format; implement compression + chunker and a simple reassembly routine.

## Component
- [x] QR Generator
- [ ] QR Scanner
- [ ] UI/UX
- [ ] Other

---

## 5. File-Type Detection & Capacity Guidance in Generator UI

**Description:**
Detect MIME/type on upload and show QR capacity limits (per version & error-correction level). Warn or suggest chunking/compression when a file exceeds capacity.

**Reproduction Steps:**
1. Upload a file to the generator — no capacity estimate or guidance shown.

**Acceptance Criteria:**
- UI displays estimated capacity for selected QR version and ECL.
- On file upload, show whether file fits or suggest chunking/compression.
- “Show details” capacity table available.

**Files to change:**
- [index.html](index.html)
- [js/script.js](js/script.js)

**Labels:** generator, ux, docs, medium
**Difficulty:** medium
**First steps:** Add capacity lookup table, detect file type via `File.type`, display dynamic guidance.

## Component
- [x] QR Generator
- [ ] QR Scanner
- [x] UI/UX
- [ ] Other

---


## 7. Extract & Harden Reed‑Solomon / GF(256) Module + Tests

**Description:**
Replace the ad-hoc error-correction logic with a structured Reed–Solomon / GF(256) module, include a small test harness, and support multiple ECLs.

**Reproduction Steps:**
1. Inspect current generator ECC implementation — it’s limited and untested.

**Acceptance Criteria:**
- New `rs` module with encode/decode API.
- Supports standard generator polynomials and multiple ECLs.
- Minimal test suite/examples validating known vectors.
- Generator uses the new module.

**Files to change / add:**
- Add `js/lib/rs.js` (or split from [js/script.js](js/script.js))
- Add `tests/` or `examples/` (browser-based or Node)

**Labels:** algorithm, refactor, testing, hard
**Difficulty:** hard
**First steps:** Extract ECC code into module; implement Galois field ops and polynomial division; add small test runner.

## Component
- [x] QR Generator
- [ ] QR Scanner
- [ ] UI/UX
- [ ] Other

---

## 8. Migration Plan & Minimal Scaffold for React / Next.js

**Description:**
Create a migration plan and minimal scaffold showing how to convert the app to React/Next.js while keeping the vanilla app available.

**Reproduction Steps:**
1. Review repo — app is vanilla JS and contributors asked for modernization.

**Acceptance Criteria:**
- `migration.md` added with step-by-step migration plan and component mapping.
- Minimal `next/` scaffold or component examples included (`components/Generator`, `components/Scanner`).
- Instructions on how to run both codepaths.

**Files to change / add:**
- [CONTRIBUTING.md](CONTRIBUTING.md) (link migration doc)
- Add `next/` scaffold folder (optional)

**Labels:** roadmap, architecture, enhancement, hard
**Difficulty:** hard
**First steps:** Draft `migration.md` and scaffold a tiny Next app demonstrating core component stubs.

## Component
- [x] QR Generator
- [x] QR Scanner
- [x] UI/UX
- [x] Other

---

## 9. Make Site a PWA & Improve Mobile Camera UX

**Description:**
Add a Web App Manifest, service worker, and mobile-first improvements so the site is installable and camera scanning works reliably on mobile (with iOS fallbacks).

**Reproduction Steps:**
1. Open site on mobile — not installable and camera UX unoptimized.

**Acceptance Criteria:**
- `manifest.json` and `service-worker.js` added and referenced in [index.html](index.html).
- Basic offline caching for static assets and generation UI.
- Mobile camera UX optimized (touch targets, permission guidance, iOS notes).
- “Add to Home Screen” affordance on supported devices.

**Files to change / add:**
- Add `manifest.json`
- Add `service-worker.js`
- [index.html](index.html)
- [css/style.css](css/style.css)

**Labels:** pwa, mobile, enhancement, medium
**Difficulty:** medium
**First steps:** Add manifest and simple service worker; update meta viewport and touch target styles.

## Component
- [ ] QR Generator
- [x] QR Scanner
- [x] UI/UX
- [x] Other

---

## 10. Add Issue & PR Templates, Label Definitions, Update CONTRIBUTING Links

**Description:**
Improve contributor experience by adding [.github/ISSUE_TEMPLATE](.github/ISSUE_TEMPLATE) and [.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md), document label usage, and link templates from [CONTRIBUTING.md](CONTRIBUTING.md).

**Reproduction Steps:**
1. Browse repo — [CONTRIBUTING.md](CONTRIBUTING.md) exists but [.github](.github) templates and label docs are missing.

**Acceptance Criteria:**
- Bug, Feature, and Good First Issue templates added under [.github/ISSUE_TEMPLATE](.github/ISSUE_TEMPLATE).
- PR template at [.github/PULL_REQUEST_TEMPLATE.md](.github/PULL_REQUEST_TEMPLATE.md) present (existing file can be moved/used).
- [CONTRIBUTING.md](CONTRIBUTING.md) updated to link templates and list labels.
- Optionally include `labels.yml` for maintainers.

**Files to change / add:**
- [CONTRIBUTING.md](CONTRIBUTING.md)
- Add `.github/ISSUE_TEMPLATE/bug.md`
- Add `.github/ISSUE_TEMPLATE/feature.md`
- Add `.github/ISSUE_TEMPLATE/good-first-issue.md`
- Use or update [.github/pull_request_template.md](.github/pull_request_template.md)

**Labels:** docs, maintenance, good-first-issue, beginner-friendly
**Difficulty:** easy
**First steps:** Create template files and update [CONTRIBUTING.md](CONTRIBUTING.md) with links to them.



## Component
- [ ] QR Generator
- [ ] QR Scanner
- [x] UI/UX
- [x] Other

---
