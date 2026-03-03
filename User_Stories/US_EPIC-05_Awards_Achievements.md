# User Stories — EPIC-05: Awards & Achievements

---

## US-0501: View Awards & Achievements Page

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0501                                                                 |
| **Epic**            | EPIC-05 – Awards & Achievements                                       |
| **Priority**        | Medium                                                                  |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 3–4                                                                |

### User Story

> **As a** student or visitor,  
> **I want to** view a page showcasing awards and achievements,  
> **So that** I feel inspired and motivated to perform well.

### Acceptance Criteria

1. **Given** I visit the Awards page, **When** the page loads, **Then** I see a list of achievements with title, description, and date.
2. **Given** achievements are displayed, **When** I scroll through them, **Then** they are visually organized with images and text.
3. **Given** the page is responsive, **When** I view it on mobile, **Then** the layout adjusts gracefully.

### Technical Notes

- Achievement model: `{ id, title, description, date, images[], createdAt }`
- Display in a timeline or card grid layout

---

## US-0502: Browse Award Image Gallery

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0502                                                                 |
| **Epic**            | EPIC-05 – Awards & Achievements                                       |
| **Priority**        | Medium                                                                  |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 3–4                                                                |

### User Story

> **As a** student or visitor,  
> **I want to** browse through award photos in a gallery,  
> **So that** I can see award ceremonies and achievements visually.

### Acceptance Criteria

1. **Given** I am on the Awards page, **When** I see the image gallery, **Then** photos are displayed in a grid layout.
2. **Given** I click on a photo, **When** the lightbox opens, **Then** I see the full-size image with navigation (previous/next).
3. **Given** the gallery is displayed, **When** images load, **Then** lazy loading is applied for performance.

### Technical Notes

- Lightbox component for full-size image viewing
- Lazy loading with `loading="lazy"` attribute
- Image optimization: thumbnails for gallery, full-size for lightbox

---

## US-0503: Admin Manages Awards Content

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0503                                                                 |
| **Epic**            | EPIC-05 – Awards & Achievements                                       |
| **Priority**        | Medium                                                                  |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 4                                                                  |

### User Story

> **As an** admin,  
> **I want to** add, edit, and remove awards and achievement entries,  
> **So that** the Awards page stays updated with the latest recognitions.

### Acceptance Criteria

1. **Given** I am logged in as admin, **When** I navigate to "Manage Awards", **Then** I see a list of all award entries.
2. **Given** I add a new award, **When** I provide title, description, date, and upload images, **Then** the award is published on the Awards page.
3. **Given** an award exists, **When** I edit or delete it, **Then** changes are reflected on the public page.

### Technical Notes

- Multiple image upload per award entry
- Image storage with file-size limits (e.g., max 5MB per image)
- Admin can reorder awards (drag-and-drop or sort order field)
