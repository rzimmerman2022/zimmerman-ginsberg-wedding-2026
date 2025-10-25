# Quick Start Guide

Welcome to your wedding planning repository! This guide will help you get started using this system effectively.

---

## First Steps

### 1. Review the README
Start by reading [README.md](README.md) to understand the project structure and current phase.

### 2. Set Your Budget
Open [docs/budget-breakdown.md](docs/budget-breakdown.md) and:
- Fill in your total budget
- Adjust the percentage allocations to your priorities
- Use this as your financial north star

### 3. Review the Timeline
Check [docs/timeline.md](docs/timeline.md) to:
- Understand what phase you're in (currently 12-18 months before)
- See what tasks should be happening now
- Plan ahead for upcoming milestones

### 4. Start the Master Checklist
Open [planning-tools/checklists/master-checklist.md](planning-tools/checklists/master-checklist.md):
- Begin checking off completed items
- Focus on "12-18 Months Before" section first
- Mark off items as you complete them

---

## Key Initial Tasks (Do These First)

### Task 1: Set Budget (This Week)
- [ ] Discuss total budget with Jordyn
- [ ] Determine who's contributing what
- [ ] Fill in budget amounts in `docs/budget-breakdown.md`
- [ ] Commit changes to git

### Task 2: Create Guest List Draft (This Week)
- [ ] Each person creates their preliminary list
- [ ] Combine lists
- [ ] Get rough headcount
- [ ] Create file: `guests/draft-guest-list.xlsx`

### Task 3: Start Venue Research (This Week)
- [ ] Research Arizona wedding venues
- [ ] Narrow to top 5 venues
- [ ] Use venue comparison template for each
- [ ] Schedule venue tours

### Task 4: Choose Wedding Party (This Month)
- [ ] Decide on wedding party size
- [ ] Choose bridesmaids and groomsmen
- [ ] Ask them to participate
- [ ] Record decisions in `docs/decision-log.md`

---

## How to Use This Repository

### Daily/Weekly Planning
1. Review the master checklist for current phase tasks
2. Update documents as decisions are made
3. Commit changes to git regularly
4. Track expenses in budget document

### Vendor Research
1. Copy the appropriate comparison template from `/research/[vendor-type]/`
2. Fill out template for each vendor you meet
3. Save as `vendor-name-comparison.md` in same folder
4. Compare side-by-side to make decisions

### Decision Making
1. When you make a major decision, document it in `docs/decision-log.md`
2. Record the date, what was decided, why, and impact
3. This helps maintain consistency and remember reasoning

### Budget Tracking
1. Update `docs/budget-breakdown.md` when you:
   - Book a vendor (move from estimate to actual)
   - Make a deposit
   - Pay a final payment
2. Review budget monthly to stay on track

---

## Git Workflow (Version Control)

### Basic Commands

**See what's changed:**
```bash
git status
```

**Add changes:**
```bash
git add .
```

**Commit changes:**
```bash
git commit -m "Describe what you changed"
```

**View history:**
```bash
git log --oneline
```

### Recommended Commit Frequency
- After booking each major vendor
- When completing a section of planning
- After major budget updates
- Weekly for ongoing progress

### Sample Commit Messages
- "Booked venue: Desert Botanical Garden"
- "Updated budget after photographer booking"
- "Added three venue comparisons"
- "Finalized guest list at 120 people"
- "Completed ceremony music selection"

---

## Vendor Research Workflow

### 1. Initial Research
- Use `/docs/vendor-requirements.md` to understand what to look for
- Search online, ask friends, check WeddingWire/The Knot
- Create shortlist of 3-5 vendors per category

### 2. Vendor Meetings
- Copy the appropriate comparison template
- Bring template to meeting or fill out after
- Take notes on pros, cons, and gut feeling

### 3. Comparison & Decision
- Review all completed comparison templates side-by-side
- Consider: quality, value, personality fit, availability
- Record final decision in `docs/decision-log.md`

### 4. Booking
- Review contract thoroughly
- Sign contract
- Pay deposit
- Update budget tracker
- Save contract in `/contracts/vendor-agreements/`
- Commit to git

---

## File Organization Tips

### Naming Conventions
- Use lowercase with hyphens: `venue-name.md`
- Include dates when relevant: `budget-2025-10.xlsx`
- Use descriptive names: `photographer-john-smith-comparison.md`

### Folder Usage
- **docs/**: Main planning documents (read these frequently)
- **research/**: Vendor comparisons and notes
- **budget/**: Financial tracking and quotes
- **guests/**: Guest list and RSVP tracking
- **contracts/**: Signed agreements (mark as -signed in filename)
- **planning-tools/**: Checklists and templates
- **inspiration/**: Photos, color palettes, design ideas

### What to Commit to Git
✅ Planning documents  
✅ Vendor comparison templates (completed)  
✅ Timelines and checklists  
✅ Decision logs  
✅ Budget templates  

❌ Signed contracts with signatures  
❌ Guest addresses and phone numbers  
❌ Credit card info or bank details  
❌ Large image files  
❌ Vendor passwords or credentials  

---

## Staying Organized

### Weekly Planning Session (30 minutes)
1. Review master checklist
2. Check off completed items
3. Identify 3-5 tasks for the upcoming week
4. Update budget if any expenses occurred
5. Commit changes to git

### Monthly Review (1-2 hours)
1. Review timeline - are you on track?
2. Reconcile budget - where do you stand?
3. Evaluate vendor booking progress
4. Update decision log with recent choices
5. Plan next month's priorities

### Before Bed Each Night (5 minutes)
- Check off any completed tasks
- Note any wedding-related expenses
- Set reminder for tomorrow's wedding tasks

---

## Tips for Success

### Communication
- **Be a team**: Make big decisions together
- **Regular check-ins**: Set aside dedicated planning time
- **Divide tasks**: Play to each other's strengths
- **Stay aligned**: Review the decision log together regularly

### Budget
- **Track everything**: Every expense, no matter how small
- **Build buffer**: Aim to spend 90% of budget (10% buffer for surprises)
- **Prioritize**: Know your top 3 budget priorities
- **Question everything**: Ask vendors what's included vs. extra

### Stress Management
- **One thing at a time**: Don't try to do everything at once
- **Delegate**: Accept help from wedding party and family
- **Take breaks**: Schedule wedding-free days/weeks
- **Remember the why**: It's about marriage, not just a wedding

### Decision Making
- **Trust your gut**: If something feels off, it probably is
- **Don't settle**: This is a once-in-a-lifetime event
- **Ask questions**: No question is too small or silly
- **Get it in writing**: All agreements, changes, promises

---

## Common First-Month Questions

**Q: What should we do first?**  
A: Set budget, create guest list, and start venue research. Everything else flows from these.

**Q: How do we know if we're on track?**  
A: Check the timeline.md file for your current phase (12-18 months before). If you're completing tasks in that section, you're on track.

**Q: When should we book vendors?**  
A: Venue first (now), then photographer/caterer/florist/entertainment (9-11 months before), then everything else.

**Q: How much should we spend on [X]?**  
A: See the budget-breakdown.md percentages, but adjust based on your priorities. No wedding is exactly the same.

**Q: What if we're behind schedule?**  
A: Don't panic! Wedding planning is flexible. Focus on the must-haves (venue, caterer, photographer) and work through the rest systematically.

---

## Resources

### Websites
- **WeddingWire**: Vendor reviews and planning tools
- **The Knot**: Checklists and vendor search
- **Wedding planning subreddits**: Real advice from other couples
- **Arizona wedding blogs**: Local vendor recommendations

### Tools You Might Want
- **Google Sheets/Excel**: Budget tracking, guest list management
- **Google Drive**: Shared access to documents with Jordyn
- **Trello or Notion**: Visual task management (optional)
- **Wedding planning apps**: Alternatives to this system if preferred

---

## Getting Help

### When You Need More Templates
Copy and adapt existing templates in the `/research/` folders for new vendor types.

### When You're Overwhelmed
1. Review the master checklist
2. Pick just 3 tasks for this week
3. Everything else can wait
4. Consider hiring a wedding planner for support

### When You Disagree on Decisions
1. Revisit your wedding vision and priorities
2. Review budget constraints
3. Find compromises
4. Remember: small details won't matter on the day

---

## Next Actions

**Right Now:**
- [ ] Read through this guide completely
- [ ] Review the README
- [ ] Skim the master timeline
- [ ] Open the master checklist

**This Week:**
- [ ] Set overall budget with Jordyn
- [ ] Create draft guest list
- [ ] Start Arizona venue research
- [ ] Schedule your first weekly planning session

**This Month:**
- [ ] Tour top 5 venues
- [ ] Make venue decision
- [ ] Book venue
- [ ] Choose wedding party
- [ ] Research top vendors (photographer, caterer, etc.)

---

## Congratulations!

You're organized, you have a system, and you're ready to plan an amazing wedding. Take it one step at a time, enjoy the process, and remember: this is about celebrating your love and commitment to each other.

**Happy Planning!** 🎉💍

---

**Questions or need to customize this system?**  
Feel free to modify any documents to fit your specific needs. This is YOUR wedding planning system.

**Last Updated:** October 2025
