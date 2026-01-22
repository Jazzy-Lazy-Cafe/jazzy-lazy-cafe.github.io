# Setup Guide for Root Domain

Follow these steps to deploy your root domain landing page.

## Step 1: Create New GitHub Repository

1. Go to [GitHub](https://github.com) and sign in
2. Click the **+** icon in the top right → **New repository**
3. **IMPORTANT**: Repository name must be exactly: `jazzy-lazy-cafe.github.io`
4. Description: "Root landing page for Jazzy Lazy AI"
5. Set to **Public**
6. Do NOT initialize with README (we already have files)
7. Click **Create repository**

## Step 2: Push These Files to GitHub

Open a terminal in this directory (`jazzy-lazy-cafe.github.io-root/`) and run:

```bash
# Initialize git repository
git init

# Add all files
git add .

# Commit
git commit -m "Initial commit: Add root landing page"

# Add remote (replace YOUR_USERNAME with your GitHub username)
git remote add origin https://github.com/Jazzy-Lazy-Cafe/jazzy-lazy-cafe.github.io.git

# Push to GitHub
git branch -M main
git push -u origin main
```

## Step 3: Enable GitHub Pages

1. Go to your new repository on GitHub
2. Click **Settings** (top right)
3. Click **Pages** in the left sidebar
4. Under **Source**:
   - Select **Deploy from a branch**
   - Branch: Select **main** (or **master** if that's your default)
   - Folder: Select **/ (root)**
5. Click **Save**

## Step 4: Wait for Deployment

1. GitHub will build and deploy your site (usually takes 1-2 minutes)
2. Refresh the Pages settings page to see the deployment status
3. Once deployed, you'll see: "Your site is live at https://jazzy-lazy-cafe.github.io"

## Step 5: Test

Visit `https://jazzy-lazy-cafe.github.io` in your browser:
- You should see the jazzy lazy landing page
- After 2 seconds, it will automatically redirect to your magazine
- Or click the "Enter Magazine" button to go immediately

## What This Does

- **Root URL** (`https://jazzy-lazy-cafe.github.io`): Shows landing page, then redirects to magazine
- **Magazine URL** (`https://jazzy-lazy-cafe.github.io/ai-magazine/`): Your main magazine site (unchanged)

## Troubleshooting

### 404 Error
- Make sure repository name is exactly `jazzy-lazy-cafe.github.io`
- Check that GitHub Pages is enabled in Settings → Pages
- Wait 2-3 minutes for initial deployment

### Redirect Not Working
- Clear your browser cache
- Try in incognito/private mode
- Check browser console for errors

### Still Getting 404
- Verify the repository is public
- Make sure `index.html` is in the root directory (not in a subfolder)
- Check GitHub Actions tab for build errors

## Optional: Update SEO References

Once the root domain is working, you may want to update references in your magazine's `_config.yml`:

```yaml
# Current
url: "https://jazzy-lazy-cafe.github.io"
baseurl: "/ai-magazine"

# Can optionally change to:
url: "https://jazzy-lazy-cafe.github.io/ai-magazine"
baseurl: ""
```

But this is **NOT required** - your current setup will continue to work perfectly.

## Success!

Once deployed, anyone visiting `https://jazzy-lazy-cafe.github.io` will see your beautiful landing page and be redirected to the magazine.

Your magazine at `https://jazzy-lazy-cafe.github.io/ai-magazine/` remains completely unchanged.