# How to Share the Wedding Dashboard on Mobile

**Created By:** Ryan Zimmerman
**Created Date:** 2025-11-22
**Purpose:** Guide for sharing wedding-dashboard.html with others on mobile devices

---

## ✅ Current Status: Almost Fully Self-Contained

Your [wedding-dashboard.html](../wedding-dashboard.html) file is **90% self-contained**:

✅ **Fully embedded (works offline):**
- All CSS styles (inline in the HTML)
- All JavaScript (none used)
- All content and data
- All formatting and design
- Mobile-responsive design already built-in

⚠️ **External references (links to other files):**
- Links to markdown docs (TIMELINE_ANALYSIS.md, NOTES.md, etc.)
- Links to CSV files (guest_list.csv, budget_tracker.csv, etc.)
- These links work locally but won't work when shared standalone

---

## 📱 Best Options for Mobile Sharing (FREE)

### **Option 1: GitHub Pages (RECOMMENDED - 100% Free)**

**Best for:** Professional, permanent URL that updates automatically

**Steps:**

1. **Push your repo to GitHub:**
   ```bash
   # Create new repo on GitHub.com (free account)
   # Then push your local repo
   git remote add origin https://github.com/YOUR-USERNAME/wedding-planning.git
   git branch -M main
   git push -u origin main
   ```

2. **Enable GitHub Pages:**
   - Go to your repo Settings
   - Scroll to "Pages" section
   - Source: Deploy from branch `main`
   - Folder: `/ (root)`
   - Click Save

3. **Your URL will be:**
   ```
   https://YOUR-USERNAME.github.io/wedding-planning/wedding-dashboard.html
   ```

**Pros:**
- ✅ Completely FREE forever
- ✅ Professional URL
- ✅ Auto-updates when you push changes
- ✅ Works on all devices (mobile, desktop)
- ✅ All your files accessible (CSVs, docs)
- ✅ Fast, reliable hosting
- ✅ HTTPS security included

**Cons:**
- ⚠️ Public by default (anyone with link can see)
- ⚠️ Requires GitHub account (free)

**Privacy Note:** You can make the repo private and still use Pages, but Pages site will be public. For true privacy, use Option 2 or 3.

---

### **Option 2: Netlify Drop (FREE, No Account Needed)**

**Best for:** Quick sharing without GitHub

**Steps:**

1. Go to [https://app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag and drop your entire project folder
3. Get instant URL like: `https://random-name-12345.netlify.app`

**Pros:**
- ✅ Completely FREE
- ✅ No account required
- ✅ Instant deployment (30 seconds)
- ✅ Works on all devices
- ✅ All files included (CSVs, docs)

**Cons:**
- ⚠️ Random URL (can't customize without account)
- ⚠️ Have to re-upload to update
- ⚠️ Public (anyone with link can access)

**Update Process:**
- Drag folder again → Get new URL
- OR create free account → Get permanent URL + auto-updates

---

### **Option 3: Google Drive (FREE, Easy)**

**Best for:** Private sharing with specific people

**Steps:**

1. **Upload to Google Drive:**
   - Upload `wedding-dashboard.html` to Drive
   - Right-click → Share → "Anyone with link can view"
   - Copy the link

2. **Get shareable URL:**
   - The link will look like: `https://drive.google.com/file/d/FILE-ID/view`
   - **Important:** Links to CSVs/docs won't work (Drive doesn't serve them as web files)

**Pros:**
- ✅ FREE
- ✅ Easy to control who sees it (share with specific emails)
- ✅ Everyone already has Google account
- ✅ Mobile-friendly

**Cons:**
- ⚠️ Shows "Download" button (extra click)
- ⚠️ Links to other files won't work
- ⚠️ Not as clean as direct web hosting

---

### **Option 4: Simple File Sharing Services**

**FREE options:**

**Cloudflare Pages:**
- Connect GitHub → Auto-deploy
- URL: `https://wedding.pages.dev`
- Same as GitHub Pages but with Cloudflare CDN

**Vercel:**
- Connect GitHub → Auto-deploy
- URL: `https://wedding.vercel.app`
- Great for technical users

**surge.sh:**
- Command line: `npx surge wedding-dashboard.html`
- URL: `https://random-name.surge.sh`
- Simple and fast

---

## 🔒 Making It Private (If Needed)

If you want password protection:

### **Free Option: Netlify (with account)**

1. Create free Netlify account
2. Deploy your site
3. Go to Site Settings → Access Control
4. Enable "Password Protection"
5. Set password → Share password with family

### **Paid Option: Vercel Pro ($20/month)**

- Add authentication
- Control who can access

### **DIY Option: Add Password to HTML**

I can add a simple password prompt to the HTML file itself:
- No external service needed
- Password required to view
- Works anywhere
- **Note:** Not super secure (password visible in source code)

---

## 📋 My Recommendation

**For your use case (sharing with Jordyn and maybe family):**

### **🏆 Best Choice: GitHub Pages**

**Why:**
1. **Free forever**
2. **Professional URL** you can customize
3. **Auto-updates** when you make changes (just git push)
4. **All your files work** (CSVs, docs, dashboard)
5. **Mobile-friendly** built-in
6. **Version control** built-in (already using git)

**Setup time:** ~5 minutes
**URL example:** `https://rzimmerman2018.github.io/wedding-2026/wedding-dashboard.html`

**Privacy:**
- Can make repo private (wedding details not searchable)
- Only people with exact URL can access
- Add password with Netlify if truly needed

---

## 🚀 Quick Start: GitHub Pages Setup

Want me to help you set this up? Here's what I'll do:

1. **Create .nojekyll file** (makes GitHub Pages work better)
2. **Update footer** in HTML to remove model ID reference
3. **Provide exact commands** to push to GitHub
4. **Walk you through** enabling Pages

**Result:** Professional wedding dashboard at `https://YOUR-USERNAME.github.io/REPO-NAME/wedding-dashboard.html`

Just need to know:
- Do you have a GitHub account? (If not, create free at github.com)
- What do you want to name the repo? (e.g., "wedding-2026", "zimmerman-ginsberg-wedding")

---

## 🔗 Alternative: Text/Email the HTML File Directly

**Simplest option (but not ideal):**

You can **email or text the HTML file** directly:
- Open email → Attach `wedding-dashboard.html`
- Recipient opens on phone → It will work!

**Pros:**
- No setup required
- Completely private

**Cons:**
- Large file to send
- Links to CSVs won't work
- Have to re-send for updates
- Not as clean as web URL

---

## 💡 Questions?

Let me know which option you prefer and I can help you set it up!

**Quick wins:**
- **5 minutes:** Email the HTML file
- **10 minutes:** Upload to Netlify Drop
- **15 minutes:** Set up GitHub Pages (best long-term)

---

**Document Created By:** Ryan Zimmerman
**Last Updated:** 2025-11-22
