# EPIC-07: Admin Portal

| Field            | Details                                      |
|------------------|----------------------------------------------|
| **Epic ID**      | EPIC-07                                      |
| **Epic Name**    | Admin Portal                                 |
| **Priority**     | P1 – Critical                                |
| **Project**      | Educational Website                          |
| **Sprint Target**| Week 1–2                                     |
| **Owner**        | Siddhi and Team                              |
| **Client**       | Prashant                                     |

---

## Description

Build a secure admin dashboard that enables teachers/admins to manage all platform content — quizzes, games, videos, blog posts, awards, and student registrations. The admin portal is the central management hub for the entire educational website.

---

## Business Value

- Empowers non-technical staff to manage content independently
- Centralizes all content management in one place
- Enables daily operations (quiz uploads, result declarations)
- Reduces dependency on developers for routine content updates

---

## Acceptance Criteria

1. Admin can securely log in with admin credentials
2. Admin dashboard provides an overview of platform activity
3. Admin can create, edit, and delete quizzes
4. Admin can declare quiz results and publish leaderboards
5. Admin can upload and manage educational games
6. Admin can manage video entries, blog posts, and awards
7. Admin can approve/reject student registrations
8. Admin portal is accessible only to authorized admin users

---

## User Stories

| Story ID | Title                                | Priority |
|----------|--------------------------------------|----------|
| US-0701  | Admin Login                          | Critical |
| US-0702  | Admin Dashboard Overview             | Critical |
| US-0703  | Manage Quizzes (CRUD)                | Critical |
| US-0704  | Declare Quiz Results & Publish Leaderboard | Critical |
| US-0705  | Manage Educational Games             | High     |
| US-0706  | Manage Video Entries                 | High     |
| US-0707  | Manage Blog Posts                    | High     |
| US-0708  | Manage Awards Content                | Medium   |
| US-0709  | Approve/Reject Student Registrations | Critical |

---

## Dependencies

- EPIC-06: Student Login & Profile System (shared auth infrastructure)

---

## Risks & Assumptions

- **Risk:** Unauthorized access to admin portal
- **Assumption:** Admin credentials are set up during deployment (not self-registration)
- **Assumption:** Role-based access — only admin role exists (no multi-tier roles)
