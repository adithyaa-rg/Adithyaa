# Your New Personal Website — Complete Setup Guide

🎉 **Congratulations!** Your modern personal website is ready to use.

---

## 📦 What You're Getting

Your zip file `Adithyaa-Website.zip` contains:

```
Adithyaa-new/
├── index.html              ← Main website (open this in browser)
├── README.md              ← Comprehensive customization guide
├── QUICK_START.md         ← Quick reference for common changes
├── assets/                ← Folder for your images/videos
│   └── (empty, add images here)
├── documents/             ← Your PDFs (already included!)
│   ├── Academic_CV_Adithyaa.pdf
│   ├── IITM_Transcript.pdf
│   └── KTH_Transcript.pdf
└── projects/              ← Folder for project-specific assets
    └── (empty, add here as needed)
```

---

## 🚀 Get Started in 30 Seconds

### Step 1: Extract the zip
- **Mac/Linux:** Double-click the zip or `unzip Adithyaa-Website.zip`
- **Windows:** Right-click → Extract All

### Step 2: Open the website
- Double-click `index.html`
- Your website opens in your default browser

### Step 3: It works! ✨
- Try clicking the navigation menu
- View different pages (About, Research, Projects, etc.)

---

## 🎨 What's Changed From Your Old Website

### ✨ **Design Improvements**
- ✅ **Roboto Font** – Professional, clean typography (no more Cormorant Garamond serif)
- ✅ **Lighter Background** – Pure white/very light gray (#fafafa) instead of beige
- ✅ **Modern Colors** – Bright blue accent (#2563eb) with better contrast
- ✅ **Card-based Layout** – Projects and entries are now in elegant cards with hover effects
- ✅ **Better Spacing** – More breathing room, cleaner visual hierarchy

### 🎯 **Functional Improvements**
- ✅ **Multi-page Navigation** – Switch between sections seamlessly (no scrolling long pages)
- ✅ **Side-by-Side Layout** – Photo on left, bio on right (cleaner About page)
- ✅ **Project Media Support** – Add images/videos to projects easily
- ✅ **Document Links** – Quick access to CV and transcripts from About page
- ✅ **Responsive Design** – Perfect on mobile, tablet, and desktop
- ✅ **Zero Dependencies** – Pure HTML/CSS/JavaScript, no build process

### 📝 **Content Updates**
- ✅ **Updated Bio** – Uses your new description emphasizing research breadth
- ✅ **New Research Interests Page** – Dedicated section explaining your focus areas
- ✅ **Expanded Projects** – Projects now display in modern cards with tags
- ✅ **Better Organization** – Separate pages for Experience, Education, Skills

---

## ⚙️ How to Customize

### Quick Changes (Use Ctrl+F to find and replace)

#### 1. Change Your Name
```
Find: Adithyaa Rettaikudi Gurumoorthi
Replace with: Your Name
```

#### 2. Change Your Tagline
```
Find: Robotics • Machine Learning • AI Systems
Replace with: Your Fields Here
```

#### 3. Update Email
```
Find: mailto:adithyaa.off@gmail.com
Replace with: mailto:your.email@gmail.com
```

#### 4. Update LinkedIn Profile
```
Find: https://www.linkedin.com/in/adithyaa-rg
Replace with: https://www.linkedin.com/in/your-profile
```

#### 5. Update GitHub Profile
```
Find: https://github.com/adithyaa-rg
Replace with: https://github.com/your-username
```

### In-Depth Changes

**For detailed customization instructions:**
- Read `README.md` (complete guide with all sections)
- Read `QUICK_START.md` (common tasks quick reference)

---

## 🖼️ Adding Your Profile Photo

### The Easy Way:

1. **Save your photo** as `profile.jpg` in the `assets/` folder
2. **Open `index.html`** in a text editor
3. **Find line ~440** with `id="profilePhoto"`
4. **Replace:**
   ```html
   <!-- Old (with placeholder) -->
   <img src="data:image/svg+xml,..." alt="Adithyaa" class="profile-photo" id="profilePhoto">
   
   <!-- New (with your photo) -->
   <img src="assets/profile.jpg" alt="Your Name" class="profile-photo" id="profilePhoto">
   ```
5. **Save and refresh browser** (Ctrl+Shift+R)

### Using an Online Photo:
```html
<img src="https://example.com/your-photo.jpg" alt="Your Name" class="profile-photo">
```

---

## 📸 Adding Project Images/Videos

### Add a Project Image:

1. **Save image** as `project-name.jpg` in `assets/` folder
2. **Find the project card** in index.html
3. **Replace placeholder with:**
   ```html
   <div class="project-media">
       <img src="assets/project-name.jpg" alt="Project Name">
   </div>
   ```

### Add a Project Video:

1. **Save video** as `demo.mp4` in `assets/` folder
2. **Replace image with:**
   ```html
   <div class="project-media">
       <video controls>
           <source src="assets/demo.mp4" type="video/mp4">
       </video>
   </div>
   ```

### Add YouTube Video:

```html
<div class="project-media">
    <iframe width="100%" height="200" 
        src="https://www.youtube.com/embed/VIDEO_ID" 
        frameborder="0" allowfullscreen></iframe>
</div>
```

---

## 📄 Managing Documents (CV & Transcripts)

Your documents are already linked! They're in the `documents/` folder:

- `Academic_CV_Adithyaa.pdf` – Linked from About page
- `IITM_Transcript.pdf` – Linked from About page
- `KTH_Transcript.pdf` – Linked from About page

### To Update a Document:

1. Replace PDF file in `documents/` folder (keep filename same)
2. Or change the filename and update the link in index.html:

```html
<!-- Find this line (around line 450) -->
<a href="documents/Academic_CV_Adithyaa.pdf" class="doc-link">📄 CV</a>

<!-- Update filename if needed -->
<a href="documents/NewCV.pdf" class="doc-link">📄 CV</a>
```

### To Add a New Document Link:

```html
<a href="documents/filename.pdf" class="doc-link" target="_blank">📄 Document Name</a>
```

---

## 🎨 Changing the Theme Color

### Find the Color Settings

Open `index.html`, go to top of file, find:

```css
:root {
    --accent: #2563eb;        /* Blue - change this */
    --accent-dark: #1e40af;   /* Darker blue - change this */
    ...
}
```

### Change to Your Color

Find a hex code you like at [colorhexa.com](https://colorhexa.com)

**Examples:**
- **Purple:** `#7c3aed` / `#6d28d9`
- **Green:** `#059669` / `#047857`
- **Red:** `#dc2626` / `#b91c1c`
- **Orange:** `#f97316` / `#ea580c`

Replace both `--accent` colors and refresh browser.

---

## 🔗 Update Research Interests Section

The Research page explains your research areas. It's organized in sections.

### To Update a Research Area:

1. Find `<div id="research" class="page">` (around line 490)
2. Look for the research section:
   ```html
   <div class="section">
       <div class="section-title">Imitation Learning</div>
       <div class="entry">
           <p class="entry-description">
               Your description...
           </p>
           <div class="entry-tags">
               <span class="tag">Tag1</span>
               <span class="tag">Tag2</span>
           </div>
       </div>
   </div>
   ```

3. Update:
   - `<div class="section-title">` → Research area name
   - `<p class="entry-description">` → Your description
   - `<span class="tag">` → Keywords/skills

---

## 💼 Update Work Experience

### Find It:
Around line 620, look for `<div class="section-title">Work Experience</div>`

### Format for Each Job:
```html
<div class="entry">
    <div class="entry-header">
        <div>
            <div class="entry-title">Your Job Title</div>
            <div class="entry-subtitle">Company, Location</div>
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

**To add a new job:** Copy this entire block and update all fields.

---

## 🎓 Update Education Section

### Find It:
Around line 700, look for `<div id="education" class="page">`

### Update Education Cards:
```html
<div class="education-card">
    <div class="education-degree">DEGREE TYPE</div>
    <div class="education-institution">University Name</div>
    <div class="education-details">
        <strong>Program Name</strong><br>
        <strong>CGPA:</strong> X.XX / Y.YY<br>
        <strong>Duration:</strong> Month Year – Month Year
    </div>
    <a href="documents/TranscriptFile.pdf" class="education-cta" target="_blank">View Transcript →</a>
</div>
```

**Make sure:**
- PDF filename is correct
- File exists in `documents/` folder

---

## 🔧 Update Projects

### Find It:
Around line 530, look for `<div id="projects" class="page">`

### Each Project Card Has:
```html
<div class="project-card">
    <!-- Image/Video -->
    <div class="project-media">
        <img src="assets/image.jpg" alt="Project">
    </div>
    
    <div class="project-content">
        <div class="project-title">Project Name</div>
        <div class="project-subtitle">Role / Type</div>
        <p class="project-description">Description...</p>
        <div class="project-meta">
            <span>Dates</span>
            <span>Organization</span>
        </div>
        <div class="project-tags">
            <span class="tag">Tech1</span>
            <span class="tag">Tech2</span>
        </div>
        <a href="#" class="project-link">View Details</a>
    </div>
</div>
```

**To edit:** Update title, description, dates, organization, add image/video, update tags.

---

## 📱 Testing on Different Devices

### Test Mobile:
- **Chrome DevTools:** F12 → Click phone icon → Select device
- **Real Phone:** Open in browser or send link
- **Test these:** 
  - Navigation menu responsive?
  - Images scale properly?
  - Text readable?
  - All links working?

### Test Responsiveness:
Resize browser window – layout should adapt smoothly at:
- 1200px+ (desktop)
- 768px–1199px (tablet)
- < 768px (mobile)

---

## 🚀 Deploy Your Website

### Option 1: GitHub Pages (Best for developers)
```bash
# 1. Create repo: username.github.io
# 2. Upload files
# 3. Site goes live: https://username.github.io
```

### Option 2: Netlify (Easiest, recommended)
1. Go to [netlify.com](https://netlify.com)
2. Drag & drop your folder
3. Auto-deploys on GitHub push
4. Free hosting ✨

### Option 3: Vercel (Excellent performance)
1. Go to [vercel.com](https://vercel.com)
2. Connect GitHub or upload
3. Deploy instantly

### Option 4: Any Web Host
- Upload via FTP/SSH
- Point domain to server
- Done!

---

## 🐛 Troubleshooting

| Problem | Solution |
|---------|----------|
| Changes not showing | Hard refresh: Ctrl+Shift+R (Cmd+Shift+R) |
| Image not loading | Check filename, ensure in `assets/` folder |
| PDF won't open | Verify PDF in `documents/` folder, check href |
| Link broken | Check URL is correct, open in new tab |
| Color wrong | Clear browser cache, refresh page |
| Mobile looks weird | Test in DevTools, check media queries |

---

## ✅ Pre-Launch Checklist

Before sharing/deploying:

- [ ] Profile photo added and displays
- [ ] Name and contact info updated
- [ ] Email link working
- [ ] LinkedIn URL correct
- [ ] GitHub URL correct
- [ ] Bio updated with your info
- [ ] Research interests personalized
- [ ] Projects descriptions accurate
- [ ] Work experience dates correct
- [ ] Education info updated
- [ ] Transcripts linked and working
- [ ] All PDFs in `documents/` folder
- [ ] Skills section reflects your expertise
- [ ] Footer shows current year
- [ ] Tested on mobile phone
- [ ] All links clickable and working
- [ ] No broken images
- [ ] Theme colors look good

---

## 📖 Where to Find Help

### For Common Tasks:
→ **Read `QUICK_START.md`** (quick reference with examples)

### For Complete Guide:
→ **Read `README.md`** (comprehensive documentation)

### Specific Areas:
- **Profile photo:** QUICK_START.md → "Add profile photo"
- **Colors:** README.md → "Customize Colors"
- **Projects:** QUICK_START.md → "Add a Project"
- **Deployment:** README.md → "Deployment Options"

---

## 💡 Pro Tips

1. **Use Ctrl+F to find text** – Easiest way to locate things to edit
2. **Keep backups** – Save old versions before major changes
3. **Test locally first** – Always refresh in browser before deploying
4. **Version control** – Use Git to track changes
5. **Comment your changes** – Mark what you modified with `<!-- comment -->`
6. **Update footer date** – Change "Last updated" when you make changes
7. **Optimize images** – Compress before adding to reduce file size
8. **Write good alt text** – Helps accessibility and SEO

---

## 🎯 Suggested First Changes

1. **Add your profile photo** (5 min)
2. **Update your name** (1 min)
3. **Update contact links** (5 min)
4. **Personalize bio** (10 min)
5. **Update research interests** (15 min)
6. **Add/update projects** (20 min)
7. **Deploy to web** (5-10 min)

**Total time:** ~1 hour to have a polished, live website!

---

## 📞 Still Need Help?

### Check These First:
1. `QUICK_START.md` – 90% of questions answered here
2. `README.md` – Complete detailed guide
3. Browser DevTools (F12) – Check Console for errors
4. Search within files (Ctrl+F) – Find exact line to edit

### Common Issues:
- **Images not showing:** Make sure file is in `assets/` folder
- **PDFs not opening:** File must be in `documents/` folder with exact name
- **Formatting looks wrong:** Hard refresh browser (Ctrl+Shift+R)
- **Colors not changing:** Check both `--accent` and `--accent-dark`

---

## 🎉 You're All Set!

Your modern, professional website is ready to:
- ✅ Showcase your work
- ✅ Share your research
- ✅ Impress employers/collaborators
- ✅ Be easily maintained

**Next steps:**
1. Extract the zip
2. Open `index.html`
3. Follow `QUICK_START.md` for first changes
4. Deploy to the web
5. Share with the world!

---

**Happy customizing!** 🚀

*Questions? Check the README.md or QUICK_START.md first—they have detailed examples.*

**Version:** 1.0 | **Date:** September 2026
