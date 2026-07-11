## Project Title
Social Blogger

## Description
A full-stack web application where users can create accounts, publish blog posts, comment on other users’ posts, and manage their personal profiles. The platform should feel like a lightweight social media experience focused on content creation, interaction, and profile ownership.

## Purpose & Target Audience
- Audience: Individuals who want to publish short-form content or blog posts. Readers who want to discover and comment on content. Early-stage communities or creators who need a lightweight social publishing platform
- Purpose: The purpose of this platform is to provide a simple yet engaging space for users to share ideas, publish content, interact with others through comments, and maintain a public profile.

## User Stories
1. As a new visitor, I want to create an account so that I can access the platform and start publishing content.
2. As an authenticated user, I want to create a blog post so that I can share content with others.
3. As a visitor or user, I want to view posts so that I can browse content and discover authors.
4. As an author, I want to edit my existing post so that I can correct or improve its content.
5. As an authenticated user, I want to comment on a post so that I can engage with the author and other readers.

## Acceptance Criteria
### Story 1: Create an account
- A visitor can register with a valid email and password.
- The system validates required fields and rejects invalid input.
- A new account is created successfully and the user is redirected to a signed-in experience.
- Duplicate accounts are handled with a clear error message.

### Story 2: Create a post
- A user can create a post with a title, content, and optional cover image or metadata.
- The post is saved and displayed on the main feed or user profile.
- Validation prevents empty or invalid submissions.
- The user receives confirmation that the post was published.

### Story 3: Add a comment
- A signed-in user can submit a comment on a post.
- Comments appear immediately or after refresh in the correct thread.
- Empty comments are rejected.
- The system associates the comment with the correct post and user.

## Technical Requirements
- Framework: Next.js App Router
- Language: TypeScript in strict mode
- Styling: Tailwind CSS
- Data: PostgreSQL
- Auth: Clerk
- Performance: Server components by default; client components only where interactivity is needed

## Core API Endpoints
- GET /api/posts
- GET /api/posts/:id
- POST /api/posts
- PUT /api/posts/:id
- DELETE /api/posts/:id
- GET /api/posts/:id/comments
- POST /api/posts/:id/comments
- PUT /api/posts/:id/comments/:id
- DELETE /api/posts/:id/comments/:id
- GET /api/users/:id
- POST /api/users/signup
- PUT /api/users/:id
- DELETE /api/users/:id

## Implementation Priority
- P0: Sign up, sign in, sign out, browse posts, create post, create comment
- P1: Authentification, edit account, delete account, data validation, error handling
- P2: Edit post, edit comment, delete post, delete comment