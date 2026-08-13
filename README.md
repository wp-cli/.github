wp-cli/.github
===================

🌐 Centralized community health files for all repositories

Quick links: [Using](#using) | [Installing](#installing) | [Contributing](#contributing) | [Support](#support)

## Using

This package cannot be used directly. It is a container to provide centralized fallback for community health files for the `wp-cli` Github organization.

See: [https://help.github.com/en/articles/creating-a-default-community-health-file-for-your-organization](https://help.github.com/en/articles/creating-a-default-community-health-file-for-your-organization)

### GitHub Actions Workflows

This repository contains reusable GitHub Actions workflows that are automatically synced to all WP-CLI repositories:

- **Code Quality Checks** (`code-quality.yml`) - Runs linting, PHPCS, PHPStan, and other code quality tools
- **Regenerate README** (`regenerate-readme.yml`) - Automatically regenerates README.md files from source
- **Check Branch Alias** (`check-branch-alias.yml`) - Monitors and updates Composer branch-alias configuration

#### Branch Alias Checker

The branch alias checker workflow automatically ensures that the Composer `branch-alias` in each repository's `composer.json` is up-to-date. It:

1. Runs on every release or can be triggered manually
2. Checks the latest release tag
3. On a new major release (`vX.0.0`), updates the branch-alias to `X.x-dev`
4. Skips minor and patch releases, as the branch-alias should remain unchanged
5. Creates a pull request if an update is needed

For example, if a repository releases `v2.2.6` or `v2.3.0`, the branch-alias stays at `2.x-dev`. Only when releasing `v3.0.0` should it change to `3.x-dev`.

## Installing

There's nothing to install, this package cannot be used directly.

## Contributing

We appreciate you taking the initiative to contribute to this project.

Contributing isn’t limited to just code. We encourage you to contribute in the way that best fits your abilities, by writing tutorials, giving a demo at your local meetup, helping other users with their support questions, or revising our documentation.

For a more thorough introduction, [check out WP-CLI's guide to contributing](https://make.wordpress.org/cli/handbook/contributing/). This package follows those policy and guidelines.

### Reporting a bug

Think you’ve found a bug? We’d love for you to help us get it fixed.

Before you create a new issue, you should [search existing issues](https://github.com/wp-cli/.github/issues?q=label%3Abug%20) to see if there’s an existing resolution to it, or if it’s already been fixed in a newer version.

Once you’ve done a bit of searching and discovered there isn’t an open or fixed issue for your bug, please [create a new issue](https://github.com/wp-cli/.github/issues/new). Include as much detail as you can, and clear steps to reproduce if possible. For more guidance, [review our bug report documentation](https://make.wordpress.org/cli/handbook/bug-reports/).

### Creating a pull request

Want to contribute a new feature? Please first [open a new issue](https://github.com/wp-cli/.github/issues/new) to discuss whether the feature is a good fit for the project.

Once you've decided to commit the time to seeing your pull request through, [please follow our guidelines for creating a pull request](https://make.wordpress.org/cli/handbook/pull-requests/) to make sure it's a pleasant experience. See "[Setting up](https://make.wordpress.org/cli/handbook/pull-requests/#setting-up)" for details specific to working on this package locally.

## Support

Github issues aren't for general support questions, but there are other venues you can try: https://wp-cli.org/#support
