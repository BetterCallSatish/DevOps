# 🐙 Complete Git Guide for Satish – Advanced Edition

---

## 1️⃣ Git Basics – Setup & Initial Commit

```bash
# Configure user
git config --global user.name "Satish"
git config --global user.email "satish@example.com"

# Verify configuration
git config --list

# Initialize a new repo
mkdir MyLinuxBlog
cd MyLinuxBlog
git init
```

**Explanation:**

* Sets your identity
* `git init` creates a `.git` folder to track changes

**Add first file & commit:**

```bash
echo "# Satish's Linux Commands" > satish_commands.md
git status
git add satish_commands.md
git commit -m "Add initial Linux commands file"
```

**Git Log:**

```
a1b2c3d (HEAD -> main) Add initial Linux commands file
```

---

## 2️⃣ Common Git Commands

| Command                       | Explanation                 | Example                                |
| ----------------------------- | --------------------------- | -------------------------------------- |
| `git status`                  | Show current changes        | `$ git status`                         |
| `git diff`                    | Show changes before staging | `$ git diff`                           |
| `git add <file>`              | Stage changes               | `$ git add satish_commands.md`         |
| `git commit -m "msg"`         | Commit staged changes       | `$ git commit -m "Add basic commands"` |
| `git log`                     | Show commit history         | `$ git log --oneline`                  |
| `git branch`                  | Show branches               | `$ git branch`                         |
| `git checkout <branch>`       | Switch branch               | `$ git checkout advanced-commands`     |
| `git merge <branch>`          | Merge another branch        | `$ git merge advanced-commands`        |
| `git remote add origin <url>` | Connect remote repo         | `$ git remote add origin <URL>`        |
| `git push`                    | Push commits to remote      | `$ git push -u origin main`            |
| `git pull`                    | Pull changes from remote    | `$ git pull origin main`               |

---

## 3️⃣ Branching Workflows

**Feature Branch Workflow (Recommended):**

```
main ──●────●────●
        \
feature ──●────●
```

**Commands:**

```bash
git branch feature-login
git checkout feature-login
# Make changes
git add .
git commit -m "Add login feature"
git checkout main
git merge feature-login
```

**Explanation:**

* Main branch stays stable
* Features developed in separate branch
* Merge back when complete

---

## 4️⃣ Advanced Commands

### 4.1 Reverting Changes

```bash
# Undo last commit but keep changes staged
git reset --soft HEAD~1

# Undo last commit and discard changes
git reset --hard HEAD~1

# Revert a commit safely
git revert <commit-id>
```

---

### 4.2 Stashing Work

```bash
git stash save "WIP"
git stash list
git stash apply
git stash pop
git stash drop
```

**Explanation:**

* Save unfinished work temporarily
* Switch branches safely

---

### 4.3 Tagging Releases

```bash
git tag -a v1.0 -m "First release"
git push origin v1.0
```

---

### 4.4 Cherry-Pick a Commit

```bash
git checkout main
git cherry-pick <commit-id>
```

**Explanation:**

* Apply a specific commit from another branch
* Useful to bring only important fixes

---

### 4.5 Rebasing Branches

```bash
git checkout feature
git rebase main
```

**Explanation:**

* Reapply commits on top of another branch
* Keeps history **linear and clean**

---

### 4.6 Git Blame & History

```bash
git blame satish_commands.md
git log --stat
git log --graph --oneline --all
```

**Explanation:**

* See **who changed what**
* Track history visually

---

## 5️⃣ Collaboration Workflow

1. **Clone repo**

```bash
git clone https://github.com/Satish/MyLinuxBlog.git
```

2. **Create new feature branch**

```bash
git checkout -b feature-xyz
```

3. **Make changes & commit**

```bash
git add .
git commit -m "Implement xyz"
```

4. **Pull latest changes from main**

```bash
git checkout main
git pull origin main
```

5. **Merge feature branch**

```bash
git checkout main
git merge feature-xyz
```

6. **Push to remote**

```bash
git push origin main
```

---

## 6️⃣ Real-Time Example: Advanced Flow

```bash
# Create project
mkdir MyLinuxBlog && cd MyLinuxBlog && git init

# Add file
echo "# Satish Linux Commands" > satish_commands.md
git add . && git commit -m "Initial commit"

# Create feature branch
git checkout -b feature-advanced

# Add advanced commands
echo "- grep" >> satish_commands.md
echo "- awk" >> satish_commands.md
git add . && git commit -m "Add advanced commands"

# Merge into main
git checkout main
git merge feature-advanced

# Push to GitHub
git remote add origin https://github.com/Satish/MyLinuxBlog.git
git push -u origin main
```

**Resulting File Content:**

```
# Satish Linux Commands
- ls
- cd
- grep
- awk
```

**Branch Diagram:**

```
main ──●────●────●
        \
feature-advanced ──●
```

---

## 7️⃣ Summary – Git Flows

* **Basic Flow:** Add → Commit → Push
* **Feature Flow:** Branch → Commit → Merge → Push
* **Advanced Flow:** Rebase → Cherry-pick → Stash → Tag

**Visualization of Full Workflow:**

```
main ──●────●────●────●
        \
feature-login ──●────●
        \
feature-bugfix ──●
```


