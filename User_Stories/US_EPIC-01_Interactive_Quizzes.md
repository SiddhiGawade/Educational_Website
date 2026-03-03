# User Stories — EPIC-01: Interactive Quizzes

---

## US-0101: Admin Uploads Daily Quiz

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0101                                                                 |
| **Epic**            | EPIC-01 – Interactive Quizzes                                           |
| **Priority**        | Critical                                                                |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 1                                                                  |

### User Story

> **As an** admin/teacher,  
> **I want to** create and upload a daily quiz through the admin portal,  
> **So that** students have fresh quiz content every day to test their knowledge.

### Acceptance Criteria

1. **Given** I am logged in as admin, **When** I navigate to "Manage Quizzes", **Then** I see options to create a new quiz.
2. **Given** I am creating a quiz, **When** I fill in the quiz title, subject, standard (8/9/10), questions (MCQ), options, and correct answers, **Then** the quiz is saved successfully.
3. **Given** a quiz is created, **When** I set a publish date, **Then** the quiz becomes available to students on that date.
4. **Given** a quiz is published, **When** I view the quiz list, **Then** I can see its status (Draft / Published / Results Declared).
5. **Given** a quiz exists, **When** I edit or delete it before students attempt it, **Then** changes are reflected immediately.

### Technical Notes

- Quiz data model: `{ id, title, subject, standard, questions[], publishDate, status, createdAt }`
- Question model: `{ id, questionText, options[], correctAnswer, marks }`
- Status enum: `DRAFT`, `PUBLISHED`, `RESULTS_DECLARED`

---

## US-0102: Student Attempts Quiz

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0102                                                                 |
| **Epic**            | EPIC-01 – Interactive Quizzes                                           |
| **Priority**        | Critical                                                                |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 1–2                                                                |

### User Story

> **As a** student,  
> **I want to** attempt the daily quiz after logging in,  
> **So that** I can test my understanding of the topic.

### Acceptance Criteria

1. **Given** I am logged in as a student, **When** I navigate to the Quiz section, **Then** I see the quiz available for today (if any).
2. **Given** a quiz is available, **When** I click "Start Quiz", **Then** the quiz loads with all questions displayed.
3. **Given** I am attempting a quiz, **When** I select answers and click "Submit", **Then** my responses are saved.
4. **Given** I have submitted the quiz, **When** I try to attempt it again, **Then** I see a message "Already Attempted" (one attempt per quiz).
5. **Given** results are not yet declared, **When** I check my score, **Then** I see "Results will be announced tomorrow."

### Technical Notes

- Submission model: `{ studentId, quizId, answers[], submittedAt, score (null until declared) }`
- Enforce single-attempt per student per quiz
- Auto-save draft answers (optional stretch goal)

---

## US-0103: Teacher Declares Results

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0103                                                                 |
| **Epic**            | EPIC-01 – Interactive Quizzes                                           |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** teacher/admin,  
> **I want to** declare quiz results the next day,  
> **So that** students can see their scores and the leaderboard is published.

### Acceptance Criteria

1. **Given** a quiz has been attempted by students, **When** I click "Declare Results" in the admin portal, **Then** all submissions are auto-graded based on correct answers.
2. **Given** results are declared, **When** students visit their dashboard, **Then** they can see their score for that quiz.
3. **Given** results are declared, **When** the leaderboard is generated, **Then** it ranks students by score (highest first).
4. **Given** results are already declared, **When** I try to declare again, **Then** I see a warning "Results already declared."

### Technical Notes

- Auto-grading compares submitted answers against correct answers
- Score = sum of marks for correct answers
- Update quiz status to `RESULTS_DECLARED`
- Trigger leaderboard generation

---

## US-0104: View Quiz Leaderboard

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0104                                                                 |
| **Epic**            | EPIC-01 – Interactive Quizzes                                           |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want to** view the quiz leaderboard after results are declared,  
> **So that** I can see how I rank against my peers.

### Acceptance Criteria

1. **Given** quiz results are declared, **When** I visit the Leaderboard page, **Then** I see a ranked list of top performers with names and scores.
2. **Given** the leaderboard is displayed, **When** I look for my name, **Then** my rank is highlighted.
3. **Given** multiple quizzes have been completed, **When** I filter by quiz/date, **Then** the leaderboard updates accordingly.
4. **Given** results are not yet declared, **When** I visit the Leaderboard page, **Then** I see "Leaderboard will be available after results are announced."

### Technical Notes

- Leaderboard shows top 10 (configurable) students per quiz
- Optional: cumulative leaderboard across all quizzes
- Highlight current student's row with a distinct style

---

## US-0105: Student Views Quiz History

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0105                                                                 |
| **Epic**            | EPIC-01 – Interactive Quizzes                                           |
| **Priority**        | High                                                                    |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want to** view my past quiz attempts and scores,  
> **So that** I can track my learning progress over time.

### Acceptance Criteria

1. **Given** I am logged in, **When** I navigate to "My Quiz History" on the dashboard, **Then** I see a list of all quizzes I have attempted.
2. **Given** the history is displayed, **When** I look at each entry, **Then** I see quiz title, date, my score, and total marks.
3. **Given** results are pending for a quiz, **When** I view that entry, **Then** the score shows "Pending."

### Technical Notes

- Query all submissions for the logged-in student, sorted by date (newest first)
- Join with quiz data to show title and total marks
