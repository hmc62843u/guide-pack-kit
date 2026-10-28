# Guide Pack Kit

Help startup founders explore what to try next. Create source-supported **Guide Packs** for [Startup Guide](https://github.com/hmc62843u/startup-guide), using an assistant and direct JSON editing. No Node, Python or packaging script is required.

## Try an existing pack

| Download | What to expect in Startup Guide |
| --- | --- |
| [Research Guide Pack](dist/guide-pack.json) | Nine investor/program records and three startup snapshots. Seven profiles are reference-only. Matching startup lessons can appear as startup-only suggestions; no investor-topic connections are currently documented. |
| [Fictional Guide Pack](examples/demo-guide-pack.json) | Two invented investor profiles, one startup snapshot, two suggested actions and seven self-tests. Demonstrates complete connections without making claims about real organizations. |

1. Download either complete JSON file.
2. Open Startup Guide, then **Libraries & settings**. Choose the file and inspect its preview.
3. Select **Use this Guide Pack**. Imports stay in your browser; downloading or previewing a file does not activate it.

For the fictional pack, set **Marketplace · Exploring an idea · Test demand**, choose **Fictional Discovery Fund** in the Home investor lens, and expect **Explore demand with a bounded reservation test**. For a real example, set **Marketplace · Testing with users / pre-seed · Test demand** and expect **Try a bounded local service**, supported by the DoorDash snapshot. Selecting firstminute does not establish investor alignment.

New app workspaces already include this research pack. The app's **Try demo scenarios** mode uses its separate built-in fictional library; importing this kit's smaller fictional pack tests the community-provider workflow. [App walkthrough and testing steps](https://github.com/hmc62843u/startup-guide/blob/main/GUIDE.md).

## Make your own

**Sources → facts → topics and rules → suggested experiments → review → complete JSON → app import.**

1. Choose what to improve in [CONTRIBUTING.md](CONTRIBUTING.md).
2. Give your assistant [AUTHORING_PROMPT.md](AUTHORING_PROMPT.md) and a scope: the investor/program, startup, historical date and learning question.
3. Follow its focused prompts, inspect the sources and review the result. [PACK_FORMAT.md](PACK_FORMAT.md) defines the supported contract.
4. Write the complete `dist/guide-pack.json`, increase its version when JSON content changes, then preview and test it in Startup Guide.

For your own community pack, choose distinct provider/library IDs in `package-metadata.json`. Keep them stable for later versions. Do not reuse the reference provider identity for an unrelated library.

| I want to change… | Start here |
| --- | --- |
| An individual investor profile | [profiles/firstminute_capital.json](profiles/firstminute_capital.json) |
| An individual startup snapshot | [startups/doordash_2013_01_12.json](startups/doordash_2013_01_12.json) |
| Which records are included | [catalog.json](catalog.json) — repository-relative paths |
| Investor topics, matching rules or expected cases | [components/matching.json](components/matching.json) |
| Actions, interpretation and cautions | [components/suggestions.json](components/suggestions.json) |
| Research, matching or suggestion quality | [CONTRIBUTING.md](CONTRIBUTING.md) and [prompts/](prompts/) |
| The app's executable matching behavior | [Startup Guide development](https://github.com/hmc62843u/startup-guide/blob/main/DEVELOPMENT.md#extension-points-and-contracts) |

Individual records illustrate authoring. **The app imports one complete Guide Pack**, not loose profile or snapshot files. The source files, catalog and components remain editable inputs; `dist/guide-pack.json` is the assembled deliverable.

## Know what the evidence supports

| Available support | What the app can show |
| --- | --- |
| Investor topic and startup lesson connected by supported context rules | A connected suggestion; not investment, endorsement or evidence of causality. |
| Investor interest only | The relevant sourced interest beside a separate general exercise. |
| Compatible startup lesson only | A startup-only example to inspect and adapt, without investor alignment. |
| Neither | A general exercise. |

A raw snapshot needs an authored context rule before becoming a startup-only suggestion. The complete-connection matcher described in PACK_FORMAT.md also drives provider self-tests; an empty expected set means **no complete connection**, even if the UI can display a startup-only example. Passing self-tests is not a quality certification. Current research pack 0.7.0 has four no-match tests and no positive investor-connection coverage; fictional pack 1.2.0 has seven cases, including positive coverage.

Research accuracy, matching agreement and suggestion usefulness require separate assessment. Provider identity and quality metadata are declarations, not authenticated identities or independent ratings. The kit has no automated export gate; the app validates structure, not source truth or rights.

## Share with sources and limits

Retain [LICENSE.md](LICENSE.md), [SOURCES.md](SOURCES.md), [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and [DATA_NOTICE.md](DATA_NOTICE.md). The editorial licence covers only rights held by the publisher; underlying sources retain theirs. The fictional example has its own MIT notice in its JSON.

Keep exact-byte review hashes for changed research/components in [review-register.json](review-register.json). Documentation-only improvements need no invented review dates or JSON version bump. Publish the kit as its own repository; keep private research, browser exports and credentials outside it. Uploading the prepared files requires no development runtime. Commit the complete pack in `dist/` with its source inputs and notices.

When separately authorized to refresh Startup Guide's distribution copies, copy both JSON packs and their notices together. Follow [prompts/package.md](prompts/package.md); do not silently change app defaults or activate a package for users.
