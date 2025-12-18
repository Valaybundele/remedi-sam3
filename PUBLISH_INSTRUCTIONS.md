# How to Publish Your Website Online

## Option 1: GitHub Pages (Recommended - Free)

### Step 1: Create a GitHub Repository
1. Go to https://github.com/new
2. Repository name: `yourusername.github.io` (replace `yourusername` with your GitHub username)
   - Example: If your username is `john`, name it `john.github.io`
3. Make it **Public**
4. **Do NOT** initialize with README, .gitignore, or license
5. Click "Create repository"

### Step 2: Push Your Files to GitHub

Run these commands in your terminal (replace `yourusername` with your GitHub username):

```bash
cd /home/bundeleva/Desktop/nerfies.github.io-main

# Add all files
git add .

# Commit
git commit -m "Initial commit: ReMeDI-SAM3 project website"

# Add your GitHub repository as remote (replace YOUR_USERNAME)
git remote add origin https://github.com/YOUR_USERNAME/YOUR_USERNAME.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

### Step 3: Enable GitHub Pages
1. Go to your repository on GitHub
2. Click **Settings** tab
3. Scroll down to **Pages** section (in the left sidebar)
4. Under **Source**, select **Deploy from a branch**
5. Select branch: **main**
6. Select folder: **/ (root)**
7. Click **Save**

### Step 4: Access Your Website
- Your website will be available at: `https://yourusername.github.io`
- It may take a few minutes to deploy (usually 1-5 minutes)

---

## Option 2: Using a Custom Repository Name

If you want a different repository name (not `username.github.io`):

1. Create repository with any name (e.g., `remedi-sam3-website`)
2. Follow Step 2 above (use your actual repository URL)
3. In GitHub Settings → Pages:
   - Source: **Deploy from a branch**
   - Branch: **main**, folder: **/ (root)**
4. Your site will be at: `https://yourusername.github.io/remedi-sam3-website/`

**Note:** You'll need to update all internal links in `index.html` to use relative paths starting with `/remedi-sam3-website/` instead of `./`

---

## Option 3: Other Hosting Services

- **Netlify**: Drag and drop the folder at https://app.netlify.com/drop
- **Vercel**: Connect your GitHub repository at https://vercel.com
- **GitHub Pages** (as described above) is the easiest and free option

---

## Troubleshooting

- **404 Error**: Wait a few minutes for GitHub Pages to deploy
- **Images not showing**: Make sure image paths use `./static/images/` (relative paths)
- **Styling broken**: Check that all CSS is inline or paths are correct

