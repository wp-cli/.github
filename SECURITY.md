# Security Policy

WP-CLI is used to administer WordPress sites in production, frequently with
elevated privileges, so we take security reports seriously.

This is the organization-wide default policy for repositories in the
[`wp-cli` organization](https://github.com/wp-cli). A repository that publishes
its own `SECURITY.md` overrides this one.

## Reporting a vulnerability

**Please do not report security vulnerabilities through public GitHub issues,
pull requests, or discussions.**

Report them through the WordPress bug bounty program on HackerOne, which covers
WP-CLI alongside WordPress core and related projects:

<https://hackerone.com/wordpress>

Before you submit, please read the full guidance in the WP-CLI handbook:

<https://make.wordpress.org/cli/handbook/contributions/security-vulnerability-reporting/>

That handbook page is the authoritative description of what we treat as a
vulnerability, what to include in a report, and what to expect during
coordinated disclosure. A valid report may be eligible for a CVE and a bounty.

## What makes a report actionable

A vulnerability report needs to show how someone outside a trust boundary gains
something they could not otherwise obtain. Please state plainly:

- who the attacker is and what access they begin with,
- what they gain that they should not have,
- the steps to reproduce it.

Reports that do not demonstrate an actual exploit are likely to be declined.
Note that WP-CLI runs as a trusted local user by design: someone who can already
execute `wp` on a server can generally already act as that user, so that alone
is not a privilege boundary.

## Build and release infrastructure

Reports about this organization's shared CI configuration — the reusable
GitHub Actions workflows in [`wp-cli/.github`](https://github.com/wp-cli/.github)
and the credentials they use — are in scope and are best sent through the same
channel above.
