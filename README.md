# Cohort_2.0

# Git & GitHub Cheat Sheet
## 🔧 Configuration
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
git config --list

## 📁 Repository Setup
git init                    # Initialize a new repo
git clone <repo-url>        # Clone an existing repo

## 📄 Checking Status & History
git status                  # Check working tree status
git log                     # Commit history
git log --oneline --graph   # Compact visual history

## ➕ Staging & Committing
git add <file>              # Stage a file
git add .                   # Stage all changes
git commit -m "message"     # Commit staged changes
git commit -am "message"    # Add & commit tracked files

## 🌿 Branching
git branch                  # List branches
git branch <name>           # Create new branch
git checkout <name>         # Switch branch
git checkout -b <name>      # Create & switch branch
git branch -d <name>        # Delete branch

## 🔀 Merging & Rebasing
git merge <branch>          # Merge branch into current
git rebase <branch>         # Rebase current branch

## 🌍 Remote (GitHub)
git remote -v               # View remotes
git remote add origin <url> # Add remote repo
git push origin <branch>    # Push to remote
git pull origin <branch>    # Pull from remote

## 🔄 Syncing Changes
git fetch                   # Fetch without merging
git pull                    # Fetch + merge
git push                    # Push local commits

## ♻️ Undo & Fix
git restore <file>          # Discard file changes
git restore --staged <file> # Unstage file
git reset --soft HEAD~1     # Undo last commit (keep changes)
git reset --hard HEAD~1     # Undo last commit (discard changes)

## 🧹 Clean Up
git clean -n                # Preview files to delete
git clean -f                # Delete untracked files

## 🏷️ Tags
git tag                     # List tags
git tag <tag-name>          # Create tag
git push origin <tag-name>  # Push tag

## 🚀 Common Workflow
git checkout -b feature-x
git add .
git commit -m "Add feature X"
git push origin feature-x

## 🧠 Helpful Tips
* Commit often with **clear messages**
* Pull before pushing to avoid conflicts
* Use branches for features & fixes
* Never commit secrets 🔒

# How the Internet Works

## Web Evolution
- Web 1.0 → Static, read-only websites
- Web 2.0 → Social, user-generated content
- Web 3.0 → Decentralized, blockchain-based, user-owned data

## Computer Communication
- Every device has an IP address
- Uses TCP/IP protocol
- Data is split into packets
- Packets are reassembled at destination

## Data Travel
- Routers decide best path
- Switches connect local devices
- Undersea cables connect continents
- Internet auto-reroutes on failure

## Identity on the Internet
- Domain Name → Human-friendly address (google.com)
- IP Address → Numeric device/server ID
- MAC Address → Permanent hardware ID
- Routing → Fastest & safest data path

## ISP & DNS
- ISP provides internet access
- DNS converts domain names to IPs

Flow:
google.com → DNS → IP → ISP → Server


# Client-Server Architecture

## Client-Server Model
- Client → Requests data (browser, mobile app)
- Server → Stores, processes, responds with data
- Relationship → Client asks → Server responds

Example:
You request google.com → Server sends webpage

---

## HTTP Request-Response Cycle
1. User enters URL
2. Browser sends HTTP/HTTPS request
3. Server processes request (logic, database)
4. Server sends response (HTML, JSON, images)
5. Browser renders page

---

## What Happens When You Visit a Website
1. Enter website URL
2. DNS converts domain → IP
3. Connect via ISP
4. Browser sends HTTP request
5. Server sends data
6. Browser displays website

---

## Frontend vs Backend

### Frontend (Client-Side)
- Visible UI
- Built with HTML, CSS, JavaScript
- Handles user interaction

### Backend (Server-Side)
- Hidden logic on server
- Handles authentication, databases, APIs

---

## Static vs Dynamic Websites

### Static
- Same content for everyone
- Pre-written HTML
- Fast, limited interactivity

### Dynamic
- Content changes based on user/data
- Uses backend + database

---

## Web Hosting
- Renting server space for your website
- Keeps website online 24/7

### Types of Hosting
- Shared → Multiple sites, cheaper
- VPS/Dedicated → More power, higher cost
- Cloud → Scalable (AWS, Google Cloud, Azure)


# Internet Protocols

## TCP (Transmission Control Protocol)
- Reliable, ordered, error-checked delivery
- Breaks large data into packets
- Resends lost/corrupted packets
- Ensures correct packet order

### TCP 3-Way Handshake
1. SYN → Client: "Can we connect?"
2. SYN-ACK → Server: "Yes, I'm ready."
3. ACK → Client: "Okay, let's start."

(Connection established after handshake)

### Used For
- Web browsing
- Email
- File transfer (FTP)

---

## UDP (User Datagram Protocol)
- Fast, connectionless communication
- No handshake
- No error correction
- No guaranteed packet order
- Low latency

### How UDP Works
Client → Directly sends packets → Server  
(Some packets may be lost)

### Used For
- Video streaming
- Online gaming
- Voice/video calls

---

## TCP vs UDP

| Feature      | TCP | UDP |
|-------------|------|------|
| Connection  | Connection-oriented (3-way handshake) | Connectionless |
| Reliability | Reliable (error checking, resend) | Unreliable |
| Speed       | Slower | Faster |
| Packet Order| Maintains order | May arrive out of order |
| Use Cases   | Web, Email, FTP | Gaming, Streaming, Calls |


# Understanding HTTP & HTTPS

## What is HTTP?
HTTP (HyperText Transfer Protocol) defines how clients (browsers) and servers communicate using requests and responses.

### HTTP Versions
- HTTP/1.0 → New connection for every request (slow)
- HTTP/1.1 → Persistent connections (keep-alive)
- HTTP/2 → Multiplexing, binary protocol, faster
- HTTP/3 → Built on QUIC (UDP), faster & better for real-time apps

---

## HTTP Status Codes

- 1xx → Informational
- 2xx → Success (200 OK)
- 3xx → Redirection (301, 302)
- 4xx → Client Errors (400, 401, 404)
- 5xx → Server Errors (500, 503)

Example:
Wrong URL → 404 Not Found

---

## What is HTTPS?
HTTPS = Secure version of HTTP  
Uses SSL/TLS encryption to protect data.

Prevents:
- Eavesdropping
- Data tampering
- Identity theft

Used for:
- Banking
- Payments
- Login forms

---

## SSL/TLS
Security protocols that ensure:
1. Encryption → Data cannot be read
2. Authentication → Website is genuine
3. Integrity → Data not modified

(TLS is modern & more secure than SSL)

---

## Proxy vs Reverse Proxy

### Proxy
- Between client and internet
- Hides client identity (IP)
- Used for privacy, filtering, accessing blocked content

### Reverse Proxy
- Sits in front of servers
- Hides actual server details
- Used for load balancing, security, caching

---

## VPN (Virtual Private Network)
- Creates secure encrypted tunnel
- Hides real IP/location
- Prevents ISP monitoring
- Useful on public Wi-Fi

Example:
Appears browsing from US even if in India

# Git Explained Simply

## What is Git?
Git is a version control system.
- Tracks file changes over time
- Allows collaboration
- Lets you revert to older versions
- Enables safe experimentation using branches

---

## Core Concepts

- Repository (Repo) → Project folder tracked by Git
- Working Directory → Where you edit files
- Staging Area → Where changes are prepared for commit
- Commit → Snapshot of changes with a message
- Branch → Separate timeline for development
- Remote Repository → Online repo (GitHub, GitLab, Bitbucket)

---

## Basic Setup

git config --global user.name "Your Name"
git config --global user.email "you@email.com"
git init
git clone <repo_url>
git status

---

## Working with Changes

git add <file>
git add .
git commit -m "message"
git diff
git restore <file>
git restore --staged <file>

---

## Viewing History

git log
git log --oneline
git show <commit_hash>

---

## Branching

git branch
git branch <branch_name>
git checkout <branch_name>
git checkout -b <branch_name>
git merge <branch_name>
git branch -d <branch_name>

---

## Remote Repositories

git remote add origin <repo_url>
git remote -v
git push origin <branch_name>
git pull origin <branch_name>
git fetch origin

---

## Good Practices

- Commit frequently
- Write clear commit messages
- Use branches for features/fixes
- Pull before pushing

---

## Typical Workflow

1. Create branch
2. Make changes
3. git add .
4. git commit -m "feature added"
5. git push origin branch-name
6. Merge into main


# HTML Basics

## What is HTML?

HTML (HyperText Markup Language) is the structure of every website.

- Defines layout of text, images, links, and media  
- Helps SEO & accessibility  
- Works on all browsers/devices  
- Styled later using CSS  

---

## Basic HTML Boilerplate

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Page Title</title>
</head>
<body>
  Content goes here
</body>
</html>
```

---

## Headings

```html
<h1>Main Heading</h1>
<h2>Sub Heading</h2>
<h3>Smaller Heading</h3>
```

---

## Paragraph

```html
<p>This is a paragraph.</p>
```

---

## Text Formatting

```html
<b>Bold</b>
<i>Italic</i>
<u>Underline</u>
```

### Superscript & Subscript

```html
H<sup>2</sup>O
CO<sub>2</sub>
```

---

## Lists

### Ordered List

```html
<ol>
  <li>Wake up</li>
  <li>Brush teeth</li>
  <li>Go to work</li>
</ol>
```

### Unordered List

```html
<ul>
  <li>Apples</li>
  <li>Bananas</li>
  <li>Mangoes</li>
</ul>
```

---

## Anchor (Link)

```html
<a href="https://example.com" target="_blank">Visit Website</a>
```

- `href` → Destination URL  
- `target="_blank"` → Opens link in new tab  

---

## Image

```html
<img src="image.png" alt="Description of image">
```

- `src` → Image path  
- `alt` → Alternative text (important for SEO & accessibility)  

---

## Line Break & Horizontal Rule

```html
<br>
<hr>
```

- `<br>` → Line break  
- `<hr>` → Horizontal divider  

(Self-closing tags: `<img>`, `<br>`, `<hr>`)

---

## Comments

```html
<!-- This is a comment -->
```

Comments are not visible in the browser.

---

## Quick Tag Summary

| Tag | Purpose |
|-----|----------|
| `<h1>` – `<h6>` | Headings |
| `<p>` | Paragraph |
| `<b>`, `<i>`, `<u>` | Formatting |
| `<sup>`, `<sub>` | Superscript & Subscript |
| `<ol>`, `<ul>`, `<li>` | Lists |
| `<a>` | Links |
| `<img>` | Images |
| `<br>`, `<hr>` | Line & Divider |
| `<!-- -->` | Comment |

---

# HTML Advanced Concepts

## Performance & Best Practice Tips

- Use `<meta charset="UTF-8">` to prevent weird characters  
- Use viewport meta for responsive design  
- Use `defer` on scripts for faster loading  
- Always provide `alt` in images  
- Use `loading="lazy"` for performance  

---

## Images (Advanced Usage)

```html
<img 
  src="photo.jpg" 
  alt="My Photo" 
  width="300" 
  height="200" 
  loading="lazy"
>
```

### Important Attributes
- `alt` → Accessibility & SEO
- `width` / `height` → Prevent layout shift
- `loading="lazy"` → Better performance
- `srcset` / `<picture>` → Responsive images

---

## Video

```html
<video controls width="640" height="360" poster="poster.jpg">
  <source src="video.mp4" type="video/mp4">
  <track src="captions.vtt" kind="captions" srclang="en">
</video>
```

### Attributes
- `controls`
- `autoplay`
- `muted`
- `loop`
- `poster`

Use `<track>` for captions (accessibility).

---

## Audio

```html
<audio controls preload="auto">
  <source src="song.mp3" type="audio/mpeg">
</audio>
```

Attributes:
- `controls`
- `loop`
- `preload`

Add transcripts for accessibility.

---

## Embedding (iframe)

```html
<iframe 
  src="https://youtube.com/embed/123"
  title="Intro Video"
  width="560"
  height="315"
  loading="lazy"
  sandbox
  allowfullscreen>
</iframe>
```

- `title` → Required for accessibility  
- `sandbox` → Security  
- `loading="lazy"` → Performance  

---

## Collapsible Content

```html
<details>
  <summary>How do refunds work?</summary>
  <p>Refunds within 14 days.</p>
</details>
```

Useful for FAQs and expandable sections.

---

## Dropdowns

```html
<label for="country">Country</label>
<select id="country" name="country">
  <option value="">Select</option>
  <option value="in">India</option>
</select>
```

- `optgroup` → Group options  
- `multiple` → Allow multi-select  

---

## Forms & Inputs

```html
<form action="/signup" method="post">
  <label for="email">Email</label>
  <input type="email" id="email" name="email" required>
  <button type="submit">Sign Up</button>
</form>
```

### Important Attributes
- `action` → Where data goes  
- `method` → GET or POST  
- `name` → Key for backend  
- `required`, `pattern`, `autocomplete`  

---

## Meta Tags (SEO & Social Sharing)

```html
<meta name="description" content="Page description">
<meta property="og:title" content="Page title">
<meta name="twitter:card" content="summary_large_image">
```

Improves SEO and social media previews.

---

## Title & Favicon

```html
<title>Course – Sheryians Coding School</title>
<link rel="icon" type="image/png" href="/favicon.png">
```

---

## Semantic HTML

Instead of generic `<div>`, use semantic tags:

```html
<header></header>
<nav></nav>
<main></main>
<section></section>
<article></article>
<footer></footer>
```

Semantic HTML improves:
- SEO
- Accessibility
- Code readability

---

## Tables

```html
<table>
  <thead>
    <tr>
      <th>Name</th>
      <th>Score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Amy</td>
      <td>92</td>
    </tr>
  </tbody>
</table>
```

---

## Accessibility Checklist

- Use semantic HTML
- Always provide `alt`
- Label forms properly
- Ensure high color contrast
- Make site keyboard accessible

---

## Common Mistakes

- Missing `alt` attribute
- Using `<div>` everywhere
- Forgetting `name` in forms
- Large unoptimized images

# CSS Basics (Day 10)

---

# 1️⃣ What is CSS?

**Definition:**  
CSS (Cascading Style Sheets) styles HTML elements.

**Why It Matters:**  
Without CSS → website looks plain.  
With CSS → layout, colors, fonts, spacing.

**Memory Trigger:**  
HTML = Structure 🧱  
CSS = Design 🎨  

**Quick Recall:**  
CSS = Style + Layout + Presentation

---

# 2️⃣ Why Do We Use CSS?

- Make websites beautiful
- Control layout
- Reusable styling (1 file → many pages)
- Responsive design
- Better UX

**Interview Angle:**  
CSS separates content from presentation.

---

# 3️⃣ Types of CSS

## 1. Inline CSS

```html
<p style="color: red; font-size: 20px;">Inline styled text</p>
```

⚠️ Avoid for large projects.

---

## 2. Internal CSS

```html
<head>
  <style>
    h1 {
      color: blue;
      text-align: center;
    }
  </style>
</head>
```

Used for single-page styling.

---

## 3. External CSS (Best Practice)

```html
<head>
  <link rel="stylesheet" href="style.css">
</head>
```

```css
p {
  color: green;
  font-size: 18px;
}
```

**Memory Trigger:**  
Inline ❌  
Internal ⚠️  
External ✅ (Professional way)

---

# 4️⃣ CSS Syntax

```css
selector {
  property: value;
}
```

Example:

```css
p {
  color: red;
  font-size: 20px;
}
```

**Quick Recall:**  
Selector → Property → Value

---

# 5️⃣ Selecting Elements

## Universal Selector

```css
* {
  margin: 0;
  padding: 0;
}
```

## Tag Selector

```css
h1 {
  color: blue;
}
```

## Class Selector (Reusable)

```css
.highlight {
  color: green;
}
```

## ID Selector (Unique)

```css
#special {
  color: red;
}
```

**Memory Trigger:**  
`.` → Class (Reusable)  
`#` → ID (Unique)

---

# 6️⃣ Text & Color Properties

```css
p {
  color: purple;
  font-size: 18px;
  font-family: Arial, sans-serif;
  font-weight: bold;
  font-style: italic;
  text-align: center;
  text-transform: uppercase;
}
```

**Common Properties:**
- `color`
- `background-color`
- `font-size`
- `font-family`
- `font-weight`
- `text-align`
- `text-transform`

---

# 7️⃣ Fonts

## Google Fonts

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'Poppins', sans-serif;
}
```

---

## Local Font (@font-face)

```css
@font-face {
  font-family: "MyFont";
  src: url("MyFont.woff2") format("woff2");
}

p {
  font-family: "MyFont", sans-serif;
}
```

**Interview Tip:**  
Google Fonts → CDN  
@font-face → Local file hosting

---

# 8️⃣ ID vs Class

```html
<p id="unique">Uses ID</p>
<p class="note">Uses Class</p>
<p class="note">Reusable Class</p>
```

```css
#unique { color: red; }
.note { color: green; }
```

**Golden Rule:**  
ID → One element  
Class → Many elements  

---

# 9️⃣ Div in CSS

```html
<div class="box"></div>
```

```css
.box {
  width: 200px;
  height: 100px;
  background-color: lightblue;
  border: 2px solid blue;
}
```

**Definition:**  
`<div>` = empty container.

**Memory Trigger:**  
Div = Box 📦  
CSS gives it shape & style.

---

# 🔥 Mini Revision Block (30-Second Recall)

- CSS = Styling language
- 3 Types → Inline / Internal / External
- Syntax → selector { property: value; }
- Selectors → * , tag, .class, #id
- Class reusable, ID unique
- External CSS = Professional standard

---

# 🚨 Common Beginner Mistakes

- Using inline CSS everywhere
- Using ID instead of class
- Forgetting external stylesheet link
- Writing CSS without selector

---

# 🎯 Interview Quick Answers

**Q: What does "Cascading" mean?**  
Order of rules decides priority.

**Q: Best type of CSS?**  
External CSS.

**Q: Difference between class & ID?**  
Class reusable, ID unique.

---

# CSS – Div, Backgrounds & Box Model

---

# 1️⃣ What is `<div>`?

**Definition:**  
`<div>` is a generic container that groups elements.

**Key Idea:**  
No visual effect by default → CSS gives it shape & style.

**Memory Trigger:**  
Div = Empty Box 📦  
CSS paints it 🎨

---

## Example

```html
<div class="container">
  <h2>Welcome</h2>
  <p>This is inside a div container.</p>
</div>
```

---

# 2️⃣ Making a Box with `<div>`

```html
<div class="box">Hello World</div>
```

```css
.box {
  width: 200px;
  height: 100px;
  background-color: lightblue;
  border: 2px solid blue;
}
```

**Used For:**
- Cards
- Product listings
- Profile boxes
- Layout sections

---

# 3️⃣ Background Properties

---

## 🎨 Background Color

```css
div {
  background-color: lightgreen;
}
```

Used for:
- Buttons
- Headers
- Sections

---

## 🌈 Linear Gradient

```css
div {
  background: linear-gradient(to right, red, yellow);
}
```

Used for:
- Navigation bars
- Gradient effects

Memory:  
Linear → Straight line

---

## 🔵 Radial Gradient

```css
div {
  background: radial-gradient(circle, blue, white);
}
```

Used for:
- Spotlight effects
- Circular highlights

Memory:  
Radial → Circle from center

---

## 🥧 Conic Gradient

```css
div {
  background: conic-gradient(red, yellow, green, blue);
}
```

Used for:
- Pie-chart style designs

---

## 🖼 Background Image

```css
div {
  background-image: url("pattern.png");
}
```

Used in:
- Hero sections
- Full-width banners

---

## 📏 Background Size

```css
div {
  background-size: cover;
}
```

Options:
- `cover` → fills whole area
- `contain` → fits inside element
- Custom → `100px 200px`

Memory Trick:
Cover = Fill  
Contain = Fit

---

## 📍 Background Position

```css
div {
  background-position: center;
}
```

Options:
- top
- left
- right
- center

---

## 🔁 Background Repeat

```css
div {
  background-repeat: no-repeat;
}
```

Options:
- repeat (default)
- repeat-x
- repeat-y
- no-repeat

---

# 4️⃣ CSS Box Model

Every element is a box:

1. Content → Text / Images  
2. Padding → Inside spacing  
3. Border → Outline  
4. Margin → Outside spacing  

**Visual Memory:**

Margin  
⬜ Border  
⬜ Padding  
⬜ Content  

---

## 📦 Margin (Outside Space)

```css
div {
  margin: 20px;
}
```

Adds space outside the element.

---

## 📦 Padding (Inside Space)

```css
div {
  padding: 15px;
}
```

Adds space inside the element.

Common use: Buttons

---

## 🧱 Border

```css
div {
  border: 1px solid black;
}
```

Styles:
- solid
- dashed
- dotted
- double

---

## 🔵 Border Radius

```css
div {
  border-radius: 15px;
}
```

Rounded corners.

Make circle:

```css
border-radius: 50%;
```

Used for:
- Profile pictures
- Badges

---

# 🔥 30-Second Revision Block

- Div = container box
- Background → color, image, gradient
- Cover = fill area
- Contain = fit inside
- Box Model → Content + Padding + Border + Margin
- Margin = outside space
- Padding = inside space
- border-radius: 50% → circle

---

# 🚨 Common Mistakes

- Confusing margin & padding
- Using background-size incorrectly
- Forgetting no-repeat
- Applying border-radius without width/height

---

# 🎯 Interview Quick Answers

**Q: What is the CSS Box Model?**  
Every element consists of content, padding, border, and margin.

**Q: Difference between margin & padding?**  
Margin = outside space  
Padding = inside space  

**Q: How to make a circle in CSS?**  
Set equal width & height + `border-radius: 50%`

---

# CSS Positioning

---

# 1️⃣ What is CSS Positioning?

**Definition:**  
The `position` property controls how elements are placed and how they interact with surrounding elements.

**Why It Matters:**  
Used to control exact element placement in layouts.

**Common Values:**
- static (default)
- relative
- absolute
- fixed
- sticky

---

# 2️⃣ position: static (Default)

**Definition:**  
Normal document flow.

No top/left/right/bottom effect.

```css
div {
  position: static;
}
```

📌 Rarely written explicitly.

---

# 3️⃣ position: relative

**Definition:**  
Moves element relative to its original position.

```html
<div class="box">Relative Box</div>
```

```css
.box {
  position: relative;
  top: 20px;
  left: 30px;
}
```

🧠 Memory Trigger:  
Relative = Moves from original spot

🎯 Real-life Use:
- Fine-tuning icon placement
- Adjusting spacing slightly

---

# 4️⃣ position: absolute

**Definition:**  
Positions element relative to nearest positioned ancestor.

If no positioned parent → relative to viewport.

```html
<div class="parent">
  <div class="child">Absolute Box</div>
</div>
```

```css
.parent {
  position: relative;
}

.child {
  position: absolute;
  top: 50px;
  left: 50px;
}
```

🧠 Memory Trigger:  
Absolute = Escapes normal flow

🎯 Real-life Use:
- Badges
- Tooltips
- Pop-ups
- Overlays

---

# 5️⃣ position: fixed

**Definition:**  
Fixed relative to viewport.

Stays in place while scrolling.

```css
.fixed-btn {
  position: fixed;
  bottom: 20px;
  right: 20px;
}
```

🧠 Memory Trigger:  
Fixed = Glued to screen

🎯 Real-life Use:
- Chat buttons
- "Back to Top"
- Floating action buttons

---

# 6️⃣ position: sticky

**Definition:**  
Acts like relative → becomes fixed after scroll threshold.

```css
.sticky-header {
  position: sticky;
  top: 0;
}
```

🧠 Memory Trigger:  
Sticky = Scroll → Stick

🎯 Real-life Use:
- Sticky headers
- Navbars
- Sidebar menus

---

# 7️⃣ Position Summary Table

| Type      | Description | Real-Life Use |
|-----------|------------|--------------|
| relative  | Moves from original spot | Fine-tuning placement |
| absolute  | Positioned inside nearest positioned parent | Tooltips, overlays |
| fixed     | Stays fixed to viewport | Chat buttons |
| sticky    | Scroll → becomes fixed | Navbars |

---

# 8️⃣ flex-shrink

**Definition:**  
Controls how flex items shrink when space is limited.

```css
.item {
  flex-shrink: 0;
}
```

🧠 Memory Trigger:  
Shrink = How much it compresses

---

# 9️⃣ :hover (Pseudo-class)

**Definition:**  
Applies style when mouse hovers over element.

```css
button:hover {
  background-color: black;
  color: white;
}
```

🧠 Memory Trigger:  
Hover = Interaction

🎯 Used for:
- Buttons
- Links
- Cards

---

# 🔥 30-Second Revision Block

- static → default
- relative → moves from original
- absolute → inside positioned parent
- fixed → sticks to screen
- sticky → scroll then stick
- flex-shrink → controls shrinking
- :hover → adds interactivity

---

# 🚨 Common Mistakes

- Using absolute without positioned parent
- Forgetting top/left values
- Confusing fixed & sticky
- Not setting top for sticky

---

# 🎯 Interview Quick Answers

**Q: Difference between relative & absolute?**  
Relative moves from original position.  
Absolute removes element from normal flow.

**Q: When does sticky work?**  
When scroll threshold is reached + `top` is defined.

**Q: How to make floating button?**  
Use `position: fixed;`

---

# CSS – Flexbox Deep Recall + GitHub Hosting

---

# 1️⃣ Flexbox Mental Model

Flexbox works on:

Main Axis → Horizontal (default)  
Cross Axis → Vertical  

🧠 Memory Trigger:
Main = justify-content  
Cross = align-items  

---

# 2️⃣ display: flex

```css
.container {
  display: flex;
}
```

✔ Turns block elements into flex items  
✔ Default direction → row  

🎯 Interview Point:
Flexbox is one-dimensional (row OR column).

---

# 3️⃣ align-items (Cross Axis Control)

Controls vertical alignment (default row layout).

```css
.container {
  align-items: center;
}
```

Values:
- flex-start
- flex-end
- center
- stretch (default)

🧠 Quick Trick:
Align = Vertical

---

# 4️⃣ justify-content (Main Axis Control)

Controls horizontal alignment.

```css
.container {
  justify-content: space-between;
}
```

Values:
- flex-start
- flex-end
- center
- space-between
- space-around
- space-evenly

🧠 Quick Trick:
Justify = Horizontal

---

# 5️⃣ gap (Modern Spacing)

```css
.container {
  gap: 20px;
}
```

✔ Cleaner than margin  
✔ Works in flex & grid  

🚨 Avoid:
Using margin on every child unnecessarily.

---

# 6️⃣ Perfect Navbar Layout Example

```css
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 20px;
}
```

This creates:
✔ Vertical centering  
✔ Equal horizontal spacing  
✔ Clean layout  

---

# 7️⃣ Remix Icon (Icon System)

## Step 1: Add CDN

```html
<link href="https://cdn.jsdelivr.net/npm/remixicon/fonts/remixicon.css" rel="stylesheet">
```

## Step 2: Use Icon

```html
<i class="ri-github-fill"></i>
```

🧠 Memory:
`ri-` = Remix Icon  

✔ Lightweight  
✔ No image files needed  

---

# 8️⃣ GitHub Pages (Free Hosting)

---

## Hosting Flow (4-Step Recall Model)

1. Create Account
2. Create Public Repository
3. Upload Files
4. Enable Pages

---

## Enable Pages

GitHub → Settings → Pages  
Select main branch  
Save  

Live URL format:

```
https://username.github.io/repository-name/
```

🎯 Real-World Use:
- Portfolio sites
- Resume websites
- Demo projects

---

# 🔥 30-Second Ultra Recall

Flex = Row by default  
Align = Vertical  
Justify = Horizontal  
Gap = Clean spacing  
Remix = Icon CDN  
GitHub Pages = Free hosting  

---

# 🎯 Interview Deep Questions

Q: Why use flex instead of float?  
A: Flex handles alignment and spacing automatically.

Q: Difference between space-between & space-around?  
A: Between → no space at edges  
Around → equal space on both sides

Q: Can gap replace margin?  
A: Yes, inside flex/grid layouts.

Q: Is GitHub Pages free?  
A: Yes, for public repositories.

---

# 🚨 Common Mistakes

- Forgetting display: flex
- Confusing align-items & justify-content
- Not selecting correct branch in Pages
- Using private repo for free Pages (limitations apply)

---

# 🧠 Engineer-Level Summary

Flexbox = Layout Control System  
Icons = CDN-based UI enhancement  
GitHub Pages = Deployment platform  

Frontend flow:
Build → Style (Flex) → Add Icons → Deploy

---
