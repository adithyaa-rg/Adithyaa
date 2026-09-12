# Adithyaa's Personal Website

A modern, professional personal portfolio website built with **HTML5, CSS3, and vanilla JavaScript**. Zero dependencies, fully static, easy to customize and deploy.

---

## 🎨 Features

✨ **Multi-page Navigation** – Separate sections for About, Research, Projects, Experience, Education, Skills
✨ **Responsive Design** – Mobile-friendly on all devices
✨ **Roboto Font** – Professional, clean typography
✨ **Light Theme** – Bright, airy background (#fafafa) with accent colors
✨ **Project Media Support** – Add images/videos to project cards
✨ **Document Links** – Easy access to CV and transcripts
✨ **Zero Setup Required** – Just open index.html in browser or deploy as-is

---

## 📁 File Structure

```
Adithyaa-new/
├── index.html              # Main website (all-in-one file)
├── documents/              # PDFs (CV, transcripts)
│   ├── Academic_CV_Adithyaa.pdf
│   ├── IITM_Transcript.pdf
│   └── KTH_Transcript.pdf
├── assets/                 # (Optional) Images & videos
│   └── profile-photo.jpg
├── projects/               # (Optional) Project details/images
└── README.md              # This file
```

---

## 🚀 Quick Start

### Option 1: Open Locally
```bash
# Just double-click index.html or open in any browser
open index.html
```

### Option 2: Deploy to Web
- **GitHub Pages**: Push to repository, enable Pages in settings
- **Netlify**: Drag & drop folder (free hosting)
- **Vercel**: Connect Git repo or upload folder
- **Any static host**: Just upload the files

---

## ✏️ How to Customize

### 1. **Update Your Information**

#### Profile Photo
Open `index.html`, find the line with `id="profilePhoto"` (around line 440):

```html
<img src="data:image/svg+xml,..." alt="Adithyaa" class="profile-photo" id="profilePhoto">
```

**Option A:** Replace with local image
```html
<img src="assets/profile-photo.jpg" alt="Adithyaa" class="profile-photo" id="profilePhoto">
```

**Option B:** Replace with online image URL
```html
<img src="https://example.com/your-photo.jpg" alt="Your Name" class="profile-photo">
```

1. Add your image to the `assets/` folder (create if needed)
2. Update the `src` attribute with the path

---

#### Contact Links
Find the social links section (around line 460):

```html
<div class="social-links">
    <a href="mailto:adithyaa.off@gmail.com" class="social-link">
        <span>📧</span>
        <span>Email</span>
    </a>
    <a href="https://www.linkedin.com/in/adithyaa-rg" class="social-link" target="_blank">
        <span>💼</span>
        <span>LinkedIn</span>
    </a>
    <!-- Update URLs here -->
</div>
```

Replace:
- `mailto:adithyaa.off@gmail.com` → your email
- `https://www.linkedin.com/in/adithyaa-rg` → your LinkedIn URL
- `https://github.com/adithyaa-rg` → your GitHub URL
- `https://scholar.google.com/citations?user=YOUR_ID` → your Google Scholar (or update)

---

#### Bio Text
Around line 455, update the bio paragraphs:

```html
<div class="bio-text">
    <p>My research background spans...</p>  <!-- UPDATE THIS -->
    <p style="margin-top: 1rem;">I'm seeking to apply...</p>  <!-- UPDATE THIS -->
    <p style="margin-top: 1rem; font-style: italic;">Outside the lab...</p>  <!-- UPDATE THIS -->
</div>
```

---

### 2. **Update About Page Heading**

Around line 437:
```html
<h1>Adithyaa Rettaikudi Gurumoorthi</h1>  <!-- UPDATE YOUR NAME -->
<p class="tagline">Robotics • Machine Learning • AI Systems</p>  <!-- UPDATE TAGLINE -->
```

---

### 3. **Update Research Interests Page**

Around line 490 (Research page), update:

```html
<div class="section">
    <div class="section-title">Your Research Area</div>
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

**Pattern:**
- `<div class="section-title">` → Research area name
- `<p class="entry-description">` → Description text
- `<span class="tag">` → Skill/keyword tags

---

### 4. **Update Projects Page**

Around line 530, each project card looks like this:

```html
<div class="project-card">
    <!-- PROJECT IMAGE/VIDEO -->
    <div class="project-media">
        <img src="path/to/image.jpg" alt="Project Name">
        <!-- OR for video: -->
        <!-- <video controls><source src="path/to/video.mp4"></video> -->
    </div>

    <div class="project-content">
        <div class="project-title">Project Name</div>
        <div class="project-subtitle">Role/Status</div>
        <p class="project-description">
            Description of the project...
        </p>
        <div class="project-meta">
            <span>Date Range</span>
            <span>Organization</span>
        </div>
        <div class="project-tags">
            <span class="tag">Technology1</span>
            <span class="tag">Technology2</span>
        </div>
        <a href="#" class="project-link">View Details</a>
    </div>
</div>
```

#### To Add Project Media:

1. **For Images:**
   ```html
   <div class="project-media">
       <img src="assets/project-screenshot.png" alt="Project Name">
   </div>
   ```

2. **For Videos:**
   ```html
   <div class="project-media">
       <video controls style="width: 100%; height: 100%; object-fit: cover;">
           <source src="assets/project-demo.mp4" type="video/mp4">
       </video>
   </div>
   ```

3. **For Links:**
   ```html
   <a href="https://github.com/username/project" class="project-link">View on GitHub</a>
   ```

---

### 5. **Update Experience Page**

Around line 620, work experience section:

```html
<div class="entry">
    <div class="entry-header">
        <div>
            <div class="entry-title">Your Job Title</div>
            <div class="entry-subtitle">Company Name, Location</div>
        </div>
        <div class="entry-time">Month Year – Month Year</div>
    </div>
    <ul class="entry-points">
        <li>Achievement 1</li>
        <li>Achievement 2</li>
        <li>Achievement 3</li>
    </ul>
    <div class="entry-tags">
        <span class="tag">Skill1</span>
        <span class="tag">Skill2</span>
    </div>
</div>
```

---

### 6. **Update Education Page**

Around line 700, education cards:

```html
<div class="education-card">
    <div class="education-degree">YOUR DEGREE TYPE</div>
    <div class="education-institution">University Name</div>
    <div class="education-details">
        <strong>Program Name</strong><br>
        <strong>GPA/CGPA:</strong> X.XX / Y.YY<br>
        <strong>Date Range:</strong> Month Year – Month Year
    </div>
    <a href="documents/YourTranscript.pdf" class="education-cta" target="_blank">View Transcript →</a>
</div>
```

**Update PDFs:**
1. Place your PDF in `documents/` folder
2. Update the href: `href="documents/YourFileName.pdf"`

---

### 7. **Update Skills Page**

Around line 760, update skill blocks:

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

Add/remove skill blocks as needed by duplicating the pattern above.

---

### 8. **Update Footer**

Around line 840:

```html
<p>Crafted with <span style="color: var(--accent);">♥</span> by Your Name | Last updated: Month Year</p>
<p style="margin-top: 1rem; font-size: 0.85rem;">
    Built with HTML, CSS & JavaScript | <a href="https://github.com/username" target="_blank">View Source</a>
</p>
```

---

## 🎨 Customize Colors

The color scheme is defined at the top of `index.html` in the `:root` CSS section:

```css
:root {
    /* Light, clean color scheme */
    --bg: #fafafa;                    /* Main background */
    --bg-secondary: #ffffff;          /* Card backgrounds */
    --border: #e5e5e5;                /* Borders */
    --text: #333333;                  /* Main text */
    --text-muted: #666666;            /* Secondary text */
    --text-light: #999999;            /* Light text */
    --accent: #2563eb;                /* Primary accent (blue) */
    --accent-dark: #1e40af;           /* Darker accent */
    --success: #059669;               /* Success color (green) */
}
```

**To change colors:**
1. Find the `:root` section (lines 34-44)
2. Update hex codes:
   - Change `--accent: #2563eb;` to your preferred color
   - Use [colorhexa.com](https://www.colorhexa.com) to find hex codes

**Example: Change accent to orange**
```css
--accent: #f97316;
--accent-dark: #ea580c;
```

---

## 📱 Responsive Breakpoints

The website automatically adapts to:
- **Desktop** (1200px+) → Full layout
- **Tablet** (768px–1199px) → Stacked layout, adjusted spacing
- **Mobile** (< 768px) → Single column, touch-friendly

No additional changes needed – it's automatic!

---

## 🔗 Document Management

### Adding New PDFs
1. Add PDF files to the `documents/` folder
2. Link them in HTML:

```html
<a href="documents/filename.pdf" class="doc-link" target="_blank">📄 Document Name</a>
```

### Current Documents
- `Academic_CV_Adithyaa.pdf` – Your CV
- `IITM_Transcript.pdf` – IIT Madras transcript
- `KTH_Transcript.pdf` – KTH Stockholm transcript

---

## 🖼️ Adding Project Media

### Images
1. Add image to `assets/` folder
2. Use in project card:
```html
<div class="project-media">
    <img src="assets/project-name.jpg" alt="Project Name">
</div>
```

### Videos
1. Add MP4 video to `assets/` folder
2. Use in project card:
```html
<div class="project-media">
    <video controls>
        <source src="assets/demo.mp4" type="video/mp4">
    </video>
</div>
```

### YouTube Embeds
```html
<div class="project-media">
    <iframe width="100%" height="200" src="https://www.youtube.com/embed/VIDEO_ID" 
            frameborder="0" allowfullscreen></iframe>
</div>
```

---

## 🚀 Deployment Options

### GitHub Pages (Free)
```bash
# 1. Create GitHub repo
# 2. Push this folder to main branch
# 3. Go to Settings → Pages → Enable
# 4. Your site: https://username.github.io/repo-name
```

### Netlify (Free, recommended)
1. Go to [netlify.com](https://netlify.com)
2. Drag & drop this folder
3. Done! (auto-deploys on push to GitHub)

### Vercel (Free)
1. Go to [vercel.com](https://vercel.com)
2. Connect GitHub repo or upload folder
3. Deploy automatically

### Self-Hosted
1. Upload all files to your web server
2. No build process needed
3. Works immediately

---

## ⌨️ Keyboard Shortcuts

- **Any key** → Currently no shortcuts (can be added)
- **Click nav items** → Jump between sections
- **ESC** → Can be used to clear focus

---

## 🔍 SEO & Meta Tags

Update these in the `<head>` section of `index.html`:

```html
<title>Your Name - Your Tagline</title>
<meta name="description" content="Brief description of who you are">
```

---

## 📊 Analytics (Optional)

To add Google Analytics, add this before `</body>`:

```html
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_ID');
</script>
```

Replace `GA_ID` with your Google Analytics ID.

---

## 🎓 JavaScript Customization

The `showPage()` function handles navigation:

```javascript
function showPage(pageId) {
    // Hide all pages
    const pages = document.querySelectorAll('.page');
    pages.forEach(page => page.classList.remove('active'));

    // Show requested page
    const targetPage = document.getElementById(pageId);
    if (targetPage) {
        targetPage.classList.add('active');
    }

    // Update nav
    const navItems = document.querySelectorAll('.nav-item');
    navItems.forEach(item => item.classList.remove('active'));
    event.target.classList.add('active');

    // Scroll to top
    window.scrollTo(0, 0);
}
```

Add custom behavior by modifying this function.

---

## 🐛 Common Issues & Fixes

### Images not loading?
- Check path is correct: `assets/image.jpg` not `./assets/image.jpg`
- Ensure image file exists in `assets/` folder
- Use full URL if hosting externally

### Colors look different?
- Clear browser cache (Ctrl+Shift+Del / Cmd+Shift+Del)
- Check CSS variables in `:root` section
- Verify hex codes are correct (#RRGGBB format)

### Navigation not working?
- Ensure `<div id="pageId">` matches `showPage('pageId')`
- Check browser console for JavaScript errors
- Refresh page and try again

### PDFs not opening?
- Ensure PDF files are in `documents/` folder
- Use correct filename in href attribute
- Test with full path: `documents/filename.pdf`

---

## 💡 Tips & Best Practices

1. **Keep content organized** – Use consistent formatting for entries
2. **Use meaningful tags** – Help readers understand your skills
3. **Update regularly** – Mark "Last updated" date in footer
4. **Test responsiveness** – Open in mobile browser before deploying
5. **Backup regularly** – Keep old versions in git history
6. **Use descriptive alt text** – For accessibility and SEO
7. **Optimize images** – Compress before adding to reduce load time

---

## 📝 Checklist Before Deployment

- [ ] Profile photo added/updated
- [ ] All contact links correct
- [ ] Bio text personalized
- [ ] Projects description accurate
- [ ] Experience dates correct
- [ ] Education information updated
- [ ] Skills match your expertise
- [ ] All PDFs in `documents/` folder
- [ ] Footer shows correct year
- [ ] Tested on mobile device
- [ ] All links working (test by opening in new tab)

---

## 🆘 Need Help?

### Common Tasks
- **Add a new project:** Copy a project-card div, update content
- **Remove a section:** Delete the entire `<div class="section">` block
- **Change theme color:** Find `--accent: #2563eb;` and change hex code
- **Add social link:** Duplicate social-link div and update href/icon

### Debugging
1. Right-click → Inspect (F12) → Console tab
2. Check for red error messages
3. Use Ctrl+F to find specific text
4. Test changes in browser before saving

---

## 📄 File Naming Conventions

- Images: lowercase with hyphens: `project-name.jpg`
- Folders: lowercase: `assets/`, `documents/`
- Documents: CamelCase: `Academic_CV.pdf`
- HTML IDs: lowercase with hyphens: `profile-photo`

---

## 🎉 You're All Set!

Your website is ready to customize. Start by:

1. Updating your profile photo
2. Changing contact links
3. Updating your bio
4. Adding your projects
5. Deploying to a hosting service

Good luck! Questions? Check back to this guide.

---

**Last Updated:** September 2026
**Version:** 1.0
**Status:** Production Ready ✨
