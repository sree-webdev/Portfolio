# 🚀 How to Push Your Code to GitHub

Your repository is created but not yet pushed. Here's how to do it:

## Option 1: Using Personal Access Token (Recommended) ✅

### Step 1: Create a Personal Access Token
1. Go to: https://github.com/settings/tokens/new
2. Set these values:
   - **Token name**: `portfolio-push`
   - **Expiration**: 90 days
   - **Scopes**: Check `repo` (all checkboxes under repo)
3. Click "Generate token"
4. **COPY the token immediately** (you won't see it again!)

### Step 2: Push Your Code
Open PowerShell and run:

```powershell
cd "D:\downloads 11.05.2026\SreePortfolio"
git push https://YOUR_TOKEN@github.com/sree-webdev/Portfolio.git main
```

Replace `YOUR_TOKEN` with the token you just generated.

**Example:**
```powershell
git push https://ghp_abc123xyz@github.com/sree-webdev/Portfolio.git main
```

---

## Option 2: Using Windows Credentials Manager

### Step 1: Set Up Credentials Helper
```powershell
git config --global credential.helper wincred
```

### Step 2: Push Your Code
```powershell
cd "D:\downloads 11.05.2026\SreePortfolio"
git push -u origin main
```

### Step 3: When Prompted
- **Username**: `sree-webdev`
- **Password**: Paste your Personal Access Token

---

## After Push: Enable GitHub Pages Hosting 🌐

Once code is pushed:

1. Go to: https://github.com/sree-webdev/Portfolio
2. Click **Settings** (gear icon)
3. Go to **Pages** (left menu)
4. Under **Source**:
   - Branch: `main`
   - Folder: `/ (root)`
5. Click **Save**
6. Wait 1-2 minutes

### Your site will be live at:
```
https://sree-webdev.github.io/Portfolio/
```

---

## Verify the Push

After pushing, verify with:
```powershell
git remote -v
git log --oneline
```

You should see:
- Remote pointing to GitHub
- Your commits in the log

---

## Troubleshooting

### "Authentication failed"
- Generate a new Personal Access Token
- Make sure token hasn't expired
- Token needs `repo` scope

### "fatal: not a git repository"
- Make sure you're in: `D:\downloads 11.05.2026\SreePortfolio`

### Push is slow
- Normal for first push
- Be patient, especially with large files (resumes)

---

**You're all set! Push your code now! 🚀**
