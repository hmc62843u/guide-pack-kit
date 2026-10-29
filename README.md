# Guide Pack Kit

**Turn research into small experiments for [Startup Guide](https://github.com/hmc62843u/startup-guide).**

An author and an assistant encode evidence, matching criteria and suggestion content. Startup Guide applies the rules locally. No Node, Python or packaging script is required to author or use prepared packs.

## Try a pack

| Pack | Browser file | What it demonstrates |
| --- | --- | --- |
| Research | [active-pack.js](dist/active-pack.js) | Nine investor/program profiles and three startup snapshots. Startup-only suggestions; no investor-topic connections documented. Seven profiles are reference-only. |
| Fictional | [demo-active-pack.js](examples/demo-active-pack.js) | Two invented profiles and one snapshot. Demonstrates complete and partial support. |

Download the raw browser file, copy it into Startup Guide's **packs/** folder as **active-pack.js**, then refresh. One pack is configured at a time. [Setup and four test cases](LOCAL_APP.md).

## Make your own

**Sources → facts → connections → experiments → review → pack.**

1. Give your assistant [AUTHORING_PROMPT.md](AUTHORING_PROMPT.md) and your research scope.
2. Review the evidence and the three components below. Preserve missing information as unknown.
3. Deliver the complete JSON plus its browser wrapper and notices. Test it using [LOCAL_APP.md](LOCAL_APP.md).

| Component | Edit | Purpose |
| --- | --- | --- |
| Research | [profiles/](profiles/), [startups/](startups/), [catalog.json](catalog.json) | Facts, dates, sources and limitations |
| Matching | [components/matching.json](components/matching.json) | Investor topics, context rules and expected cases |
| Suggestions | [components/suggestions.json](components/suggestions.json) | Actions, interpretation and cautions |

Start with an individual [investor profile](profiles/firstminute_capital.json) or [startup snapshot](startups/doordash_2013_01_12.json). These are editable inputs; the deliverables are [dist/guide-pack.json](dist/guide-pack.json) and its synchronized browser file. Use your own provider/library IDs for a separate community pack.

## Go deeper

[Authoring guide](GUIDE_PACKS.md) · [Methodology and quality](REFERENCE.md) · [Improve a pack](CONTRIBUTING.md) · [Exact format and diagrams](PACK_FORMAT.md)

Research accuracy, matching agreement and suggestion usefulness need separate assessment. Provider declarations and passing self-tests are not independent ratings. A connection does not establish investment, endorsement or what caused a startup to survive.

Research retains its [editorial licence](LICENSE.md), [source bases](SOURCES.md), [third-party notices](THIRD_PARTY_NOTICES.md) and [data notice](DATA_NOTICE.md). Transferred documentation and the methodology illustration retain their [MIT licence](APP_DOCS_LICENSE.md). Keep private research and credentials outside this repository.
