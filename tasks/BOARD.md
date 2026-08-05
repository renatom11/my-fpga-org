# Program Board

**Live program state.** The orchestrator updates this file in the same commit
as any state change it describes. A fresh orchestrator session rehydrates by
reading: this board → `agents/PROTOCOL.md` → `ORG_CHART.md` → journal tails of
agents with open work.

## Current milestone

**FOUNDED — org generic.** This repository is `renatom11`'s org generic:
its own copy of the canonical shell, cloned once at the organization's
founding. **It runs no project and answers no intake** (ADR-0011,
`docs/FEDERATION.md` §0). Its standing duties are two: to be the template
this organization's projects are forked from, and to receive those
projects' lessons landings (`docs/FEDERATION.md` §5.1). Default branch:
`main`.

Founded 2026-08-05 from the canonical shell at
`b5f94aacc8a06bb519685371d355044ef5347beb` (C37), by the founding
orchestrator session, per BOOTSTRAP Stage 0. Sponsor decision on the
record: **org generic**, not solo-collapsed — the project slot stays
empty here and is filled in each project fork.

Founding verification, by the founding session's own hands at C37:
enforcement self-test **47 passed, 0 failed** (41 scenarios);
`check_journals.sh --all` green over the full history with the journal
volume chain verified at range head (R10); the sole `journal-check` CI
failure the **R-ROLE-1** unrecorded-fork wedge, which this founding
commit clears by recording the role.

**Stage 0 status** (BOOTSTRAP Stage 0, the org-generic founding checklist):

| Step | Item | State |
|---|---|---|
| 1 | Actions enabled; `journal-check` runs | **Done** — runs observed on `main` |
| 2 | `protect-history` ruleset on `main` **and `fed/**`** | **OPEN — sponsor** (E0) |
| 3 | Self-test + full-history check green by the founder's hands | **Done** — see above |
| 4 | Role + This-repository lines recorded, on the default branch | **Done** — this commit |
| 5 | Freeze re-scoped to this repository's own end condition | **Done** — this commit |
| 6 | Defect channel seeded (upstream issues; local log empty) | **Done** — this commit |
| 7 | Stop: green on the default branch before anything forks from here | **Blocked on step 2** |

**Nothing may be forked from this repository until step 7 holds** — the
default branch carries this founding commit and its CI is green. A copy
taken from a red or pre-founding default branch mis-founds as a copy of
the shell (the third field defect, recorded below).

## Milestone roadmap

An org generic has no project milestones — the M0/M1+ roadmap, the G0
gate, and the E0 escalation rows below are **shipped template state**
(ADR-0011): they activate in the project forks taken from this
repository, never here. They are carried, not run.

| Milestone | Scope | Status |
|---|---|---|
| M0 | Bring-up: G0 intake, org ratification, branch protection, enforcement self-test green | Template state — activates in a project fork |
| M1+ | Set at G0 intake — recorded here and in README.md's phase table | Template state — activates in a project fork |

## Gates

| Gate | Status | Checklist |
|---|---|---|
| G0 | Template state — activates in a project fork | [docs/gates/G0-checklist.md](../docs/gates/G0-checklist.md) |

## Open work orders

_None._

## Pending escalations to sponsor

**Live here — one, class E0 (founding)**: the Stage 0 ruleset (step 2
above). It is the last open item of this repository's own founding.

- **Rulesets** — the sponsor configures `protect-history` (Active, empty
  bypass list, Restrict deletions + Block force pushes) targeting `main`
  **and `fed/**`**, the federation staging namespace
  (`docs/FEDERATION.md` §5.2 clause 10). Without it PROTOCOL §5 R9 is
  convention only, and Stage 0 step 7 cannot close.

**Template state — the three G0 rows** (PROTOCOL §8, ADR-0013): E0 exists
only at a project's G0, and in an org generic these are shipped template
state that activates in the project forks taken from here (ADR-0011).
They are never answered in this repository.

- **G0 ratification** — the sponsor ratifies the org: this protocol, the
  roster, the charters (or amends them before ratifying).
- **Branch protection** — the sponsor configures branch protection on `main`
  and the working branch (no force push, no deletion, `journal-check`
  required, no admin bypass); without it PROTOCOL §5 R9 is convention only.
- **G0 intake** — the sponsor states the project: scope, phases, success
  criteria, and license classes for external references, recorded in
  README.md's phase table per PROTOCOL §1.

## Decisions on record

- **This repository**:
  https://github.com/renatom11/my-fpga-org — the copy's own
  URL, re-recorded at every founding (BOOTSTRAP Stage 0 step 4 / G0 row
  B6). A session whose `git remote get-url origin` disagrees with this
  line is in a **fresh, unfounded copy** of whatever the role line below
  claims (`CLAUDE.md`, First session).
- **Repo role**: `org-generic` (values: canonical-shell / org-generic /
  project / solo-collapsed — ADR-0011). Recorded at this repository's
  founding, 2026-08-05, discharging the rule that **a fork's first act is
  updating this line**. An org generic runs no program: it runs BOOTSTRAP
  Stage 0 once and then waits to be forked from, answering no intake
  (`CLAUDE.md`, `docs/FEDERATION.md` §0). The M0/G0 rows above are shipped
  template state that activates in the project forks taken from here.
- Constitution ADR-0001..0007 pre-adopted at seeding (see each ADR's
  provenance).
- **Declared domain packs**: _n/a — template state; this repository runs
  no intake_. A project forked from here declares and loads its packs at
  its own G0, from the inventory this org generic carries, and records
  them on its own board. **Pack inventory carried here** (the library
  projects inherit, and the destination tier-2 landings accumulate into):
  `docs/domains/ethernet-networking.md`.
- **Federation upstream** (`docs/FEDERATION.md` §0, §7):
  https://github.com/renatom11/generic-agentic-fpga-org — the canonical
  shell. **Confirmed at this repository's founding, 2026-08-05**: an
  **org generic** keeps this line as the canonical shell (a **project**
  re-records it at its G0 row B6 to point at *this* repository). This is
  the destination of this org's outer hop (§7) and the address of its
  shell-defect channel (below).
- **Project slug**: _n/a — template state_. An org generic has no slug of
  its own; each project fork sets its own at G0 B6, lowercase-hyphenated
  and unique within this org, keying its landings here
  (`docs/FEDERATION.md` §5.1).
- **Fork-point harvest baseline**: _n/a — template state_ (ADR-0010).
  Each project fork records its own baseline at G0 B6 — the last entry id
  per journal chain it inherited from this repository at fork time; its
  first harvest tiles from baseline + 1.
- **Federation sent-ledger** (append-only; one line per landing:
  `<parent-record-id>` · landing SHA(s) · outer-hop PR URL or `—` ·
  obligation ids + states or `—`, ADR-0014):
  _none yet_. A landing's ledger line is written in the same commit as
  its transcription (`docs/FEDERATION.md` §5.1 step 5).
- **Amendment obligations** (open promotion obligations — the recurrence
  threshold, ADR-0010 / `docs/FEDERATION.md` §8; the read-path promotion
  channel rides the same ledger): _none open_. One line per obligation:
  entry id · opened by (landing / recurrence) · **state** — DISCHARGED
  (ADR-NNNN) / NARRATIVE-ONLY (reason) / DEFERRED (reason · discharging
  event). Every landing dispositions its own and sweeps the DEFERRED
  backlog (`docs/FEDERATION.md` §5.1 step 4c, ADR-0014) — landings are
  this fence's only cadence.
- **Outer-hop standing pre-answer** (`docs/FEDERATION.md` §7): _none —
  the per-gate question stands_. The sponsor may replace this value
  with a standing YES or NO (e.g. *STANDING CLOSED — pre-answered NO,
  for every gate and every backlog*); while a standing line is recorded
  here the gate-time question is not asked, the harvest block cites
  this line instead, and only the sponsor changes it. Confirmed at
  every founding (G0 row B6). **Confirmed unset at this repository's
  founding, 2026-08-05** — the sponsor was not asked to pre-answer, so
  the per-gate default-yes question stands for this org's outer hop.
- **Feature freeze: ENGAGED — re-scoped at this repository's founding**
  (BOOTSTRAP Stage 0 step 5, 2026-08-05). The end condition, stated as an
  event **this repository can observe**: *no new law lands in
  `renatom11/my-fpga-org` until its first lessons landing completes*
  (`docs/FEDERATION.md` §5.1) — that is, until a project forked from here
  lands its first harvest in this org generic. New law means protocol,
  charter, or ADR changes and enforcement-script changes; it does not mean
  the founding record itself, nor the routine landing transcriptions the
  §5.1 pipeline requires. Until then this repository is operated, not
  developed. The sponsor may lift or scope-override the freeze at any
  time, on the ADR-0008 pattern (a named round with a written end
  condition, which re-engages the freeze when it closes).
  The canonical shell's own freeze history — the three closed
  sponsor-directed overrides carrying ADR-0008..0016 — is inherited law
  in this tree and is **not** this repository's freeze; its end
  conditions reference events this copy cannot observe and never bound it
  as written.
- **First-trial findings absorbed** (2026-08-04, sponsor hand-relay from
  the first org generic founded from this shell, since retired): SD-0001
  → R-ROLE-1 wedge check (ADR-0015); SD-0002 (unobservable freeze) and
  SD-0003 (no defect channel) → already fixed in the zero-question
  founding commit; SD-0004 (fork-button impossibility) → clone-and-push
  now leads the founding docs; its ADR-0014 (obligation discharge)
  adopted as this shell's ADR-0014.
- **Second-trial defect fixed (2026-08-05)**: the first field founding
  from this shell hit an R-ROLE-1 false positive — the check
  substring-matched `canonical-shell` against the whole role line, and
  the shipped line carries the value enumeration as plain text on the
  same physical line, so every founded copy went permanently red (and
  the false red stops the next founding at the project M0 red-check).
  Fixed same-day: exact backticked-value comparison, regression
  scenario S40 (ADR-0015 Amendment A1). Reported live by the founding
  session through the upstream defect channel; its issue closes against
  the fix commit when it lands.
- **Third-trial defect fixed (2026-08-05)**: the second field founding
  parked its Stage 0 founding commit on a working branch, leaving the
  org generic's default branch carrying the pre-founding board; the
  project cloned from that branch inherited the shell's identity and
  mis-founded as an org generic — correct boot logic on poisoned
  state. Fixed same-day, docs-only (freeze-legal founding surfaces):
  Stage 0 step 4 mandates the founding commit lands on the default
  branch, step 7 gates Stage 0 completion on the default branch being
  green, README adds the fork-only-from-green rule, CLAUDE.md's boot
  line carries the branch mandate. The R-ROLE-1 red on the unfounded
  default branch was the designed signal all along — the fix makes it
  a stop condition instead of a judgement call.
- **Queued law-debt (behind the freeze)**: generalize the R-ROLE-1 CI
  check from the canonical-shell claim to every role, keyed on the
  This-repository line (script change + scenario, §11) — the boot logic
  already applies the generalized rule; only the machine backstop waits.
  Second item (2026-08-05, from the third field defect): a MACHINE
  guard in `agent_commit.sh` refusing any commit that sets the board's
  Repo role line to `org-generic` on a branch other than the default
  branch (script change + scenario, §11). C36's Stage 0 branch mandate
  is PROSE — determined, but instructed; this backstop would make the
  side-branch founding mechanically impossible. Lands at the freeze's
  end, or earlier under a sponsor-directed override.
- **Independent claims audit (2026-08-05), on the record**: an
  independent agent audited the orchestrator's architecture claims
  against this tree. Verdicts: 9/13 confirmed or confirmed-with-caveat;
  4/13 refuted in part — the claimed-but-nonexistent standing
  pre-answer (C4); "lessons never touch working files", false in the
  solo-collapsed topology (C7); "lessons move only inside gate-closing
  commits", false of outer-hop PRs (C11); and "45 scenarios, signed
  commits" — 40 scenarios carrying 45 assertions, trailer-attributed,
  not cryptographically signed (C13). Corrected in law under override
  #3 (ADR-0016): the audit's two live tree contradictions — the §8.1
  "three screens" line and the harvest block's stale "informational
  sponsor row" phrase — and the missing standing pre-answer, made law
  on its merits; the remaining overclaims were reporting errors,
  corrected by the standing findings below and the MACHINE/PROSE
  discipline, not by tree edits. A follow-up verification audit
  (2026-08-05) confirmed the three fixes and required the completing
  sweep that landed with ADR-0016 Amendment A1. Standing findings
  every future report must honor: **the federation pipeline has zero
  mechanical test coverage — the 47 self-test assertions (41 scenarios)
  test journal/commit hygiene only, and the first end-to-end landing is
  the pipeline's designated first test**; commits are trailer-attributed,
  not cryptographically signed; enforcement claims are tagged MACHINE or
  PROSE (`CLAUDE.md` iron rule).
- **Inherited shell history vs. this repository's history.** The four
  bullets above — the first/second/third-trial defects, the queued
  law-debt, and the independent claims audit — are the **canonical
  shell's** operating record, carried into this tree at the fork. They
  are inherited context, not events in `renatom11/my-fpga-org`, and the
  queued law-debt is the shell's to discharge (it reaches this
  repository only on a future re-fork or landing, never by local
  patching while the freeze holds). This repository's own history begins
  at its founding commit.
- **Upstream defect channel — seeded at founding** (BOOTSTRAP Stage 0
  step 6, 2026-08-05): shell defects — wrong claims, broken steps, gaps
  found while operating this copy — file as **GitHub issues on the
  federation upstream**, https://github.com/renatom11/generic-agentic-fpga-org
  (the line above); they never travel through the lessons pipeline, which
  carries lessons only. Never patch shell law locally while the freeze
  holds. Local defect log (one line per defect: date · one-line summary ·
  upstream issue URL): _empty — no defect found in this repository's
  founding_.
