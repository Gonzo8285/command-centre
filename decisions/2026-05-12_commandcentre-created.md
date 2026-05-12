---
date: 2026-05-12
author: PPC
status: closed
tags: [meta, durability]
---

# Command Centre created

## Trigger
Paul lost a PowerShell snippet to chat scrollback. Real risk: with multiple
projects in flight and async work across PPC + 151, anything that lives
only in a conversation will eventually be lost.

## Decision
Stand up `G:\My Drive\ClaudeBridge\CommandCentre\` as the single durable
place for:

- Scripts (paths + what they do, not duplicates — the canonical script
  stays in its project folder).
- Runbook commands (copy-paste blocks).
- Project state (one card per workstream).
- Decisions log (this folder, append-only).
- Reference paths.

The page is a single self-contained `index.html`. No build step, no CDN
dependency, no server. Opens from Drive in any browser, on any host
that has Drive synced.

## Rule going forward
Every script PPC sends Paul also gets a row registered in the Latest /
Scripts section of `index.html`, with the canonical path on Drive.
The chat is for discussion; the Command Centre is the source of truth.

## Open follow-ups
- Phase A of Bridge v2 still needs Paul to run `install-bridge.ps1` on
  PPC and then on 151.
- Once bridge is up, decision-log entries should also be mirrored to the
  cloud status pack so 151 sees them.
