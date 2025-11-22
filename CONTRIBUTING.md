# Contributing to Zimmerman-Ginsberg Wedding 2026 Planning

**Document Version:** 1.0.0
**Created By:** claude-sonnet-4-5-20250929
**Created Date:** 2025-11-22
**Last Updated:** 2025-11-22

---

## Table of Contents

- [Overview](#overview)
- [Metadata Requirements](#metadata-requirements)
- [CSV Update Guidelines](#csv-update-guidelines)
- [Git Workflow](#git-workflow)
- [Data Standards](#data-standards)
- [Commit Message Convention](#commit-message-convention)
- [File-Specific Guidelines](#file-specific-guidelines)
- [Review Process](#review-process)

---

## Overview

This document provides guidelines for updating the wedding planning repository. Whether you're Ryan, Jordyn, or an AI assistant, following these standards ensures data quality, traceability, and collaboration.

**Core Principles:**

1. **Metadata First:** Every change must include who, when, and why
2. **Git Always:** All changes tracked via version control
3. **Data Integrity:** Maintain consistent formats and validation
4. **Transparency:** Clear commit messages and documentation
5. **Privacy:** Never commit sensitive personal data to shared repositories

---

## Metadata Requirements

### For AI Model Contributions

Every file created or modified by an AI model MUST include:

```csv
# File: <filename>
# Created By: <model-id>
# Created Date: <YYYY-MM-DD>
# Last Modified By: <model-id>
# Last Modified Date: <YYYY-MM-DD HH:MM:SS TZ>
# Description: <purpose of this file>
```

**Example:**

```csv
# File: wedding_guest_list.csv
# Created By: claude-sonnet-4-5-20250929
# Created Date: 2025-11-22
# Last Modified By: claude-sonnet-4-5-20250929
# Last Modified Date: 2025-11-22 14:30:00 UTC
# Description: Master guest tracking list with RSVP and attendance data
```

### For Human Contributions

Manual updates should include:

```csv
# Last Modified By: <Your Name>
# Last Modified Date: <YYYY-MM-DD>
# Modification: <brief description>
```

**Example:**

```csv
# Last Modified By: Ryan Zimmerman
# Last Modified Date: 2025-11-22
# Modification: Added 5 guests from college friend group
```

---

## CSV Update Guidelines

### 1. Guest List Updates

**File:** `wedding_guest_list.csv`

**When updating:**

- Always increment `Guest_ID` sequentially
- Set `Guest_Side` to exactly: `Jordyn`, `Ryan`, or `Both`
- Use `Number_Adults` and `Number_Children` (never blank, use 0)
- Update `Last_Modified Date` in metadata header
- Validate email addresses (basic format check)
- Use consistent date format: `YYYY-MM-DD`

**Valid Status Values:**

- `Invite_Status`: `Not Sent`, `Sent`, `Bounced`
- `Attending_Status`: `Pending`, `Yes`, `No`, `Maybe`
- `RSVP_Received`: `Yes`, `No`
- Event attendance: `Yes`, `No`
- `Thank_You_Sent`: `Yes`, `No`, `N/A`

**Example Row:**

```csv
6,Sarah,Johnson,Jordyn,College Friend,123 Main St,Boston,MA,02101,sarah@email.com,555-1234,Sent,Yes,Yes,Yes,2,0,,Vegetarian,Salmon,No,Yes,Yes,Yes,No,5,No,,No,Close friend from college
```

### 2. Budget Tracker Updates

**File:** `wedding_budget_tracker.csv`

**Rules:**

- Keep `Estimated_Cost` as original estimate (don't change retroactively)
- Update `Actual_Cost` only when final price confirmed
- Set `Deposit_Amount` to exact amount paid
- Use ISO date format for `Deposit_Paid_Date` and `Final_Payment_Date`
- Priority: `High`, `Medium`, or `Low` only
- Contract_Signed: `Yes`, `No`, `Pending`, `N/A`

**Recalculations:**

After updates, manually verify:

- Total Estimated Budget = SUM(Estimated_Cost)
- Total Spent = SUM(Actual_Cost)
- Total Deposits Paid = SUM(Deposit_Amount where Deposit_Paid_Date is not empty)
- Balance Due = Actual_Cost - Deposit_Amount

### 3. Vendor Tracker Updates

**File:** `wedding_vendor_tracker.csv`

**Status Values:**

- `Contract_Status`: `Not Contacted`, `Contacted`, `Quoted`, `Negotiating`, `Booked`, `Declined`, `Cancelled`
- `Decision_Status`: `Research`, `Contacted`, `Under Consideration`, `Booked`, `Rejected`, `Backup`

**Required Fields:**

- Must have: `Vendor_Category`, `Vendor_Name`
- Should have: `Contact_Person`, `Email` OR `Phone`
- Nice to have: `Website`, `Rating`, `Pros`, `Cons`

**Rating Scale:** 1-5 stars (use: `1`, `2`, `3`, `4`, `5`)

### 4. Metrics Summary Updates

**File:** `wedding_metrics_summary.csv`

**Update Frequency:**

- Guest Count metrics: After every guest list change
- Budget metrics: Weekly or after significant expense
- Vendor metrics: After vendor meetings/bookings
- Timeline metrics: Weekly

**Update Process:**

1. Change the `Current_Value`
2. Set `Last_Updated` to today's date (YYYY-MM-DD)
3. Add notes in `Notes` column if significant change
4. If changing target, document why in notes

---

## Git Workflow

### Basic Workflow

```bash
# 1. Check current status
git status

# 2. Review what changed
git diff wedding_guest_list.csv

# 3. Add specific files
git add wedding_guest_list.csv
git add wedding_metrics_summary.csv

# 4. Commit with descriptive message
git commit -m "feat(guests): Add 5 guests from Ryan's side, update metrics"

# 5. Push to remote (if configured)
git push origin main
```

### Before Making Changes

```bash
# Pull latest changes
git pull origin main

# Create a backup (optional)
cp wedding_guest_list.csv wedding_guest_list.csv.backup
```

### After Making Changes

```bash
# Verify your changes
git diff

# Check what files changed
git status

# Review the changes in detail
git diff --stat
```

---

## Data Standards

### Date & Time Formats

- **Dates:** `YYYY-MM-DD` (e.g., `2025-11-22`)
- **Timestamps:** `YYYY-MM-DD HH:MM:SS TZ` (e.g., `2025-11-22 14:30:00 UTC`)
- **Never use:** `MM/DD/YYYY`, `DD/MM/YYYY`, or other ambiguous formats

### Text Standards

- **Names:** Proper case (e.g., `John Smith`, not `JOHN SMITH` or `john smith`)
- **States:** Two-letter abbreviations (e.g., `MA`, `CA`, `NY`)
- **Phone:** Consistent format `555-1234` or `(555) 555-1234`
- **Email:** Lowercase (e.g., `john@example.com`)

### Currency

- **Format:** No currency symbols in CSV, numbers only
- **Example:** `15000` not `$15,000` or `15,000.00`
- Decimals allowed: `15000.50`

### Boolean Values

Use consistent values:

- `Yes` / `No` (preferred)
- `True` / `False` (acceptable for programmatic fields)
- Never use: `Y/N`, `1/0`, `yes/no`, `TRUE/FALSE`

---

## Commit Message Convention

Follow **Conventional Commits** specification:

### Format

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### Types

- `feat`: New data or functionality added
- `fix`: Correcting errors in data
- `data`: General data updates (RSVPs, metrics)
- `docs`: Documentation changes only
- `refactor`: Restructuring without data changes
- `chore`: Maintenance, file moves, etc.

### Scopes

- `guests`: Guest list changes
- `budget`: Budget tracker changes
- `vendors`: Vendor tracker changes
- `metrics`: Metrics summary changes
- `docs`: Documentation updates
- `venue`: Venue-related changes

### Examples

**Good Commit Messages:**

```bash
feat(guests): Add 8 guests from Jordyn's family side
fix(budget): Correct venue deposit from $5000 to $5500
data(guests): Update 12 RSVPs from pending to confirmed
docs(readme): Add section on budget calculation formulas
feat(vendors): Add photographer and videographer contacts
data(metrics): Weekly metrics update - 45 total guests now
```

**Bad Commit Messages:**

```bash
update stuff
fixed things
changes
added data
wip
```

### Commit Body (Optional)

For significant changes, add detail:

```bash
feat(guests): Add 15 guests from Ryan's extended family

Added aunts, uncles, and cousins from Ryan's mother's side.
Updated metrics summary to reflect new headcount.
Current total: 48 adults + 7 children = 55 total guests.

Closes #12
```

---

## File-Specific Guidelines

### wedding_guest_list.csv

**Before editing:**

```bash
# Count current guests
wc -l wedding_guest_list.csv

# Check for duplicates
sort -t, -k2,3 wedding_guest_list.csv | uniq -d
```

**After editing:**

- Verify no duplicate Guest_IDs
- Check that all emails are valid format
- Confirm Number_Adults + Number_Children sums correctly
- Update wedding_metrics_summary.csv with new counts

### wedding_budget_tracker.csv

**Validation checklist:**

- [ ] All costs are numeric (no $ symbols)
- [ ] Deposit <= Actual_Cost (if both populated)
- [ ] Dates are ISO format YYYY-MM-DD
- [ ] Priority is High/Medium/Low only
- [ ] Update metrics summary Total Budget if Estimated_Cost changed

### wedding_vendor_tracker.csv

**Before adding vendor:**

- Research and get at least email OR phone
- Set Contract_Status to "Not Contacted" initially
- Leave Quote_Amount empty until received

**After booking vendor:**

- Set Contract_Status to "Booked"
- Set Decision_Status to "Booked"
- Add entry in budget_tracker.csv
- Update metrics: Vendors Booked count

### wedding_metrics_summary.csv

**Update triggers:**

| Trigger | Metrics to Update |
|---------|-------------------|
| Guest added/removed | Total Invited, Total Combined, Guest counts by side |
| RSVP received | RSVP Yes/No counts, Pending RSVPs, Final Headcount |
| Expense paid | Total Spent, Remaining Budget, Cost Per Guest |
| Vendor booked | Vendors Booked, Contracts Signed |
| Date milestone | Days Until Wedding, Timeline status |

---

## Review Process

### Self-Review Checklist

Before committing changes:

- [ ] Metadata header updated with your name/model and date
- [ ] All new data follows format standards (dates, status values)
- [ ] Related metrics updated (e.g., guest count → metrics summary)
- [ ] No sensitive data (full SSNs, credit cards) committed
- [ ] Commit message follows convention
- [ ] Changes match what commit message describes

### Data Validation

Run basic checks:

```bash
# Check for blank required fields in guest list
grep -E "^[0-9]+,,,|,,,," wedding_guest_list.csv

# Verify all dates are ISO format
grep -v -E "[0-9]{4}-[0-9]{2}-[0-9]{2}" wedding_guest_list.csv

# Count total guests
tail -n +2 wedding_guest_list.csv | wc -l
```

### Collaborative Review

For major changes:

1. Create descriptive commit message
2. Push to repository
3. Notify partner: "Updated guest list with your family members"
4. Allow 24h for review
5. Discuss any questions or corrections

---

## Common Workflows

### Adding New Guests

```bash
# 1. Open guest list CSV
# 2. Add new row(s) with sequential Guest_ID
# 3. Fill required fields: First_Name, Last_Name, Guest_Side
# 4. Set Number_Adults and Number_Children
# 5. Set Attending_Status to "Pending"
# 6. Update metadata header with date
# 7. Save file
# 8. Update wedding_metrics_summary.csv
# 9. Git add, commit, push

git add wedding_guest_list.csv wedding_metrics_summary.csv
git commit -m "feat(guests): Add 5 guests from Ryan's college friends

Updated metrics:
- Ryan's side: 20 → 25 guests
- Total invited: 55 → 60 guests"
git push
```

### Recording Vendor Payment

```bash
# 1. Open budget_tracker.csv
# 2. Find vendor row
# 3. Update Deposit_Amount or Actual_Cost
# 4. Add Deposit_Paid_Date or Final_Payment_Date
# 5. Set Payment_Method (e.g., "Credit Card", "Check", "Venmo")
# 6. Update metadata header
# 7. Save file
# 8. Update wedding_metrics_summary.csv Total Spent
# 9. Commit

git add wedding_budget_tracker.csv wedding_metrics_summary.csv
git commit -m "data(budget): Record $5000 venue deposit payment

Paid via check on 2025-11-22
Updated total spent: $0 → $5000"
git push
```

### Weekly Metrics Update

```bash
# 1. Review all data files for changes
# 2. Open wedding_metrics_summary.csv
# 3. Update Current_Value for changed metrics
# 4. Set Last_Updated to today
# 5. Add notes for significant changes
# 6. Update metadata header
# 7. Commit

git add wedding_metrics_summary.csv
git commit -m "data(metrics): Weekly metrics update 2025-11-22

Key changes:
- Total RSVP Yes: 30 → 42
- Vendors booked: 2 → 4
- Budget spent: 45% → 52%"
git push
```

---

## Privacy & Security

### Never Commit

- Full Social Security Numbers
- Credit card numbers
- Bank account details
- Passwords or API keys
- Highly sensitive personal information

### Handling Sensitive Data

If you need to track sensitive information:

1. Create a file with `_PRIVATE` suffix (e.g., `guest_addresses_PRIVATE.csv`)
2. It's already in .gitignore and won't be committed
3. Store securely, share only via encrypted methods

### Recommended Practices

- Use private GitHub repository (not public)
- Enable two-factor authentication
- Don't share repository access with vendors
- For shared spreadsheets, export/import CSVs rather than direct editing

---

## Questions or Issues

**For Git questions:**

- Check: `git status`, `git log`, `git diff`
- Undo last commit: `git reset --soft HEAD~1`
- Discard changes: `git checkout -- <file>`

**For data questions:**

- Refer to README.md for file structure
- Check CHANGELOG.md for recent changes
- Review this CONTRIBUTING.md for standards

**For AI assistants:**

- Always include your model ID in metadata
- Add timestamp in UTC
- Reference this document in prompts
- Update CHANGELOG.md for significant changes

---

**Document Maintained By:** claude-sonnet-4-5-20250929
**Last Updated:** 2025-11-22
**Version:** 1.0.0
