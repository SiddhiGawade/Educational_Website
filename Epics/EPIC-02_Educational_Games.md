# EPIC-02: Educational Games

| Field            | Details                                      |
|------------------|----------------------------------------------|
| **Epic ID**      | EPIC-02                                      |
| **Epic Name**    | Educational Games                            |
| **Priority**     | P1 – Critical                                |
| **Project**      | Educational Website                          |
| **Sprint Target**| Week 2–3                                     |
| **Owner**        | Siddhi and Team                              |
| **Client**       | Prashant                                     |

---

## Description

Develop interactive, curriculum-aligned educational games that make learning fun for students of Std 8–10. Each game tracks individual student scores, provides a responsive interface that works across devices, and reinforces subject concepts through gamified activities.

---

## Business Value

- Makes learning engaging and fun, increasing time-on-site
- Gamification improves knowledge retention
- Score tracking motivates students to improve
- Differentiates the platform from static learning resources

---

## Acceptance Criteria

1. At least one interactive educational game is available at launch
2. Games are responsive and work on desktop, tablet, and mobile
3. Each student's game score is tracked and saved to their profile
4. Admin can upload/manage games through the admin portal
5. Games load quickly and provide smooth user interaction

---

## User Stories

| Story ID | Title                                | Priority |
|----------|--------------------------------------|----------|
| US-0201  | Student Plays Educational Game       | Critical |
| US-0202  | Track Game Scores Per Student        | Critical |
| US-0203  | Responsive Game Interface            | High     |
| US-0204  | Admin Manages Games                  | High     |

---

## Dependencies

- EPIC-06: Student Login & Profile System (score tracking requires login)
- EPIC-07: Admin Portal (game management)

---

## Risks & Assumptions

- **Risk:** Game performance on low-end student devices
- **Assumption:** Games are browser-based (HTML5/JS), no plugins required
- **Assumption:** Admin uploads game assets; games are pre-built
