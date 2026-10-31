# Placeholders

CI fails while any of these is still open in a new repository.

| Placeholder | Where | Fill with |
|---|---|---|
| `{{SLUG}}` | README, `docs/install.md` | Repository name (lower case, hyphens, no platform names). |
| `{{PROJECT_TITLE}}` | README | Display name, no platform or vendor marks. |
| `{{ONE_LINE_PURPOSE}}` | README | One sentence: what it does and for whom. |
| `{{QUICKSTART_COMMANDS}}` | README, `docs/install.md` | A few copy-paste install commands. |
| `{{COMPONENT}}`, `{{SUPPORTED_RANGE}}` | `docs/install.md` | Runtime requirements. |
| `{{SPDX_ID}}` | README | Licence id, see [licenses/CHOOSING.md](licenses/CHOOSING.md). |
| `{{AUTHOR_NAME}}`, `{{YEAR}}` | personal byline, `LICENSE`, `NOTICE` | Copyright holder and year of first publication. |
| `{{VERSION}}` | `docs/upgrade.md` | Version an upgrade note applies to. |

Also check: `docs/brand/` (regenerate for the new slug), and the required checks
`ci / lint-test`, `secrets / gitleaks`, `pr / pr-title`, `DCO` in the ruleset.
