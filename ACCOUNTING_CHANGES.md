# Changes from upstream zeropaper (alejandroll10/zeropaper)

Branch `accounting` of this fork changes the journal bar from top-3 finance
(JF / JFE / RFS) to top accounting journals (TAR / JAR / JAE).

Files changed (11 values, nothing else):

- `deploy_assets/templates/agents/finance/vocab.json`
  - `SUBMISSION_TIER`, `QUESTION_REFEREE_ROLE`, `QUESTION_IMPORTANCE_BAR`,
    `QUESTION_POSER_ROLE`, `IDEA_GEN_ROLE`, `IDEA_REVIEWER_ROLE`,
    `IDEA_TOP_PAPER_EXAMPLE`, `IDEA_SEARCH_QUERY`, `REFEREE_JOURNAL_ROLE`,
    and the example list inside `IMPORTANCE_100`
- `deploy_assets/templates/agents/finance_modes/empirical_first/vocab.json`
  - `REFEREE_JOURNAL_ROLE`

Not changed: the Variant-context journal list in
`deploy_assets/scripts/setup/resolve_config.sh`, the finance identification
checklist in the empirical-extension agent bodies, and the tier names
(`top-3-fin`, `field`, `letters`) in the pipeline code.

LICENSE is unchanged; this branch remains under the
Auto Research Pipeline — Research Use License v1.1.
