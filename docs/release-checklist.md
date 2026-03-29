# Release Checklist

## Before First Public Push

- replace every placeholder value and example hostname
- replace `assets/app-icon.png`
- rename `template-aio.xml`
- confirm README, SECURITY, and FUNDING are accurate
- confirm `Support`, `Project`, `TemplateURL`, and `Icon` URLs are correct
- add a screenshot or demo visual if the app has a UI
- set the repo About description, topics, and social preview image

## Before Enabling Actions

- set `ENABLE_AIO_AUTOMATION=true`
- set all required Actions variables
- add `SYNC_TOKEN`
- verify branch protection and secret scanning are enabled

## Before Unraid Submission

- install from the XML in a clean Unraid environment
- verify first boot works with defaults
- verify advanced settings stay optional
- verify generated credentials persist if applicable
- confirm GHCR package is public and pullable
- confirm `awesome-unraid` contains the XML and icon
