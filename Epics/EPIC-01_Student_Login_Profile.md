# EPIC-01: Student Login & Profile System
**Priority:** P1 – Critical | **Sprint:** Week 1 | **Depends On:** None

## Description
Secure student authentication with registration (admin approval), login/logout, and a personalized dashboard showing quiz history, game scores, and leaderboard ranking. This is the **foundation** — all other features depend on it.

## Acceptance Criteria
- Students can register with name, email, password, standard (8/9/10), school
- Registration requires admin approval before login is allowed
- Secure login/logout with session persistence
- Student dashboard shows quiz history, game scores, leaderboard ranking
- Students can view and edit their profile
- Passwords stored securely (hashed)

## User Stories

| ID | Story | Points |
|----|-------|--------|
| US-01 | **Student Registration** – As a student, I want to register with my details so I can create an account | 8 |
| US-02 | **Student Login** – As a student, I want to log in with email/password so I can access my dashboard | 5 |
| US-03 | **Student Logout** – As a student, I want to log out securely so my account is safe on shared devices | 2 |
| US-04 | **Student Dashboard** – As a student, I want a dashboard showing my quiz scores, game scores, and rank | 8 |
| US-05 | **View & Edit Profile** – As a student, I want to view and update my profile information | 3 |
