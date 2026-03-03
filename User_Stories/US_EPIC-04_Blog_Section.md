# User Stories — EPIC-04: Blog Section

---

## US-0401: Browse Blog Posts

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0401                                                                 |
| **Epic**            | EPIC-04 – Blog Section                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 5                                                                       |
| **Sprint**          | Week 3                                                                  |

### User Story

> **As a** student,  
> **I want to** browse educational blog posts,  
> **So that** I can read supplementary learning material at my own pace.

### Acceptance Criteria

1. **Given** I visit the Blog Section, **When** the page loads, **Then** I see a list of blog posts with title, excerpt, author, date, and category.
2. **Given** posts are listed, **When** I scroll down, **Then** older posts load (pagination or infinite scroll).
3. **Given** a blog post has a category, **When** I click the category tag, **Then** I see all posts in that category.

### Technical Notes

- Blog post list: paginated (10 posts per page)
- Display: card layout with featured image (optional), title, excerpt (first 150 chars), date, category

---

## US-0402: Search Blog Posts

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0402                                                                 |
| **Epic**            | EPIC-04 – Blog Section                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 3                                                                  |

### User Story

> **As a** student,  
> **I want to** search blog posts by keyword,  
> **So that** I can quickly find articles on specific topics.

### Acceptance Criteria

1. **Given** I am on the Blog page, **When** I type a keyword in the search bar, **Then** results update to show matching posts.
2. **Given** I search for a term, **When** matches are found in title or content, **Then** the matching posts are displayed.
3. **Given** no results match, **When** the search completes, **Then** I see "No posts found for your search."

### Technical Notes

- Client-side search for small datasets; server-side for larger datasets
- Search across title, content, and tags

---

## US-0403: Read Full Blog Post

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0403                                                                 |
| **Epic**            | EPIC-04 – Blog Section                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 3                                                                  |

### User Story

> **As a** student,  
> **I want to** click on a blog post and read the full article,  
> **So that** I can learn from the complete content.

### Acceptance Criteria

1. **Given** I click on a blog post card, **When** the page loads, **Then** I see the full article with title, author, date, category, and formatted content.
2. **Given** I am reading a post, **When** I reach the end, **Then** I see "Related Posts" suggestions.
3. **Given** the post has images or embedded media, **When** the page renders, **Then** all media loads correctly.

### Technical Notes

- Blog post model: `{ id, title, content (rich text/HTML), author, category, tags[], featuredImage, createdAt, updatedAt }`
- Support rich text formatting (headings, lists, bold, italic, links, images)

---

## US-0404: Admin Manages Blog Posts

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0404                                                                 |
| **Epic**            | EPIC-04 – Blog Section                                                 |
| **Priority**        | High                                                                    |
| **Story Points**    | 8                                                                       |
| **Sprint**          | Week 3                                                                  |

### User Story

> **As an** admin,  
> **I want to** create, edit, and delete blog posts through the admin portal,  
> **So that** I can keep the blog content fresh and educational.

### Acceptance Criteria

1. **Given** I am logged in as admin, **When** I navigate to "Manage Blog", **Then** I see a list of all blog posts with status.
2. **Given** I create a new post, **When** I fill in title, content (rich text editor), category, tags, and featured image, **Then** the post is published.
3. **Given** I edit an existing post, **When** I save changes, **Then** the updated content is visible to students.
4. **Given** I delete a post, **When** I confirm, **Then** the post is removed from the blog.

### Technical Notes

- Rich text editor integration (e.g., TinyMCE, Quill, or CKEditor)
- Image upload for featured images
- Draft/Published status support

---

## US-0405: Filter Blog by Category/Tags

| Field               | Details                                                                 |
|---------------------|-------------------------------------------------------------------------|
| **Story ID**        | US-0405                                                                 |
| **Epic**            | EPIC-04 – Blog Section                                                 |
| **Priority**        | Medium                                                                  |
| **Story Points**    | 3                                                                       |
| **Sprint**          | Week 3                                                                  |

### User Story

> **As a** student,  
> **I want to** filter blog posts by category or tags,  
> **So that** I can find content relevant to a specific subject or topic.

### Acceptance Criteria

1. **Given** I am on the Blog page, **When** I click on a category filter, **Then** only posts in that category are displayed.
2. **Given** blog posts have tags, **When** I click on a tag, **Then** I see all posts with that tag.
3. **Given** a filter is active, **When** I clear the filter, **Then** all posts are displayed again.

### Technical Notes

- Sidebar or top-bar filter with category list
- Tags displayed as clickable chips/badges
- Active filter highlighted visually
