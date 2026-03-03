# User Stories — EPIC-02: Educational Games

---

## US-0201: Student Plays Educational Game

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0201                                                                 |
| **Epic**            | EPIC-02 – Educational Games                                            |
| **Priority**        | Critical                                                                |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want to** play interactive educational games on the website,  
> **So that** I can learn concepts in a fun and engaging way.

### Acceptance Criteria

1. **Given** I am on the Games page, **When** I view available games, **Then** I see a list/grid of games with title, thumbnail, and description.
2. **Given** I select a game, **When** I click "Play", **Then** the game loads in the browser without requiring any plugins.
3. **Given** I am playing a game, **When** the game session ends, **Then** my score is calculated and displayed.
4. **Given** I complete a game, **When** I return to the Games page, **Then** I can see my best score for that game.

### Technical Notes

- Games are HTML5/JS-based, embedded via iframe or direct component
- Game assets (HTML, JS, CSS, images) are served from the platform

---

## US-0202: Track Game Scores Per Student

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0202                                                                 |
| **Epic**            | EPIC-02 – Educational Games                                            |
| **Priority**        | Critical                                                                |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want** my game scores to be saved to my profile,  
> **So that** I can track my progress and compete with peers.

### Acceptance Criteria

1. **Given** I complete a game, **When** my score is recorded, **Then** it is saved against my student profile.
2. **Given** I have played a game multiple times, **When** I view my scores, **Then** I see my best score and most recent score.
3. **Given** I visit my dashboard, **When** I check the "Game Scores" section, **Then** I see a summary of all games played with scores.

### Technical Notes

- Game score model: `{ studentId, gameId, score, playedAt }`
- Store both best score and history of all attempts
- Dashboard shows aggregated game performance

---

## US-0203: Responsive Game Interface

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0203                                                                 |
| **Epic**            | EPIC-02 – Educational Games                                            |
| **Priority**        | High                                                                    |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2–3                                                                |

### User Story

> **As a** student,  
> **I want** the games to work smoothly on my phone, tablet, or computer,  
> **So that** I can play and learn from any device.

### Acceptance Criteria

1. **Given** I open a game on a mobile device, **When** the game loads, **Then** it adapts to the screen size without horizontal scrolling.
2. **Given** I am on a tablet, **When** I interact with game elements, **Then** touch controls work correctly.
3. **Given** I am on a desktop, **When** I play, **Then** keyboard/mouse controls work as expected.

### Technical Notes

- Responsive canvas/layout using CSS media queries
- Touch event handlers for mobile/tablet
- Test on common resolutions: 360px, 768px, 1024px, 1440px

---

## US-0204: Admin Manages Games

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0204                                                                 |
| **Epic**            | EPIC-02 – Educational Games                                            |
| **Priority**        | High                                                                    |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2–3                                                                |

### User Story

> **As an** admin,  
> **I want to** upload and manage educational games from the admin portal,  
> **So that** I can keep the game library fresh and relevant.

### Acceptance Criteria

1. **Given** I am logged in as admin, **When** I navigate to "Manage Games", **Then** I see a list of all uploaded games.
2. **Given** I want to add a game, **When** I fill in the title, description, upload game files, and submit, **Then** the game is added to the platform.
3. **Given** a game exists, **When** I edit its details or delete it, **Then** changes are reflected on the student-facing Games page.
4. **Given** I upload a game, **When** I set it as active/inactive, **Then** only active games are visible to students.

### Technical Notes

- Game upload: zip file containing HTML/JS/CSS assets
- Server extracts and serves the game files
- Game metadata: `{ id, title, description, thumbnail, status, uploadedAt }`
