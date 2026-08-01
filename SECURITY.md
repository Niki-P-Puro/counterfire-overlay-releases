# Counterfire Security Policy

## Reporting A Vulnerability

Do not open a public issue for vulnerabilities, exposed credentials, authorization
bypasses, private server details, or reports containing user data.

Use GitHub's **Report a vulnerability** button on the repository Security page when
private vulnerability reporting is available. If that option is unavailable, open a
public issue containing no vulnerability details and ask the owner to establish a
private reporting channel.

Please include:

- the affected Counterfire version
- the affected component: installer, updater, Windows client, or multiplayer backend
- reproducible steps and expected impact
- whether the issue is actively being exploited

Do not include live lobby codes, access tokens, private network credentials, signing
keys, or unrelated personal information.

## Supported Version

Counterfire is an early test release. Security fixes are delivered through the latest
published version only. Update to the newest release before reporting an issue that
may already have been corrected.

## Release Integrity

Official Windows releases are published only in this repository. Counterfire validates
an Ed25519-signed update manifest and verifies the installer size and SHA-256 hash before
an in-app update is accepted. These checks protect update integrity but do not replace
Windows Authenticode signing or SmartScreen reputation.
