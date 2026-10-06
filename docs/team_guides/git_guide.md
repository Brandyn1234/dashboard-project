# Team Git Guide & Workflow

## 0. Prerequisites & Terminal Setup

Git does not come pre-installed on Windows. You **must** install Git for Windows to run these commands.

### 0.1 Install Git & Recommended Terminal
1. Download **Git for Windows** from [git-scm.com](https://git-scm.com/).
2. Run the installer and use the recommended defaults. 
3. **Recommended Shell:** Use **Git Bash** (installed automatically with Git for Windows). It provides a full Unix terminal environment, shows your active Git branch in color, and supports standard bash commands.
   * *Alternative:* If you prefer Windows Terminal or PowerShell, Git commands will work there too once installed, but Git Bash is strongly recommended to follow this guide 1:1.

### 0.2 Configure Your Git Identity (One-Time Setup)
Open **Git Bash** and configure your username and email so your commits are linked to your GitHub account:

```bash
git config --global user.name "Your Name"
git config --global user.email "your-github-email@example.com"
```

Follow these steps to clone the project to your computer and set up your workspace.

---

## 1. Initial Setup (One-Time Setup)

### Step 1.1: Clone the Repository
Open **Git Bash** (or your preferred terminal), navigate to the directory where you want to keep your project files, and run:

```bash
git clone https://github.com/Brandyn1234/dashboard-project.git
```

### Step 1.2: Enter the Project Folder
```bash
cd dashboard-project
```

**Verification:** Look at your command line prompt in Git Bash. You should see `(main)` highlighted at the end of the line, indicating you are inside the repository and connected to the main branch.


## 2. Daily Workflow (Branching & Pushing) ⚠️ CURRENTLY UNAVAILABLE!

### Step 1:
### Before beginning any work run these commands one at a time to get the latest version of main:
1. `git checkout main`
2. `git pull origin main`

### Now create your own branch to build your feature:
3. `git checkout -b feature/<feature-name>`

**Example:** If you are working on the drone schedule, replace <feature-name> with drone-schedule
* `git checkout -b feature/drone-schedule`

---

### Step 2: Save and Push Your Work to GitHub ⚠️ CURRENTLY UNAVAILABLE!

You can now make changes to the project and build your feature.

**Checklist to Save and Push:**
1. `git status` (review which files you changed or created)
2. `git add <files>` (or `git add .` to stage all changes)
3. `git commit -m "brief explanation of what you did"`
4. `git push -u origin feature/<feature-name>`

**Example push before taking a break or opening a PR:**
* `git push -u origin feature/drone-schedule`
