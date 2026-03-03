# EPIC-01: Interactive Quizzes

| Field            | Details                                      |
|------------------|----------------------------------------------|
| **Epic ID**      | EPIC-01                                      |
| **Epic Name**    | Interactive Quizzes                           |
| **Priority**     | P1 – Critical                                |
| **Project**      | Educational Website                          |
| **Sprint Target**| Week 1–2                                     |
| **Owner**        | Siddhi and Team                              |
| **Client**       | Prashant                                     |

---

## Description

Build a comprehensive interactive quiz system that allows administrators to upload daily quizzes and students (Std 8–10) to attempt them after login. Quiz results and leaderboard rankings are revealed the **next day** after teacher announcement, encouraging daily engagement and healthy competition.

---

## Business Value

- Drives daily student engagement and return visits
- Provides measurable learning outcomes via score tracking
- Encourages healthy competition through leaderboards
- Gives teachers a tool to assess student understanding

---

## Acceptance Criteria

1. Admin can create and upload quizzes daily through the admin portal
2. Students can attempt quizzes only after logging in
3. Quiz results remain hidden until the teacher publishes them (next day)
4. A leaderboard displays the top performers after results are declared
5. Students can view their quiz history and past scores on their dashboard

---

## User Stories

| Story ID | Title                                | Priority |
|----------|--------------------------------------|----------|
| US-0101  | Admin Uploads Daily Quiz             | Critical |
| US-0102  | Student Attempts Quiz                | Critical |
| US-0103  | Teacher Declares Results             | Critical |
| US-0104  | View Quiz Leaderboard                | Critical |
| US-0105  | Student Views Quiz History           | High     |

---

## Dependencies

- EPIC-06: Student Login & Profile System (students must be logged in)
- EPIC-07: Admin Portal (admin must be able to upload quizzes)

---

## Risks & Assumptions

- **Risk:** Concurrent quiz submissions under peak load (50–100 students)
- **Assumption:** Quizzes are objective-type (MCQ) for automated grading
- **Assumption:** One quiz per day is the standard cadence
