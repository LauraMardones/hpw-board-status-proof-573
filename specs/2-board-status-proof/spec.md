# Epic #2: Hosted board-status lifecycle proof

**Epic issue:** #2

## Goal

Obtain actual hosted evidence for LauraMardones/headless-pr-workflow#573 AC 2 in the approved disposable private repository and board, without merging production PR #609 to activate its own test.

## Scope

In:

- Use test repository LauraMardones/hpw-board-status-proof-573 and test project LauraMardones/4.
- Exercise the paired workflows and writer code from production checkpoint 317db12c54e40acf641b7f17dcb04baa8c38c499. Record the installed commit and verify that test fixture additions change no workflow or runtime-writer blobs.
- Use a genuinely refined proof story and a linked PR that follows the ordinary CI, independent-review and merge gates.
- Capture draft-opened, ready-for-review and merged events and their changed board statuses, including delivery, hosted queue/start, sync and verified read-back timestamps.
- Observe the event writer while a real dispatcher session remains active, respecting existing usage limits and reserves.

Out:

- Production changes, production deployment or merge of production PR #609.
- Changes to production dispatcher variables, Claude reserves or credential copying.
- Manufacturing refinement, review, dispatcher-session or timing evidence.
- Replacing actual hosted measurements with local fake-transport replay.

## Acceptance Criteria

- **E1:** For one genuinely refined test story, the linked draft PR produces In implementation, readiness produces In review, and merge produces Done. Each verified status change occurs within 120 seconds of its actual GitHub event. In implementation and In review are observed while those PR states still hold.
  - **Verified by:** Durable event URLs/timestamps, run and job IDs, queue/start timestamps, timestamped successful board-write/read-back logs and board read-back values. Preserve delivery, queue, setup, sync and total durations separately.
- **E2:** The event writer changes status while a real dispatcher session remains active, and the paired writers retain their shared non-cancelling concurrency group.
  - **Verified by:** Overlapping real dispatcher-session and event-writer intervals and logs, with unchanged workflow/writer blob provenance. Do not represent an idle dispatcher poll or a synthetic sleep as a model session.
- **E3:** The proof preserves pause-switch and off-default dry-run behavior, and it passes the applicable CI, refinement, independent review and merge gates.
  - **Verified by:** Recorded guard/dry-run observations, current-head pytest and independent review evidence, plus the authorized test-PR merge record. Any required separate session and merge are arranged before those steps.

## Decisions

### Isolated environment

**Chosen:** The PO approved provisioning the isolated test repository and board for production #573 verification; setup is tracked in #1. This spec proposes the bounded proof contract for PO approval by merge.
**Rejected:** Merging production PR #609 to activate its own test, changing production settings, or calling local replay hosted latency evidence.

## Checked Against

- Production #573 AC 2 and its latest refinement — requires actual hosted timing before implementation handoff.
- docs/PROJECT-STATUS.md and ADR-008 to ADR-011 — board status follows facts; refinement requires a merged spec, and PO approval is the spec merge.
- .claude/commands/implement.md and docs/MERGE-POLICY.md — no implementer self-review, approval or merge; current-head checks and independent review remain required.

## Delegated to the Tech Lead

- Slice this test-only proof into a Feature and story with traceable criteria, and choose a minimal harmless proof-PR artifact.
- Select timing collection and provenance commands without changing workflow/runtime-writer blobs.
- Arrange available, authorized dispatcher-session coverage while respecting existing credentials, pause controls, usage limits and reserves.

## Dependencies

- Installed paired workflows on test main and maintainer-supplied PROJECT_TOKEN; the initial access probe succeeded on 2026-11-18.
- PO merge of this test spec, genuine refinement, an authorized real dispatcher session, independent review and separately authorized proof-PR merge.
- Production PR #609 remains Draft until its AC 2 evidence is complete and pytest is green for its exact current head.

## Open Questions

None.
