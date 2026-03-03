# User Stories — EPIC-03: Video Section

---

## US-0301: Browse Video Gallery by Subject

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0301                                                                 |
| **Epic**            | EPIC-03 – Video Section                                                |
| **Priority**        | High                                                                    |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want to** browse educational videos organized by subject and topic,  
> **So that** I can quickly find videos relevant to what I am studying.

### Acceptance Criteria

1. **Given** I visit the Video Section, **When** the page loads, **Then** I see a list of subjects (e.g., Math, Science, English).
2. **Given** I select a subject, **When** the videos filter, **Then** only videos for that subject are displayed.
3. **Given** videos are displayed, **When** I view each video card, **Then** I see a YouTube thumbnail, video title, and short description.
4. **Given** videos exist for multiple standards, **When** I filter by my standard (8/9/10), **Then** I see relevant videos only.

### Technical Notes

- Video data model: `{ id, title, description, youtubeUrl, subject, standard, thumbnail, createdAt }`
- Thumbnail can be auto-generated from YouTube URL: `https://img.youtube.com/vi/{VIDEO_ID}/0.jpg`
- Filter by subject and standard

---

## US-0302: View Video Card and Open YouTube

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0302                                                                 |
| **Epic**            | EPIC-03 – Video Section                                                |
| **Priority**        | High                                                                    |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 2                                                                  |

### User Story

> **As a** student,  
> **I want to** click on a video card and be redirected to the YouTube video,  
> **So that** I can watch the educational video on YouTube.

### Acceptance Criteria

1. **Given** I see a video card, **When** I click on it, **Then** a new browser tab opens with the YouTube video.
2. **Given** the YouTube URL is provided, **When** the card renders, **Then** the thumbnail is fetched and displayed correctly.
3. **Given** a video card is displayed, **When** I hover over it, **Then** I see a visual indication (play icon overlay, hover effect).

### Technical Notes

- Use `target="_blank"` with `rel="noopener noreferrer"` for security
- Play button overlay on hover using CSS

---

## US-0303: Admin Manages Video Entries

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0303                                                                 |
| **Epic**            | EPIC-03 – Video Section                                                |
| **Priority**        | High                                                                    |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 2–3                                                                |

### User Story

> **As an** admin,  
> **I want to** add, edit, and remove video entries through the admin portal,  
> **So that** the video library stays current and organized.

### Acceptance Criteria

1. **Given** I am logged in as admin, **When** I navigate to "Manage Videos", **Then** I see a table of all video entries.
2. **Given** I add a new video, **When** I provide the YouTube URL, title, description, subject, and standard, **Then** the video entry is saved and visible to students.
3. **Given** a video entry exists, **When** I edit its details, **Then** changes are reflected immediately.
4. **Given** I delete a video entry, **When** I confirm deletion, **Then** the video is removed from the gallery.

### Technical Notes

- Auto-extract YouTube video ID from various URL formats
- Auto-generate thumbnail URL from video ID
- Validate YouTube URL format on submission
