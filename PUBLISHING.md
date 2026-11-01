# Publishing checklist

## New repository

- [ ] Create it from this template as **private**; untick *Template repository* if it was copied.
- [ ] Fill the README and every [placeholder](PLACEHOLDERS.md); delete the template-only note.
- [ ] Brand files: add the repo to brand-repos, copy `out/<slug>/studio/*` to `docs/brand/` and
      `out/<slug>/NOTICE` to `NOTICE`; `python3 scripts/set_byline.py verify --expect studio`.
      Ansible collections: use `README-snippet.md` as the header and add `docs/brand` to
      `build_ignore` in `galaxy.yml`.
- [ ] Licence: see [licenses/CHOOSING.md](licenses/CHOOSING.md).
- [ ] Tests: replace `tests/` and set `test-command` in `ci.yml` and `release.yml` if needed.
- [ ] Settings: required checks `ci / lint-test`, `secrets / gitleaks`, `pr / pr-title`, `DCO`
      (the ruleset is in luminare-dev/.github `rulesets/main.json`); allow Actions to create pull
      requests; immutable releases on.

## Before going public

- [ ] `gitleaks git --redact --config .gitleaks.toml .` is clean over the full history.
- [ ] No personal data, internal IPs or hostnames; example IPs and domains only.
- [ ] No platform or vendor marks in any name (FiveM, Cfx, RedM, txAdmin, GTA, Rockstar, ...).
- [ ] `python3 scripts/forbidden_words.py` passes, also on the commit history and with the
      private term list (`--extra-terms`).
- [ ] Sponsorships off, no funding file. <!-- rule-text -->
- [ ] Social preview uploaded, description and topics set; FXServer projects keep "Not affiliated".
- [ ] Private vulnerability reporting, secret scanning and Dependabot alerts on.
- [ ] Project page and `luminare-dev/.github` links work; check the repo logged out.
- [ ] Added to `repos.json` in oss-metrics.

## Releases

Conventional PR titles only; release-please keeps the release PR up to date. Close and reopen
the release PR once so its checks run. After the merge, verify:

```bash
gh release download vX.Y.Z -R luminare-dev/<slug>
sha256sum -c SHA256SUMS
gh attestation verify <slug>-X.Y.Z.tar.gz -R luminare-dev/<slug>
```

Monthly: check the Actions tab and bump the pinned gitleaks and actionlint downloads by hand.

## Local checks

```bash
python3 scripts/forbidden_words.py --template-mode
python3 scripts/set_byline.py verify --expect studio
python3 scripts/check_workflows.py --list
python3 -m unittest discover -s tests -v
gitleaks git --redact --config .gitleaks.toml .
yamllint --strict . && markdownlint-cli2 "**/*.md" && actionlint && zizmor --offline .github/workflows
```
