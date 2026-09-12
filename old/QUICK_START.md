# Quick Start Guide – Common Changes

> **Pro Tip:** Use Ctrl+F (Cmd+F on Mac) to find and replace text in `index.html`

---

## 🎯 First Things First

### 1. Open the website
Double-click `index.html` to open in your browser

### 2. Update your name
```
Find: Adithyaa Rettaikudi Gurumoorthi
Replace with: Your Name
```

### 3. Update tagline
```
Find: Robotics • Machine Learning • AI Systems
Replace with: Your Field 1 • Your Field 2 • Your Field 3
```

### 4. Add your profile photo
1. Save your photo as `profile.jpg` in the `assets/` folder
2. Find: `<img src="data:image/svg+xml,...` (around line 440)
3. Replace with: `<img src="assets/profile.jpg" alt="Your Name"`

---

## 📧 Quick Links to Update

### Email
```
Find: mailto:adithyaa.off@gmail.com
Replace with: mailto:your.email@gmail.com
```

### LinkedIn
```
Find: https://www.linkedin.com/in/adithyaa-rg
Replace with: https://www.linkedin.com/in/your-profile
```

### GitHub
```
Find: https://github.com/adithyaa-rg
Replace with: https://github.com/your-username
```

### Google Scholar
```
Find: https://scholar.google.com/citations?user=YOUR_ID
Replace with: Your actual Google Scholar URL
```

---

## 📝 Update Your Bio

Find this section (around line 455):
```html
<div class="bio-text">
    <p>My research background spans...</p>
```

Replace the entire `<p>` paragraph with your bio. Keep the formatting:
- First `<p>`: Main research interests
- Second `<p>` (with style): Current goals
- Third `<p>` (italic): Personal interests

---

## 🔬 Update Research Interests

Find: `<div id="research" class="page">` (around line 490)

Each research area follows this pattern:
```html
<div class="section">
    <div class="section-title">Research Area Name</div>
    <div class="entry">
        <p class="entry-description">
            Your description here...
        </p>
        <div class="entry-tags">
            <span class="tag">Tag1</span>
            <span class="tag">Tag2</span>
        </div>
    </div>
</div>
```

**To add a new research area:** Copy the entire `<div class="section">...</div>` block and update text.

---

## 🎨 Add a Project

Find: `<div id="projects" class="page">` (around line 530)

Look for a project card that looks like:
```html
<div class="project-card">
    <div class="project-media">
        <img src="data:image/svg+xml,..." alt="Project Name">
    </div>
    <div class="project-content">
        <div class="project-title">State-Only Offline...</div>
        <div class="project-subtitle">Research (In Progress)</div>
        <p class="project-description">...</p>
        ...
    </div>
</div>
```

### To Edit Existing Project:
1. **Title:** Change `<div class="project-title">`
2. **Role:** Change `<div class="project-subtitle">`
3. **Description:** Change `<p class="project-description">`
4. **Date:** Change first `<span>` in `<div class="project-meta">`
5. **Organization:** Change second `<span>` in `<div class="project-meta">`
6. **Image:** Replace `src="data:image/svg+xml,..."` with `src="assets/project-image.jpg"`
7. **Tags:** Update `<span class="tag">` values

### To Add New Project:
1. Copy entire `<div class="project-card">...</div>` block
2. Paste it after another project card
3. Update all content as above
4. Add image to `assets/` folder

### With Video Instead of Image:
Replace:
```html
<div class="project-media">
    <img src="...">
</div>
```

With:
```html
<div class="project-media">
    <video controls>
        <source src="assets/video.mp4" type="video/mp4">
    </video>
</div>
```

---

## 💼 Update Work Experience

Find: `<div class="section-title">Work Experience</div>` (around line 620)

Each experience entry:
```html
<div class="entry">
    <div class="entry-header">
        <div>
            <div class="entry-title">Job Title</div>
            <div class="entry-subtitle">Company, Location</div>
        </div>
        <div class="entry-time">Month Year – Month Year</div>
    </div>
    <ul class="entry-points">
        <li>Achievement 1</li>
        <li>Achievement 2</li>
    </ul>
    <div class="entry-tags">
        <span class="tag">Skill1</span>
        <span class="tag">Skill2</span>
    </div>
</div>
```

**To add entry:** Copy the entire `<div class="entry">` block and update all fields.

---

## 🎓 Update Education

Find: `<div id="education" class="page">` (around line 700)

Education cards format:
```html
<div class="education-card">
    <div class="education-degree">DEGREE TYPE</div>
    <div class="education-institution">University Name</div>
    <div class="education-details">
        <strong>Program Name</strong><br>
        <strong>CGPA/GPA:</strong> X.XX / Y.YY<br>
        <strong>Dates:</strong> Month Year – Month Year
    </div>
    <a href="documents/transcript.pdf" class="education-cta">View Transcript →</a>
</div>
```

**To update:**
1. Change degree type (e.g., "DUAL DEGREE", "BACHELOR'S", "EXCHANGE")
2. Update university name
3. Update program, CGPA, dates
4. Ensure PDF exists in `documents/` folder with correct filename

---

## 🔧 Update Skills

Find: `<div id="skills" class="page">` (around line 760)

Skill block format:
```html
<div class="skill-block">
    <div class="skill-category">Category Name</div>
    <ul class="skill-list">
        <li>Skill 1</li>
        <li>Skill 2</li>
        <li>Skill 3</li>
    </ul>
</div>
```

**To add category:** Copy entire `<div class="skill-block">` and update category name and skills.

---

## 🎨 Change Theme Color

Find the `:root` section at the top of `index.html` (around line 34):

```css
:root {
    ...
    --accent: #2563eb;          /* Change this color */
    --accent-dark: #1e40af;     /* And this one */
    ...
}
```

### Popular Color Options:
- **Blue** (current): `#2563eb` / `#1e40af`
- **Purple**: `#7c3aed` / `#6d28d9`
- **Green**: `#059669` / `#047857`
- **Red**: `#dc2626` / `#b91c1c`
- **Orange**: `#f97316` / `#ea580c`
- **Teal**: `#0891b2` / `#0e7490`

Find hex codes at: [colorhexa.com](https://colorhexa.com)

---

## 🔗 Update Document Links

On the About page, there are three document links (around line 450):

```html
<a href="documents/Academic_CV_Adithyaa.pdf" class="doc-link" target="_blank">📄 CV</a>
<a href="documents/IITM_Transcript.pdf" class="doc-link" target="_blank">🎓 IIT Transcript</a>
<a href="documents/KTH_Transcript.pdf" class="doc-link" target="_blank">🇸🇪 KTH Transcript</a>
```

**To update:**
1. Ensure PDF files are in `documents/` folder with exact filename
2. Update `href="documents/filename.pdf"` to match
3. Change emoji and text as needed

---

## 📝 Update Footer

Find the footer section (around line 840):

```html
<p>Crafted with ♥ by Adithyaa | Last updated: Sept 2026</p>
```

Change to:
```html
<p>Crafted with ♥ by Your Name | Last updated: [Month Year]</p>
```

---

## 🚀 Before Deploying

- [ ] Profile photo added
- [ ] All contact links updated
- [ ] Bio text personalized
- [ ] Projects descriptions correct
- [ ] Experience dates accurate
- [ ] Education information updated
- [ ] Skills listed
- [ ] PDFs in `documents/` folder
- [ ] Footer date current
- [ ] Test on phone/tablet
- [ ] All links working (click each one!)

---

## 📤 How to Deploy

### GitHub Pages (Free, recommended for developers)
1. Create new GitHub repo named `username.github.io`
2. Upload files to repo
3. Your site goes live at `https://username.github.io`

### Netlify (Free, easiest)
1. Go to [netlify.com](https://netlify.com)
2. Drag & drop your entire folder
3. Done! Your site is live

### Vercel (Free, best performance)
1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Upload folder or connect GitHub
4. Deploy!

### Custom Server/Domain
1. Upload all files via FTP or SSH
2. Point domain to server IP
3. Done!

---

## 💡 Common Edits Cheat Sheet

| What to Change | Where to Find | Find Text | Replace With |
|---|---|---|---|
| Name | Top of nav | `ARG` | Your initials |
| Name (Full) | About page | `Adithyaa Rettaikudi Gurumoorthi` | Your full name |
| Tagline | About page | `Robotics • Machine Learning • AI Systems` | Your tagline |
| Email | Social links | `mailto:adithyaa.off@gmail.com` | Your email |
| LinkedIn | Social links | `adithyaa-rg` | Your profile |
| GitHub | Social links | `adithyaa-rg` | Your username |
| Theme Color | CSS :root | `#2563eb` | Your color hex |
| Footer Text | Footer | `Sept 2026` | Current month/year |

---

## 🆘 Troubleshooting

### Changes not showing?
→ Hard refresh: Ctrl+Shift+R (Cmd+Shift+R on Mac)

### Image not loading?
→ Check filename matches exactly (case-sensitive)
→ Ensure file is in `assets/` folder
→ Use `assets/filename.jpg` not `./assets/filename.jpg`

### Link not working?
→ Check `href="documents/filename.pdf"` matches PDF name exactly
→ Try opening link in new tab
→ Right-click → Open in New Tab to test

### Color changed everywhere, wanted only accent?
→ Only update `--accent:` and `--accent-dark:` colors
→ Don't change `--bg`, `--text`, `--border` colors

### PDF won't open?
→ Ensure PDF is in `documents/` folder
→ Check filename is exact (e.g., `KTH_Transcript.pdf`)
→ Try downloading and opening locally first

---

## 📞 Need More Help?

**Read the full guide:** `README.md`
**Check the code:** Use Ctrl+F to search for text
**Inspect errors:** Press F12 → Console tab
**Test changes:** Always refresh browser after saving

---

Good luck! You've got this! 🚀

*Last Updated: September 2026*
