# Unraid AIO Template

A hardened starter repository for building beginner-friendly but power-user-capable Unraid Community Applications templates and their companion AIO container images.

This template is designed for the exact workflow you are building around `awesome-unraid`:

- one repo per application image/template
- GitHub Actions for smoke-test and GHCR publish
- optional sync automation into `awesome-unraid`
- strong default repo hygiene, docs, and security scaffolding

## What This Template Includes

- starter `Dockerfile` for wrapping an upstream image with `s6-overlay`
- starter Unraid CA XML at [`template-aio.xml`](/tmp/unraid-aio-template/template-aio.xml)
- reusable smoke-test harness at [`scripts/smoke-test.sh`](/tmp/unraid-aio-template/scripts/smoke-test.sh)
- GitHub Actions for build/publish and template sync
- starter docs, changelog, funding, and security files
- issue templates, PR template, and CODEOWNERS
- repo settings and release checklists under [`docs/`](/tmp/unraid-aio-template/docs)

## How To Use It

1. Create a new private repo from this template.
2. Rename `template-aio.xml` to your app slug, for example `myapp-aio.xml`.
3. Replace placeholder values in:
   - [`Dockerfile`](/tmp/unraid-aio-template/Dockerfile)
   - [`template-aio.xml`](/tmp/unraid-aio-template/template-aio.xml)
   - [`rootfs/`](/tmp/unraid-aio-template/rootfs)
   - [`scripts/smoke-test.sh`](/tmp/unraid-aio-template/scripts/smoke-test.sh)
   - [`README.md`](/tmp/unraid-aio-template/README.md)
4. Replace [`assets/app-icon.png`](/tmp/unraid-aio-template/assets/app-icon.png) with the app icon you want used in CA and `awesome-unraid`.
5. Follow the checklist in [`docs/repo-settings.md`](/tmp/unraid-aio-template/docs/repo-settings.md).
6. Set the required Actions variables and secrets from the same checklist.
7. When the repo is customized and ready, set the repository variable `ENABLE_AIO_AUTOMATION=true`.

## Required Repository Variables

Set these in `Settings -> Secrets and variables -> Actions -> Variables`.

- `ENABLE_AIO_AUTOMATION=true`
- `TEMPLATE_XML=yourapp-aio.xml`
- `AWESOME_UNRAID_REPOSITORY=JSONbored/awesome-unraid`
- `AWESOME_UNRAID_XML_NAME=yourapp-aio.xml`
- `AWESOME_UNRAID_ICON_NAME=yourapp.png`

Optional variables:

- `IMAGE_NAME_OVERRIDE=jsonbored/yourapp-aio`
- `TEMPLATE_ICON_PATH=assets/app-icon.png`

## Required Repository Secrets

- `SYNC_TOKEN`
  - Fine-grained personal access token
  - Repository access: `JSONbored/awesome-unraid`
  - Permission: `Contents: Read and write`

## Repository Standards

Every repo created from this template should aim for:

- a single-container first-run experience where practical
- safe defaults for beginners
- advanced knobs exposed but hidden behind Unraid advanced settings
- repeatable smoke tests before publish
- pinned or current official Actions, minimal token permissions, and protected `main`
- enough README proof and screenshots that the repo works as a trust asset, not just a code host

## Release Checklist

Use [`docs/release-checklist.md`](/tmp/unraid-aio-template/docs/release-checklist.md) before making any repo public or submitting it to CA.

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=JSONbored/unraid-aio-template&type=date&legend=top-left)](https://www.star-history.com/#JSONbored/unraid-aio-template&Date)
