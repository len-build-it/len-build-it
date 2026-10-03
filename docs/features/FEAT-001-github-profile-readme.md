# FEAT-001: GitHub profile README refresh

## October 3 authorized maintenance amendment

Recorded: 2026-10-03T18:13:18+08:00
Len explicitly requested refreshing the folder's new/deleted photographs and AqOne's RSTW championship in this task.
For this maintenance, the prior restriction on changing hero media is superseded by that request.
Rebuild the existing hero from current photographs, remove deleted images from its content, and preserve the reduced-motion fallback.
Add the user-supplied October 2 RSTW championship and scheduled October 8-10 Enactus participation.
Keep project blocks text-only and preserve the approved professional positioning.
Success: all current photographs appear, deleted photographs are absent, image references resolve, the award and upcoming dates are accurate to the supplied announcement, and no new dependency is introduced.

## Original September 27 specification

Created: 2026-09-27T20:20:38+08:00
Updated: 2026-09-27T20:31:31+08:00
Revision: 1
Status: Approved

## Purpose and success

Help peers and recruiters quickly understand Len's current direction, how he uses generative AI, and what he has been building.
Success means readers can identify his professional focus and scan the three featured projects without parsing repeated biography or decorative content.

## Scope and non-goals

This update changes only the profile `README.md` and the minimal project documentation needed to govern the work.
The headline will identify Len as an aspiring Generative AI Specialist and a Software Engineering student.
The README will describe AI as part of Len's development process for building real-world solutions, without claiming that all existing products embed AI features.
The Featured builds section will present AqOne, Warang, and Project Tabang as concise text-only, tile-like blocks that retain their existing repository links.
The project blocks will not contain screenshots, and no new demo or contact links will be invented.
Use GitHub-supported Markdown and HTML only, keep the existing hero image and reduced-motion fallback, and use the hero as the README's existing motion element.
The repeated AqOne biography and detailed AI co-worker list may be condensed so the projects and current practice stay prominent.
This work does not change project repositories, claim new product capabilities, add dependencies, or add new image assets.

## User flows

A peer or recruiter opens the GitHub profile, reads the identity and AI-development statement, scans the three project descriptions and their repository links, then uses the existing repository or profile links to continue.

## Requirements and acceptance criteria

| ID | Required behavior | Observable pass/fail criterion |
| --- | --- | --- |
| REQ-001 | Present the intended professional direction. | The opening identifies Len as an aspiring Generative AI Specialist and Software Engineering student, replacing the AI Solutions Architect wording. |
| REQ-002 | Describe current AI use accurately. | The README says Len uses generative AI during development to build real-world solutions and does not imply existing products all contain AI features. |
| REQ-003 | Make featured work easy to scan. | AqOne, Warang, and Project Tabang each have a concise text-only description and retain their current repository link. |
| REQ-004 | Keep the presentation GitHub-compatible and accessible. | The README uses supported Markdown or HTML, includes no screenshots or new media, preserves meaningful alt text and the reduced-motion fallback, and remains readable on narrow screens. |
| REQ-005 | Keep the profile focused on evidence of work. | Repeated AqOne copy and the detailed AI co-worker list are removed or shortened without removing the project result, technical skills, awards, or responsible-use statement. |

## Data and interfaces

There are no application data or runtime interfaces.
Existing repository links and local image paths are the only profile interfaces in scope.

## Quality constraints

Keep project descriptions short and readable on desktop and mobile widths.
Do not add dependencies, remote animation services, screenshots, unsupported CSS, or JavaScript.
Preserve meaningful image alternative text and the existing reduced-motion image source.

## Decisions and assumptions

Confirmed: peers and recruiters are the primary audiences.
Confirmed: the professional label is aspiring Generative AI Specialist.
Confirmed: AI use is in the development process today; AI inside products is a possible future direction, not a current README claim.
Confirmed: project descriptions should be short, text-only, and linked to their existing repositories.
Proposed for approval: the existing hero remains the sole animated visual; project blocks use static GitHub-compatible markup because the requested text-only tiles have no screenshot media to animate.
Assumption: current project descriptions and competition claims remain factually accurate; this update does not independently verify them.
Len approved FEAT-001 revision 1 and the paired implementation plan revision 1 in chat on 2026-09-27 before implementation.

## Open questions and readiness

There are no blocking content questions in the agreed scope.
This revision is approved for Phase 1 implementation.
