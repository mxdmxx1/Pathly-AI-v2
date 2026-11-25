# Proposed Database Plan

Conceptual starting point only; final schema and access policies require review before implementation.

## Candidate tables

### profiles
Authenticated user ID, optional display name, pathway (VCE/VM), year level and timestamps.

### subjects
Subject or learning-area name, pathway, curriculum version and active status.

### student_subjects
User ID, selected subject/learning-area ID and creation date.

### learning_modules
Subject ID, title, description, sequence and content version.

### lessons
Module ID, title, content reference and sequence.

### lesson_progress
User ID, lesson ID, status and completion timestamp.

### practice_questions
Subject ID, topic, question type, content reference, source type and review status.

### practice_attempts
User ID, question ID, response/feedback references and timestamp.

### pathway_options
Provider, qualification, pathway type, location, requirements summary, official source URL, applicable year and last-checked date.

### student_goals
User ID, goal type, title, target date and status.

## Security principles
- Enable row-level security on student-owned data.
- Users can access only records they are authorised to access.
- Never expose service-role credentials to browsers.
- Avoid unnecessary sensitive information.
- Define retention and deletion processes.
- Keep AI conversation storage minimal and transparent.

## Data quality
Curriculum and pathway records need source, version and review-date metadata. Generated or unverified information must not be represented as authoritative.
