# Recommended GitHub Settings

Apply these to every derived repo.

## General

- Keep the repo private until the container, docs, and Actions are validated
- Enable Issues and Discussions only if you plan to support them
- Disable Wikis and Projects unless you actively use them

## Branch Protection

Create a ruleset for `main`:

- require pull request before merge
- require status checks to pass before merge
- require signed commits
- require linear history
- block force pushes
- block branch deletion
- include administrators

Suggested required checks:

- `smoke-test`

## Actions

- Set `Workflow permissions` to `Read repository contents and packages`
- Enable `Allow GitHub Actions to create and approve pull requests` only if you explicitly want that
- Prefer `Allow select actions and reusable workflows`
- Allow GitHub-authored actions and verified creators

## Security

- Enable Dependabot alerts
- Enable Dependabot security updates
- Enable secret scanning
- Enable push protection
- Enable private vulnerability reporting
- Enable code scanning later if you add a relevant analyzer

## Packages

- After the first successful publish, make the GHCR package public if the repo is public
- Verify the package name matches the intended CA XML repository value

## Secrets and Variables

Required variables:

- `ENABLE_AIO_AUTOMATION=true`
- `TEMPLATE_XML`
- `AWESOME_UNRAID_REPOSITORY`
- `AWESOME_UNRAID_XML_NAME`
- `AWESOME_UNRAID_ICON_NAME`

Optional variables:

- `IMAGE_NAME_OVERRIDE`
- `TEMPLATE_ICON_PATH`

Required secret:

- `SYNC_TOKEN`
