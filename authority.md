# VADE Authority and Decision Rights

*Public governance document. Canonical source for the VADE project's
authority hierarchy and decision rights. This file exists so that
any third party — contributor, auditor, collaborator, or curious
reader — can verify whether a given action attributed to VADE or to
a VADE agent was within the authority of whoever performed it.*

*Operational details of how the VADE COO agent is prompted,
configured, and booted are deliberately not included in this
document. Those live in a private repository.*

---

## Authority hierarchy

1. **BDFL (Benevolent Dictator For Life)** — Ven Popov. Final
   authority on all decisions for the VADE project. Linus-style.
   The BDFL's decisions are final and may only be appealed by
   persuading the BDFL to revise them.

2. **COO agent** — an AI agent operating under delegated
   operational authority from the BDFL. The COO drafts plans,
   maintains continuity across sessions, tracks active work,
   pushes back constructively, and executes routine operational
   tasks within the scope defined below. The COO does not hold
   independent authority — all actions occur under explicit or
   standing delegation from the BDFL.

3. **Task agents (future)** — AI agents scoped to specific
   repositories or work streams. Task agents hold no cross-cutting
   authority and may not modify governance, identity, or budget.

External contributors, when the project opens for external
contribution, will fit into this hierarchy via a scheme to be
defined before that phase begins.

## What the COO may do under standing delegation

- Create branches and draft pull requests in any `vade-app`
  repository.
- Read, write, and revise files in designated scratch and
  self-infrastructure areas.
- Propose architecture, design, and process changes for BDFL
  review.
- Run shell commands in sandboxed environments.
- Read external documentation and search the web.
- Draft documents, scaffolds, and templates for BDFL review.
- Update status trackers to reflect completed work or new
  priorities, within BDFL-set direction.

## What the COO may not do without explicit BDFL approval

- Merge any pull request to a `main` branch.
- Delete repositories, branches, or files outside designated
  scratch areas.
- Modify any document in this repository.
- Modify canonical product documents in place. (Derivative drafts
  and proposed revisions are allowed; replacing the canonical in
  place is not.)
- Spend money. Sign up for paid services. Authorize API spend.
  Move funds.
- Execute trades, place orders, or initiate financial transactions
  on behalf of the BDFL in any context.
- Authorize new third-party integrations against the organization
  or the BDFL's personal accounts.
- Take any irreversible action without flagging it explicitly
  first and receiving explicit approval.

## Decision rights matrix

| Category | COO authority | BDFL authority |
|---|---|---|
| Process and protocol | Propose, document, and draft | Veto or revise |
| Active project status tracking | Update freely within set priorities | Sets priorities |
| New project creation | Draft for review | Approves |
| Architecture (VADE core) | Draft ADRs, surface trade-offs, push back | Decides |
| Code merges to `main` | Draft PRs, request review | Approves and merges |
| Spend and paid services | Flag costs, surface recommendations | Authorizes |
| Identity and governance edits | Propose as drafts | Approves |
| Decision records (case-law memos) | Issue within delegated scope | Can override via new memo |
| External communications | Draft for review | Sends |

## Escalation triggers

The COO is required to explicitly surface (not silently proceed)
when any of the following conditions apply:

- An action is irreversible.
- A decision exceeds delegated scope as defined above.
- Two prior decisions appear to conflict in a way that simple
  newest-wins precedence does not cleanly resolve.
- Memory, canonical files, or governance documents appear stale,
  missing, or corrupted.
- Costs are about to be incurred, even if within standing spend
  authority.
- A risk has materialized that was not previously flagged.

These triggers exist so that the BDFL retains control over anything
that could materially affect the project's direction, finances, or
integrity.

## Branch protection (enforced via repository settings)

- `main` branches require a pull request with at least one BDFL
  approval before merge.
- Required status checks must pass before merge.
- Stale approvals are dismissed on new commits.
- `CODEOWNERS` routes review requests to the BDFL for all paths
  until task agents earn delegated review rights via a future
  governance revision.

## Verifying a claimed COO action

If someone external to the project receives a communication or
sees an action attributed to the VADE COO, the authenticity and
authority of that action can be verified by:

1. Checking whether the action falls within the "may do under
   standing delegation" list above. If it does not, the COO was
   not authorized to perform it unilaterally.
2. For commits, pull requests, or repository changes: verifying
   the commit author and signature against GitHub. During the
   bootstrap phase of the VADE project, commits authored via the
   COO's operational surfaces are attributed to the BDFL directly,
   not to a separate bot identity.
3. For external communications claimed to come from the COO: the
   COO does not currently send external communications under its
   own identity. Any such message should be treated as
   unauthenticated until the BDFL confirms.

## Revision

This document is revised by BDFL approval only. Proposed revisions
follow the normal pull-request flow with BDFL review required for
merge. Material changes are accompanied by a decision record in the
project's private memo ledger explaining the reasoning.

## License

This document is released under
[CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/).
Adapt freely for other projects; attribution appreciated but not
required.
