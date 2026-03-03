# User Stories — EPIC-03: Interactive Quizzes

> **Depends On:** EPIC-01 (student login), EPIC-02 (admin quiz management)

---

## US-09: Admin Uploads Daily Quiz

> **As an** admin, **I want to** create and upload a daily quiz, **so that** students have fresh content to test their knowledge.

**Acceptance Criteria:**
- Admin fills in quiz title, subject, standard, questions (MCQ), options, correct answers
- Quiz saved with status: Draft or Published
- Can set a publish date for the quiz
- Can edit or delete a quiz before students attempt it

---

## US-10: Student Attempts Quiz

> **As a** student, **I want to** attempt the daily quiz, **so that** I can test my understanding.

**Acceptance Criteria:**
- Today's quiz shown on Quiz section (if available)
- Click "Start Quiz" loads all questions
- Submit saves responses (one attempt per quiz)
- Already attempted → show "Already Attempted"
- Results not declared → show "Results will be announced tomorrow"

---

## US-11: Teacher Declares Results

> **As an** admin, **I want to** declare quiz results the next day, **so that** students can see their scores.

**Acceptance Criteria:**
- "Declare Results" auto-grades all submissions
- Students can see their score on dashboard after declaration
- Leaderboard generated and published
- Already declared → show warning

---

## US-12: View Quiz Leaderboard

> **As a** student, **I want to** view the leaderboard, **so that** I can see how I rank against peers.

**Acceptance Criteria:**
- Ranked list of top performers with names and scores
- Current student's rank highlighted
- Filter by quiz/date
- Results not declared → show "Available after results are announced"

---

## US-13: View Quiz History

> **As a** student, **I want to** view my past quiz attempts and scores, **so that** I can track my progress.

**Acceptance Criteria:**
- List of all attempted quizzes sorted by date (newest first)
- Each entry shows quiz title, date, score, total marks
- Pending results → score shows "Pending"
