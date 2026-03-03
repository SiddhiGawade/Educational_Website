# User Stories — EPIC-02: Admin Portal

> **Depends On:** EPIC-01 (shared auth infrastructure)

---

## US-06: Admin Login

> **As an** admin, **I want to** log in securely, **so that** I can access the admin portal.

**Acceptance Criteria:**
- Valid admin credentials → redirect to Admin Dashboard
- Invalid credentials → show "Invalid admin credentials"
- Student credentials cannot access admin login
- Session persists across admin pages

---

## US-07: Admin Dashboard Overview

> **As an** admin, **I want to** see a summary of platform activity, **so that** I can monitor engagement.

**Acceptance Criteria:**
- Summary cards: total students, active quizzes, pending registrations, total games, total videos, total blog posts
- Pending registrations badge with link to approvals
- Today's quiz status shown (submission count, declared or not)
- Quick-action buttons: Upload Quiz, Approve Students

---

## US-08: Approve/Reject Student Registrations

> **As an** admin, **I want to** approve or reject student registrations, **so that** only legitimate students access the platform.

**Acceptance Criteria:**
- Pending registrations list: student name, email, standard, school
- "Approve" → student status changes to Approved (can log in)
- "Reject" → student status changes to Rejected (cannot log in)
- Bulk select and approve/reject multiple students at once
