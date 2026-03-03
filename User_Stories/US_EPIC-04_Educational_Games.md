# User Stories — EPIC-04: Educational Games

> **Depends On:** EPIC-01 (student login for score tracking), EPIC-02 (admin game management)

---

## US-14: Student Plays Educational Game

> **As a** student, **I want to** play interactive learning games, **so that** I can learn in a fun way.

**Acceptance Criteria:**
- Games page shows available games with title, thumbnail, description
- Click "Play" loads the game in browser
- Score displayed at end of game session
- Best score shown on Games page

---

## US-15: Track Game Scores Per Student

> **As a** student, **I want** my game scores saved, **so that** I can track my progress.

**Acceptance Criteria:**
- Score saved to student profile after each game
- Best score and most recent score visible
- Dashboard "Game Scores" section shows summary of all games played

---

## US-16: Responsive Game Interface

> **As a** student, **I want** games to work on my phone, tablet, or computer, **so that** I can learn from any device.

**Acceptance Criteria:**
- Games adapt to screen size without horizontal scrolling
- Touch controls work on mobile/tablet
- Keyboard/mouse controls work on desktop

---

## US-17: Admin Manages Games

> **As an** admin, **I want to** upload and manage games, **so that** the game library stays fresh.

**Acceptance Criteria:**
- List of all uploaded games with title, status, upload date
- Upload game with title, description, thumbnail, game files
- Edit game details or delete games
- Toggle active/inactive — only active games visible to students
