# ADR 001: Flatten Directory Structure to Root

**Date:** 2025-10-25
**Status:** Accepted
**Decision Maker:** Ryan Zimmerman
**Model:** claude-sonnet-4.5-20250929
**Session ID:** flatten-restructure-001

---

## Context

The wedding planning repository was initially created by a previous AI model with an organized subdirectory structure:
- `docs/` - Core planning documents
- `research/` - Vendor research and templates
- `guests/` - Guest management files
- `budget/` - Budget tracking
- `contracts/` - Vendor agreements
- `planning-tools/` - Checklists and templates
- `inspiration/` - Design references

This structure followed software engineering best practices for organization but created navigation complexity for the primary users (Ryan and Jordyn) who may not be familiar with nested directory structures.

---

## Decision

**Flatten all files to the root directory, eliminating all subdirectories except for ADR/documentation infrastructure.**

All wedding planning content files will reside in the root directory with no nested folders.

---

## Rationale

### Why Flatten?
1. **Simplicity for Non-Technical Users**: Jordyn and Ryan need immediate access to files without navigating folder hierarchies
2. **Reduced Cognitive Load**: All files visible in one location, no mental mapping of "where did I put that?"
3. **Mobile/Cloud Accessibility**: Easier to access files from phone/tablet file browsers
4. **User Preference**: Ryan explicitly requested flattening after seeing the original structure

### Trade-offs Accepted
1. **Less Organization**: Root directory will have 15+ files, harder to visually scan
2. **No Logical Grouping**: Related files (all budget docs, all vendor docs) not physically grouped
3. **Scalability Issues**: As project grows, flat structure becomes unwieldy
4. **Goes Against Software Best Practices**: Standard project organization principles sacrificed

---

## Alternatives Considered

### Alternative 1: Keep Original Subdirectory Structure
**Pros:**
- Better organization
- Scalable as project grows
- Follows best practices
- Logical grouping of related files

**Cons:**
- More complex navigation
- Requires understanding of folder structure
- Additional clicks to access files
- May be intimidating for non-technical users

**Rejected because:** User explicitly preferred flat structure

### Alternative 2: Hybrid Approach
Create only 2-3 top-level folders:
- `planning/` - All planning docs
- `research/` - All research/templates
- Root - Just README and QUICK-START

**Pros:**
- Balances organization with simplicity
- Only one level of nesting
- Still manageable for non-technical users

**Cons:**
- Still requires some folder navigation
- Doesn't fully address user preference

**Rejected because:** User wanted complete flattening

### Alternative 3: Use Naming Prefixes Instead of Folders
Keep flat structure but use systematic prefixes:
- `PLAN_timeline.md`
- `PLAN_budget-breakdown.md`
- `RESEARCH_venue-comparison.md`
- `TEMPLATE_guest-list.md`

**Pros:**
- Files logically grouped by name sorting
- Completely flat but organized
- Easy to find related files

**Cons:**
- Longer file names
- Prefixes may be confusing
- Additional typing required

**Rejected because:** Not explicitly requested, can be implemented later if needed

---

## Implementation

### Files Moved
```bash
docs/budget-breakdown.md → budget-breakdown.md
docs/decision-log.md → decision-log.md
docs/timeline.md → timeline.md
docs/vendor-requirements.md → vendor-requirements.md
guests/guest-list-template.md → guest-list-template.md
planning-tools/checklists/master-checklist.md → master-checklist.md
research/photographers/photographer-comparison-template.md → photographer-comparison-template.md
research/venues/venue-comparison-template.md → venue-comparison-template.md
```

### Directories Removed
- `budget/`
- `contracts/`
- `docs/`
- `guests/`
- `inspiration/`
- `planning-tools/`
- `research/`

### Directories Preserved/Created
- `docs/decisions/` - ADR documentation (infrastructure)
- `docs/handoffs/` - Session handoff documents (infrastructure)
- `state/` - Session state files (infrastructure)
- `outputs/` - Run outputs (infrastructure)

---

## Consequences

### Positive
- **Immediate:** All files accessible in single directory view
- **User Experience:** Reduced friction for accessing wedding planning documents
- **Simplicity:** No learning curve for directory navigation
- **Mobile Friendly:** Easier to browse on phone/tablet

### Negative
- **Scalability:** Will become cluttered as more files are added
- **Organization:** No physical grouping of related documents
- **Reference Breakage:** All internal file path references need updating
- **Future Migration Risk:** May need to reorganize later if complexity grows

### Neutral
- **Git History:** All files tracked as moves, history preserved
- **ADR Infrastructure:** Separate docs folder for project infrastructure doesn't conflict with wedding planning files
- **Reversibility:** Can re-organize into folders later if needed (moderate effort)

---

## Follow-Up Actions Required

1. ✅ Move all files to root directory
2. ⏳ Update all file path references in README.md
3. ⏳ Update all file path references in QUICK-START.md
4. ⏳ Update all file path references in COMPREHENSIVE-VENUE-ANALYSIS.md
5. ⏳ Update all file path references in VENUE-RESEARCH-TLDR.md
6. ⏳ Update README.md repository structure section
7. ⏳ Commit changes with comprehensive message
8. ⏳ Push to GitHub

---

## Review Schedule

**Review Date:** 2026-01-25 (3 months)
**Review Criteria:**
- Has the flat structure caused confusion or problems?
- Has the root directory become too cluttered?
- Are users struggling to find specific files?
- Would re-organizing into folders improve workflow?

---

## References

- Git commit: 9c93bab ("Flatten directory structure and add venue research")
- Original structure: Git commit 39184f9 ("Add quick start guide and guest list template")
- User request: Session conversation 2025-10-25

---

**Confidence Level:** High (0.9)
**Reversibility:** Moderate (requires updating all file references again)
**Impact:** Medium (affects daily usage but not functionality)
