# Upload instructions for GitHub Pages

This folder is already set up as a static website. You do **not** need Jekyll, npm, or any build step.

## What to edit first

Open `index.html` and update these items if needed:

1. The **Code** button URL.
2. The author list or affiliations.
3. Any external links you want to point to your final paper, poster, slides, or video.

## Fastest path: upload with the GitHub web UI

### Option A: personal website
Use this if you want the site at `https://YOUR-USERNAME.github.io/`.

1. On GitHub, create a new repository named `YOUR-USERNAME.github.io`.
2. Upload **all files inside this folder** to the repository root.
3. Go to **Settings -> Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Set **Branch** to `main` and **Folder** to `/ (root)`.
6. Click **Save**.
7. Wait about 1-5 minutes, then open `https://YOUR-USERNAME.github.io/`.

### Option B: project website
Use this if you want the site at `https://YOUR-USERNAME.github.io/REPO-NAME/`.

1. Create a new repository, for example `diversed`.
2. Upload **all files inside this folder** to the repository root.
3. Go to **Settings -> Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Set **Branch** to `main` and **Folder** to `/ (root)`.
6. Click **Save**.
7. Wait about 1-5 minutes, then open `https://YOUR-USERNAME.github.io/REPO-NAME/`.

Because this page uses **relative asset paths**, it works for both Option A and Option B without changing any paths.

## Upload with git from your terminal

If you prefer git instead of the web UI:

```bash
cd diversified_page
git init
git add .
git commit -m "Initial project page"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```

Then go to **Settings -> Pages** and set:
- **Source**: Deploy from a branch
- **Branch**: `main`
- **Folder**: `/ (root)`

## Why `.nojekyll` is included

GitHub Pages normally runs Jekyll for branch-based publishing. The `.nojekyll` file tells GitHub Pages to serve the site as plain static files, which is the safest option for a hand-written HTML page like this.

## Optional custom domain

If you later want a custom domain:

1. Go to **Settings -> Pages**.
2. Add your domain under **Custom domain**.
3. Update your DNS records with your domain provider.
4. Re-enable **Enforce HTTPS** after the certificate is issued.

## Common mistakes

- Uploading the **zip file itself** instead of the extracted files.
- Forgetting to enable GitHub Pages in **Settings -> Pages**.
- Putting `index.html` inside a nested folder instead of the repository root.
- Waiting only a few seconds: the first deployment can take a couple of minutes.

## Suggested quick improvements

- Add a short demo video or GIF near the top.
- Add author homepage links.
- Add a short “How to cite” copy button with JavaScript.
- Add poster / slides / code badges once public.
