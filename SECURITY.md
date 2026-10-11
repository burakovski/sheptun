# Security Policy

## Supported versions

Security fixes are applied to the latest `main` branch of **sheptun**.

## Threat model (short)

- Sheptun is designed so **user audio stays in the browser**
- Models and libraries are loaded from **public CDNs** (supply-chain risk is real)
- There is **no first-party backend** in this repo that stores transcripts

## Reporting a vulnerability

Please **do not** open a public issue for security problems.

Prefer:

1. GitHub **Private vulnerability reporting** (Security tab), if enabled on the repo  
2. Or email the maintainer listed on the GitHub profile / release notes

Include:

- Description and impact
- Steps to reproduce
- Browser / OS / Sheptun commit or version
- Whether the issue involves CDN / model loading, XSS, or data exfiltration

We aim to acknowledge reports within **7 days**.

## Safe research

- Do not upload others’ private recordings to public trackers
- Do not perform DoS against third-party model hosts as “tests”
