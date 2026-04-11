# vade-governance

**Public authority and decision-rights document for the
[VADE project](https://github.com/vade-app).**

VADE is an open-source project modeled on Linus-style BDFL
governance. This repository is the **canonical public source** for
the authority hierarchy, decision rights, escalation triggers, and
branch-protection rules that govern how the project is run and what
agents operating on behalf of the project may or may not do.

## What's here

- [`authority.md`](authority.md) — authority hierarchy, decision
  rights matrix, escalation triggers, and verification procedures
  for claimed agent actions.
- [`LICENSE`](LICENSE) — CC0 1.0 Universal. Adapt freely.

## What's deliberately not here

Internal operational details of how project agents are configured,
prompted, or booted are not published in this repository. Those
details are implementation-level and do not need to be public for
third parties to verify the legitimacy of any action taken on
behalf of the project. If you're looking for the authority and
scope rules — everything you need is in `authority.md`.

## BDFL

Ven Popov ([@vencislav.popov](https://github.com/vencislav.popov)).
Final authority on all project decisions. Pull requests against
this repository require BDFL approval before merge.

## Why public?

Transparency is load-bearing in BDFL-governed open-source projects.
Publishing the rules that govern agent authority allows anyone —
contributor, auditor, or third party who has received a
communication attributed to a VADE agent — to verify whether a
given action was within its delegated scope. Publishing the rules
does not grant anyone authority to act on behalf of the project;
authority flows from the BDFL, not from reading this document.

## Contributing

The VADE project is in bootstrap phase and is not yet open for
external contribution. A contribution scheme will be defined and
published here before external contribution opens.

## License

`authority.md` and the governance documents in this repository are
released under
[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).
Adapt for your own projects freely; attribution appreciated but not
required.
