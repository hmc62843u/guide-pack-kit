# Author and verify a Guide Pack

**One complete JSON library, three components, one browser file for local use.**

This guide and [the methodology reference](REFERENCE.md) retain their [original MIT licence](APP_DOCS_LICENSE.md). Research data keeps its separate notices.

## Inputs and deliverables

| File or folder | Role |
| --- | --- |
| profiles/ and startups/ | Source-supported records; see catalog.json for the selected files |
| components/matching.json | Topics, context rules and provider-authored self-tests |
| components/suggestions.json | Actions, interpretations and limits |
| package-metadata.json | Provider/library identity, version, rights and quality declarations |
| review-register.json and source notices | Exact-byte review record and attribution |
| dist/guide-pack.json | Complete assembled research library |
| dist/active-pack.js | Same complete data in the local browser wrapper |

The fictional examples/demo-guide-pack.json and demo-active-pack.js are separate test fixtures. Never combine real records with invented connections.

## Add a supported connection

1. **Research the investor interest.** Find a source supporting a specific topic, with dates and a qualified statement. Stage/sector overlap alone is not an interest in a particular experiment.
2. **Research the startup approach.** Record the dated facts and their sources. A later account must remain labelled as retrospective; later success is not proof that the approach caused it.
3. **Encode the topic and rule.** In components/matching.json, connect the investor topic with a snapshot, supported business models, startup stages, learning questions and known evidence fields. Follow [PACK_FORMAT.md](PACK_FORMAT.md); do not add executable operators.
4. **Write the suggested experiment.** In components/suggestions.json, resolve the rule's suggestion ID and provide a bounded action, interpretation and cautions. Distinguish the sourced observation from your proposed exercise.
5. **Review and test.** Add expected matching and nonmatching cases before running them. Check missing topics, unknown context and reference-only investors. Review research support and usefulness separately.

A compatible startup lesson can appear without investor alignment. An investor interest without a matching startup lesson stays a perspective beside a general exercise. Missing connections are valid results, not blanks to fill with guesses.

## Assemble and deliver

Follow [AUTHORING_PROMPT.md](AUTHORING_PROMPT.md) and [prompts/package.md](prompts/package.md). Copy catalog-selected records in order, annotate their data kind and include both component files in full. Preserve stable identities; increase the package version when JSON content changes. A different community pack needs its own provider/library IDs.

Review changed records/components and their exact bytes. Update applicable source notices, hashes and quality declarations honestly. Documentation-only changes need no new research date or JSON version.

Write the synchronized browser file with only the data assignment described in [LOCAL_APP.md](LOCAL_APP.md). Copy that trusted file into the app as packs/active-pack.js, retain required notices and refresh. The app validates assigned data; arbitrary scripts are not made safe by schema validation. Authoring requires no runtime installation.

## Provider self-tests

Up to 50 hypothetical cases can describe a startup context, investor IDs, expected suggestion IDs and rationale. See [the exact case format](PACK_FORMAT.md#portable-recipe-self-tests). The app's development evaluation function tests complete connections, independently of next-move priority or saved progress; there is no self-test preview panel in the lean interface.

| Current pack | Cases | What passing establishes |
| --- | --- | --- |
| Research 0.7.0 | Four no-match cases | Agreement on those missing complete connections; no positive connection coverage |
| Fictional 1.2.0 | Seven cases: three positive, four negative | Agreement on those invented examples |

These cases do not evaluate source truth, startup-only UI suggestions, ranking, usefulness or outcomes. Compatible data can still be stale, incomplete or wrong. Keep actual results and limitations distinct from provider-declared quality.

## Use in Startup Guide

[LOCAL_APP.md](LOCAL_APP.md) covers copying packs, four support-state tests and save/reload checks. [The app guide](https://github.com/hmc62843u/startup-guide/blob/main/GUIDE.md) describes Situation, Next move, Investor and Startup. [App development](https://github.com/hmc62843u/startup-guide/blob/main/DEVELOPMENT.md) owns executable behavior and software checks. No research or automatic source updates run in the app.
