# Configure the lean Startup Guide

**Prepare one trusted pack → copy its browser script → refresh the app.** No import or settings screen is needed. No Node or Python is required for this manual workflow.

## Copy a ready-made file

1. Download [research active-pack.js](dist/active-pack.js) or [fictional demo-active-pack.js](examples/demo-active-pack.js). Download the raw file, not a GitHub HTML page.
2. Replace Startup Guide’s packs/active-pack.js with it. Rename the fictional file to active-pack.js.
3. Refresh the app. The header says Research examples or Fictional demo.

Required research notices already accompany the app; retain them. A different community pack must bring its own applicable notices. The prepared scripts contain the same complete data as their corresponding JSON files.

## Local files

| File | Purpose |
| --- | --- |
| dist/guide-pack.json | Complete researched JSON, still the canonical authoring deliverable |
| examples/demo-guide-pack.json | Entirely fictional complete/partial connection test data |
| Startup Guide: packs/active-pack.js | Browser-readable configured pack; works from file URLs |

Copy the entire chosen JSON object into a plain UTF-8 file with this wrapper, then save it as **packs/active-pack.js** in Startup Guide, replacing the existing file:

~~~javascript
globalThis.STARTUP_GUIDE_PACK = /* the complete JSON object goes here */;
~~~

The line above is a template, not a working pack. Replace the comment with the full JSON object (starting with { and ending with }), without Markdown fences. An assistant can prepare that file using the [authoring prompt](AUTHORING_PROMPT.md). Do not fetch or import the JSON from JavaScript: direct-file browsers restrict such requests.

The wrapper must contain only that assignment. A browser script can execute code, so use trusted locally reviewed files. The app validates the assigned data and refuses malformed packs; data validation does not make arbitrary JavaScript safe. Retain the pack's required source/licence notices beside the app. Do not mix real records and fictional connections.

Refresh with Ctrl+R using the same browser profile and app path. New provider/library/version identities have separate notes. Returning to an earlier configured version restores its workspace. No automatic downloads, pack switching, or background research occur.

For app developers, the normal build regenerates active-pack.js from packs/guide-pack.json. If using that workflow, replace the JSON and required notices together, then rebuild. A manual active-pack.js replacement needs no rebuild but will be overwritten by the next development build. Browser offline caches require an online reload after a served-site file change; direct-file use reads the local script.

## Test four evidence states

Copy examples/demo-active-pack.js into the app as packs/active-pack.js (or wrap examples/demo-guide-pack.json yourself). On Situation choose the following, then on Investor select the named fictional profile:

| Model / stage / question | Investor | Expected support |
| --- | --- | --- |
| Marketplace / Idea / Demand | Fictional Discovery Fund | Both sides connected |
| Hardware / Idea / Demand | Fictional Discovery Fund | Investor interest only; general exercise |
| Marketplace / Idea / Demand | Fictional Formation Studio | Startup example only |
| Hardware / Idea / Demand | Fictional Formation Studio | Neither; general exercise |

Use a fresh browser profile for a clean run. An existing saved experiment may remain the current move. Before selecting an investor, a complete connection is only a preview. Reference-only profiles can be inspected but cannot be selected.

Save a custom action and note **TEST-LEAN-01**, refresh, change investor selection and confirm both remain. Check that sources are present for supported examples and absent from general exercises. Full sources and limitations are available on demand; the everyday four-screen flow is compact.
