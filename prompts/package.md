# Package and verify: assemble the agreed contract

**Inputs:** catalog-selected facts, matching and suggestion files, completed review results and package metadata.
**Outputs:** package-metadata.json, complete dist/guide-pack.json and a report of checks actually performed. Do not rewrite research claims or invent missing connections during assembly.

- Increase version for changed package content, set the actual updated_date and preserve the provider/library IDs for a continuation. Do not impersonate another provider. repository_url and provider.url may remain null for local packages; never insert a local path or invented GitHub URL. Rights-review metadata must reflect a completed assessment. Quality entries for research, matching and suggestions must be honest: not_evaluated, self_reviewed or independent_review with supporting statement and actual review date where evaluated. Do not fabricate independent reviewers, metrics or certifications.

- Write one complete UTF-8 JSON object, without Markdown fences or comments. Begin with every field in package-metadata.json, which includes schema_version:2, provider, dataset_kind and quality. Add components.research.profiles and components.research.snapshots by copying the catalog-selected facts exactly in catalog order and adding data_kind matching the package kind to each embedded record. Add components.matching and components.suggestions by copying their component files in full. No unindexed/private records, missing annotations, summaries or silent source-URL changes. The JSON is the full library, not a patch.

- Keep the 5 MB, 250-profile, 250-snapshot, 500-topic, 500-rule and 500-suggestion limits. Cross-check unique IDs, provider metadata, dates, allowed field values, licence declarations, reference integrity and known evidence. V2's app-owned matcher performs the context/topic join; a new operator requires separately authorized app work. No executable provider code is produced.

- Research and fictional datasets cannot be mixed. The example package is wholly invented and uses existing local fictional specifications. Do not label real records fictional to bypass review. Preserve the existing real library's empty investor topics until evidence supports new ones.

## Verify and deliver

- Preview the package in startup-guide's Libraries & settings → Guide Packs. Inspect provider, dataset kind, version, component counts, declarations and sources; activate explicitly. Test a complete connection only if the pack documents the needed investor topic and startup lesson. For the current real pack, expect startup-only suggestions where a context rule fits; do not report a failed complete connection as a failed import. Also check nonmatching context, missing topic and reference-only investors. Inspect the source types actually present. Clear the lens separately to check preview behavior. Complete-connection self-tests do not score startup-only UI suggestions. Test reload, switching and notes isolation. If browser control is unavailable or the user has not tested import, report that verification remains outstanding.

- No development runtime or local server is needed for import. The kit has no automated exporter gate. App import validates structure, not source truth, provider identity or reuse rights. Do not bypass validation to make a generated file import.

- When authorized to refresh startup-guide, copy the exact JSON and LICENSE.md, SOURCES.md, THIRD_PARTY_NOTICES.md and DATA_NOTICE.md into its packs/ folder together; update its provenance README and preserve the app's researched default and optional fictional demo. This copy operation must not change users' saved library selections. App development tests are separate from this runtime-free kit. Do not automatically activate, fetch updates, combine providers or migrate old notes.

- Report package/provider/version, included counts, reference-only count, component changes, new supported connections or missing evidence, review basis and actual validation/import status. Commit locally or publish only when requested.

Changing prompts or documentation alone does not change package content and needs no package version increase. Do not regenerate record hashes or claim new quality reviews for an unchanged JSON deliverable.
