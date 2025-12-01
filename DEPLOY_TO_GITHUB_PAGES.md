# Deploy to GitHub Pages - Step by Step Guide

## Option 1: Create New Repository (Recommended)

### Step 1: Create New Repository on GitHub

1. Go to [GitHub](https://github.com) and sign in
2. Click the **+** icon → **New repository**
3. Repository name: `ai-cybersecurity-demo` (or any name you prefer)
4. Description: "Interactive Cybersecurity Knowledge Platform Demo"
5. Set to **Public** (required for free GitHub Pages)
6. **DO NOT** initialize with README, .gitignore, or license
7. Click **Create repository**

### Step 2: Initialize Git in Portfolio Demo Folder

Open PowerShell/Terminal in the `portfolio-demo` folder:

```powershell
# Navigate to portfolio-demo folder
cd C:\projects21\ai-cybersecurity-honeypot\portfolio-demo

# Initialize git (if not already initialized)
git init

# Add all files
git add .

# Commit files
git commit -m "Initial commit: Cybersecurity Knowledge Platform Demo"

# Add remote repository (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/YOUR_USERNAME/ai-cybersecurity-demo.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section (left sidebar)
4. Under **Source**, select:
   - Branch: `main` (or `master`)
   - Folder: `/` (root)
5. Click **Save**
6. Wait 1-2 minutes for GitHub to build your site

### Step 4: Access Your Demo

Your demo will be available at:
```
https://YOUR_USERNAME.github.io/ai-cybersecurity-demo/
```

---

## Option 2: Use Existing Honeypot Repository (Not Recommended)

If you want to use the existing honeypot repository:

### Option 2A: Deploy from a Subfolder

1. Push the `portfolio-demo` folder to your honeypot repository
2. In GitHub Pages settings, select:
   - Branch: `main`
   - Folder: `/portfolio-demo`
3. Your demo will be at: `https://YOUR_USERNAME.github.io/AI-Cybersecurity_honeypot/portfolio-demo/`

### Option 2B: Use GitHub Pages Branch

1. Create a new branch called `gh-pages`
2. Copy `portfolio-demo` contents to root of `gh-pages` branch
3. Push `gh-pages` branch
4. GitHub Pages will automatically deploy from `gh-pages` branch

**Note:** This might interfere with your main honeypot project structure.

---

## ✅ Recommended Approach

**Create a new repository** - This is the cleanest approach because:
- ✅ No interference with honeypot project
- ✅ Clean, focused repository
- ✅ Easy to manage and update
- ✅ Can link from your portfolio website
- ✅ Separate deployment pipeline

---

## 🔄 Updating Your Demo

After making changes:

```powershell
cd C:\projects21\ai-cybersecurity-honeypot\portfolio-demo

git add .
git commit -m "Update: [describe your changes]"
git push origin main
```

GitHub Pages will automatically rebuild (usually takes 1-2 minutes).

---

## 🐛 Troubleshooting

### Pages Not Loading
- Check repository is **Public**
- Verify GitHub Pages is enabled in Settings → Pages
- Wait 2-3 minutes after enabling Pages
- Check Actions tab for build errors

### Map Not Showing
- Ensure Leaflet.js CDN links are accessible
- Check browser console for CORS errors
- Verify internet connection (map tiles load from external CDN)

### Styling Issues
- Clear browser cache
- Check if all CSS is embedded in `index.html`
- Verify no conflicting styles

---

## 📝 Next Steps

1. ✅ Create new repository
2. ✅ Push portfolio-demo files
3. ✅ Enable GitHub Pages
4. ✅ Test the live URL
5. ✅ Add link to your portfolio website
6. ✅ Share with recruiters!

