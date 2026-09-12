<!--
Template: documentation or tutorial repository README.
Before publishing: replace every {{PLACEHOLDER}}, keep only sections backed by the
checkout, and remove all comments. Do not claim a hosted site, translations, build
pipeline, or compatibility that has not been verified.
Minimum existing entry point: an actual guide source such as docs/, a README-linked
tutorial, or a configured site entry. If a site build exists, name its real config
and command; otherwise remove the site section. Minimum layout should name the
source entry, any real site config, and a test/preview command only when present.
Label paths and commands as tested, documented, or illustrative; remove
illustrative content before publishing.
-->

# {{PROJECT_NAME}}

{{AUDIENCE}} can use this guide to {{CONCRETE_OUTCOME}}.

<!-- Derive the title, description, and topics from the documented audience and
outcome. Retain an existing repository name unless a rename is explicitly requested. -->

## Start here

Prerequisites: {{REAL_PREREQUISITES_AND_VERSIONS}}

1. Read [{{FIRST_GUIDE_PATH}}]({{FIRST_GUIDE_LINK}}).
2. Run the smallest verified command:

   ```console
   $ {{VERIFIED_FIRST_USE_COMMAND}}
   {{OBSERVED_OUTPUT_OR_ARTIFACT}}
   ```

Evidence status: `{{tested|documented|illustrative}}`; source: `{{EVIDENCE_SOURCE_PATH_OR_URL}}`.

<!-- Replace the command/output with an actual run, or explicitly say that this is a
read-only guide and remove the block. Mark it tested, documented, or illustrative;
do not leave a guessed command in a public README. -->

## Guide map

| If you need to… | Read | What you should have afterward |
| --- | --- | --- |
| {{TASK_ONE}} | [{{PATH_ONE}}]({{LINK_ONE}}) | {{EXPECTED_RESULT_ONE}} |
| {{TASK_TWO}} | [{{PATH_TWO}}]({{LINK_TWO}}) | {{EXPECTED_RESULT_TWO}} |

<!-- Keep paths aligned with the current tree. A short map is more useful than a
long table of every file. -->

## Canonical workflow

1. {{STEP_ONE_WITH_SOURCE_LINK}}
2. {{STEP_TWO_WITH_SOURCE_LINK}}
3. {{STEP_THREE_WITH_SOURCE_LINK}}

{{EVIDENCE_OR_EXPECTED_ARTIFACT_DESCRIPTION}}

<!-- Delete this section when the guide is reference-only. If steps depend on a
version, record the version/date beside the source rather than hiding it. -->

## Compatibility and limits

| Environment / version | Status | Evidence and date |
| --- | --- | --- |
| {{ENVIRONMENT}} | tested / documented / unknown | {{SOURCE_OR_COMMAND}} — {{YYYY-MM-DD}} |

- {{KNOWN_PREREQUISITE_OR_LIMIT}}
- {{UNSUPPORTED_CASE_OR_SECURITY_BOUNDARY}}

## Troubleshooting *(optional)*

### {{OBSERVED_PROBLEM}}

{{RECOVERY_FROM_A_REAL_SOURCE_OR_RUN}}

<!-- Remove this section when no verified recovery exists. Link to the canonical
source rather than preserving stale copied instructions. -->

## Site or generated output *(optional)*

The published output is {{REAL_SITE_OR_ARTIFACT}}. Build it with:

```console
$ {{VERIFIED_BUILD_OR_PREVIEW_COMMAND}}
{{OBSERVED_BUILD_RESULT}}
```

<!-- Keep only when a site config and working command exist in the repository. -->

## Contributing

Fix the source at `{{DOCS_SOURCE_PATH}}`, then run `{{VERIFIED_DOC_CHECK_COMMAND}}`.
For an issue or pull request, include the page/path, audience, expected wording or
behavior, observed problem, and a small reproducible example. Remove the check when
the repository has no documented one; do not add a mandatory CI service.

## License

{{LICENSE_NAME}} — see [{{LICENSE_PATH}}]({{LICENSE_LINK}}).
