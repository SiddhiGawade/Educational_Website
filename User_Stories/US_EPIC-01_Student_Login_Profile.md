# User Stories — EPIC-01: Student Login & Profile System

> **Depends On:** None — this is the first epic to be developed.

---

## US-01: Student Registration

> **As a** student, **I want to** register with my details, **so that** I can create an account.

**Acceptance Criteria:**
- Student fills in name, email, password, standard (8/9/10), school name
- Account is created with status "Pending Approval"
- Duplicate email shows error "Email already registered"
- Pending account cannot log in — shows "Account pending approval"
- Validation errors for empty/invalid fields

---

## US-02: Student Login

> **As a** registered student, **I want to** log in with email and password, **so that** I can access my dashboard.

**Acceptance Criteria:**
- Valid credentials → redirect to Student Dashboard
- Wrong credentials → show "Invalid email or password"
- Unapproved account → show "Account pending approval"
- Session persists across pages

---

## US-03: Student Logout

> **As a** logged-in student, **I want to** log out securely, **so that** my account is safe on shared devices.

**Acceptance Criteria:**
- Clicking "Logout" terminates the session
- Accessing protected pages after logout → redirect to Login
- Browser back button does not restore logged-in state

---

## US-04: Student Dashboard

> **As a** student, **I want to** see a dashboard with my quiz scores, game scores, and leaderboard rank, **so that** I can track my progress.

**Acceptance Criteria:**
- Welcome message with student's name
- Quiz section: recent scores and overall average
- Games section: game scores summary
- Ranking section: current leaderboard position
- No activity yet → friendly prompts to start

---

## US-05: View & Edit Profile

> **As a** student, **I want to** view and update my profile, **so that** my details are accurate.

**Acceptance Criteria:**
- Profile shows name, email, standard, school
- Can edit name, school, standard
- Can change password (requires current password)
- Weak password shows validation error
- Email cannot be changed
