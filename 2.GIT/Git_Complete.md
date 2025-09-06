
# 🐙 Complete Git Guide for Satish

---

## 1️⃣ What is Git?

Git is a **version control system (VCS)** that helps track changes in files and projects over time.

* Created by **Linus Torvalds** in 2005.
* Git is **distributed**, meaning every developer has a full copy of the project history.
* Git allows teams to **collaborate safely**, experiment with new features, and revert mistakes easily.

**Analogy:**
Imagine writing a book — every change is saved as a snapshot. Git lets you **go back to any version at any time**.

---

## 2️⃣ Why Use Git?

* **Track changes**: Keep history of every change.
* **Collaboration**: Multiple developers can work safely on the same project.
* **Experiment safely**: Branches let you test new features without affecting main code.
* **Backup & recovery**: Restore previous versions anytime.
* **Versioning & releases**: Tag versions like v1.0, v2.0.
* **Accountability**: See who changed what and when.

---

## 3️⃣ Advantages of Git

| Advantage           | Explanation                                   |
| ------------------- | --------------------------------------------- |
| Distributed         | Every developer has full history locally      |
| Fast                | Most commands run locally                     |
| Branching & Merging | Safe experimentation and parallel development |
| Open-source         | Free and widely supported                     |
| GitHub Integration  | Collaborate easily with remote repos          |

---

## 4️⃣ Git Installation & Setup

```bash
# Configure your name and email
git config --global user.name "Satish"
git config --global user.email "satish@example.com"

# Check configuration
git config --list
```

---

## 5️⃣ Initialize Project & First Commit

```bash
# Create project folder
mkdir MyLinuxBlog
cd MyLinuxBlog

# Initialize Git repository
git init
```

**File structure:**

```
MyLinuxBlog/
└── .git/
```

```bash
# Create first file
echo "# Satish's Linux Commands" > satish_commands.md

# Check status
git status

# Stage & commit
git add satish_commands.md
git commit -m "Add initial Linux commands file"
```

**Git log:**

```
a1b2c3d (HEAD -> main) Add initial Linux commands file
```

---

## 6️⃣ Adding More Commands

```bash
echo "- ls" >> satish_commands.md
echo "- cd" >> satish_commands.md
git add satish_commands.md
git commit -m "Add basic Linux commands"
```

**File content:**

```
# Satish's Linux Commands
- ls
- cd
```

---

## 7️⃣ Branching Workflow

```bash
# Create a branch for advanced commands
git branch advanced-commands
git checkout advanced-commands

# Add advanced commands
echo "- grep" >> satish_commands.md
echo "- awk" >> satish_commands.md
git add satish_commands.md
git commit -m "Add advanced Linux commands"
```

**Branch Diagram:**

```
main ──●────●
        \
advanced-commands ──●
```

---

## 8️⃣ Merging Branches

```bash
git checkout main
git merge advanced-commands
```

**File content after merge:**

```
# Satish's Linux Commands
- ls
- cd
- grep
- awk
```

---

## 9️⃣ Undo Mistakes

```bash
# Undo unstaged changes
git checkout -- satish_commands.md

# Unstage a file
git reset HEAD satish_commands.md

# Revert a commit safely
git revert <commit-id>

# Reset completely (dangerous!)
git reset --hard <commit-id>
```

---

## 🔟 Stashing Work

```bash
echo "- sed" >> satish_commands.md
git stash save "Add sed command"
git stash list
git stash apply
```

**Explanation:**

* Stash saves unfinished work temporarily
* Useful when switching branches without committing

---

## 1️⃣1️⃣ Tagging Releases

```bash
git tag -a v1.0 -m "Initial release of Satish's Linux Commands"
git push origin v1.0
```

---

## 1️⃣2️⃣ Advanced Commands

| Command                             | Use                                                      |
| ----------------------------------- | -------------------------------------------------------- |
| `git cherry-pick <commit>`          | Apply specific commit from another branch                |
| `git rebase <branch>`               | Reapply commits on top of another branch, linear history |
| `git blame <file>`                  | See who changed each line                                |
| `git log --graph --oneline --all`   | Visualize history                                        |
| `git submodule add <repo> <folder>` | Add external repo as a submodule                         |

---

## 1️⃣3️⃣ Collaboration Workflow

1. **Clone repository:**

```bash
git clone https://github.com/Satish/MyLinuxBlog.git
```

2. **Create feature branch:**

```bash
git checkout -b feature-xyz
```

3. **Make changes & commit:**

```bash
git add .
git commit -m "Implement xyz"
```

4. **Update main branch:**

```bash
git checkout main
git pull origin main
```

5. **Merge feature branch:**

```bash
git checkout main
git merge feature-xyz
```

6. **Push changes to remote:**

```bash
git push origin main
```

---

## 1️⃣4️⃣ Real-Time Example – Satish Project

```bash
mkdir MyLinuxBlog && cd MyLinuxBlog && git init

echo "# Satish Linux Commands" > satish_commands.md
git add . && git commit -m "Initial commit"

git checkout -b feature-advanced
echo "- grep" >> satish_commands.md
echo "- awk" >> satish_commands.md
git add . && git commit -m "Add advanced commands"

git checkout main
git merge feature-advanced

git remote add origin https://github.com/Satish/MyLinuxBlog.git
git push -u origin main
```

**Resulting file:**

```
# Satish Linux Commands
- ls
- cd
- grep
- awk
```

**Branch diagram:**

```
main ──●────●────●
        \
feature-advanced ──●
```

---

## 1️⃣5️⃣ Summary – Full Git Workflow

* **Initialize repo → Add → Commit → Push**
* **Branch → Commit → Merge → Push**
* **Stash → Apply → Revert → Tag → Push**
* **Advanced: Rebase → Cherry-pick → Submodules → Log/Graph/Blame**

**Visual Workflow:**

```
main ──●────●────●────●
        \
feature-login ──●────●
        \
feature-bugfix ──●
```

---

