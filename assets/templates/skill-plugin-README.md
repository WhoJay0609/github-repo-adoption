<!--
Template: skill or plugin repository README.
Before publishing: replace every {{PLACEHOLDER}}, verify each path and command,
and delete comments plus optional sections that do not apply. Do not ship a
placeholder command, invented output, unsupported harness, or empty scaffold.
Minimum existing entry point: one real */SKILL.md. If this is a plugin, also name
the existing manifest path (for example .codex-plugin/plugin.json); remove the
manifest row and plugin sections for a plain skill. Minimum layout should name the
skill path, manifest (if any), and only the supporting `references/` or `assets/`
directories that exist. Label each command/path as tested, documented, or
illustrative; remove illustrative content before publishing.
-->

# {{PROJECT_NAME}}

{{ONE_SENTENCE_PURPOSE_WITH_REAL_SCOPE}}

<!-- Keep this opening to one or two sentences. State the user task and the harness
or plugin that is actually supported; do not use stars, ranking, or vague “works
everywhere” claims as proof. Repository title/description/topics should use the
same truthful task keywords; retain an existing repository name unless a rename is
explicitly requested. -->

## What is included

| Component | Existing path | Loaded or used when |
| --- | --- | --- |
| Skill | `{{SKILL_PATH}}/SKILL.md` | `{{TRIGGER_OR_TASK_MATCH}}` |
| Plugin manifest *(optional)* | `{{PLUGIN_MANIFEST_PATH}}` | `{{CATALOG_OR_INSTALL_EVENT}}` |
| Supporting assets *(optional)* | `{{ASSETS_PATH}}` | `{{WHEN_USED}}` |

<!-- Keep only rows that exist in the checkout. Link to the actual files so a user
can inspect the contract before installing. Add an evidence label when a path is
documented rather than observed. -->

## Install

### {{HARNESS_OR_PLUGIN_NAME}}

Requirements: {{REAL_RUNTIME_AND_VERSION_SOURCE}}

```console
$ {{VERIFIED_INSTALL_COMMAND}}
{{OBSERVED_INSTALL_OUTPUT}}
```

<!-- Replace the command and output with a run from this repository or remove this
block and explain why installation could not be verified. For a local skill, show
the supported destination and trigger. For a plugin, show the real marketplace or
manifest command; do not invent a catalog entry. -->

## First use

```console
$ {{VERIFIED_SKILL_INVOCATION_OR_PLUGIN_COMMAND}}
{{OBSERVED_RESULT_OR_OUTPUT}}
```

{{ONE_REAL_TASK_EXAMPLE_AND_RESULT}}

Evidence status: `{{tested|documented|illustrative}}`; source: `{{EVIDENCE_SOURCE_PATH_OR_URL}}`.

<!-- A first-use result may be a short terminal transcript, generated file path, or
other observable artifact. Keep secrets and machine-specific paths out of it. -->

## Compatibility

| Harness / platform | Status | Evidence and date |
| --- | --- | --- |
| {{HARNESS_OR_OS}} | tested / documented / unknown | {{COMMAND_OR_SOURCE}} — {{YYYY-MM-DD}} |

<!-- “Supported” requires a real test or an explicit upstream contract. If only the
README says it, use documented. Delete rows that are not relevant. -->

## Boundaries and configuration

- {{WHAT_THE_SKILL_OR_PLUGIN_DOES}}
- {{INPUTS_PERMISSIONS_DATA_OR_NETWORK_BOUNDARY}}
- {{KNOWN_LIMIT_OR_UNSUPPORTED_CASE}}

<!-- Keep safety, data, and permission boundaries next to the first-use path. Remove
this section only when the project has no meaningful boundary to explain. -->

## Contributing

1. Change the existing source under `{{SOURCE_PATH}}`.
2. Run `{{VERIFIED_CHECK_COMMAND}}` and include the observed result.
3. In an issue or pull request, name the path, task, expected behavior, actual
   behavior/output, and the smallest proposed change.

<!-- Replace the path/check with real repository commands. Remove a step that does
not exist; do not add a mandatory CI or framework just for this template. -->

## License

{{LICENSE_NAME}} — see [{{LICENSE_PATH}}]({{LICENSE_LINK}}).
