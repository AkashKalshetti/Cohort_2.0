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

