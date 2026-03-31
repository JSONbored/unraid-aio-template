# Releases

`unraid-aio-template` uses normal semver releases such as `v0.1.0`.

This repository is not tied to a single wrapped upstream application, so it should not use the app-style `upstream-version-aio.N` format that the derived AIO repos use.

## What a template release means

A template release is a versioned milestone for the scaffolding itself, including:

- CI and workflow changes
- release automation updates
- documentation and support-thread templates
- XML and catalog sync defaults
- generic Docker and rootfs scaffolding improvements

## Release flow

1. Trigger the **Release / Template** workflow from `main`.
2. The workflow computes the next semver version with `git-cliff --bumped-version`.
3. It opens a release PR that updates `CHANGELOG.md`.
4. Merge that PR into `main`.
5. After merge, the workflow creates the Git tag and GitHub Release automatically.
