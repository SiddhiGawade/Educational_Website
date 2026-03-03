# User Stories — EPIC-06: Student Login & Profile System

---

## US-0601: Student Registration

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0601                                                                 |
| **Epic**            | EPIC-06 – Student Login & Profile System                               |
| **Priority**        | Critical                                                                |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As a** new student,  
> **I want to** register on the platform with my details,  
> **So that** I can create an account and access learning features after approval.

### Acceptance Criteria

1. **Given** I am on the Registration page, **When** I fill in my name, email, password, standard (8/9/10), and school name, **Then** I can submit the form.
2. **Given** I submit the form, **When** validation passes, **Then** my account is created with status "Pending Approval."
3. **Given** I submit the form with an already-registered email, **When** validation runs, **Then** I see "Email already registered."
4. **Given** my account is pending, **When** I try to log in, **Then** I see "Your account is pending admin approval."
5. **Given** input validation, **When** I submit with empty/invalid fields, **Then** I see appropriate error messages.

### Technical Notes

- Student model: `{ id, name, email, passwordHash, standard, school, status, createdAt }`
- Status enum: `PENDING`, `APPROVED`, `REJECTED`
- Password: minimum 8 characters, hashed with bcrypt
- Client-side + server-side validation

---

## US-0602: Admin Approves Student Registration

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0602                                                                 |
| **Epic**            | EPIC-06 – Student Login & Profile System                               |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As an** admin,  
> **I want to** review and approve/reject student registrations,  
> **So that** only legitimate students gain access to the platform.

### Acceptance Criteria

1. **Given** I am logged in as admin, **When** I navigate to "Pending Registrations", **Then** I see a list of students awaiting approval.
2. **Given** I review a registration, **When** I click "Approve", **Then** the student's status changes to "Approved" and they can log in.
3. **Given** I review a registration, **When** I click "Reject", **Then** the student's status changes to "Rejected" and they cannot log in.
4. **Given** I approve a student, **When** the student tries to log in next, **Then** they are granted access.

### Technical Notes

- Admin notification: badge/count of pending registrations on admin dashboard
- Optional: email notification to student upon approval/rejection

---

## US-0603: Student Login

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0603                                                                 |
| **Epic**            | EPIC-06 – Student Login & Profile System                               |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As a** registered and approved student,  
> **I want to** log in with my email and password,  
> **So that** I can access my dashboard, quizzes, games, and personalized content.

### Acceptance Criteria

1. **Given** I am on the Login page, **When** I enter valid credentials, **Then** I am redirected to my Student Dashboard.
2. **Given** I enter wrong credentials, **When** I submit, **Then** I see "Invalid email or password."
3. **Given** my account is not approved, **When** I try to log in, **Then** I see "Account pending approval."
4. **Given** I am logged in, **When** I navigate the site, **Then** my session persists across pages.

### Technical Notes

- Authentication: JWT or session-based
- Session timeout: configurable (e.g., 24 hours)
- Rate limiting on login attempts to prevent brute force

---

## US-0604: Student Logout

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0604                                                                 |
| **Epic**            | EPIC-06 – Student Login & Profile System                               |
| **Priority**        | Critical                                                                |
| **Story Points**    | 2                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As a** logged-in student,  
> **I want to** securely log out of the platform,  
> **So that** my account remains safe, especially on shared devices.

### Acceptance Criteria

1. **Given** I am logged in, **When** I click "Logout", **Then** my session is terminated.
2. **Given** I have logged out, **When** I try to access any protected page, **Then** I am redirected to the Login page.
3. **Given** I log out, **When** I press the browser back button, **Then** I am not taken back to a logged-in state.

### Technical Notes

- Clear JWT token / destroy session on logout
- Invalidate server-side session if using session-based auth

---

## US-0605: View Student Dashboard

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0605                                                                 |
| **Epic**            | EPIC-06 – Student Login & Profile System                               |
| **Priority**        | Critical                                                                |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 1–2                                                                |

### User Story

> **As a** logged-in student,  
> **I want to** see a dashboard that summarizes my quiz history, game scores, and leaderboard ranking,  
> **So that** I can track my overall progress in one place.

### Acceptance Criteria

1. **Given** I log in, **When** the dashboard loads, **Then** I see a welcome message with my name.
2. **Given** I have attempted quizzes, **When** I look at the Quiz section, **Then** I see my recent quiz scores and overall average.
3. **Given** I have played games, **When** I look at the Games section, **Then** I see my game scores summary.
4. **Given** leaderboard data is available, **When** I look at the Ranking section, **Then** I see my current leaderboard position.
5. **Given** I have no activity yet, **When** I look at the dashboard, **Then** I see friendly prompts to take a quiz or play a game.

### Technical Notes

- Aggregate data from quiz submissions, game scores, and leaderboard
- Dashboard widgets: Quiz Summary Card, Game Summary Card, Leaderboard Rank Card
- Performance: efficient queries to avoid slow dashboard loading

---

## US-0606: View and Edit Profile

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0606                                                                 |
| **Epic**            | EPIC-06 – Student Login & Profile System                               |
| **Priority**        | High                                                                    |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want to** view and update my profile information,  
> **So that** my account details are always accurate.

### Acceptance Criteria

1. **Given** I am logged in, **When** I navigate to "My Profile", **Then** I see my name, email, standard, and school.
2. **Given** I click "Edit Profile", **When** I update my name or school, **Then** changes are saved.
3. **Given** I want to change my password, **When** I enter current password and new password, **Then** my password is updated.
4. **Given** I try to change to a weak password, **When** I submit, **Then** I see a validation error.

### Technical Notes

- Email cannot be changed (used as unique identifier)
- Standard can be changed (student may advance to next standard)
- Password change requires current password verification
