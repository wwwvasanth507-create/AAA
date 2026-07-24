You can use **Git** to track changes locally and **GitHub** to store them online. Here's the complete workflow.

## Step 1: Install Git

Download and install Git:

[https://git-scm.com/downloads](https://git-scm.com/downloads)

Verify installation:

```bash
git --version
```

---

## Step 2: Create a GitHub Repository

1. Go to [https://github.com](https://github.com)
2. Click **New Repository**
3. Enter a repository name
4. Choose Public or Private
5. Click **Create Repository**

Do **not** initialize it with a README if your project already exists.

---

## Step 3: Open Terminal in Your Project Folder

Example:

```bash
cd "C:\V\MyProject"
```

---

## Step 4: Initialize Git

```bash
git init
```

---

## Step 5: Configure Git (One Time Only)

```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

Check:

```bash
git config --list
```

---

## Step 6: Add All Files

```bash
git add .
```

---

## Step 7: Commit

```bash
git commit -m "Initial commit"
```

---

## Step 8: Connect to GitHub

Replace the URL with your repository.

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```

Verify:

```bash
git remote -v
```

---

## Step 9: Push to GitHub

If the default branch is `main`:

```bash
git branch -M main
git push -u origin main
```

After this, your files are on GitHub.

---

# Every Time You Modify Files

Whenever you make changes:

### Check changes

```bash
git status
```

### Stage all changes

```bash
git add .
```

### Commit

```bash
git commit -m "Describe what changed"
```

Example:

```bash
git commit -m "Added login page"
```

### Upload to GitHub

```bash
git push
```

That's all. Repeat these three commands after every set of changes:

```bash
git add .
git commit -m "Your message"
git push
```

---

# If You Work on Another PC

Clone the repository:

```bash
git clone https://github.com/USERNAME/REPOSITORY.git
```

Before editing:

```bash
git pull
```

After editing:

```bash
git add .
git commit -m "Updated project"
git push
```

---

# Useful Commands

```bash
git status          # Show changed files
git log             # Commit history
git pull            # Download latest changes
git push            # Upload changes
git add .           # Stage all changes
git commit -m ""    # Save changes locally
git remote -v       # Show connected GitHub repository
```

---

# Recommended Folder Structure

```
MyProject/
│
├── .git/
├── app.py
├── requirements.txt
├── README.md
├── static/
├── templates/
└── uploads/
```

Add a `.gitignore` file to avoid uploading unnecessary files:

```gitignore
__pycache__/
*.pyc
venv/
.env
node_modules/
dist/
build/
uploads/
```

---

## Make it even easier with VS Code

If you use **Visual Studio Code**:

1. Open your project folder.
2. Go to the **Source Control** tab (or press **Ctrl + Shift + G**).
3. Review changed files.
4. Enter a commit message.
5. Click **Commit**.
6. Click **Sync Changes** (or **Push**) to upload to GitHub.

This provides a graphical interface, so you don't need to remember all the Git commands.
