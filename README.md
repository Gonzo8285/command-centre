# Command Centre

One durable place for everything PPC and Paul work on together.

## Layout

```
CommandCentre/
├── index.html       ← open this. The dashboard.
├── README.md        ← this file.
├── decisions/       ← append-only decision log (one .md per decision).
└── runbook/         ← long-form runbook entries that don't fit a code block.
```

## Rule

The dashboard is the source of truth. Chats are ephemeral. If PPC sends
Paul a script and it isn't registered in `index.html`, PPC has failed at
the rule.

## Adding to it

- New script: drop the canonical copy in its project folder. Add a row in
  the **Latest** or **Scripts** section of `index.html` with the path.
- New decision: write a dated `.md` in `decisions/`. Mirror a one-line
  summary in the Decisions section of `index.html`.
- New runbook command: add a `<div class="code">` block in the Runbook
  section. Copy-button is automatic.

## Open shortcut

```
start "" "G:\My Drive\ClaudeBridge\CommandCentre\index.html"
```
