# Suggestions: write a useful next action

**Inputs:** supported snapshot evidence, investor topics, proposed rules and existing task destinations.
**Outputs:** components/suggestions.json; send missing evidence or overbroad conditions back to research or matching instead of hiding them in persuasive wording.

**Suggestion content:** update components/suggestions.json. Each entry has id, title, target_task_id, approach, interpretation and caution. Every suggestion has a rule. If investor evidence is missing, the app may still offer a matching startup-only example, labeled without investor alignment; no complete investor-connected match is established. Keep actions bounded and adaptable, interpretations explicitly editorial, and cautions meaningful. Reuse an ID only for the same action. Do not claim investor endorsement, investment relationships, success probabilities or historical quantities as targets.

## Review usefulness separately from matching

For each changed action, make the next step understandable, bounded in effort and adaptable to the founder's constraints. Explain what can be learned and what evidence would inform continuing, changing or stopping. Put that guidance in the existing approach, interpretation and caution fields; do not invent new schema fields or numerical success targets.

Ask reviewers or founders whether they understand the step, can attempt it, see why it applies and know what learning to record. Record the actual sample size, feedback and changes made. If no user review occurred, say so. A correctly matched suggestion is not automatically useful, endorsed by an investor or causally supported by a startup outcome.

Next-move selection and general fallback copy belong to Startup Guide, not this pack file.
