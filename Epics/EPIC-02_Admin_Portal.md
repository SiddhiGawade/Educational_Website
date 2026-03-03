# EPIC-02: Admin Portal
**Priority:** P1 – Critical | **Sprint:** Week 1–2 | **Depends On:** EPIC-01

## Description
Secure admin dashboard to manage all platform content — quizzes, games, videos, blog posts, awards, and student registrations. Central hub for teacher/admin operations. Depends on EPIC-01 for shared authentication infrastructure.

## Acceptance Criteria
- Admin can log in with admin credentials (separate from student login)
- Dashboard shows summary: total students, active quizzes, pending registrations
- Admin can approve/reject student registrations
- Admin can manage quizzes, games, videos, blog posts, and awards (CRUD)
- Admin can declare quiz results and publish leaderboards
- Portal is accessible only to authorized admin users

## User Stories

| ID | Story | Points |
|----|-------|--------|
| US-06 | **Admin Login** – As an admin, I want to log in securely to access the admin portal | 3 |
| US-07 | **Admin Dashboard Overview** – As an admin, I want a summary of platform activity at a glance | 5 |
| US-08 | **Approve/Reject Registrations** – As an admin, I want to approve or reject student registrations | 5 |
