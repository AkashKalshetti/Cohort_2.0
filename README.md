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

