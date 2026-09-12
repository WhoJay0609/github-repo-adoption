# Evidence and source notes

This reference supports the `github-repo-adoption` workflow. It separates a public
repository's discovery surfaces from first-use and runtime evidence. Counts below
are a frozen internal snapshot captured **2026-09-12** (analysis version
`codex-discoverability-analysis-v1`), supplied to shape this skill and templates.
They are not live GitHub measurements and do not establish a causal relationship
between README wording, stars, ranking, or agent recommendations.

## Frozen snapshot

The convenience sample used two GitHub repository-search families (`topic:codex`
and `codex in:name,description`), five star bands, and 30 frozen searches. Each
family/band took up to the first three 100-row pages; zero-star rows were ordered by
recent update. Forks and archived repositories were excluded. README retrieval and
admission were separate from search inclusion.

| Stage or stratum | Count |
| --- | ---: |
| Distinct repository IDs collected | 2,475 |
| Successful README responses | 2,440 |
| Classifier admissions before manual overrides | 1,280 |
| Manual exclusions of old/unrelated Codex API uses | 5 |
| Raw evidence-backed admissions | 1,275 |
| Final rows after one exact README SHA-256 duplicate was folded | **1,274** |
| Final star bands: 0 / 1–9 / 10–99 / 100–999 / 1,000+ | 223 / 284 / 274 / 260 / 233 |
| Final age bands: 0–6m / 6–12m / 1–2y / 2–5y / 5y+ | 893 / 319 / 54 / 7 / 1 |

Admission required README evidence of a current Codex tool, integration, workflow,
skill, configuration, or user-facing capability. A name, topic, incidental link, or
“built with Codex” sentence alone was insufficient. The corpus was not run end to
end: README feature flags such as `has_install`, `has_example`, and
`has_compatibility` are text-presence proxies.

The exact SHA-256 fold catches byte-identical README content only; it cannot detect
near-copies, mirrors, or independently maintained duplicates. A deterministic
stratified manual audit checked 50 admission descriptions and evidence excerpts,
not all 1,274 README files. That spot check supports the recorded admission rule;
it is not a full accuracy estimate.

For orientation, the 0-star and 1,000+ bands had the following visible README
signals:

| Signal present in README | 0 stars (`n=223`) | 1,000+ (`n=233`) |
| --- | ---: | ---: |
| Installation text | 79.4% | 93.6% |
| Quick start text | 22.0% | 55.4% |
| Example text | 43.5% | 64.8% |
| Demo text | 14.8% | 39.1% |
| Usage text | 35.9% | 56.2% |
| Troubleshooting text | 14.8% | 28.3% |
| Claude mention | 52.0% | 86.7% |
| Repository basename contains `codex` | 24.7% | 12.4% |

Across the final 1,274 rows, metadata contained `codex` in the description for
73.8%, in topics for 62.7%, and in the basename for 17.3%. README text contained
installation for 88.8%, examples for 54.8%, usage for 47.1%, compatibility for
56.3%, and a `llms.txt` mention for 1.7%. These are sample proportions, not product
requirements or growth targets.

For a compact, machine-readable audit trail, [study-2026-09-12.csv](study-2026-09-12.csv)
contains the 1,274 final rows and only repository metadata plus the Boolean fields
used in the tables. It was derived from the final cohort on 2026-09-12; it contains
no README bodies, excerpts, credentials, or machine-specific paths. Load it only
when checking final-cohort sizes, star/age bands, Codex metadata proportions, or
the star-band comparison table. The collection funnel, compatibility and
`llms.txt` proportions, and purpose-label counts rely on the internal study;
their underlying fields are not included in this compact export.

## Bias and interpretation boundary

- This is a query-stratified convenience sample, not a GitHub census or random
  sample. Low-star bands were deliberately included and high-star bands were
  oversampled within their strata; ordering was still search/API dependent.
- The query vocabulary contains `codex`, so Codex terms are overrepresented. Keyword
  categories are multi-label: 448 rows matched at least two purpose labels and 347
  matched none. English/Chinese and heading flags are character/text proxies.
- Project age, author reach, promotion, existing users, function value, and license
  compatibility were not controlled. Star totals cannot show organic growth,
  recommendation propensity, usefulness, or a wording effect.
- A README that documents a command is not proof that the command works. A local
  skill description controls installed-harness matching, not GitHub indexing. A
  marketplace/catalog is a separate distribution path. Do not collapse these into
  one “discoverability score.”

## Documented mechanisms

These portable sources describe the mechanisms used in the workflow:

| Surface | Source and bounded implication |
| --- | --- |
| Repository search | [GitHub repository search](https://docs.github.com/en/search-github/searching-on-github/searching-for-repositories): without `in:readme`, repository search targets name, description, and topics; `in:readme` explicitly targets README text. |
| README first screen | [About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes): explain what a project is, why it is useful, how to start, get help, and maintain it. |
| Topics | [Classify your repository with topics](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/classifying-your-repository-with-topics): topics help people find and relate repositories; they are separate metadata, not star evidence. |
| Codex skills | [Build skills](https://learn.chatgpt.com/docs/build-skills): Codex starts with skill `name`/`description`, then loads `SKILL.md` when the task matches; concise trigger-first descriptions support local routing. |
| Codex plugins | [Plugins](https://learn.chatgpt.com/docs/plugins) and [plugin build guidance](https://developers.openai.com/plugins/build/plugins): plugin manifests and marketplaces are a distribution/catalog path, separate from a standalone GitHub README. |
| Codex instructions | [Agent configuration](https://learn.chatgpt.com/docs/agent-configuration/agents-md): layered `AGENTS.md` files guide runtime behavior; the page does not say they affect GitHub indexing or ranking. |
| Claude skills | [Claude Code skills](https://code.claude.com/docs/en/skills): local skill directories and automatic description matching are another harness's local mechanism; compatibility must be tested separately. |
| Claude `AGENTS.md` boundary | [Claude memory](https://code.claude.com/docs/en/memory): Claude Code does not read `AGENTS.md` unless a `CLAUDE.md` import or symlink connects it. |
| Vendor docs indexes | [OpenAI `llms.txt`](https://developers.openai.com/llms.txt) and [Claude Code `llms.txt`](https://code.claude.com/docs/llms.txt) are vendor documentation indexes; neither establishes automatic ingestion of arbitrary repository files. |

## Representative patterns, cited at the original repositories

These examples were selected from the frozen sample because their visible structure
helps a template author. Their star totals are not presented as causes or targets.

| Pattern to borrow | Original evidence |
| --- | --- |
| Small, concrete install paths and a short quick start | [openai/codex README](https://github.com/openai/codex/blob/main/README.md) |
| A real workflow example, input table, permission boundary, and OS notes | [openai/codex-action README](https://github.com/openai/codex-action/blob/main/README.md) |
| Per-harness installation choices, native/legacy distinction, compatibility and troubleshooting | [affaan-m/ECC README](https://github.com/affaan-m/ECC/blob/main/README.md) |
| CLI-first install, first-use examples, supported stacks, output examples, and troubleshooting | [nextlevelbuilder/ui-ux-pro-max-skill README](https://github.com/nextlevelbuilder/ui-ux-pro-max-skill/blob/main/README.md) |
| Lifecycle commands, project structure, adoption path, and contributor workflow | [addyosmani/agent-skills README](https://github.com/addyosmani/agent-skills/blob/main/README.md) |
| A catalog with install/usage entry points and category navigation | [taishi-i/awesome-ChatGPT-repositories README](https://github.com/taishi-i/awesome-ChatGPT-repositories/blob/main/README.md) |

Use the patterns as prompts for real evidence: inspect the target repository's
manifest, entry point, tests, and current output before writing a command or claim.
