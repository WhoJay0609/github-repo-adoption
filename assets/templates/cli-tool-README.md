<!--
Template: executable CLI repository README.
Before publishing: replace every {{PLACEHOLDER}}, verify commands against the
manifest and executable entry point, and remove unused optional sections. Do not
ship fake output, a made-up package name, or a framework/CI scaffold.
Minimum existing entry point: an executable declaration in pyproject.toml,
package.json, Cargo.toml, a Go main package, or an equivalent source path.
Minimum layout should name that manifest/declaration, its source entry point, and
tests or docs only when they exist. Label commands and paths as tested, documented,
or illustrative; remove illustrative content before publishing.
-->

# {{PROJECT_NAME}}

`{{BINARY_NAME}}` {{ONE_SENTENCE_JOB_AND_PRIMARY_INPUT}}

<!-- Derive the title, description, and topics from this binary's actual task,
inputs, and supported platforms. Retain an existing repository name unless a rename
is explicitly requested. -->

## Install

Requirements: {{RUNTIME_AND_VERSION_FROM_MANIFEST}}

```console
$ {{VERIFIED_INSTALL_COMMAND}}
{{OBSERVED_INSTALL_OUTPUT}}
```

<!-- Copy the smallest command that actually installs this binary. Include a package
manager or source-build path only when the repository supplies it. Mark the block
tested or documented; use illustrative only while drafting and remove it later. -->

## First run

```console
$ {{BINARY_NAME}} {{VERIFIED_HELP_OR_VERSION_COMMAND}}
{{OBSERVED_HELP_OR_VERSION_OUTPUT}}
```

Evidence status: `{{tested|documented|illustrative}}`; source: `{{EVIDENCE_SOURCE_PATH_OR_URL}}`.

<!-- This is a real transcript placeholder: replace it before publishing or remove
the block. Keep output short enough to scan and redact secrets. -->

## Common tasks

| Task | Command | Input / output |
| --- | --- | --- |
| {{TASK_ONE}} | `{{VERIFIED_COMMAND_ONE}}` | {{OBSERVED_RESULT_ONE}} |
| {{TASK_TWO}} | `{{VERIFIED_COMMAND_TWO}}` | {{OBSERVED_RESULT_TWO}} |

<!-- Keep only commands that exist in the current CLI. Link to the source or test
that defines non-obvious flags, formats, exit codes, or generated files. -->

## Inputs, outputs, and configuration

- Input: {{REAL_INPUT_CONTRACT}}
- Output: {{REAL_OUTPUT_CONTRACT}}
- Configuration: `{{CONFIG_PATH_OR_ENV}}` — {{DEFAULTS_AND_SECRET_HANDLING}}
- Exit behavior: {{DOCUMENTED_OR_TESTED_EXIT_CODES}}

<!-- Remove a bullet that is not part of the interface. Never promise a file, API,
or environment variable that the implementation does not read. -->

## Compatibility

| Platform / runtime | Status | Evidence and date |
| --- | --- | --- |
| {{PLATFORM_OR_RUNTIME}} | tested / documented / unknown | {{COMMAND_OR_SOURCE}} — {{YYYY-MM-DD}} |

## Troubleshooting *(optional)*

### {{OBSERVED_ERROR_MESSAGE}}

{{CAUSE_AND_RECOVERY_FROM_REAL_LOG_OR_SOURCE}}

<!-- Keep only errors a user can actually encounter. Remove this section if there is
no verified troubleshooting guidance. -->

## Development and contribution

```console
$ {{VERIFIED_DEV_OR_TEST_COMMAND}}
{{OBSERVED_CHECK_RESULT}}
```

Contributions should identify the command/path involved, the expected and observed
behavior, a reproducible input, and the smallest fix. Remove this block when the
repository does not expose a development command; do not require new CI or tooling.

## License

{{LICENSE_NAME}} — see [{{LICENSE_PATH}}]({{LICENSE_LINK}}).
