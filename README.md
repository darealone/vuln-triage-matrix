# Vulnerability Triage Matrix

An interactive, single-file web tool for triaging security advisories: which to fix first, how to contain each one, and what you've already handled.

**▶ Live version:** https://darealone.github.io/vuln-triage-matrix/

## What it does
- **Prioritises by real-world risk.** Advisories that are being exploited in the wild (e.g. on the CISA KEV list) rank above higher-CVSS bugs nobody is attacking yet.
- **Filters** by attack surface, exploitation, triage status, minimum CVSS, and free-text search (press `/`).
- **Explains each advisory:** affected versions, impact, the "blind spot" people usually miss, and immediate containment steps with copy-ready commands.
- **Tracks your progress.** Mark each item Open / Investigating / Mitigated. This is saved in your browser only.
- **Exports** a Markdown checklist (for Slack/Jira) or a CSV (for Excel/Sheets).
- **Links sources** for every entry so you can verify before acting.

## Data
A snapshot as of **2026-10-29**, covering 9 advisories (Linux kernel TCP/MPTCP, LiteLLM supply-chain compromise, Chrome/Safari chains, Brotli "Node2Shell", PHP2Shell, Tailscale "Tailworm", Cisco ASA/FTD, Windows HTTP.sys, VMware ESXi).

> ⚠️ Patch status changes daily. Always confirm against the linked vendor advisories before making changes in production, and test commands on one machine first.

## Editing
Everything is in `index.html`. To add or update an advisory, edit the `ADVISORIES` array near the top of the `<script>`. The counts, filters and slider range update automatically.

## Usage
Open `index.html` in any modern browser. No build step, no dependencies, works offline.
