# User Stories — EPIC-07: Admin Portal

---

## US-0701: Admin Login

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0701                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | Critical                                                                |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As an** admin/teacher,  
> **I want to** securely log in to the admin portal,  
> **So that** I can manage platform content and student accounts.

### Acceptance Criteria

1. **Given** I am on the Admin Login page, **When** I enter valid admin credentials, **Then** I am redirected to the Admin Dashboard.
2. **Given** I enter invalid credentials, **When** I submit, **Then** I see "Invalid admin credentials."
3. **Given** a student tries the admin login, **When** they enter student credentials, **Then** access is denied.
4. **Given** I am logged in as admin, **When** I navigate admin pages, **Then** my session persists.

### Technical Notes

- Separate admin auth or role-based access control
- Admin credentials pre-configured during setup
- Admin login URL may be separate from student login for security

---

## US-0702: Admin Dashboard Overview

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0702                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As an** admin,  
> **I want to** see a dashboard overview of platform activity,  
> **So that** I can monitor student engagement and content status at a glance.

### Acceptance Criteria

1. **Given** I log in as admin, **When** the dashboard loads, **Then** I see summary cards: total students, active quizzes, pending registrations, total games, total videos, total blog posts.
2. **Given** there are pending registrations, **When** I see the notification badge, **Then** I can click to navigate to the pending registrations page.
3. **Given** a quiz is active today, **When** I check the dashboard, **Then** I see the quiz status (submissions count, declared/not).

### Technical Notes

- Aggregate queries for summary statistics
- Real-time or near-real-time data (refresh on page load)
- Quick-action buttons for common tasks (e.g., "Upload Quiz", "Approve Students")

---

## US-0703: Manage Quizzes (CRUD)

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0703                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | Critical                                                                |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 1–2                                                                |

### User Story

> **As an** admin,  
> **I want to** create, read, update, and delete quizzes from the admin portal,  
> **So that** I can manage the daily quiz content for students.

### Acceptance Criteria

1. **Given** I am on the Manage Quizzes page, **When** I view the list, **Then** I see all quizzes with title, date, standard, subject, and status.
2. **Given** I click "Create Quiz", **When** I fill in quiz details and questions, **Then** the quiz is saved as Draft or Published.
3. **Given** I edit a quiz, **When** I modify questions or details, **Then** changes are saved (if quiz not yet attempted).
4. **Given** I delete a quiz, **When** I confirm, **Then** the quiz and associated submissions are removed.
5. **Given** students have already attempted the quiz, **When** I try to edit, **Then** I see a warning about existing submissions.

### Technical Notes

- Dynamic form to add/remove questions during quiz creation  
- Bulk import questions (optional: CSV upload)  
- Quiz preview functionality for admin before publishing

---

## US-0704: Declare Quiz Results & Publish Leaderboard

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0704                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As an** admin,  
> **I want to** declare quiz results and publish the leaderboard,  
> **So that** students can see their scores and rankings.

### Acceptance Criteria

1. **Given** a quiz has submissions, **When** I click "Declare Results", **Then** all submissions are auto-graded and scores are published.
2. **Given** results are declared, **When** the leaderboard is generated, **Then** it shows ranked students with their scores.
3. **Given** I want to review before publishing, **When** I click "Preview Results", **Then** I see a summary of all submissions and scores.
4. **Given** results are declared, **When** students visit the platform, **Then** they can see their score and the leaderboard.

### Technical Notes

- Auto-grading: compare submitted answers with correct answers  
- Leaderboard sorted by score descending, then by submission time  
- Email/notification trigger (optional stretch goal)

---

## US-0705: Manage Educational Games

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0705                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2–3                                                                |

### User Story

> **As an** admin,  
> **I want to** upload, edit, and remove educational games,  
> **So that** the game library stays current and engaging.

### Acceptance Criteria

1. **Given** I am on the Manage Games page, **When** I view the list, **Then** I see all games with title, status, and upload date.
2. **Given** I upload a new game, **When** I provide title, description, thumbnail, and game files (zip), **Then** the game is added and accessible to students.
3. **Given** I edit a game, **When** I update its details, **Then** changes are reflected.
4. **Given** I deactivate a game, **When** I toggle status, **Then** the game is hidden from students.

### Technical Notes

- File upload: accept `.zip` format containing game assets  
- Extract and serve game files from a designated directory  
- Game thumbnail: accept image upload (JPEG/PNG)

---

## US-0706: Manage Video Entries

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0706                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 2–3                                                                |

### User Story

> **As an** admin,  
> **I want to** manage video entries (add/edit/delete YouTube video links),  
> **So that** the video gallery remains organized and up-to-date.

### Acceptance Criteria

1. **Given** I am on the Manage Videos page, **When** I view the list, **Then** I see all video entries with title, subject, standard, and YouTube URL.
2. **Given** I add a video, **When** I paste a YouTube URL, **Then** the thumbnail is auto-fetched and a preview is shown.
3. **Given** I edit a video entry, **When** I save changes, **Then** the updated entry is displayed in the gallery.
4. **Given** I delete a video, **When** I confirm, **Then** it is removed from the gallery.

### Technical Notes

- YouTube URL validation and video ID extraction  
- Auto-thumbnail using `https://img.youtube.com/vi/{ID}/0.jpg`

---

## US-0707: Manage Blog Posts

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0707                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 3                                                                  |

### User Story

> **As an** admin,  
> **I want to** create, edit, and delete blog posts with a rich text editor,  
> **So that** I can publish educational articles for students.

### Acceptance Criteria

1. **Given** I am on the Manage Blog page, **When** I view the list, **Then** I see all posts with title, category, status, and date.
2. **Given** I create a new post, **When** I use the rich text editor and fill in title, content, category, and tags, **Then** the post is published.
3. **Given** I edit a post, **When** I save changes, **Then** the updated content is visible on the blog.
4. **Given** I delete a post, **When** I confirm, **Then** the post is removed.
5. **Given** I save a post as Draft, **When** I view it, **Then** it is only visible in admin, not on the public blog.

### Technical Notes

- Rich text editor with image embedding support  
- Category and tags management (CRUD)  
- Draft/Published status toggle

---

## US-0708: Manage Awards Content

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0708                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | Medium                                                                  |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 3–4                                                                |

### User Story

> **As an** admin,  
> **I want to** manage awards and achievements content,  
> **So that** the Awards page reflects the latest recognitions and achievements.

### Acceptance Criteria

1. **Given** I am on the Manage Awards page, **When** I view the list, **Then** I see all awards with title, date, and image count.
2. **Given** I add an award, **When** I provide title, description, date, and images, **Then** the award is published.
3. **Given** I edit or delete an award, **When** I save, **Then** changes are reflected on the Awards page.

### Technical Notes

- Multi-image upload per award entry  
- Drag-and-drop image ordering (optional)

---

## US-0709: Approve/Reject Student Registrations

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0709                                                                 |
| **Epic**            | EPIC-07 – Admin Portal                                                 |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As an** admin,  
> **I want to** review, approve, or reject pending student registrations,  
> **So that** only genuine students can access the platform.

### Acceptance Criteria

1. **Given** new registrations exist, **When** I navigate to "Pending Registrations", **Then** I see a list with student name, email, standard, and school.
2. **Given** I review a student, **When** I click "Approve", **Then** the student's status changes to Approved.
3. **Given** I review a student, **When** I click "Reject", **Then** the student's status changes to Rejected.
4. **Given** I have bulk registrations, **When** I select multiple students, **Then** I can approve/reject in bulk.

### Technical Notes

- Bulk action: select-all checkbox + batch approve/reject  
- Filter pending registrations by standard or date  
- Notification badge on admin dashboard for pending count
