# EPIC-03: Video Section

| Field            | Details                                      |
|------------------|----------------------------------------------|
| **Epic ID**      | EPIC-03                                      |
| **Epic Name**    | Video Section                                |
| **Priority**     | P2 – High Priority                           |
| **Project**      | Educational Website                          |
| **Sprint Target**| Week 2–3                                     |
| **Owner**        | Siddhi and Team                              |
| **Client**       | Prashant                                     |

---

## Description

Create a video gallery section where educational videos are organized by subject and topic. Each video is presented as a card with a YouTube thumbnail, title, and description. Clicking a video card redirects the student to the corresponding YouTube video.

---

## Business Value

- Provides visual/audio learning for different learning styles
- Leverages existing YouTube content (no video hosting costs)
- Organized by subject for easy navigation
- Enhances learning experience with multimedia content

---

## Acceptance Criteria

1. Videos are displayed as cards with thumbnail, title, and description
2. Videos are organized and filterable by subject/topic
3. Clicking a video card opens the YouTube video (new tab)
4. Admin can add, edit, or remove video entries
5. Video gallery is responsive across devices

---

## User Stories

| Story ID | Title                                | Priority |
|----------|--------------------------------------|----------|
| US-0301  | Browse Video Gallery by Subject      | High     |
| US-0302  | View Video Card and Open YouTube     | High     |
| US-0303  | Admin Manages Video Entries          | High     |

---

## Dependencies

- EPIC-07: Admin Portal (video management)

---

## Risks & Assumptions

- **Assumption:** Videos are hosted on YouTube; the website only stores metadata
- **Assumption:** YouTube thumbnails are fetched via embed URL or stored manually
- **Risk:** YouTube links could become unavailable over time
