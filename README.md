# SAE IIITDM Kurnool website

A static website using HTML, CSS, and browser JavaScript. No installation,
build command, database, or application server is required for hosting.

## Files

- `index.html`: home, about, activities, and update previews.
- `blogs.html`: update cards.
- `gallery.html`: gallery layout and image lightbox.
- `css/styles.css`: shared styles and responsive layouts.
- `js/main.js`: mobile menu, scrolling, animations, and lightbox.
- `assets/`: add real team photos, logos, and documents here.

## Preview locally

From this folder, run:

```bash
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000>. Stop the server with Ctrl+C.

## Current content status

The pages are a draft. Social/contact links and article links using `href="#"`
need real destinations. The gallery contains emoji placeholders rather than
photos. Existing event dates, participation claims, awards, and attendance
figures need confirmation by the team before publication. There is no member
roster yet.

For an informational team site, prioritize the about section, verified team
members/roles, projects, official social links, contact details, and photos.
Keep blogs only if the team intends to maintain them.

At inspection, this folder had no Git repository, remote, deployment workflow,
or custom-domain configuration. An existing remote repository or deployment
could not be verified without its account or URL.

## Publish on GitHub Pages

1. Create an empty GitHub repository under the intended team account or
   organization. A public repository supports GitHub Pages on GitHub Free.
2. From this folder, initialize and push the site. Replace `OWNER` and
   `REPOSITORY` with the actual GitHub account and repository names:

   ```bash
   git init -b main
   git add index.html blogs.html gallery.html css js assets README.md .nojekyll
   git commit -m "Add static SAE team website"
   git remote add origin https://github.com/OWNER/REPOSITORY.git
   git push -u origin main
   ```

3. In the repository, open **Settings > Pages**. Select **Deploy from a branch**,
   branch **main**, and folder **/(root)**, then save.
4. Wait for the Pages deployment to succeed. Use the published URL shown in
   Pages settings. Normally it is `https://OWNER.github.io/REPOSITORY/`.
5. Open all three pages at the published URL and check navigation, images,
   official links, and the mobile menu.

The `.nojekyll` file tells Pages to serve the static files without Jekyll
processing. Keep site asset and navigation paths relative, as they are now,
so they work under the repository URL. Subsequent pushes to the publishing
branch automatically publish updates.

References:
- [About GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages)
- [Configure a publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
