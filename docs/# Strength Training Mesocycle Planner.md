# Strength Training Mesocycle Planner

## High-Level Scope

This project is a purpose-built strength training analysis and planning tool for a single user, designed to ingest, clean, edit, and analyze data exported from the Strong app. Rather than replacing the Strong app's workout tracking features immediately, this tool will focus on:

1. **Accurate import and normalization of Strong-exported data**
2. **Editing capabilities for any historical workout session**
3. **Tracking exercise performance across time and mesocycles**
4. **Analyzing performance within and across mesocycles**

The system should prioritize data integrity, consistency, and usefulness over interface polish or multi-user features. Future workout planning is allowed, but real-time logging or exporting to other platforms is deferred.

---

## Detailed Feature Set (User Stories & Acceptance Criteria)

### Epic 1 – Exercise Management & Progress Tracking

#### User Story 1.1 – Create and Manage Exercises

* Create, edit, delete exercises in a centralized list
* Fields: name, category/tag, unit (kg/lb)
* Cannot delete if in use without warning
* View exercises in a searchable, filterable list

#### User Story 1.2 – Use Exercise in a Session

* Select exercises from master list when editing sessions
* Show metadata: last used date, previous PR

#### User Story 1.3 – View Past Data for an Exercise

* Chronological session list for each exercise
* Includes date, total volume, top set, etc.

#### User Story 1.4 – Visualize Volume Over Time

* Charts with daily, weekly, monthly toggles
* Hover shows date and total volume

#### User Story 1.5 – Visualize PR Progression

* Show 1RM/3RM/5RM progression (configurable)
* Chart points show date, reps, weight
* Updates with edits to historical data

---

### Epic 2 – Workout Session Editing

#### User Story 2.1 – View All Workout Sessions

* List view with sortable, filterable sessions
* Metadata shown: date, total volume, number of exercises

#### User Story 2.2 – View a Single Workout Session

* Group exercises with sets shown (reps, weight, RPE, notes)

#### User Story 2.3 – Edit a Workout Session

* Edit any field: date, exercise, sets, reps, weights, notes
* Immediate persistence; edits reflected in analytics

#### User Story 2.4 – Add or Remove Exercises from a Session

* Add from master list
* Define sets immediately
* Remove with confirmation

#### User Story 2.5 – Maintain Edit History or Mark Edited Sessions

* Mark edited sessions visually
* Store original imported version in background

---

### Epic 3 – Mesocycle Organization & Analysis

#### User Story 3.1 – Define and Manage Mesocycles

* Create/edit/delete mesocycles
* Fields: name, start/end date

#### User Story 3.2 – Assign Sessions to Mesocycles

* Manually or bulk assign by date range
* Session belongs to only one mesocycle

#### User Story 3.3 – View Sessions Within a Mesocycle

* Chronological list with date, volume, PRs, etc.

#### User Story 3.4 – Analyze Mesocycle Performance

* Show total volume per exercise, weekly intensity, PR count
* Filterable by exercise or tag

#### User Story 3.5 – Plan Future Mesocycles and Workouts

* Allow draft sessions within future mesocycles
* Drafts don’t affect PRs unless marked complete

---

### Epic 4 – Strong-Data Import & Conflict Resolution

#### User Story 4.1 – Import a Strong App CSV Export

* Parse and transform into native data
* Show import summary and malformed rows

#### User Story 4.2 – Prevent Duplicate Imports

* Detect and skip exact duplicates via hashing

#### User Story 4.3 – Detect and Resolve Conflicts on Import

* Show differences and allow resolution:

  * Keep current, replace, or merge

#### User Story 4.4 – Preserve Edited Data

* Flag and protect edited sessions from overwrite

#### User Story 4.5 – Re-Import Flexibility and Logging

* Idempotent import
* Track and display import history with results

---

Next sections will cover:

* Data model & API contracts
* UI/UX wireframes
* Milestones & timelines
* Risk & dependency analysis

(TBD)
