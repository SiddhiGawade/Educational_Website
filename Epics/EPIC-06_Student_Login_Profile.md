# EPIC-06: Student Login & Profile System

| Field            | Details                                      |
|------------------|----------------------------------------------|
| **Epic ID**      | EPIC-06                                      |
| **Epic Name**    | Student Login & Profile System               |
| **Priority**     | P1 – Critical                                |
| **Project**      | Educational Website                          |
| **Sprint Target**| Week 1                                       |
| **Owner**        | Siddhi and Team                              |
| **Client**       | Prashant                                     |

---

## Description

Implement a secure student authentication system with registration (pending admin approval), login/logout, and a personalized dashboard. The dashboard aggregates each student's quiz history, game scores, leaderboard ranking, and profile information in one place.

---

## Business Value

- Enables personalized learning experience
- Tracks individual student progress over time
- Admin approval ensures only legitimate students access the platform
- Foundation for all other features that require user identity

---

## Acceptance Criteria

1. Students can register with required details (name, standard, email, etc.)
2. Registration requires admin approval before access is granted
3. Students can securely log in and log out
4. Student dashboard displays quiz history with scores
5. Student dashboard displays game scores
6. Student dashboard displays leaderboard ranking
7. Students can view and edit their profile information
8. Passwords are stored securely (hashed)

---

## User Stories

| Story ID | Title                                | Priority |
|----------|--------------------------------------|----------|
| US-0601  | Student Registration                 | Critical |
| US-0602  | Admin Approves Student Registration  | Critical |
| US-0603  | Student Login                        | Critical |
| US-0604  | Student Logout                       | Critical |
| US-0605  | View Student Dashboard               | Critical |
| US-0606  | View and Edit Profile                | High     |

---

## Dependencies

- EPIC-07: Admin Portal (registration approval)

---

## Risks & Assumptions

- **Risk:** Security vulnerabilities in authentication flow
- **Assumption:** Students have a valid email address for registration
- **Assumption:** Forgot-password flow is handled via email
- **Risk:** GDPR/data privacy compliance for minor students
