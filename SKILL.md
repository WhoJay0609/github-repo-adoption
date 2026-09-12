---
name: github-repo-adoption
description: Audit or improve a GitHub repository's metadata, README, and local skill surface so a real user or agent can find, understand, and try it; make minimal evidence-backed docs or function changes without promising ranking or star growth.
---

# GitHub repository adoption

Use this skill for a repository whose public description, first-use path, or installed
skill/plugin entry is hard to find, understand, or verify. Treat “adoption” as a
better path from discovery to a working first use; it is not a promise of search
ranking, recommendations, stars, or growth.

Keep these surfaces separate:

- **Metadata:** repository name, description, and topics are public search inputs.
- **README:** the first-screen explanation and a linkable first-use path.
- **Local skill/plugin:** `name`, `description`, manifest, and installed paths control
  local harness routing or catalog distribution. `AGENTS.md`, `CLAUDE.md`, and
  `llms.txt` are separate mechanisms; adding one does not prove public discovery.

Read [references/evidence.md](references/evidence.md) when choosing sections,
explaining these boundaries, or citing the dated study. It contains portable source
URLs and a frozen snapshot; it is not live ranking evidence. Read one matching file
under [assets/templates](assets/templates) when the requested output is a README;
replace every placeholder and remove every unused optional section before delivery.

Choose templates by the real entry point: `skill-plugin-README.md` for an existing
`SKILL.md` (and optional plugin manifest), `cli-tool-README.md` for an executable
declaration, `guide-README.md` for a documentation/tutorial entry, and
`curated-catalog-README.md` for an existing catalog source. Describe task keywords,
title, description, and topics from that capability. Keep an existing repository
name unless renaming is explicitly requested.

## Workflow

1. **Freeze scope and state.** Record the repository, requested outcome, files you may
   edit, and whether an external publication is authorized. Run `git status --short`
   when this is a Git checkout and preserve unrelated dirty or untracked work. A
   read-only audit ends with findings; an edit request authorizes only the named
   scope and the smallest necessary adjacent file.

   Done means the scope and existing changes are recorded, with no reset, cleanup,
   or unrequested publication.

2. **Trace the real entry point.** Read the current README, manifest, package scripts,
   executable declarations, source entry points, tests, and relevant configuration.
   Use `rg --files` and `rg` first. Derive commands from the repository (for example,
   a `pyproject.toml` console script, `package.json` `bin`, Cargo binary, Make target,
   or documented script); never invent a CLI, plugin manifest, framework, or install
   path to make the project look more discoverable.

   Done means each claimed install, command, output, and compatibility target has a
   source location or is marked unknown.

3. **Audit the first-use path.** Find the smallest safe install/version/help/test
   command. Run it only when the environment and authorization allow it, and keep
   the observed output. Classify each statement as `tested`, `documented`, or
   `unknown`; a README claim alone is not runtime compatibility evidence. Check
   required files, input/output shape, exit behavior, OS/runtime constraints, and
   failure messages against the actual implementation.

   Done means a new user could follow one concrete path, or the missing evidence and
   exact blocker are visible.

4. **Map the discovery surfaces.** Check whether the task is about public repository
   search (metadata, or README only when a query uses `in:readme`), a fetched README,
   an installed local skill (`SKILL.md` frontmatter), or a marketplace/plugin
   catalog. Improve only the surface that causes the observed failure. Keep
   cross-harness support separate unless the repository actually supplies and tests
   it.

   Metadata edits should use only truthful task terms, supported harnesses, and
   existing interfaces. Topics must match the repository's actual capability; they
   are not a place to list adjacent tools for reach.

5. **Choose the smallest correction.** Prefer a truthful metadata or README edit.
   If a documented command reaches a real function bug, trace all callers, fix the
   first wrong state in that shared path, and update the smallest affected example.
   Preserve public interfaces and project contracts. Keep existing or useful,
   verified CI/license badges when they carry evidence; avoid decorative or
   unverified badges, star graphs, SEO promises, generated boilerplate, and
   speculative wrappers. Mark examples as illustrative until a real command and
   output replace them.

6. **Apply and verify.** Edit only authorized files with a focused patch. For a README
   template, fill the minimum layout and existing entry-point paths, add one actual
   first-use command/output/evidence block, and delete sections that do not apply.
   Check relative links, placeholder removal, frontmatter, executable declarations,
   and the affected tests or `--help` path. Recheck `git diff` and `git status` so
   unrelated work remains untouched.

   If the request explicitly authorizes a public push, publication, or metadata
   update, that authorization covers the named action; this skill adds no approval
   gate. Otherwise stop before the external write and report the prepared local
   result.

## Output

Report, in this order: scope and excluded files; discovery surface; evidence with
source paths or URLs and tested/documented/unknown labels; exact changes; checks and
observed output; compatibility and remaining risk. Separate measured facts from
inference. Do not claim improved ranking, stars, recommendation, or cross-harness
support without direct evidence.
