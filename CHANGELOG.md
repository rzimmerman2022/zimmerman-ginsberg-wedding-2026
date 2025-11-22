# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [Unreleased]

### To Do
- Set wedding date (month/day in 2026)
- Finalize venue selection
- Complete guest list with actual names
- Establish total budget

---

## [0.2.3] - 2025-11-22 09:41:46 UTC
**Author:** Ryan Zimmerman

### Added
- Created `dashboard.html`, a modern single-page visual dashboard with metric cards, timeline focus, vendor snapshot (including Isabella's), budget notes, and next actions, using current snapshot data and placeholder countdown.

---

## [0.2.2] - 2025-11-22 09:41:46 UTC
**Author:** Ryan Zimmerman

### Added
- Added November 2026 timeline anchor (placeholder date, months/days countdown, RSVP target) and venue capacity target rows in `wedding_metrics_summary.csv`.
- Extended `wedding_metrics_registry.csv` with anchor-date metrics, RSVP target, and capacity target definitions.
- Inserted placeholder venue candidate rows and updated metadata in `wedding_vendor_tracker.csv`.
- Added budget-target notes for key categories and updated metadata in `wedding_budget_tracker.csv`.

---

## [0.2.1] - 2025-11-22 09:24:18 UTC
**Author:** Ryan Zimmerman

### Added
- Logged Isabella's Kitchen as a rehearsal-dinner restaurant option in `wedding_vendor_tracker.csv` (food/drinks only, patio views, Scottsdale, travel time TBD).

---

## [0.2.0] - 2025-11-22
**Author:** Ryan Zimmerman

### Added - Version Control & Documentation Enhancement

**Version Control:**
- Initialized Git repository (main branch)
- Created `.gitignore` with comprehensive exclusions for:
  - Sensitive personal data (*_PRIVATE.csv, *_SENSITIVE.csv)
  - Vendor contracts and actual expenses
  - macOS system files (.DS_Store, ._*)
  - Editor temporary files (~$*.xlsx, *.tmp)
  - Development files (.vscode, .env, node_modules)

**Documentation:**
- Expanded CHANGELOG.md with:
  - Keep a Changelog format compliance
  - Semantic Versioning adherence
  - Multi-model session tracking
  - Metadata standards for all entries
  - Comprehensive change categorization
- Created CONTRIBUTING.md (pending)
- Established documentation structure (pending)

**Data Files - Initial CSV Creation:**
- `wedding_guest_list.csv` (31 columns)
  - Guest identification (ID, names, side, relationship)
  - Contact information (address, email, phone)
  - Invitation tracking (save the date, invitation, RSVP)
  - Attendance details (adult/child counts, plus-ones)
  - Event tracking (rehearsal, welcome, ceremony, reception, after-party)
  - Logistics (dietary restrictions, meal choice, table number)
  - Gift tracking (received, description, thank you sent)
  - Status: Needs metadata header row

- `wedding_budget_tracker.csv` (14 columns, 27 categories)
  - Pre-populated categories: Venue, Catering, Photography, Videography, Florist, DJ/Band, Attire, Invitations, Decorations, Cake, Transportation, Hotel, Hair/Makeup, Planner, Musicians, Favors, Events, Honeymoon, Rings, License, Insurance, Misc
  - Fields: Estimated vs Actual costs, Deposits, Payment tracking, Priority
  - Status: Needs metadata header row

- `wedding_vendor_tracker.csv` (19 columns, 13 vendor types)
  - Pre-populated types: Venue, Catering, Photography, Videography, Florist, DJ/Band, Hair/Makeup, Planner, Transportation, Bakery, Officiant, Invitations, Rentals
  - Fields: Contact details, quotes, contract status, decision tracking
  - Status: Needs metadata header row

- `wedding_metrics_summary.csv` (6 columns, 37 metrics)
  - Categories: Guest Count, Budget, Venue, Timeline, Vendors, Tasks
  - Pre-populated with initial values:
    - Jordyn's side: 30 minimum
    - Ryan's side: 15-20 estimated
    - Combined: 28 adults + 5 children = 33 total
  - Status: Needs metadata header row

### Changed
- N/A (additive changes only)

### Security
- Implemented gitignore protection for sensitive files
- Established privacy standards for personal data

---

## [0.1.0] - 2025-11-22 09:19:18 UTC
**Author:** Ryan Zimmerman

### Added
- Created project README with structure, data standards, and operational guidance
- Introduced metric registry CSV concept to formalize definitions and ownership
- Documented version-control expectations (metadata, commit cadence)

---

## Metadata Standards

Every changelog entry MUST include:
- **Version:** Semantic version number [MAJOR.MINOR.PATCH]
- **Date:** ISO 8601 format (YYYY-MM-DD or YYYY-MM-DD HH:MM:SS TZ)
- **Author:** Author name (Ryan Zimmerman, Jordyn, etc.)
- **Category:** Added, Changed, Deprecated, Removed, Fixed, Security
- **Description:** Clear, concise description of changes
- **Impact:** (optional) Effect on metrics, budget, timeline, etc.

## Change Categories

- **Added:** New features, files, or functionality
- **Changed:** Modifications to existing functionality
- **Deprecated:** Soon-to-be removed features
- **Removed:** Deleted features or files
- **Fixed:** Bug fixes or data corrections
- **Security:** Security-related changes
