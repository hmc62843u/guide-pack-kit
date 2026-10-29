# Connections: encode conditions and expected cases

**Inputs:** reviewed or proposed research facts, existing suggestion IDs and PACK_FORMAT.md.
**Outputs:** components/matching.json and any proposed suggestion IDs for the suggestion stage. No executable algorithm is supplied by this stage.

**Matching criteria:** update components/matching.json. investor_topics entries need an existing profile_id, topic, accurate statement, source_url, published_date and retrieved_date. Use actual YYYY-MM-DD dates. The evidence must support the investor priority, not just stage/sector fit or a past investment. Rules use only context_topic_v1 and the fields in PACK_FORMAT.md. Reference existing snapshots, suggestions, known evidence fields and source IDs. Do not add a topic merely to make a match appear. No scripts, arbitrary predicates, scoring engines or LLM calls are accepted. Missing supported investor connections remain absent. A context rule with supported snapshot evidence can still supply a startup-only example; it must not gain investor alignment through wording.

## Define expectations before measuring agreement

Add evaluation_cases to components/matching.json where useful. Each case has a unique id, name, startup context, investor_ids, expected_suggestion_ids and rationale, following PACK_FORMAT.md. Use no more than 50. Expectations must refer to actual package profiles/suggestions; unknown model, stage or focus is null. Empty investor_ids means unselected-lens preview, not an empty universe of investors.

Establish expected candidate sets before running them. Include supported matches, nonmatches, missing context and missing investor topics where the dataset permits. Do not invent research to manufacture positive coverage. Keep hypothetical case inputs separate from factual historical records. The real package currently has no positive investor-linked cases; say so explicitly. These expected sets describe the complete-connection matcher. They do not assert that the UI has no startup-only example or general exercise.

In the app development environment, evaluateMatchingCases runs the candidate matcher and returns expected versus actual suggestions and positive/negative coverage. The lean interface has no self-test panel. It does not execute provider code. Differences are visible for review; a valid package is not automatically blocked merely for failing its provider's expectations. A passing self-test suite is not independent accuracy, source verification, next-move ranking validation or user-outcome evidence. Update the matching review hash, source notes, package version and honest matching-quality declaration when cases change. Report actual results and unperformed checks without inventing evaluation evidence.

Keep case selection independent of what the matcher happens to return. A disagreement may expose a bad expectation, bad rule or app defect; investigate the evidence before changing either side. Route new operators or matching-engine defects to Startup Guide.
