# Security Policy

## Supported Versions

This repository contains a Grafana dashboard and related documentation for monitoring multiple systems through Grafana, Prometheus, and external exporters.

| Version | Supported |
| ------- | --------- |
| Latest release | Yes |
| Older releases | Best effort only |
| Forks or modified dashboards | Not supported |

Security fixes, if needed, will target the latest version of the dashboard JSON and documentation.

## Project Scope

This project does not run a backend service, authentication system, database, or hosted API. The main security surface is the dashboard configuration, Prometheus queries, documentation, and any example values that may be copied into a real monitoring environment.

Security reports are relevant when they involve this repository directly, for example:

- Exposed secrets, tokens, API keys, passwords, cookies, or private credentials in the repository.
- Public examples that accidentally reveal private infrastructure details, internal hostnames, private IP addresses, serial numbers, device identifiers, or personal metrics.
- Dashboard configuration that encourages unsafe Grafana, Prometheus, or exporter exposure.
- Queries or panel settings that could unintentionally expose sensitive metrics when imported into a shared Grafana instance.
- Malicious links, unsafe download instructions, or compromised external references in the documentation.
- Supply chain concerns involving files distributed directly by this repository.

## Out of Scope

The following are normally not considered vulnerabilities in this repository:

- Security issues in Grafana, Prometheus, Node Exporter, Windows Exporter, PromDapter, Solis exporters, Tuya exporters, or any other upstream exporter. Report those to the upstream project.
- A user's own Grafana, Prometheus, reverse proxy, firewall, VPN, or exporter misconfiguration.
- Publicly exposed dashboards caused by a user's deployment choices.
- Dashboard layout bugs, broken panels, missing metrics, or incorrect visualizations unless they cause sensitive data exposure.
- The ability to edit, copy, import, or modify the dashboard after downloading it.
- Fake or local test data shown by a user's own monitoring setup.

## Reporting a Vulnerability

Do not open a public issue with sensitive security details.

Preferred reporting path:

1. Use GitHub Private Vulnerability Reporting if it is enabled for this repository.
2. If private reporting is not available, contact the maintainer through GitHub before sharing sensitive details.
3. Include enough information to reproduce or verify the issue without exposing unrelated private data.

A good report should include:

- A clear description of the issue.
- The affected file, dashboard panel, query, link, or documentation section.
- Why the issue creates a security risk.
- Steps to reproduce, if applicable.
- Suggested remediation, if known.

Please avoid sending real tokens, passwords, private keys, or full production configuration files. Redact sensitive values before submitting the report.

## Expected Response

Security reports are handled on a best effort basis.

For valid reports, the expected process is:

1. Confirm whether the issue affects this repository.
2. Remove or correct the unsafe content.
3. Release an updated dashboard or documentation change when needed.
4. Credit the reporter if requested and appropriate.

There is no guaranteed response time, paid bounty, or formal service-level agreement.

## Security Guidance for Users

Before importing or adapting this dashboard, review the configuration for your own environment.

Recommended practices:

- Keep Grafana behind authentication unless the instance is strictly local and intentionally read-only.
- Do not expose Prometheus, exporters, or metrics endpoints directly to the public internet.
- Place monitoring services behind a firewall, VPN, reverse proxy with authentication, or a private network such as Tailscale.
- Treat energy usage, hardware metrics, device names, hostnames, IP addresses, and uptime data as potentially sensitive.
- Remove or anonymize personal labels, internal hostnames, device serials, addresses, and location data before sharing screenshots or dashboard exports.
- Do not commit production `prometheus.yml`, `.env`, API tokens, Solis credentials, Tuya credentials, Grafana API keys, or datasource credentials.
- Rotate any credential immediately if it was committed, shared, or exposed through a dashboard, screenshot, log, or exported JSON.
- Review permissions before enabling anonymous Grafana access or embedding dashboards in public pages.

## Upstream Security Issues

This dashboard depends on external systems and exporters. If the vulnerability is in one of those tools, report it to the upstream maintainer instead of this repository.

Examples include:

- Grafana authentication or authorization flaws.
- Prometheus query engine or API vulnerabilities.
- Exporter vulnerabilities.
- Hardware vendor API issues.
- Tuya, Solis, HWiNFO, Windows, Linux, or PiKVM security issues.

This repository can update documentation or dashboard guidance when an upstream security issue affects safe usage, but it cannot patch upstream software directly.
