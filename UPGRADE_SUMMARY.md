---
layout: default
title: Upgrade Summary
---

## Upgrade Summary
- **From:** 0.9.1-beta
- **To:** 0.9.2-beta
- **Date:** 2026-03-06
- **Automated changes:** 5
- **Manual steps:** 2

## Automated Changes Applied

### Configuration (1 file)

- [x] Updated _config.yml: version 0.9.2-beta (2026-03-06)

### Scripts (3 files)

- [x] Updated scripts/iiif_utils.py - Fix sizes array scanning, add 96px thumbnail
- [x] Updated scripts/generate_iiif.py - Updated version header
- [x] Updated scripts/process_pdf.py - Updated version header

### Other (1 file)

- [x] Updated CHANGELOG.md - Added v0.9.2-beta changelog entry

## Manual Steps Required

Please complete these after merging:

1. Copy .github/workflows/telar-tests.yml and .github/workflows/build.yml from the latest Telar release. Workflow files cannot be updated automatically by the migration script due to GitHub Actions token permissions. The test workflow now only runs on the main Telar repos, not on user sites.
2. If your site uses self-hosted images, regenerate tiles to fix the info.json sizes array. Run your site's build workflow or run generate_iiif.py locally. This fixes tile rendering issues on Windows browsers.

## Resources

- [Full Documentation](https://telar.org/docs)
- [CHANGELOG](https://github.com/UCSB-AMPLab/telar/blob/main/CHANGELOG.md)
- [Report Issues](https://github.com/UCSB-AMPLab/telar/issues)
