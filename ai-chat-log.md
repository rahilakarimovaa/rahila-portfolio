# Subtle button shadows and hover effect
_Exported on 12/14/2025 at 20:54:24 GMT+4 from Cursor (2.2.20)_

---

**User**


Add a subtle shadow under buttons on both the Home and About pages using CSS.  
Use a soft `box-shadow` that looks clean and minimal, and apply the same style to all buttons for consistency.  
Include a hover effect that slightly increases the shadow to improve interactivity without changing layout.

---

**Cursor**


Reviewing the CSS and locating the Home and About pages to identify button styles.



Checking the Home page for buttons:



Updating the CSS to add a subtle, minimal shadow to all buttons with a hover effect. Both pages use the `.btn` class, so updating that will apply the style consistently.


```css
html, body {
  height: 100%;
}

body {
  margin: 0;
  font-family: Georgia, serif;
  background: #faf6f4;
  color: #2b2b2b;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.navbar {
  background: #f1e4df;
  padding: 18px 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  text-decoration: none;
  font-size: 30px;
  color: #6f7b7a;
  font-weight: 500;
}

.nav-right a {
  margin-left: 22px;
  text-decoration: none;
  color: #6f7b7a;
  font-size: 18px;
}
main {
  flex: 1;
}
.hero {
  background: #faf6f4;
  padding: 70px 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-text h1 {
  font-size: 54px;
  line-height: 1.08;
  color: #5b2c6f;
  margin: 0 0 22px 0;
}

.hero-text p {
  font-size: 18px;
  line-height: 1.7;
  max-width: 650px;
  color: #3a3a3a;
  margin: 0px;
}
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  margin-top: 26px;
  padding: 14px 28px;

  background: #5f7a74;
  color: #ffffff;
  text-decoration: none;

  border-radius: 999px;
  border: 0;
  font-size: 18px;
  font-weight: 600;

  transition: transform 180ms ease, box-shadow 180ms ease, background-color 180ms ease;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
  background: #4f6863;
}

.btn:active {
  transform: translateY(0px);
}
.site-footer,
footer {
  background: #f1e4df;
  padding: 26px 20px;
  text-align: center;
  margin: 0;
}

.footer-icons {
  font-size: 22px;
  margin-bottom: 10px;
}

.footer-icons a {
  text-decoration: none;
  margin: 0 10px;
}
@media (max-width: 900px) {
  .navbar { padding: 16px 24px; }
  .hero { flex-direction: column; padding: 40px 24px; text-align: center; }
  .hero-text h1 { font-size: 34px; }
}
main.hero {
  flex: 1;
}
.footer {
  margin-top: auto;
}
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-image {
  flex: 0 0 auto;
  width: 320px;       /* desktop portrait size */
  max-width: 45%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-pic {
  width: 380%;
  max-width: 380px;
  height: auto;
  aspect-ratio: 1/1;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}
@media (max-width: 900px) {
  .hero {
    flex-direction: column;
    text-align: center;
  }
  .hero-image { max-width: 70%; width: 70%; margin: 0 auto; }
  .profile-pic { max-width: 220px; }
}



```


Checking for linting errors:



Updated the button shadows in your CSS. Changes:

1. **Default shadow**: Changed from `0 10px 22px rgba(0,0,0,0.10)` to `0 2px 8px rgba(0, 0, 0, 0.08)` for a subtler look
2. **Hover shadow**: Changed from `0 16px 32px rgba(0,0,0,0.14)` to `0 4px 12px rgba(0, 0, 0, 0.12)` for a slight increase on hover

The existing transition ensures the shadow change is smooth. Since both the Home and About pages use the `.btn` class, all buttons now have consistent, minimal shadows with a subtle hover effect.

The shadow is subtle and won't affect layout, and the hover provides clear feedback.

---

**User**

Add modern animated button interactions using CSS.

On hover:
- smoothly lift the button upward
- increase box-shadow for a floating effect

On active (click):
- slightly scale the button down
- reduce shadow to simulate a press

Use smooth ease-in-out transitions.
Apply this animation to all existing buttons without changing layout or colors.


---

**Cursor**


Reviewing the current button styles, then adding hover and active animations.



Updating button styles to add smooth hover and active animations:


```css
html, body {
  height: 100%;
}

body {
  margin: 0;
  font-family: Georgia, serif;
  background: #faf6f4;
  color: #2b2b2b;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.navbar {
  background: #f1e4df;
  padding: 18px 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  text-decoration: none;
  font-size: 30px;
  color: #6f7b7a;
  font-weight: 500;
}

.nav-right a {
  margin-left: 22px;
  text-decoration: none;
  color: #6f7b7a;
  font-size: 18px;
}
main {
  flex: 1;
}
.hero {
  background: #faf6f4;
  padding: 70px 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-text h1 {
  font-size: 54px;
  line-height: 1.08;
  color: #5b2c6f;
  margin: 0 0 22px 0;
}

.hero-text p {
  font-size: 18px;
  line-height: 1.7;
  max-width: 650px;
  color: #3a3a3a;
  margin: 0px;
}
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  margin-top: 26px;
  padding: 14px 28px;

  background: #5f7a74;
  color: #ffffff;
  text-decoration: none;

  border-radius: 999px;
  border: 0;
  font-size: 18px;
  font-weight: 600;

  transition: transform 250ms ease-in-out, box-shadow 250ms ease-in-out, background-color 250ms ease-in-out;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
  background: #4f6863;
}

.btn:active {
  transform: translateY(-2px) scale(0.98);
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.06);
}
.site-footer,
footer {
  background: #f1e4df;
  padding: 26px 20px;
  text-align: center;
  margin: 0;
}

.footer-icons {
  font-size: 22px;
  margin-bottom: 10px;
}

.footer-icons a {
  text-decoration: none;
  margin: 0 10px;
}
@media (max-width: 900px) {
  .navbar { padding: 16px 24px; }
  .hero { flex-direction: column; padding: 40px 24px; text-align: center; }
  .hero-text h1 { font-size: 34px; }
}
main.hero {
  flex: 1;
}
.footer {
  margin-top: auto;
}
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-image {
  flex: 0 0 auto;
  width: 320px;       /* desktop portrait size */
  max-width: 45%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-pic {
  width: 380%;
  max-width: 380px;
  height: auto;
  aspect-ratio: 1/1;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}
@media (max-width: 900px) {
  .hero {
    flex-direction: column;
    text-align: center;
  }
  .hero-image { max-width: 70%; width: 70%; margin: 0 auto; }
  .profile-pic { max-width: 220px; }
}



```


Refining the active state to better simulate a press: scaling down without translateY to avoid layout shifts.


```css
html, body {
  height: 100%;
}

body {
  margin: 0;
  font-family: Georgia, serif;
  background: #faf6f4;
  color: #2b2b2b;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.navbar {
  background: #f1e4df;
  padding: 18px 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  text-decoration: none;
  font-size: 30px;
  color: #6f7b7a;
  font-weight: 500;
}

.nav-right a {
  margin-left: 22px;
  text-decoration: none;
  color: #6f7b7a;
  font-size: 18px;
}
main {
  flex: 1;
}
.hero {
  background: #faf6f4;
  padding: 70px 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-text h1 {
  font-size: 54px;
  line-height: 1.08;
  color: #5b2c6f;
  margin: 0 0 22px 0;
}

.hero-text p {
  font-size: 18px;
  line-height: 1.7;
  max-width: 650px;
  color: #3a3a3a;
  margin: 0px;
}
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  margin-top: 26px;
  padding: 14px 28px;

  background: #5f7a74;
  color: #ffffff;
  text-decoration: none;

  border-radius: 999px;
  border: 0;
  font-size: 18px;
  font-weight: 600;

  transition: transform 250ms ease-in-out, box-shadow 250ms ease-in-out, background-color 250ms ease-in-out;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
}

.btn:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.12);
  background: #4f6863;
}

.btn:active {
  transform: translateY(-4px) scale(0.97);
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.06);
}
.site-footer,
footer {
  background: #f1e4df;
  padding: 26px 20px;
  text-align: center;
  margin: 0;
}

.footer-icons {
  font-size: 22px;
  margin-bottom: 10px;
}

.footer-icons a {
  text-decoration: none;
  margin: 0 10px;
}
@media (max-width: 900px) {
  .navbar { padding: 16px 24px; }
  .hero { flex-direction: column; padding: 40px 24px; text-align: center; }
  .hero-text h1 { font-size: 34px; }
}
main.hero {
  flex: 1;
}
.footer {
  margin-top: auto;
}
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-image {
  flex: 0 0 auto;
  width: 320px;       /* desktop portrait size */
  max-width: 45%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-pic {
  width: 380%;
  max-width: 380px;
  height: auto;
  aspect-ratio: 1/1;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}
@media (max-width: 900px) {
  .hero {
    flex-direction: column;
    text-align: center;
  }
  .hero-image { max-width: 70%; width: 70%; margin: 0 auto; }
  .profile-pic { max-width: 220px; }
}



```


Added animated button interactions. Changes:

1. **Smooth transitions**: Changed from `ease` to `ease-in-out` with 250ms duration for smoother animations
2. **Hover effect**: 
   - Lifts upward with `translateY(-4px)`
   - Increases shadow for a floating effect
3. **Active (click) effect**:
   - Scales down to `scale(0.97)`
   - Reduces shadow to simulate a press
   - Maintains the hover lift position while adding the press effect

All buttons now use these animations. The transitions are smooth, and the effects don't change layout or colors—only transform and shadow. The active state combines the hover lift with a slight scale-down to create a press effect.

---

**User**

Add a smooth animated button effect similar to modern portfolio websites.

Requirements:
- Apply animation to all primary buttons on Home and About pages
- On hover:
  - Button slightly moves up (translateY)
  - Soft shadow appears under the button
  - Background color transitions smoothly
- On click:
  - Button slightly scales down for feedback
- Animation must be subtle, clean, and professional
- Use only CSS (no JavaScript)
- Reuse existing button classes if possible
- Ensure animation works consistently across Home and About pages

Update only the CSS and do not break existing layout or styles.


---

**Cursor**


Reviewing the current CSS to enhance button animations:



Refining button animations for a more subtle, professional effect:


```css
html, body {
  height: 100%;
}

body {
  margin: 0;
  font-family: Georgia, serif;
  background: #faf6f4;
  color: #2b2b2b;

  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
.navbar {
  background: #f1e4df;
  padding: 18px 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.brand {
  text-decoration: none;
  font-size: 30px;
  color: #6f7b7a;
  font-weight: 500;
}

.nav-right a {
  margin-left: 22px;
  text-decoration: none;
  color: #6f7b7a;
  font-size: 18px;
}
main {
  flex: 1;
}
.hero {
  background: #faf6f4;
  padding: 70px 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-text h1 {
  font-size: 54px;
  line-height: 1.08;
  color: #5b2c6f;
  margin: 0 0 22px 0;
}

.hero-text p {
  font-size: 18px;
  line-height: 1.7;
  max-width: 650px;
  color: #3a3a3a;
  margin: 0px;
}
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;

  margin-top: 26px;
  padding: 14px 28px;

  background: #5f7a74;
  color: #ffffff;
  text-decoration: none;

  border-radius: 999px;
  border: 0;
  font-size: 18px;
  font-weight: 600;

  transition: transform 300ms cubic-bezier(0.4, 0, 0.2, 1), 
              box-shadow 300ms cubic-bezier(0.4, 0, 0.2, 1), 
              background-color 300ms cubic-bezier(0.4, 0, 0.2, 1);
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
  cursor: pointer;
}

.btn:hover {
  transform: translateY(-3px);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.12);
  background: #4f6863;
}

.btn:active {
  transform: translateY(-1px) scale(0.98);
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.08);
  transition: transform 100ms cubic-bezier(0.4, 0, 0.2, 1), 
              box-shadow 100ms cubic-bezier(0.4, 0, 0.2, 1);
}
.site-footer,
footer {
  background: #f1e4df;
  padding: 26px 20px;
  text-align: center;
  margin: 0;
}

.footer-icons {
  font-size: 22px;
  margin-bottom: 10px;
}

.footer-icons a {
  text-decoration: none;
  margin: 0 10px;
}
@media (max-width: 900px) {
  .navbar { padding: 16px 24px; }
  .hero { flex-direction: column; padding: 40px 24px; text-align: center; }
  .hero-text h1 { font-size: 34px; }
}
main.hero {
  flex: 1;
}
.footer {
  margin-top: auto;
}
.hero {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 60px;
}

.hero-image {
  flex: 0 0 auto;
  width: 320px;       
  max-width: 45%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-pic {
  width: 380%;
  max-width: 380px;
  height: auto;
  aspect-ratio: 1/1;
  border-radius: 50%;
  object-fit: cover;
  display: block;
}
@media (max-width: 900px) {
  .hero {
    flex-direction: column;
    text-align: center;
  }
  .hero-image { max-width: 70%; width: 70%; margin: 0 auto; }
  .profile-pic { max-width: 220px; }
}



```


Updated button animations for a more subtle, professional effect. Changes:

1. **Smooth transitions**: Using `cubic-bezier(0.4, 0, 0.2, 1)` for smoother motion
2. **Hover effect**:
   - Moves up with `translateY(-3px)`
   - Soft shadow: `0 6px 20px rgba(0, 0, 0, 0.12)`
   - Background color transitions smoothly
3. **Click (active) effect**:
   - Scales down to `scale(0.98)`
   - Faster transition (100ms) for immediate feedback
   - Slight upward position maintained
4. **UX**: Added `cursor: pointer` for better interactivity

All buttons on the Home and About pages (using the `.btn` class) now have consistent animations. The effects are subtle and don't affect layout or existing styles.

# About Me page content cleanup
_Exported on 12/19/2025 at 22:06:14 GMT+4 from Cursor (2.2.20)_

---

**User**

Open about.md (or about.markdown) and ensure there is only ONE <main class="hero" id="about"> block. Remove any duplicated “About Me” header/paragraph so the page contains exactly one heading, one subtitle, one .about-grid, and one button. Do not change the navbar or footer.

---

**Cursor**


Searching for about.md or about.markdown.



Reading about.markdown to check its structure:



Checking for duplicate "About Me" headers or main blocks:



The file already has exactly one of each element:

- One `<main class="hero" id="about">` block (line 23)
- One "About Me" heading (line 25)
- One subtitle paragraph (lines 27-29)
- One `.about-grid` section (lines 31-51)
- One button (line 53)

The navbar and footer are unchanged. No duplicates found. The structure is correct as-is.

---

**User**

Update about.markdown to keep the current text content but improve layout.

Wrap Education, Scores, Activities, and Hobbies into a two-column grid layout using HTML inside Markdown.

Each section should be inside a div with class "info-card".

Center the grid on the page and ensure everything fits within one screen height.

Do not change the wording of the content.
Do not modify navigation, footer, or other pages.


---

**Cursor**


Checking the current structure and CSS to update the layout.



Updating the HTML to use `info-card` and adjusting CSS for a centered two-column grid that fits on one screen. Changing the card class names:


```markdown
    <section class="about-grid">
      <div class="info-card">
        <h3>Education</h3>
        <p>ADA University — first-year Bachelor student in Computer Science.</p>
      </div>

      <div class="info-card">
        <h3>Scores</h3>
        <p>SAT 1380 · IELTS 7.0 · DIM 230</p>
      </div>

      <div class="info-card">
        <h3>Activities</h3>
        <p>Volunteering, academic participation, and personal projects.</p>
      </div>

      <div class="info-card">
        <h3>Hobbies</h3>
        <p>Drawing, swimming, travelling.</p>
      </div>
    </section>
```


Adding CSS for `info-card` and adjusting spacing to ensure the content fits within one screen height:


```css
.about-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  margin: 24px auto 28px auto;
  max-width: 700px;
}

.about-card {
  background: #ffffff;
  border-radius: 20px;
  padding: 30px 26px;
  box-shadow: 0 14px 30px rgba(0, 0, 0, 0.06);
}

.about-card h2 {
  margin: 0 0 12px 0;
  font-size: 22px;
  color: #5b2c6f;
  text-align: center;
}


.about-card p {
  margin: 0;
  font-size: 16px;
  line-height: 1.6;
  color: #3a3a3a;
}

.info-card {
  background: #ffffff;
  border-radius: 20px;
  padding: 24px 22px;
  box-shadow: 0 14px 30px rgba(0, 0, 0, 0.06);
}

.info-card h3 {
  margin: 0 0 10px 0;
  font-size: 20px;
  color: #5b2c6f;
  text-align: center;
}

.info-card p {
  margin: 0;
  font-size: 16px;
  line-height: 1.6;
  color: #3a3a3a;
}
```


Checking the CSS file to ensure the changes were applied correctly:



Adjusting spacing so everything fits within one screen height:


```css
.about-subtitle {
  max-width: 720px;
  margin: 0 auto 24px auto;
  font-size: 18px;
  line-height: 1.7;
  color: #3a3a3a;
}
```

```css
#about .btn {
  margin-top: 20px;
}
```


Adjusting the hero section padding for the about page to ensure it fits within one screen height:



Adding specific CSS for the about page to reduce padding and ensure it fits within one screen height:


```css
#about.hero {
  padding: 40px 60px;
  justify-content: center;
}

#about .btn {
  margin-top: 20px;
}
```


Checking for styling issues and ensuring the about-wrap container is centered:



Adding CSS for the about-wrap container to ensure proper centering:


```css
.about-wrap {
  width: 100%;
  max-width: 900px;
  margin: 0 auto;
  text-align: center;
}

.about-header {
  font-size: 52px;
  color: #5b2c6f;
  margin-bottom: 14px;
}
```


## Changes Made:

1. **Updated HTML structure**: Changed all `about-card` classes to `info-card` for the four sections (Education, Scores, Activities, Hobbies).

2. **Added CSS for `info-card`**: Added styling that matches the original design with appropriate padding and spacing.

3. **Improved grid layout**:
   - The grid already uses two columns (`grid-template-columns: repeat(2, 1fr)`)
   - Added `max-width: 700px` to center the grid
   - Reduced gap from 28px to 20px for tighter spacing

4. **Optimized spacing for single screen height**:
   - Reduced hero section padding from 70px to 40px on the about page
   - Reduced subtitle margin from 36px to 24px
   - Reduced grid margin bottom from 40px to 28px
   - Added `.about-wrap` styling to ensure proper centering

All text content remains unchanged, and the navbar and footer are untouched. The layout is now centered with a two-column grid for the info cards, and spacing is optimized to fit within one screen height.

---

**User**

Only add a card-based layout to the existing About page content.
Do NOT change or remove any existing text

Do NOT change the title, subtitle, button, navbar, footer, or layout

Do NOT modify index.markdown or any other file

Only wrap the existing sections (Education, Scores, Activities, Hobbies) into cards

---

**Cursor**


Checking the current state of about.markdown:



The sections are already wrapped in cards with the `info-card` class. Verifying the CSS to ensure the card styling is correctly applied:



The About page already has the sections wrapped in cards. Here's what's in place:

1. All four sections (Education, Scores, Activities, Hobbies) are wrapped in `<div class="info-card">` elements (lines 33-51)
2. They're organized in a two-column grid using the `about-grid` class
3. The CSS includes card styling with:
   - White background
   - Rounded corners (20px border-radius)
   - Padding (26px 22px)
   - Box shadow for depth

The text content, title, subtitle, button, navbar, and footer are unchanged. The card-based layout is already implemented and should display correctly.

Is there anything specific about the card layout you'd like me to adjust?

---

**User**

Create a Projects page section that matches my site style exactly.

Rules:
- Do NOT change navbar, footer, icons, fonts, colors, or button styles.
- Keep the same layout structure as my About page (about.markdown).
- Only replace the main content section with a “Projects” section made of 3 cards in a 3-column layout (responsive).
- Use the existing card style (same rounded corners, shadows, spacing).
- Each card must have: Title, description (exact text I provide), and a circular image at the bottom of the card.
- Images must be loaded from: /assets/images/project1.jpg, project2.jpg, project3.jpg
- Do NOT open new tabs; keep links internal.

Card content (use EXACT text):
1) Title: How does hardware work?
   Description: A collaborative project where my team and I explored how computer hardware works. We built and tested logic gates like AND, OR, XOR, and NAND to understand how digital circuits process information.

2) Title: Hour of Code
   Description: A fun, beginner-friendly coding project that introduces basic programming concepts through interactive exercises.

3) Title: Personal Website
   Description: A personal website showcasing my skills, projects, and interests, designed with a clean and modern layout. 

---

**Cursor**


Reviewing the About page structure and CSS to match the style for the Projects page.



Checking the existing projects.markdown file:



Creating the Projects page matching the About page structure, with a 3-column grid for the project cards. Adding the necessary CSS:


```markdown
---
layout: default
title: Projects
permalink: /projects/
---

<html lang="en">
<head>
  <meta charset="utf-8">
  <title>Projects – Rahila Karimova</title>
  <link rel="stylesheet" href="{{ '/assets/style.css' | relative_url }}">
</head>
<body>

  <header class="navbar">
    <div class="brand">Rahila Karimova</div>
    <nav class="nav-right" aria-label="Primary navigation">
      <a href="{{ '/' | relative_url }}">Home</a>
      <a href="{{ '/about/' | relative_url }}">About</a>
      <a href="{{ '/projects/' | relative_url }}">Projects</a>
    </nav>
  </header>

  <main class="hero" id="projects">
  <div class="hero-text about-wrap">
    <h1 class="about-header">Projects</h1>

    <section class="projects-grid">
      <div class="project-card">
        <h3>How does hardware work?</h3>
        <p>A collaborative project where my team and I explored how computer hardware works. We built and tested logic gates like AND, OR, XOR, and NAND to understand how digital circuits process information.</p>
        <img src="{{ '/assets/images/project1.jpg' | relative_url }}" alt="How does hardware work?" class="project-image">
      </div>

      <div class="project-card">
        <h3>Hour of Code</h3>
        <p>A fun, beginner-friendly coding project that introduces basic programming concepts through interactive exercises.</p>
        <img src="{{ '/assets/images/project2.jpg' | relative_url }}" alt="Hour of Code" class="project-image">
      </div>

      <div class="project-card">
        <h3>Personal Website</h3>
        <p>A personal website showcasing my skills, projects, and interests, designed with a clean and modern layout.</p>
        <img src="{{ '/assets/images/project3.jpg' | relative_url }}" alt="Personal Website" class="project-image">
      </div>
    </section>
  </div>
</main>



  <footer class="footer" role="contentinfo">
    <div class="footer-icons">
      <a href="mailto:rkarimova25220@ada.edu.az" aria-label="Email">📩</a>
        <a
    href="https://github.com/rahilakarimovaa/rahila-portfolio"
    target="_blank"
    rel="noopener"
    class="github-icon"
    aria-label="GitHub repository"
  >
    🐙
  </a>
      <a
    href="https://www.codecademy.com/profiles/rahilakarimovaa"
    target="_blank"
    rel="noopener"
    class="codecademy-icon"
    aria-label="CodeAcademy profile"
  >
    💻
  </a>
    </div>
    <p>© 2025 Rahila Karimova</p>
  </footer>

</body>
</html>

```


Adding CSS for the Projects page: 3-column grid, project cards, and circular images at the bottom of each card.


```css
#about.hero {
  padding: 60px 60px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 32px;
  text-align: center;
}

#about .hero-text {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#about .btn {
  margin: 18px auto 0;
}

#projects.hero {
  padding: 60px 60px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 32px;
  text-align: center;
}

#projects .hero-text {
  display: flex;
  flex-direction: column;
  align-items: center;
}
```

```css
.projects-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 28px;
  margin: 26px auto 28px auto;
  max-width: 1100px;
}

.project-card {
  background: #ffffff;
  border-radius: 20px;
  padding: 26px 22px;
  box-shadow: 0 14px 30px rgba(0, 0, 0, 0.06);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.project-card h3 {
  margin: 0 0 12px 0;
  font-size: 22px;
  color: #5b2c6f;
  text-align: center;
}

.project-card p {
  margin: 0 0 20px 0;
  font-size: 16px;
  line-height: 1.6;
  color: #3a3a3a;
  text-align: center;
  flex: 1;
}

.project-image {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  display: block;
  margin-top: auto;
}

@media (max-width: 900px) {
  .about-header {
    font-size: 36px;
  }

  .about-grid {
    grid-template-columns: 1fr;
  }

  .projects-grid {
    grid-template-columns: 1fr;
  }

  #projects.hero {
    padding: 40px 24px;
  }
}
```


Verifying the Projects page structure and checking for any responsive adjustments:



Verifying the image CSS is correctly applied:



Ensuring the image is positioned at the bottom of each card:


```css
.project-image {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  object-fit: cover;
  display: block;
  margin-top: auto;
}
```


## Created Projects Page

**Structure:**
- Matches the About page layout
- Uses the same navbar and footer (unchanged)
- Same hero section structure with centered content

**3-Column Grid Layout:**
- Desktop: 3 columns
- Mobile (≤900px): 1 column

**Project Cards:**
- Same styling as info cards (white background, 20px border-radius, same shadow and spacing)
- Each card contains:
  - **Title** (h3)
  - **Description** (using your exact text)
  - **Circular image** at the bottom (120px diameter)

**Project Content:**
1. "How does hardware work?" — description included
2. "Hour of Code" — description included
3. "Personal Website" — description included

**Images:**
- Loaded from `/assets/images/project1.jpg`, `project2.jpg`, `project3.jpg`
- Circular (50% border-radius)
- Positioned at the bottom of each card using flexbox

All styling matches your site: same fonts, colors, navbar, footer, and button styles. The page is responsive and ready to use.
