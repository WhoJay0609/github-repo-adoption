<!--
Template: curated repository/catalog README.
Before publishing: replace every {{PLACEHOLDER}}, verify each data source and
refresh command, and remove optional sections that are not real. Do not add star
rankings, “best” claims, copied entries, or generated scripts without provenance.
Minimum existing entry point: a real catalog source (for example index.md,
catalog.yml, data.json, or a database) plus the navigation/generator path if one
exists. If the list is manually edited, say so and remove generator language.
Minimum layout should name the source-of-truth file, the rendered index (if
different), and a real refresh/validation path only when one exists. Label every
path and command as tested, documented, or illustrative; remove illustrative
content before publishing.
-->

# {{CATALOG_NAME}}

{{ONE_SENTENCE_SCOPE}}. Entries are selected using {{INCLUSION_RULE}}.

<!-- Derive the title, description, and topics from the catalog's maintained scope
and entry types. Retain an existing repository name unless a rename is explicitly
requested. -->

## Browse

| Area | Entries or source | How to start |
| --- | --- | --- |
| {{CATEGORY_ONE}} | {{LINK_OR_SOURCE_ONE}} | {{REAL_FIRST_USE_ACTION_ONE}} |
| {{CATEGORY_TWO}} | {{LINK_OR_SOURCE_TWO}} | {{REAL_FIRST_USE_ACTION_TWO}} |

<!-- Use categories that exist in the current catalog. Keep the first-use action
specific: open the entry, install the linked project, or run the verified search.
Remove a category row rather than filling it with placeholder projects. -->

## First use

1. Open [{{CATALOG_INDEX_PATH}}]({{CATALOG_INDEX_LINK}}) and search for `{{REAL_SEARCH_TERM}}`.
2. Choose a real entry and use the branch that matches the catalog; delete the
   other branch before publishing.

### Installable project *(optional)*

Choose [{{VERIFIED_ENTRY_NAME}}]({{VERIFIED_ENTRY_URL}}), then follow its own
verified installation or first-use command:

```console
$ {{VERIFIED_ENTRY_INSTALL_OR_USE_COMMAND}}
{{OBSERVED_RESULT_OR_OUTPUT}}
```

### Paper, dataset, or reference entry *(optional)*

Open [{{VERIFIED_REFERENCE_ENTRY_NAME}}]({{VERIFIED_REFERENCE_ENTRY_URL}}), then
{{VERIFIED_READ_FILTER_OR_COMPARE_ACTION}}. Record the observed page, filtered
rows, comparison, or other artifact:

```text
{{OBSERVED_REFERENCE_ARTIFACT_OR_RESULT}}
```

<!-- Keep one branch only when it matches the catalog. The entry and transcript or
artifact must be real and dated. A catalog cannot claim that every linked project
works; keep project-specific compatibility in its entry. -->

Evidence status: `{{tested|documented|illustrative}}`; source: `{{EVIDENCE_SOURCE_PATH_OR_URL}}`.

## Entry format

```markdown
- [{{PROJECT_NAME}}]({{PROJECT_URL}}) — {{WHAT_IT DOES}}; {{INTEGRATION_OR_COMPATIBILITY_EVIDENCE}}.
```

Required fields: a stable URL, one factual purpose sentence, and {{REQUIRED_EVIDENCE}}.
Use `{{LAST_VERIFIED_DATE}}` when freshness matters. Remove a field that this catalog
does not maintain rather than inventing data.

## Scope and exclusions

- Include: {{INCLUSION_EXAMPLES}}
- Exclude: {{EXCLUSION_EXAMPLES}}
- Ranking or star totals: {{SOURCED_DATED_POLICY_OR_NOT_USED}}

<!-- State whether entries are manually reviewed, generated from a source, or both.
Do not infer quality or popularity from order. -->

## Data source and refresh *(optional)*

Canonical source: `{{CATALOG_SOURCE_PATH_OR_URL}}`.

```console
$ {{VERIFIED_REFRESH_OR_VALIDATION_COMMAND}}
{{OBSERVED_REFRESH_RESULT}}
```

<!-- Keep only when the source and command exist. If a script generates the README,
link it and record the source-of-truth file; do not create a fake generator. -->

## Contributing

Submit an issue or pull request with the proposed entry, stable URL, factual
description, inclusion evidence, and the date or command used to verify it. Changes
to generated output must update `{{SOURCE_OF_TRUTH_PATH}}` first and run
`{{VERIFIED_CHECK_COMMAND}}`. Remove the source/check instruction when it does not
apply; do not require new CI or ranking automation.

## License

{{LICENSE_NAME}} — see [{{LICENSE_PATH}}]({{LICENSE_LINK}}).
