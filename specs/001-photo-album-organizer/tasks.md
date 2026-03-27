# Tasks: Photo Album Organizer

**Input**: Design documents from `/specs/001-photo-album-organizer/`
**Prerequisites**: plan.md (required), spec.md (required for user stories)

## Phase 1: Setup (Shared Infrastructure)

- [ ] T001 Create project structure in src/ and public/ per Vite standards
- [ ] T002 Initialize Vite project with vanilla JS template
- [ ] T003 [P] Add minimal SQLite WASM/JS library (e.g., sql.js) to project
- [ ] T004 [P] Configure basic HTML, CSS, and JS linting

## Phase 2: Foundational (Blocking Prerequisites)

- [ ] T005 Implement SQLite database schema for albums and photos in src/db/schema.js
- [ ] T006 [P] Implement local persistence for SQLite database (IndexedDB or file download) in src/db/persist.js
- [ ] T007 [P] Create base UI shell (main page, album view, tile grid) in src/

## Phase 3: User Story 1 (P1) - Organize Photos into Albums

- [ ] T008 [US1] Implement album creation, deletion, and listing in src/albums.js
- [ ] T009 [US1] Implement grouping of albums by date in src/albums.js
- [ ] T010 [US1] Implement adding/removing photos to albums in src/photos.js
- [ ] T011 [US1] Display albums grouped by date on main page in src/pages/main.js
- [ ] T012 [US1] [P] Write unit tests for album and photo CRUD in tests/unit/albums.test.js

## Phase 4: User Story 2 (P2) - Reorganize Albums via Drag-and-Drop

- [ ] T013 [US2] Implement drag-and-drop reordering of albums in src/pages/main.js
- [ ] T014 [US2] Persist album order in SQLite and update UI in src/albums.js
- [ ] T015 [US2] [P] Write unit/integration tests for drag-and-drop and order persistence in tests/integration/dragdrop.test.js

## Phase 5: User Story 3 (P3) - Preview Photos in Tile Interface

- [ ] T016 [US3] Implement tile-based photo preview in album view in src/pages/album.js
- [ ] T017 [US3] Implement lazy loading/pagination for large albums in src/pages/album.js
- [ ] T018 [US3] [P] Write unit/integration tests for tile preview and performance in tests/integration/tiles.test.js

## Phase 6: Polish & Cross-Cutting Concerns

- [ ] T019 Handle empty album state and duplicate photo uploads in src/albums.js
- [ ] T020 [P] Add accessibility and keyboard navigation to UI in src/
- [ ] T021 [P] Add user data export/import (SQLite file) in src/db/export.js
- [ ] T022 [P] Finalize documentation and quickstart in specs/001-photo-album-organizer/quickstart.md

## Dependencies

- Phase 1 → Phase 2 → US1 (P1) → US2 (P2) → US3 (P3) → Polish

## Parallel Execution Examples

- T003, T004, T006, T007 can be done in parallel after T002
- T012, T015, T018, T020, T021, T022 can be done in parallel after their respective features

## Implementation Strategy

- MVP: Complete all P1 (User Story 1) tasks for a working local album/photo organizer
- Incrementally deliver P2, P3, and polish phases

## Format validation: All tasks follow checklist format with ID, [P] for parallel, [USx] for user story, and file paths
