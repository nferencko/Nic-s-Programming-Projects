# Using Claude for Artifact 1

## Step 1: Prompted AI to help me set up the pages.
**Prompt:** How do i set up a git hub pages for a static website?  

**Result:**  
Here's the quickest path to getting a static site live on GitHub Pages.

**1. Create a repository**

Sign in at github.com, click **New repository**, and name it. If you name it `yourusername.github.io`, your site will be served at `https://yourusername.github.io`. Any other name works too, and the site will live at `https://yourusername.github.io/repo-name`. Make it public (private repos need a paid plan for Pages).

**2. Add your site files**

At minimum you need an `index.html` in the root of the repo. You can upload files through the GitHub web interface (**Add file > Upload files**), or use the command line:

```bash
git clone https://github.com/yourusername/your-repo.git
cd your-repo
# add your index.html, CSS, JS, images, etc.
git add .
git commit -m "Initial site"
git push origin main
```

**3. Turn on Pages**

1. Go to your repo's **Settings** tab.
2. Click **Pages** in the left sidebar.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose the `main` branch and the `/ (root)` folder (or `/docs` if your site files live in a docs folder), then click **Save**.

**4. Wait and visit your site**

The first deploy usually takes a minute or two. Refresh the Pages settings screen and you'll see a banner with your live URL.

**Tips**

- **Case matters.** `Image.png` and `image.png` are different files on GitHub Pages, so broken images are often a capitalization mismatch.
- **Use relative paths** (like `css/style.css`) rather than absolute ones (`/css/style.css`) if your site lives at `username.github.io/repo-name`, since absolute paths will point to the wrong place.
- **Custom domain:** in the same Pages settings, enter your domain under **Custom domain**, then add a CNAME (or A) record at your domain registrar pointing to GitHub. Check **Enforce HTTPS** once it's available.
- **Jekyll quirk:** GitHub Pages runs Jekyll by default, which ignores files and folders starting with an underscore. If that causes trouble, add an empty file named `.nojekyll` to the root.
- **Static site generators:** if you use something like Vite, Hugo, or Astro, set Source to **GitHub Actions** instead and use the starter workflow GitHub suggests, so the site is built and deployed automatically on each push.

If you tell me what you're building the site with (plain HTML, React, Hugo, etc.), I can give you more specific steps.

## Step 2: Prompt AI to Build Artifact

**Prompt:** I would like to build a small portfolio website using git hub pages to showcase 5 programming projects. There should be a card for each of the five projects. Right now, only the first card is real. The first project is the website we are building right now. The four others are placeholders for future projects.  

**Result:** I copied what it gave me in my index.html file.  

**Additional Work:** Went in to the index file and edited where it prompted me. Went through line by line trying to understand what was going on. This is my first experience with html so having AI help was nice.