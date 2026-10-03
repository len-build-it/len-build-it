# Implementation Plan: GitHub profile README refresh

## October 3 maintenance phase

Follow-up authorized by Len's report that the slideshow looks laggy.
Compare the pre-refresh GIF metadata, restore its 900x506 dimensions and 1,800 ms hold / two 150 ms fade timings with current photos, and publish using a new filename.
Local checks passed: 13 photos, 39 frames, 27.3-second loop, 8,112,163 bytes.
Checkpoint: fix(readme): restore previous slideshow pacing.

Recorded: 2026-10-03T18:13:18+08:00
Authorization: Len's October 3 request to update the current photographs and add AqOne's RSTW win.
Implementation and local checks complete.
Completion is recorded by the checkpoint commit named below.

- [x] Inspect current files and preserve unrelated edits.
- [x] Run the required len-toolkit setup check.
- [x] Update championship, Enactus dates, hero description, and reduced-motion source.
- [x] Rebuild the hero from 13 existing photographs, excluding the two deleted images.
- [x] Decode GIF and verify frame count, size, duration, and looping.
- [x] Visually inspect the championship opening frame and verify README image references.
- [x] Review the README diff and run whitespace checks.
- [x] Record evidence and current handoff.
- [x] Commit only reviewed maintenance paths in the checkpoint named below.

Checkpoint: docs(readme): refresh RSTW championship and photo slideshow.
The maintenance checkpoint was pushed as 04e9884 after Len authorized publication.
The subsequent stale-image report was reproduced with a direct download of the published GIF.
Rename the updated GIF and change its README reference, then publish under the existing push authorization and compare the remote SHA256 with the local file.
Fix checkpoint: fix(readme): use fresh URL for RSTW photo slideshow.
Checkpoint 0d33723 was pushed; the new URL returns bytes matching the local SHA256 and the live profile HTML uses that URL.

## Original September 27 implementation plan

Created: 2026-09-27T20:20:38+08:00
Updated: 2026-09-27T20:36:51+08:00
Revision: 1
Status: In progress
Feature spec and revision: [FEAT-001 revision 1](../features/FEAT-001-github-profile-readme.md)
Approved baseline and architecture revisions: Not applicable; this is a README-only editorial change with no architecture change.
Len's chat approval: Approved FEAT-001 revision 1 and this plan revision 1 by replying “Approve and proceed” to the exact-revision approval request on 2026-09-27.
Target branch: `main`, confirmed at `85d05c2` tracking `origin/main`.

## Scope

Implement FEAT-001/REQ-001 through FEAT-001/REQ-005 in `README.md` only, then update the approved feature documentation and current handoff.
Preserve all unrelated untracked and unstaged files shown in Git status.
Stage only the README and FEAT-001 documentation paths after reviewing the staged diff.

## Phase 1: Refresh profile positioning and project presentation

Requirements: FEAT-001/REQ-001, FEAT-001/REQ-002, FEAT-001/REQ-003, FEAT-001/REQ-004, FEAT-001/REQ-005.
State: In progress.

### Tasks

- [x] Replace the AI Solutions Architect label and clarify AI-assisted development as the current practice.
- [x] Present AqOne, Warang, and Project Tabang in concise text-only blocks with their existing repository links.
- [x] Condense repeated biography and tool-list content while preserving relevant project evidence and responsible AI use.
- [x] Keep the existing hero image, meaningful alt text, and reduced-motion fallback.
- [x] Review the README diff for content scope and link integrity.
- [x] Record pre-push checks and update the handoff before the content checkpoint commit.
- [ ] After the content push, inspect the rendered profile, record the result, and update the plan and handoff.

### Verification

- [x] Run `git diff --check`; it exits 0 without whitespace errors.
- [x] Inspect the changed README and linked local image paths; confirm the existing project links remain in place.
- [ ] After push, open the rendered profile README and check desktop and narrow-screen presentation; record the observed result and limitations in `HANDOFF.md`.

### Review and checkpoint

- [x] Review correctness, scope, and unrelated changes.
- [x] Update plan, evidence, and current handoff.
- [x] Stage only reviewed phase-related paths and inspect the staged diff.
- [ ] Commit the content checkpoint with the message below and verify Git reports success.
- [ ] Push the content checkpoint on `main` to `origin` as explicitly requested.
- [ ] After the rendered review, commit the final plan and handoff evidence with `docs(readme): record live profile verification`, then push it to `origin`.

Checkpoint message: `docs(readme): refresh GitHub profile positioning and project highlights`.
The follow-up evidence commit is required because the rendered profile can only be checked after the content checkpoint is pushed.

## Recovery

Follow project `AGENTS.md` for the three-attempt limit and immediate blockers.
Record any unresolved work and attempt counts in the current handoff.
Interrupted or failing work remains uncommitted and the phase remains incomplete.
