# Blog — Setup & Usage

## File Structure

```
blog/
├── blog.html          ← archive index (list of all posts)
├── style.css          ← all styles, shared across pages
├── images/            ← put all your images here
└── posts/
    ├── 03-2025.html   ← sample post (duplicate for each new post)
    └── ...
```

Link to `blog.html` from your main Cargo site however you like (external link in nav, etc).

---

## Adding a New Post

1. Duplicate `posts/03-2025.html` and rename it (e.g. `posts/04-2025.html`)
2. Update the date in `<span class="post-date">` and `<title>`
3. Replace placeholder `<img src="">` paths with your actual image filenames
4. Add/remove content blocks as needed (see below)
5. Add a new `<li>` entry to `blog.html`'s post list, pointing to the new file

---

## Content Block Types

Paste these into the `<div class="post-content">` section of any post:

### Single image
```html
<div class="block-image">
  <img src="../images/filename.jpg" alt="">
</div>
```

### Single image with caption
```html
<div class="block-image">
  <img src="../images/filename.jpg" alt="">
  <p class="caption">Your caption here</p>
</div>
```

### Two images side by side
```html
<div class="block-image-pair">
  <img src="../images/left.jpg" alt="">
  <img src="../images/right.jpg" alt="">
</div>
```

### Text paragraph(s)
```html
<div class="block-text">
  <p>Your writing here.</p>
  <p>Another paragraph.</p>
</div>
```

Mix and match blocks in any order.

---

## Hosting on GitHub Pages

1. Create a new GitHub repo (e.g. `blog`)
2. Push all these files to the `main` branch
3. Go to repo Settings → Pages → Source: `main` branch, root folder
4. Your blog will be live at `https://yourusername.github.io/blog/blog.html`

To connect a custom domain, add a `CNAME` file to the repo with your domain name, then configure your DNS.

---

## Linking from Cargo

In your Cargo site nav or page, add an external link pointing to your GitHub Pages URL (or custom domain).
