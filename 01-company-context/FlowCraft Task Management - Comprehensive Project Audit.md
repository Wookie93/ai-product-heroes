FlowCraft Task Management - Comprehensive Project Audit
## Overview
FlowCraft is a comprehensive Linear-style task management application built with Next.js,
featuring issue tracking, sprint management, team collaboration, and kanban board
visualization.
---
## Core Features
### 1. Issue Management (Issues Tab)
**Create Issues**
- Create new issues with title, description, priority (P0-P5), status, and assignee
- Assign issues to specific teams (filtered by assignee's team memberships)
- Assign issues to sprints during creation
- Automatic issue ID generation (TSK-XXX format)
- Form validation ensures all required fields are completed
**View & Filter Issues**
- Table view displaying all issues with sortable columns
- Search issues by title or description
- Filter by:
- Priority (P0-P5)
- Status (Backlog, Todo, In Progress, In Review, Done)
- Assignee
- Team (including "Unassigned" option)
- Sort by title, priority, status, or assignee
- Clear all filters with one click
- View issue count (e.g., "16 of 16 issues")
**Edit & Delete Issues**
- Edit any issue field inline from the table
- Delete issues with confirmation dialog
- Assign/reassign issues to different sprints
- Change issue status, priority, or assignee
---
### 2. Sprint Management (Sprints Tab)
**Create Sprints**
- Create sprints with name, start date, and end date
- Date validation ensures end date is after start date
- Automatic sprint status management
**Sprint Lifecycle**
- **Start Sprint**: Activate a planned sprint (only one active sprint allowed)
- **End Sprint**: Complete an active sprint
- Unfinished issues automatically return to backlog
- Sprint marked as completed with final statistics
- View sprint duration and progress
- Track issues by status within each sprint
**View Sprints**
- See all sprints (completed, active, planned)
- Filter sprints by status
- Search sprints by name
- View sprint statistics:
- Duration and date range
- Progress percentage
- Issue count by status
- Overdue indicators
**Edit & Delete Sprints**
- Edit sprint details (name, dates)
- Delete sprints with confirmation
- Cannot delete active sprints
---
### 3. Team Management (Teams Tab)
**Create Teams**
- Create teams with name and description
- Assign multiple team members from available assignees
- One user can belong to multiple teams
**Manage Teams**
- View all teams with member counts
- Edit team details and membership
- Delete teams with confirmation
- See which users are assigned to each team
**Team Benefits**
- Filter kanban boards by team
- Filter issues by team
- Assign issues to teams for better organization
- Team-based work visualization
---
### 4. Current Sprint (Kanban Board)
**Sprint Overview**
- View active sprint details (name, duration, progress)
- See sprint statistics:
- Date range and duration
- Progress percentage (completed vs total issues)
- Issue breakdown by status
**Team-Based Kanban**
- Filter kanban board by team using dropdown selector
- View "All Teams" or specific team boards
- Only shows issues assigned to team members
- Works even without teams (shows all users)
**Kanban Columns**
- Four status columns: Todo, In Progress, In Review, Done
- Issue count badges on each column
- Color-coded status indicators
**Drag & Drop**
- Drag issues between columns to change status
- Visual feedback during dragging
- Automatic status update on drop
- Responsive touch support for mobile
**Add Issues from Backlog**
- "+" button on each column header
- Opens modal showing backlog issues
- Filter backlog by team (when team is selected)
- Select multiple issues with checkboxes
- Add selected issues to sprint with chosen status
- One-click bulk assignment
**Issue Cards**
- Compact, Linear-style design
- Color-coded priority indicators
- Issue ID (TSK-XXX) with colored circle
- Issue title
- Priority badge (P0-P5)
- Assignee name
- Edit button for quick access
---
### 5. Cross-Feature Capabilities
**Search & Filter**
- Global search across issues
- Multiple filter combinations
- Real-time filtering updates
- Clear filters functionality
**Assignment Management**
- Assign issues to sprints from multiple locations:
- During issue creation
- From issue table
- From issue edit dialog
- From backlog modal in kanban view
- Reassign issues between sprints
- Remove issues from sprints
**Data Validation**
- Required field validation on all forms
- Date validation for sprints
- Team membership validation for issue assignment
- Duplicate prevention
---
### 6. User Interface Features
**Theme Support**
- Light and dark mode toggle
- Consistent Slate color palette
- Automatic theme persistence
- Smooth theme transitions
**Responsive Design**
- Mobile-friendly layouts
- Touch-optimized drag and drop
- Collapsible sidebar on mobile
- Adaptive table views
**Accessibility**
- WCAG 2.1 AA compliant
- Keyboard navigation support
- Screen reader compatibility
- Focus management
- Skip links for navigation
- Proper ARIA labels and roles
**Visual Design**
- Linear-inspired interface
- Clean, minimal card designs
- Consistent spacing and typography
- Color-coded priorities and statuses
- Dark sidebar with light content area
- Professional, modern aesthetic
---
### 7. Navigation
**Sidebar Navigation**
- Four main sections:
- Issues (table view)
- Current Sprint (kanban board)
- Sprints (sprint management)
- Teams (team management)
- Active section highlighting
- Descriptive section labels
- Theme toggle in sidebar
**Contextual Actions**
- "New Issue" button in Issues view
- "New Sprint" button in Sprints view
- "New Team" button in Teams view
- Quick edit/delete actions on cards and rows