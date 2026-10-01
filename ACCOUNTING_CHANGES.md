# Changes from upstream zeropaper (alejandroll10/zeropaper)

Branch `accounting` of this fork switches the pipeline's journal bar and
domain framing from finance (JF / JFE / RFS) to accounting (TAR / JAR / JAE).
Methods content is unchanged: identification checklists, canonical packages,
data skills, and citations to methods papers stay as upstream wrote them.
Code identifiers are unchanged: the variant is still selected with
`--variant finance`, and the tier keys keep their names (`top-3-fin` now means
TAR / JAR / JAE; `field` means RAS / CAR / Management Science).

## What changed

- `deploy_assets/scripts/setup/resolve_config.sh` (finance branch only):
  paper type, target journals, domain scope, journal list, tier examples,
  and the empirical-first / data-first paper types.
- `deploy_assets/templates/shared/tier_tables/finance.md`: tier journal lists;
  the JF Insights & Perspectives outlet note replaced by an accounting tier note.
- `deploy_assets/templates/agents/finance/vocab.json` and the
  `finance_modes/{empirical_first,data_first,report}/vocab.json` overlays:
  editor, referee, reviewer, poser, generator and theorist roles; importance
  bar; submission tier; scorer anchors; and four domain-example keys added as
  finance overrides (`CROSS_SUBFIELD_SCOPE`, `EDITOR_WRONG_FIELD_EXAMPLE`,
  `EDITOR_DOMAIN_SUFFICIENT_EXAMPLES`, `EDITOR_ADJACENT_EXAMPLE`).
- Shared agent bodies: `editor.md`, `referee-freeform.md`, `paper-writer.md`,
  `polish-identification.md`,
  `shared_modes/empirical_first/identification-designer-core.md`.
- `deploy_assets/templates/shared/docs/stage_10.md`: within-tier outlet examples.
- Empirical extension: `identification-auditor.md`, `identification-designer.md`,
  `empiricist.md`, `method-checker.md`, `agent_metadata/finance_agents.json`.
- Skills: `canonical-packages.md`, `empirical_skills.json`, and the OpenAlex
  skill docs (`openalex.md`, `openalex_skills.json`) now list accounting
  journal source IDs. No code was changed.

## Checked

Assembled theory + empirical, empirical-first, report and manual deployments.
`test_setup_config.sh`, `test_report_mode_assembly.sh` and
`test_seeded_gate4_assembly.sh` pass. `test_results_evidence_assembly.sh`
fails one check, which fails identically on unmodified upstream v2.56.0.

LICENSE is unchanged; this branch remains under the
Auto Research Pipeline — Research Use License v1.1.
