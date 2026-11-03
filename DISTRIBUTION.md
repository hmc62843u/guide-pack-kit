# Authoring for manual browser distributions

Guide Pack Kit remains the authoring layer for investor profiles, criteria, startup snapshots and optional sourced relationships. The Startup Tarot operator-distribution workflow packages an approved incubator revision for browser users.

Keep components modular: author the Guide Pack and relationship JSON separately. Their provider/pack identity, stable record IDs, source dates, limitations and licenses must remain consistent. A separate distribution manifest binds component versions and SHA-256 hashes to a release ID, audience, explicit source revision, operator review and update instructions. This does not change Guide Pack v1/v2 or relationship schema version 1.

Advance component versions when data changes. Do not put private contacts, access credentials, research runs or founder feedback into distributable research records. Excluding the private connection graph does not automatically classify free text as safe to share. Review reuse rights and supply required attribution notices for the intended audience.

The consumer implementation and commands are documented in startup-tarot/DISTRIBUTION_GUIDE.md in a full Startup Tarot checkout. The incubator reference manages/imports organization revisions; Startup Tarot builds the browser edition. Kit authoring does not automatically publish, synchronize or revoke recipient copies.
