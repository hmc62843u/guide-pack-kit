# Investor-fit research contract

This document is for Guide Pack authors. It defines the source-backed profile claims used by Startup Tarot's fundraising comparison. Application behavior, result labels and editorial sector mappings are documented in the companion app's METHODOLOGY.md; its GUIDE.md covers the founder workflow.

## Current research scope

Pack 0.8.0 has fourteen investor/program profiles and three startup snapshots. Six profiles support equity comparison: firstminute, Hustle Fund, Ada Ventures, Concept Ventures, Connect Ventures and boldstart. Seven historical records and the NSF grant program remain outside that equity shortlist.

Official pages for the six equity profiles were checked on 2026-10-30. This is a dated research statement, not a promise of current deployment capacity. The earlier 0.7.1 prototype supported firstminute alone; that earlier scope no longer describes the distributed pack.

The expansion added fundraising criteria without adding investor-topic connections for experiment matching. A mandate match does not establish a connection to a historical startup, endorsement, investment relationship or warm introduction.

## Canonical inputs and deliverables

| File | Responsibility |
| --- | --- |
| profiles/*.json | Canonical profile facts, editorial annotations and optional fit_claims |
| catalog.json | Profiles and snapshots included in the research collection |
| package-metadata.json | Provider, pack version, dates, quality declarations and terms |
| review-register.json and SOURCES.md | Exact-record review hashes, source references and reuse assessment |
| dist/guide-pack.json | Complete research, experiment matching and suggestion components |
| dist/active-pack.js | Browser wrapper assigning the same complete pack |

Keep these files synchronized. Startup Tarot carries its own copy of the reviewed complete JSON and required notices. A local application build generates its wrapper from that copy. Do not insert executable matching logic into a research pack.

## Optional fit_claims

This additive profile array works with the existing v1/v2 formats. It does not change the experiment-topic schema. The runtime accepts at most forty claims per profile.

| Field | Meaning |
| --- | --- |
| field | stage, sector, geography or check |
| basis | declared, observed or inferred; only declared mandates establish comparison alignment |
| strict | Whether the source establishes an explicit requirement rather than a focus or preference |
| statement | Independent factual paraphrase, including limitations or an editorial-mapping explanation |
| source_url | Absolute HTTP/HTTPS source URL without credentials |
| checked_date | Real calendar date in YYYY-MM-DD format when the claim was inspected |
| values | Nonempty categorical labels for stage, sector or geography |
| min, max, currency | Numeric ordered range and explicit three-letter currency for a check claim |

Checked date is not publication date. Do not manufacture a publication date for an undated page. If a publication date or locator is known, retain it in the profile's source metadata. Claim labels are editorial mappings and must not imply more than the source establishes.

## Research boundaries

- Separate declared mandates, observed investments and inferred preferences. A portfolio pattern does not become a declared criterion.
- Treat focus regions and typical check sizes as preferences unless explicit exclusions establish otherwise. Unknown or omitted conditions stay unknown.
- Distinguish an investor's initial check from follow-on participation and total round size.
- Keep the published currency. The legacy display field check_size_range_usd can contain a non-USD description and must not be parsed as a numeric USD mandate.
- Preserve requirements outside the four-field comparison in eligibility_requirements and anti_criteria. The app displays these as conditions requiring review.
- Do not derive founder suitability from school/employer pedigree or claim an introduction path without relationship evidence.
- Historical and reference-only profiles retain comparison_enabled false. Adding current research must not silently reinterpret a historical source as a present mandate.

For the current sample, Connect's published amount is a round range and Concept has only a verified maximum. Neither supports a numeric individual check-range claim. Ada's non-UK focus locations require a UK link; the current automatic geography comparison conservatively matches UK only.

## Author and review an update

1. Inspect official sources and independently paraphrase only the necessary facts. Record uncertainty and editorial mappings.
2. Update the canonical profile, claim dates and additional conditions. Review source/reuse notices and exact-record hashes for changed bytes.
3. Update collection membership if needed, increment the pack version and regenerate the complete JSON and wrapper. Do not revise unchanged source-review dates merely because a release is newer.
4. Validate the complete pack in Startup Tarot. Update affected benchmark expectations with a rationale, rather than changing expected results just to pass a test.
5. Sync the reviewed pack and notices to the application and test that source changes request assessment review without losing founder notes.

Quality declarations and this editorial review do not certify publisher rights, source truth or founder usefulness. Linked source works retain their own terms; no source endorsement is implied. Keep private source archives and founder feedback outside this repository.

## Application responsibilities

Startup Tarot owns the 180-day review policy, controlled aliases, directional sector relationships, ranking and result labels. Shortlists use a separate browser workspace across versions of the same provider/pack. They retain saved input, evidence, notes and editable drafts; they are not distributed research records.

The app's data/fit-benchmark.json has nine authored expectations, and LOCAL_RELEASE.md records pending founder-pilot and browser acceptance work. Passing implementation tests is not independent research validation. Browser exports, drafts and private verification answers must not be copied into this public pack.

## Related authoring guides

[Research methodology](REFERENCE.md), [pack format](PACK_FORMAT.md), [quality review](CONTRIBUTING.md), [source bases](SOURCES.md) and [review register](review-register.json) cover the wider collection. The [companion application](https://github.com/hmc62843u/startup-tarot) owns the user and developer documentation.

## Research-assistant use — initial integration, live acceptance pending

The companion app's intended next phase is LLM reasoning over investor criteria, dated startup snapshots and founder context to identify gaps, hypotheses and proposed investigations. Its RESEARCH_PLAN.md specifies the initial version-1 evidence packet, structured output and revision flow. These separate research contracts do not extend the current Guide Pack schema.

Keep canonical facts, editorial mappings, model interpretations and working findings distinct. Evidence packets should preserve stable record/source identifiers, known publication and event dates, check dates and limitations. A retrospective account must not be presented as information available at an earlier decision point. Do not invent missing dates or causal claims based on later startup success.

Model-generated findings or criteria require source and reuse review before entering this Kit. Founder research sessions, feedback and private notes belong outside public packs. The existing six-equity-profile collection and matching tests do not validate model reasoning or founder usefulness. The optional OAuth/model helper still needs actual account/inference acceptance; automatic source ingestion is not implemented.

## Initial research implementation update

The companion app now implements research contract version 1 separately from Guide Pack v1/v2: bounded packets, publication/cutoff checks, structured/reference validation, saved outputs/feedback and revisions. It has an optional OpenAI OAuth/model helper; actual account/inference acceptance and semantic research quality are pending. Tokens and private research history never enter this Kit. Earlier proposed-design text describes the original plan; current operational status is in the app RESEARCH_SETUP.md. Canonical facts still require separate source/reuse review before promotion.
