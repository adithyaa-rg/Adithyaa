# File Structure & Line Numbers Guide

> Quick reference to find exactly what you need to edit in `index.html`

---

## 📍 Navigation in index.html

### Top of File (Style & Colors)
```
Line 1-33    : HTML Declaration & Meta Tags
Line 34-43   : COLOR VARIABLES (--accent, --bg, etc.)
Line 45-850  : All CSS Styling
Line 851+    : HTML Body & Content
```

### CSS Color Variables (Line 34-43)
**THIS IS WHERE YOU CHANGE COLORS!**
```css
:root {
    --bg: #fafafa;                    /* Background */
    --bg-secondary: #ffffff;          /* Card backgrounds */
    --border: #e5e5e5;                /* Borders */
    --text: #333333;                  /* Text color */
    --text-muted: #666666;            /* Dimmer text */
    --text-light: #999999;            /* Light gray text */
    --accent: #2563eb;                /* MAIN COLOR - Change this! */
    --accent-dark: #1e40af;           /* Dark version - Change this too! */
    --success: #059669;               /* Green (rarely used) */
}
```

---

## 🗺️ Where Everything Is in HTML Body

### NAVIGATION BAR
```
Line 851     : <nav> starts
Line 853     : <a class="nav-logo"> - "ARG" logo
Line 855     : <div class="nav-menu"> - Navigation items
             Links to: About, Research, Projects, Experience, Education, Skills
```

### MAIN CONTENT AREA
```
Line 865     : <main> container starts (contains all pages)
```

---

## 📄 Page Sections (Each is a `<div id="name" class="page">`)

### PAGE 1: ABOUT (Line 872-925)
```
Line 872     : <div id="about" class="page active">
Line 874     : <div class="about-container"> (grid layout)

Line 876     : LEFT SIDE - Image section
Line 877     : <img id="profilePhoto"> ← YOUR PROFILE PHOTO GOES HERE
Line 879     : <div class="document-links">
Line 880     : <a href="documents/Academic_CV_Adithyaa.pdf"> ← CV LINK
Line 881     : <a href="documents/IITM_Transcript.pdf"> ← TRANSCRIPT 1
Line 882     : <a href="documents/KTH_Transcript.pdf"> ← TRANSCRIPT 2

Line 886     : RIGHT SIDE - Content section
Line 887     : <h1> ← YOUR NAME
Line 888     : <p class="tagline"> ← YOUR TAGLINE
Line 890     : <div class="bio-text">
Line 891-895 : YOUR BIO TEXT (3 paragraphs)

Line 897     : <div class="social-links">
Line 898     : <a href="mailto:..."> ← EMAIL LINK
Line 903     : <a href="linkedin.com/in/..."> ← LINKEDIN LINK
Line 908     : <a href="github.com/..."> ← GITHUB LINK
Line 913     : <a href="scholar.google.com/..."> ← GOOGLE SCHOLAR LINK
```

### PAGE 2: RESEARCH (Line 927-1010)
```
Line 927     : <div id="research" class="page">
Line 928     : <h1>Research Interests</h1>

Line 930-945 : Section 1: Imitation Learning
Line 947-960 : Section 2: Human-Machine Interfaces
Line 962-975 : Section 3: Computational Geometry
Line 977-995 : Section 4: Broader Impact Areas
```

Each section follows pattern:
```
<div class="section">
    <div class="section-title">Research Area Name</div>
    <div class="entry">
        <p class="entry-description">Description...</p>
        <div class="entry-tags">
            <span class="tag">Tag1</span>
        </div>
    </div>
</div>
```

### PAGE 3: PROJECTS (Line 1012-1370)
```
Line 1012    : <div id="projects" class="page">
Line 1013    : <h1>Projects & Publications</h1>

Line 1015    : <div class="projects-grid">
Line 1017-1045 : Project Card 1: State-Only Imitation Learning
Line 1047-1075 : Project Card 2: Interactive Steering
Line 1077-1105 : Project Card 3: De(l)Noise
Line 1107-1135 : Project Card 4: Ola Krutrim
Line 1137-1165 : Project Card 5: Hybrid A*
Line 1167-1195 : Project Card 6: Language Hierarchical Agent

Line 1198    : <h2>Publications</h2>
Line 1200-1220 : Publication entries
```

Each project card structure:
```
<div class="project-card">
    <div class="project-media">
        <img src="..."> ← IMAGE GOES HERE
    </div>
    <div class="project-content">
        <div class="project-title">Name</div>
        <div class="project-subtitle">Role</div>
        <p class="project-description">Description</p>
        <div class="project-meta">
            <span>Dates</span>
            <span>Organization</span>
        </div>
        <div class="project-tags">
            <span class="tag">Tech</span>
        </div>
        <a href="#" class="project-link">View Details</a>
    </div>
</div>
```

### PAGE 4: EXPERIENCE (Line 1222-1340)
```
Line 1222    : <div id="experience" class="page">
Line 1223    : <h1>Work & Teaching Experience</h1>

Line 1225    : <div class="section">
Line 1226    : <div class="section-title">Work Experience</div>

Line 1228-1260 : Entry 1: Data Scientist at Ather Energy
Line 1262-1290 : Entry 2: Intern at Ola Krutrim

Line 1292    : <div class="section">
Line 1293    : <div class="section-title">Teaching Experience</div>

Line 1295-1320 : Teaching Entry 1: Data Science TA
Line 1322-1340 : Teaching Entry 2: Mechanical Systems TA
```

Work experience entry structure:
```
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
    </div>
</div>
```

### PAGE 5: EDUCATION (Line 1342-1450)
```
Line 1342    : <div id="education" class="page">
Line 1343    : <h1>Education</h1>

Line 1345    : <div class="education-grid">
Line 1346-1360 : Education Card 1: IIT Madras Dual Degree
Line 1362-1376 : Education Card 2: KTH Exchange

Line 1379    : <h2>Relevant Coursework</h2>
Line 1381-1425 : Coursework sections (ML, Robotics, Geometry, Other)
```

Education card structure:
```
<div class="education-card">
    <div class="education-degree">DEGREE TYPE</div>
    <div class="education-institution">University Name</div>
    <div class="education-details">
        <strong>Program Name</strong><br>
        <strong>CGPA:</strong> X.XX / Y.YY<br>
        <strong>Dates:</strong> Month Year – Month Year
    </div>
    <a href="documents/transcript.pdf" class="education-cta">View Transcript →</a>
</div>
```

### PAGE 6: SKILLS (Line 1452-1510)
```
Line 1452    : <div id="skills" class="page">
Line 1453    : <h1>Technical Skills</h1>

Line 1455    : <div class="skills-grid">
Line 1456-1475 : Skill Block 1: Programming Languages
Line 1477-1490 : Skill Block 2: Machine Learning
Line 1492-1505 : Skill Block 3: Robotics & Control
Line 1507-1520 : Skill Block 4: Geometric Processing
Line 1522-1535 : Skill Block 5: Simulation & Tools
Line 1537-1550 : Skill Block 6: Hardware
```

Skill block structure:
```
<div class="skill-block">
    <div class="skill-category">Category Name</div>
    <ul class="skill-list">
        <li>Skill 1</li>
        <li>Skill 2</li>
    </ul>
</div>
```

### FOOTER (Line 1552-1560)
```
Line 1552    : <footer>
Line 1553    : <p> ← "Crafted with ♥ by..." - UPDATE NAME & DATE
Line 1555    : <p> ← "Built with HTML..." and GitHub link
```

---

## 🎯 Quick Edit Locations

### Change Your Name
**Find:** Line 887
```html
<h1>Adithyaa Rettaikudi Gurumoorthi</h1>
```
**Replace:** Your name

---

### Change Tagline
**Find:** Line 888
```html
<p class="tagline">Robotics • Machine Learning • AI Systems</p>
```
**Replace:** Your tagline

---

### Add Profile Photo
**Find:** Line 877
```html
<img src="data:image/svg+xml,..." class="profile-photo" id="profilePhoto">
```
**Replace with:**
```html
<img src="assets/profile.jpg" class="profile-photo" id="profilePhoto">
```

---

### Update Contact Links
| Link | Line | Find | Replace |
|------|------|------|---------|
| Email | 898 | `mailto:adithyaa.off@gmail.com` | Your email |
| LinkedIn | 903 | `linkedin.com/in/adithyaa-rg` | Your profile |
| GitHub | 908 | `github.com/adithyaa-rg` | Your username |
| Scholar | 913 | `scholar.google.com/...` | Your URL |

---

### Update Bio Text
**Find:** Lines 891-895
```html
<div class="bio-text">
    <p>My research background spans...</p>  ← Paragraph 1
    <p style="margin-top: 1rem;">I'm seeking...</p>  ← Paragraph 2
    <p style="margin-top: 1rem; font-style: italic;">Outside the lab...</p>  ← Paragraph 3
</div>
```

---

### Update CV & Transcript Links
**Find:** Lines 880-882
```html
<a href="documents/Academic_CV_Adithyaa.pdf">📄 CV</a>
<a href="documents/IITM_Transcript.pdf">🎓 IIT Transcript</a>
<a href="documents/KTH_Transcript.pdf">🇸🇪 KTH Transcript</a>
```

---

### Add/Edit Research Interests
**Find:** Lines 927-1010
Each section:
```html
<div class="section">
    <div class="section-title">Research Area</div>
    <div class="entry">
        <p class="entry-description">Description</p>
        <div class="entry-tags">
            <span class="tag">Tag</span>
        </div>
    </div>
</div>
```

---

### Add/Edit Projects
**Find:** Lines 1017-1195
Each project:
```html
<div class="project-card">
    <div class="project-media">
        <img src="assets/image.jpg">  ← Change image path
    </div>
    <div class="project-content">
        <div class="project-title">Project Name</div>  ← Update
        <div class="project-subtitle">Role</div>  ← Update
        <p class="project-description">Description</p>  ← Update
        <div class="project-meta">
            <span>Dates</span>  ← Update
            <span>Organization</span>  ← Update
        </div>
        <div class="project-tags">
            <span class="tag">Tech</span>  ← Update
        </div>
    </div>
</div>
```

---

### Add/Edit Work Experience
**Find:** Lines 1228-1290
Pattern:
```html
<div class="entry">
    <div class="entry-header">
        <div>
            <div class="entry-title">Job Title</div>  ← Update
            <div class="entry-subtitle">Company, Location</div>  ← Update
        </div>
        <div class="entry-time">Dates</div>  ← Update
    </div>
    <ul class="entry-points">
        <li>Achievement</li>  ← Update
    </ul>
    <div class="entry-tags">
        <span class="tag">Skill</span>  ← Update
    </div>
</div>
```

---

### Add/Edit Education
**Find:** Lines 1346-1376
Pattern:
```html
<div class="education-card">
    <div class="education-degree">DEGREE TYPE</div>  ← Update
    <div class="education-institution">University</div>  ← Update
    <div class="education-details">
        <strong>Program</strong>  ← Update
        <strong>CGPA:</strong> X.XX / Y.YY  ← Update
        <strong>Duration:</strong> Dates  ← Update
    </div>
    <a href="documents/transcript.pdf">View Transcript →</a>  ← Update filename
</div>
```

---

### Add/Edit Skills
**Find:** Lines 1456-1550
Pattern:
```html
<div class="skill-block">
    <div class="skill-category">Category Name</div>  ← Update
    <ul class="skill-list">
        <li>Skill 1</li>  ← Update
        <li>Skill 2</li>
    </ul>
</div>
```

---

### Update Footer
**Find:** Lines 1553-1555
```html
<p>Crafted with ♥ by Adithyaa | Last updated: Sept 2026</p>  ← Update name & date
<p style="margin-top: 1rem; font-size: 0.85rem;">
    Built with HTML, CSS & JavaScript | <a href="https://github.com/adithyaa-rg">View Source</a>  ← Update GitHub URL
</p>
```

---

## 📁 File Structure Reference

```
Adithyaa-new/
│
├── index.html                    (MAIN FILE - all editing happens here)
│   ├── <head> - Meta, styles
│   ├── <nav> - Navigation (lines 851-865)
│   ├── <main>
│   │   ├── Page: About (872-925)
│   │   ├── Page: Research (927-1010)
│   │   ├── Page: Projects (1012-1370)
│   │   ├── Page: Experience (1222-1340)
│   │   ├── Page: Education (1342-1450)
│   │   └── Page: Skills (1452-1510)
│   ├── <footer> (1552-1560)
│   └── <script> - JavaScript (1563+)
│
├── documents/                    (Your PDFs)
│   ├── Academic_CV_Adithyaa.pdf
│   ├── IITM_Transcript.pdf
│   └── KTH_Transcript.pdf
│
├── assets/                       (Your images & videos)
│   ├── profile.jpg (PUT YOUR PHOTO HERE)
│   └── project-images/
│
├── projects/                     (Optional: project-specific assets)
│   └── (add as needed)
│
├── README.md                     (Complete guide)
├── QUICK_START.md                (Quick reference)
└── (This file)
```

---

## 🔍 Search Tips

### In Your Text Editor (Ctrl+F):
```
Find Name:              "Adithyaa Rettaikudi Gurumoorthi"
Find Tagline:           "Robotics • Machine Learning"
Find Color Settings:    ":root {"
Find Nav Items:         "class="nav-item""
Find About Page:        "id="about""
Find Projects Page:     "id="projects""
Find Contact Link:      "mailto:"
Find CV Link:           "Academic_CV"
```

---

## 📊 Useful Statistics

- **Total lines in index.html:** ~1600
- **CSS lines:** ~450
- **HTML lines:** ~1150
- **JavaScript lines:** ~50
- **Colors customizable:** 9 CSS variables
- **Pages/sections:** 6
- **Project cards:** 6
- **Skill blocks:** 6
- **PDFs included:** 3

---

## ⚡ Speed Tips

### Fastest Way to Edit:
1. Open index.html in VS Code or Sublime Text
2. Use Ctrl+F to find section
3. Make change
4. Save (Ctrl+S)
5. Refresh browser (Ctrl+Shift+R)
6. Done!

### Slowest Way (avoid):
- Trying to manually scroll through 1600 lines
- Refreshing without clearing cache
- Opening in Notepad (use VS Code instead)

---

## 🎯 Most Common Edits

**Listed by frequency of change:**

1. **Profile photo** - Line 877 (change image path)
2. **Name** - Line 887 (change text)
3. **Projects** - Lines 1017-1195 (update descriptions)
4. **Experience** - Lines 1228-1290 (update jobs)
5. **Bio text** - Lines 891-895 (update description)
6. **Contact links** - Lines 898-913 (update URLs)
7. **Education** - Lines 1346-1376 (update degrees)
8. **Skills** - Lines 1456-1550 (update list)
9. **Color theme** - Lines 34-43 (change hex codes)
10. **Footer** - Line 1553 (update date/name)

---

## 🆘 Quick Help

| I want to... | Look at line(s) |
|---|---|
| Add profile photo | 877 |
| Change my name | 887 |
| Update email | 898 |
| Change accent color | 40 |
| Update research | 930-995 |
| Edit projects | 1017-1195 |
| Update experience | 1228-1290 |
| Add education | 1346-1376 |
| Update skills | 1456-1550 |
| Change footer | 1553 |

---

**Happy editing!** 🚀

*Version: 1.0 | Date: September 2026*
