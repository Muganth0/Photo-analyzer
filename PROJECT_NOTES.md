# Project Notes — Event Photo Analyzer V1.2

This repository contains recovered source code from the existing Hatchable project.

## Main files
- `index.html`: single-page UI and styling
- `app.js`: folder indexing, face detection, person clustering, heuristic scoring, filters, decisions, and JSON export

## Current workflow
1. Select an event folder in a browser that supports directory uploads.
2. Load face-api.js models from the configured external model URL.
3. Analyze photos, generate face descriptors, and approximate person clusters.
4. Review candidates, manually change Keep / Review / Reject decisions, and export JSON.

## Known limitations
- Models are fetched from third-party CDNs, so internet access is required.
- Scores are heuristic estimates, not semantic understanding of a moment.
- Current similar-frame grouping uses nearby file order and face counts, not image-level visual similarity.
- Review decisions exist in in-memory browser state and aren't stored persistently.
- Person labels are generated IDs; a full person-name/role editing flow is not implemented.
- No PhotoCraft integration or Windows desktop executable is included in this source snapshot.
- End-to-end testing with a real event folder remains outstanding.

Please verify any person matches and selection decisions manually before delivering photos.
