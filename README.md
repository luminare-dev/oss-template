<!-- header:begin: the project page on luminare.tech drops this block, because the page has its own heading -->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="docs/brand/readme-header-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="docs/brand/readme-header-light.svg">
  <img alt="{{PROJECT_TITLE}}" src="docs/brand/readme-header-light.svg">
</picture>

<!-- byline:studio -->
*a [Luminare Development](https://luminare.tech/open-source/{{SLUG}}/) open-source project*
<!-- /byline:studio -->
<!-- byline:personal
*by {{AUTHOR_NAME}} · [project page](https://luminare.tech/open-source/{{SLUG}}/)*
/byline:personal -->
<!-- header:end -->

<!-- template-only:begin -->
> [!NOTE]
> This is the template for luminare-dev repositories. Use **Use this template**, then work through
> [PUBLISHING.md](PUBLISHING.md) and fill the [placeholders](PLACEHOLDERS.md). Delete this note.
<!-- template-only:end -->

# {{PROJECT_TITLE}}

{{ONE_LINE_PURPOSE}}

[![ci](https://github.com/luminare-dev/{{SLUG}}/actions/workflows/ci.yml/badge.svg)](https://github.com/luminare-dev/{{SLUG}}/actions/workflows/ci.yml)
[![release](https://img.shields.io/github/v/release/luminare-dev/{{SLUG}}?sort=semver)](https://github.com/luminare-dev/{{SLUG}}/releases)
[![licence](https://img.shields.io/github/license/luminare-dev/{{SLUG}})](LICENSE)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/luminare-dev/{{SLUG}}/badge)](https://scorecard.dev/viewer/?uri=github.com/luminare-dev/{{SLUG}})

<!-- template: optional screenshot or GIF (docs/media/demo.gif); delete this hint if there is none. -->

## Install

```bash
{{QUICKSTART_COMMANDS}}
```

Details: [docs/install.md](docs/install.md).

## Usage

<!-- template: the essentials: one example and the options most people need. -->

## Documentation

[Install](docs/install.md) · [Configuration](docs/configuration.md) · [Upgrade](docs/upgrade.md) ·
[Troubleshooting](docs/troubleshooting.md) · [Runbook](docs/runbook.md) · [Changelog](CHANGELOG.md)

[Contributing](https://github.com/luminare-dev/.github/blob/main/CONTRIBUTING.md) ·
[Security](https://github.com/luminare-dev/.github/blob/main/SECURITY.md) ·
[Code of conduct](https://github.com/luminare-dev/.github/blob/main/CODE_OF_CONDUCT.md)

<!-- fxserver:begin -->
## Not affiliated

Not affiliated with or endorsed by Cfx.re, Rockstar Games or Take-Two. FiveM, RedM and FXServer
are named only to describe what this project works with.

<!-- template: keep this section only for FiveM/RedM projects; otherwise delete it. -->
<!-- fxserver:end -->

## Licence

[{{SPDX_ID}}](LICENSE). The project name, logo and `docs/brand/` are not covered (see [NOTICE](NOTICE)).

<!-- byline:studio -->
*a [Luminare Development](https://luminare.tech/open-source/{{SLUG}}/) open-source project*
<!-- /byline:studio -->
<!-- byline:personal
*by {{AUTHOR_NAME}} · [project page](https://luminare.tech/open-source/{{SLUG}}/)*
/byline:personal -->
