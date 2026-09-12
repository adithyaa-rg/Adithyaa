# Adithyaa's Personal Website

A minimalist, warm-toned personal portfolio site built with plain **HTML, CSS, and JavaScript** — no build tools, no frameworks, no dependencies. Everything lives in a single file, `index.html`, so you never have to hunt across a project to make a change.

This guide is written so that **you don't need to know how to code** to update the site. Every section below tells you exactly what to find (using Ctrl+F / Cmd+F), what it looks like, and what to type to change it.

---

## 0. The one rule that matters

Everything is inside **`index.html`**. Open it in any text editor (Notepad, VS Code, TextEdit, whatever you have). Every change described in this guide happens in that one file, unless it involves adding an image or PDF (in which case you also drop a file into `assets/` or `documents/`).

After editing, save the file and refresh it in your browser to see the change. If you don't see the change, hard-refresh with `Ctrl+Shift+R` (`Cmd+Shift+R` on Mac).

---

## 1. How the page is organized

The site is a **single HTML page** that behaves like several pages. Only one "section" is visible at a time, and the navigation bar at the top switches between them using a small bit of JavaScript at the bottom of the file (`showPage()`), you never need to touch that script.

There are two kinds of content blocks in `index.html`:

1. **The profile header** — your name, photo, tagline, bio, and links. This is `<div class="profile-header">`. It is **always visible**, no matter which tab is selected, because it lives outside the section blocks below.
2. **Sections (tabs)** — each is a `<div class="page" id="...">...</div>`. There are five:
   | id | Nav label | What's inside |
   |---|---|---|
   | `research` | Research | Research interest write-ups |
   | `projects` | Projects | Project cards + publications |
   | `experience` | Experience | Work history + teaching history |
   | `education` | Education | Degrees + coursework |
   | `skills` | Skills | Skill category boxes |

Each `<div class="page" id="X">` block is wrapped in an HTML comment banner like:

```html
<!-- ═════════════════════════════════════════════════════ -->
<!-- RESEARCH INTERESTS PAGE                                -->
<!-- ═════════════════════════════════════════════════════ -->
<div id="research" class="page active">
```

Search (Ctrl+F) for the ALL-CAPS banner text (e.g. `PROJECTS PAGE`) to jump straight to any section.

---

## 2. Editing the profile header (name, photo, bio, links)

Search for `class="profile-header"`. Inside you'll find:

```html
<img ... class="profile-photo" id="profilePhoto">
<h1>Adithyaa Rettaikudi Gurumoorthi</h1>
<p class="tagline">Robotics · Machine Learning · AI Systems</p>
<div class="profile-links"> ... </div>
<div class="bio-text"> ... </div>
```

### Change your name / tagline
Just edit the text inside the `<h1>` and `<p class="tagline">` tags directly.

### Change your photo
By default the photo is a placeholder beige circle. To use a real photo:
1. Put your image file in the `assets/` folder (e.g. `assets/profile.jpg`).
2. Find this line:
   ```html
   <img src="data:image/svg+xml,...long placeholder..." alt="Adithyaa" class="profile-photo" id="profilePhoto">
   ```
3. Replace the whole `src="..."` value with your file path:
   ```html
   <img src="assets/profile.jpg" alt="Adithyaa" class="profile-photo" id="profilePhoto">
   ```
The photo automatically displays as a circle and crops to fit — any roughly-square image works well.

### Add / remove a social or document link
Each link is one line inside `<div class="profile-links">`:
```html
<a href="mailto:adithyaa.off@gmail.com" class="social-link">📧 Email</a>
<a href="https://www.linkedin.com/in/adithyaa-rg" class="social-link" target="_blank">💼 LinkedIn</a>
```
- **To remove one**, delete its entire `<a ...>...</a>` line.
- **To add one**, copy an existing line, paste it, then change the `href` (the link destination), the emoji, and the label text. Use `class="social-link"` for outward links (LinkedIn, GitHub, email) and `class="doc-link"` for files you're linking to inside `documents/` (CV, transcripts) — they're styled identically, the two class names just make the code easier to read.

### Change the bio paragraphs
Edit the text inside `<div class="bio-text">`. Each paragraph is its own `<p>...</p>` line — add a new `<p>Your text</p>` line to add a paragraph, or delete one to remove it.

---

## 3. Research page

Search for `RESEARCH INTERESTS PAGE`. The page is made of repeating **section blocks**, one per research theme:

```html
<div class="section">
    <div class="section-title">Imitation Learning</div>
    <div class="entry">
        <p class="entry-description">
            Your paragraph describing this research area...
        </p>
        <div class="entry-tags">
            <span class="tag">Keyword 1</span>
            <span class="tag">Keyword 2</span>
        </div>
    </div>
</div>
```

- **To add a new research area**: copy one whole `<div class="section">...</div>` block (from the opening `<div class="section">` to its matching closing `</div>`), paste it below the last one, then edit the title, description, and tags.
- **To remove a research area**: delete its whole `<div class="section">...</div>` block, including the opening and closing tags.
- **To add/remove a tag**: each `<span class="tag">Keyword</span>` is one tag chip. Add or delete lines the same way.

---

## 4. Projects page

Search for `PROJECTS PAGE`. There are two parts: a grid of **project cards**, then a list of **publications**.

### Project cards
Each card is a `<div class="project-card">...</div>` block:

```html
<div class="project-card">
    <div class="project-media">
        <img src="..." alt="Project Name">
    </div>
    <div class="project-content">
        <div class="project-title">Project Name</div>
        <div class="project-subtitle">Optional status label</div>   <!-- delete this line if you don't need a label -->
        <p class="project-description">What the project is about.</p>
        <div class="project-meta">
            <span>Date range</span>
            <span>Organization / place</span>
        </div>
        <div class="project-tags">
            <span class="tag">Tech 1</span>
            <span class="tag">Tech 2</span>
        </div>
        <a href="#" class="project-link">View Details</a>
    </div>
</div>
```

- **Add a project**: copy a whole `<div class="project-card">...</div>` block and paste it inside `<div class="projects-grid">`, anywhere between the existing cards. Edit the title, description, dates, tags, and link.
- **Remove a project**: delete its whole `<div class="project-card">...</div>` block.
- **`.project-subtitle` is optional.** Some cards (like "Published Research") use it to flag status; plenty of cards have no subtitle at all — the date/organization line in `.project-meta` already carries that context, so only add a subtitle when it tells the reader something the meta line doesn't (e.g. "Published Research", "Published in Computers & Graphics 2025").
- **Adding project media**: replace the placeholder `<img src="...">` inside `.project-media`. Put your image in `assets/` (e.g. `assets/my-project.png`) and reference it as `src="assets/my-project.png"`. For video, replace the `<img>` with:
  ```html
  <video controls style="width:100%; height:100%; object-fit:cover;">
      <source src="assets/my-demo.mp4" type="video/mp4">
  </video>
  ```

### Publications
Each publication is a simple `<div class="entry">` block near the bottom of the Projects page:
```html
<div class="entry">
    <h3>International Journal</h3>
    <p class="entry-description">
        <strong>Paper Title</strong>
        <br>Author list
        <br><em>Venue</em>, year
    </p>
</div>
```
Add or remove these the same way as any other block — copy/paste to add, delete the block to remove.

---

## 5. Experience page

Search for `EXPERIENCE PAGE`. There are two `.section` blocks: **Work Experience** and **Teaching Experience**. Inside each, every job/role is an `.entry` block:

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
        <li>Achievement or responsibility 1</li>
        <li>Achievement or responsibility 2</li>
    </ul>
    <div class="entry-tags">
        <span class="tag">Skill</span>
    </div>
</div>
```

- **Add a role**: copy a whole `.entry` block and paste it either at the top (most recent first) or bottom of its section. Edit title, subtitle, dates, bullet points, and tags.
- **Remove a role**: delete its whole `.entry` block.
- **Add/remove a bullet point**: each `<li>...</li>` inside `.entry-points` is one bullet — add or delete lines freely.
- **Add a whole new section** (e.g. "Volunteering"): copy an entire `<div class="section">...</div>` block (including the `.section-title` and everything inside it), paste it below the existing sections, and edit.

---

## 6. Education page

Search for `EDUCATION PAGE`. There are two parts: **degree cards** at the top, and **coursework** grouped by subject below.

### Degree cards
```html
<div class="education-card">
    <div class="education-degree">DEGREE TYPE</div>
    <div class="education-institution">University Name</div>
    <div class="education-details">
        <strong>Program Name</strong><br>
        <strong>CGPA:</strong> X.XX / 10.0<br>
        <strong>Month Year – Month Year</strong>
    </div>
    <a href="documents/YourTranscript.pdf" class="education-cta" target="_blank">View Transcript →</a>
</div>
```
Copy/edit/delete `.education-card` blocks the same way as everywhere else. To link a transcript, drop the PDF into `documents/` and point `href` at `documents/YourFile.pdf`. If you don't have a transcript to link, just delete the `<a ...>View Transcript →</a>` line.

### Coursework
Each subject area is its own `.section`:
```html
<div class="section">
    <h3>Machine Learning & AI</h3>
    <div class="entry">
        <p class="entry-description">
            Course 1 (code), Course 2 (code), Course 3 (code)
        </p>
    </div>
</div>
```
Add a new subject by copying a whole `.section` block; add/remove individual courses by editing the comma-separated list in the `entry-description` paragraph.

---

## 7. Skills page

Search for `SKILLS PAGE`. Each box is a `.skill-block`:
```html
<div class="skill-block">
    <div class="skill-category">Category Name</div>
    <ul class="skill-list">
        <li>Skill 1</li>
        <li>Skill 2</li>
    </ul>
</div>
```
- **Add a skill**: add a new `<li>Skill</li>` line inside the relevant `.skill-list`.
- **Remove a skill**: delete its `<li>` line.
- **Add a whole new category**: copy a whole `.skill-block` and paste it inside `<div class="skills-grid">`; edit the category name and list.
- **Remove a category**: delete the whole `.skill-block`.

---

## 8. Adding or removing an entire page (tab)

This is a bigger change, but still just three steps:

**To add a new tab** (e.g. "Publications" as its own page instead of living inside Projects):
1. Add a nav link inside `<div class="nav-menu">`:
   ```html
   <a class="nav-item" onclick="showPage('publications', event); return false;">Publications</a>
   ```
2. Add a new page block inside `<main>`, alongside the other `<div class="page">` blocks:
   ```html
   <div id="publications" class="page">
       <h1>Publications</h1>
       <!-- your content here -->
   </div>
   ```
   The `id` here (`publications`) must exactly match the `showPage('publications', ...)` value from step 1.
3. That's it — no other file needs to change.

**To remove a tab** (e.g. remove "Skills" entirely):
1. Delete its `<a class="nav-item" onclick="showPage('skills', ...)">Skills</a>` line from `<div class="nav-menu">`.
2. Delete its whole `<div id="skills" class="page">...</div>` block from `<main>`.
3. If the page you deleted was the one shown by default (it has `class="page active"` instead of just `class="page"`), add `active` to the `class` of whichever page should now show first, e.g. `class="page active"`.

---

## 9. Colors, fonts, and spacing (the "design tokens")

Near the very top of `index.html`, inside the `<style>` tag, there's a `:root { ... }` block. Every color, font, and spacing value used across the whole site is defined **once** here and reused everywhere — so this is the only place you need to touch to re-theme the site.

```css
:root {
    --bg: #f2ece1;              /* page background (beige) */
    --bg-secondary: #faf6ee;    /* card background */
    --bg-tertiary: #ece3d3;     /* chip / hover background */
    --border: #ddd0b8;
    --text: #3c352c;
    --text-muted: #6d6152;
    --text-light: #948873;
    --accent: #a2673f;          /* terracotta accent color */
    --accent-dark: #7c4c2b;
    --accent-soft: #efe0cd;

    --font-heading: "Lora", Georgia, serif;
    --font-body: "Roboto", system-ui, sans-serif;

    --space-2xs: 0.4rem;
    --space-xs: 0.75rem;
    --space-sm: 1.25rem;
    --space-md: 2rem;
    --space-lg: 3rem;
    --space-xl: 4.5rem;
}
```

- **Change the color scheme**: edit any of the `--bg`, `--text`, or `--accent` hex codes. Use [colorhexa.com](https://www.colorhexa.com) to pick new ones. Everything using `var(--accent)` etc. updates automatically.
- **Change the fonts**: swap the font names in `--font-heading` / `--font-body`. If you pick a font that isn't Lora or Roboto, also update the Google Fonts `<link>` tags near the top of `<head>` to load it.
- **Change spacing**: the `--space-*` variables control the gaps between every card, section, and block on the site. Bumping `--space-md` up, for instance, adds breathing room between every section on every page at once — this is what keeps spacing consistent instead of having to fix margins one at a time.

---

## 10. Documents (CV, transcripts)

Put PDFs in the `documents/` folder, then link them anywhere with:
```html
<a href="documents/YourFile.pdf" class="doc-link" target="_blank">📄 Label</a>
```
(or `class="education-cta"` if it's a "View Transcript →" style link on the Education page).

---

## 11. Deploying the site

No build step is needed — this is a static site.

- **GitHub Pages**: push this folder to a repo, then enable Pages in the repo settings (Settings → Pages → deploy from `main` branch).
- **Netlify**: go to [netlify.com](https://netlify.com) and drag-and-drop this folder onto the dashboard.
- **Vercel**: go to [vercel.com](https://vercel.com), connect the repo or upload the folder, and deploy.
- **Any web host**: upload all files via FTP/SFTP — it works as-is.

---

## 12. Troubleshooting

| Problem | Fix |
|---|---|
| Changes not showing | Hard refresh: `Ctrl+Shift+R` (`Cmd+Shift+R` on Mac) |
| Image not loading | Confirm the file is actually inside `assets/` and the filename (including capitalization and extension) matches exactly what's in `src="..."` |
| PDF won't open | Confirm the file is inside `documents/` and the filename matches the `href="..."` exactly |
| Clicking a nav tab does nothing | Make sure the `id="..."` on your page `<div>` exactly matches the name used in `showPage('...')` for that nav link |
| Colors/fonts didn't change | Double check you edited inside the `:root { ... }` block near the top of the file, and hard-refresh |

---

## File structure

```
.
├── index.html          # The entire website — all HTML, CSS, and JS
├── README.md           # This file
├── assets/             # Your images and videos go here
├── documents/          # CV and transcript PDFs
│   ├── Academic_CV_Adithyaa.pdf
│   ├── IITM_Transcript.pdf
│   └── KTH_Transcript.pdf
└── projects/           # (optional) extra project-specific files, unused by default
```

---

**Last updated:** Sept 2026
