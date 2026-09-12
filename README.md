# GitHub Repo Adoption

A Codex skill for evidence-backed improvements to a repository's metadata, README,
and local skill/plugin entry point. It audits real commands and compatibility, then
keeps the smallest useful change. It makes no promise about ranking, stars, or
automatic agent discovery.

## Install

Clone the public repository, then install the checkout as a user skill:

```bash
git clone https://github.com/WhoJay0609/github-repo-adoption.git
cd github-repo-adoption
skill_root="${CODEX_HOME:-$HOME/.codex}/skills"
mkdir -p "$skill_root"
skill_link="$skill_root/github-repo-adoption"
if test -e "$skill_link" || test -L "$skill_link"; then
  printf 'Refusing to replace existing %s\n' "$skill_link" >&2
  exit 1
fi
ln -sT -- "$PWD" "$skill_link"
```

The command uses GNU `ln -sT` on Linux and refuses to replace an existing file or
link. Use the equivalent no-clobber symlink command on another host, then start a
new Codex task so the local skill catalog can refresh.

## Usage

```text
$github-repo-adoption Audit this repository's metadata, README, and local skill entry point. Trace the real first-use command, label evidence as tested/documented/unknown, and propose the smallest scoped improvement.
```

For an authorized edit:

```text
$github-repo-adoption Apply the smallest README or metadata fix supported by the repository's actual entry points. Preserve unrelated dirty work and report exact checks.
```

Read [SKILL.md](SKILL.md) for the workflow, [references/evidence.md](references/evidence.md)
for dated study boundaries and portable sources, and choose a matching file under
[`assets/templates/`](assets/templates) for a skill/plugin, CLI, guide, or curated
catalog README.

## License

MIT © 2026 WhoJay0609. See [LICENSE](LICENSE).
