# Choosing the licence

Unchanged copies of the licences used in luminare-dev repositories. Keep one as `LICENSE`.

| File | Use for |
|---|---|
| [Apache-2.0.txt](Apache-2.0.txt) | Infrastructure code: Ansible, Prometheus rules, Grafana dashboards, exporters |
| [MIT.txt](MIT.txt) | Tools, apps, libraries, docs repositories |
| [MIT-0.txt](MIT-0.txt) | Starter files users copy into their own projects |

1. Copy the file to `LICENSE` (always fresh, the template's own `LICENSE` has its year). For MIT,
   fill in the year and copyright holder; Apache-2.0 stays unchanged and the copyright goes in `NOTICE`.
2. Use the `NOTICE` that brand-repos generates.
3. Fill the `SPDX_ID` placeholder in the README.
4. Delete `licenses/` and its line in `.forbidden-words-allow` (keep `MIT-0.txt` if some files use it).
5. List vendored code in `THIRD_PARTY_NOTICES.md`.

Contributions use the DCO (`git commit -s`), inbound = outbound, no CLA.
