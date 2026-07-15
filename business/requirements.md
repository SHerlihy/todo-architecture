# Business Requirements Document

## 1. Project Overview

**Project Name:** Simple Task Tracker  
**Document Owner:** Product Owner  
**Version:** 3.0  
**Date:** 2026-07-09

### 1.1 Purpose
This document defines the business requirements for a simple task tracking application that helps users create, organize, and complete tasks in one place.

### 1.2 Business Objective
The application will reduce missed work and improve personal or team organization by providing a lightweight way to manage task lists and track progress.

Missed work is not currently quantified, so the project will establish a baseline after launch and measure improvement from that baseline rather than against a predeclared missed-work percentage.

The application supports regular daily use during business hours in a single local timezone, with no requirement for continuous 24-hour global operation in the first release.

Usage is expected to be highest at the start and end of the working day, with no known seasonal spike requirement for the initial release.

The initial release is intended for use in the United Kingdom, with the majority of users based in London and Manchester.

### 1.3 Success Criteria
- Users can create and manage tasks without training.
- Users can see their open and completed tasks at a glance.
- The core workflow works reliably on desktop and mobile browsers.
- The system supports internal and customer-facing users as needed.

## 2. Scope

### 2.1 In Scope
- Create, edit, delete, and complete tasks
- Organize tasks into lists or categories
- Set simple due dates and priorities
- Filter tasks by status
- Basic user authentication
- Support for users of the task tracker, whether internal or customer-facing

### 2.2 Out of Scope
- Advanced project management features
- Real-time collaboration
- File attachments
- Third-party integrations
- Reporting dashboards beyond basic task counts

## 3. Stakeholders

- **Business Sponsor:** Defines business goals and approves scope
- **Product Owner:** Owns requirements and prioritization
- **End Users:** Create and manage tasks
- **Development Team:** Implements and tests the solution
- **Support Team:** Handles user issues after release

### 3.1 User Definition
For this project, a user is any end user of the task tracker. The initial requirements do not restrict usage to internal-only or customer-only audiences.

## 4. User Needs

### 4.1 Primary User Need
As a user, I need a simple way to record tasks so I can remember what needs to be done.

### 4.2 Secondary User Needs
- As a user, I need to mark tasks complete so I can track progress.
- As a user, I need to organize tasks so I can focus on the most important work.
- As a user, I need to view overdue tasks so I can act on them quickly.

## 5. Functional Requirements

### 5.1 Task Management
The system shall allow users to:
- Create a task with a title
- Edit task details
- Mark a task as complete or incomplete
- Delete a task
- View task history in a simple list view

### 5.2 Organization
The system shall allow users to:
- Assign a task to a list or category
- Filter tasks by open, completed, or overdue status
- Sort tasks by due date or priority

### 5.3 Task Attributes
Each task shall support:
- Title
- Description
- Due date
- Priority
- Status
- Plain text task details only; rich media is not supported

### 5.4 Authentication
The system shall allow users to:
- Sign in securely
- Access only their own task data
- Use a standard secure sign-in flow

## 6. Non-Functional Requirements

### 6.1 Usability
- The main task list should be understandable without onboarding.
- Common actions should be available within one or two clicks.
- "At a glance" means the user can understand task status immediately on opening the main task view.

### 6.2 Performance
- The application should load the main task view quickly under normal usage.
- "Quickly" is defined as a responsive experience rather than a fixed sub-100ms or sub-10ms threshold.
- Task updates should appear immediately after save, using optimistic UI behavior where appropriate.

### 6.3 Reliability
- User data should not be lost during normal operation.
- Failed saves should return a clear error message.
- The BRD does not define a numeric failed-save tolerance; the requirement is that failures are visible and do not silently lose data.

### 6.4 Security
- User authentication must protect task data from unauthorized access.
- Sensitive data should be stored and transmitted securely.
- At minimum, data in transit must use HTTPS/TLS and data at rest must be protected.
- Task data is not treated as medical data or sensitive PII by default.

## 7. Assumptions

- Users have access to a modern web browser.
- The initial release supports individual task tracking only.
- Users do not require advanced permissions or shared workspaces.
- The initial release is intended for use in the country or countries listed in Section 1.2.
- The primary usage window is standard business hours, roughly 9am to 5pm in one local timezone.
- Demand is expected to be relatively steady within those hours, with light spikes when users start and finish their day.

## 8. Constraints

- The project should remain simple and low maintenance.
- The product is expected to be fully maintained for at least 3 years after launch.
- Two full-time engineers will be available for maintenance over the 3-year support period.
- The first release should prioritize core task management over extra features.
- The design should work well on both desktop and mobile screens.

## 9. Acceptance Criteria

The project will be considered complete when:
- A user can sign in and manage their tasks end to end
- Tasks can be created, edited, completed, filtered, and deleted
- The application stores user data correctly
- Core flows have been tested and pass acceptance checks
