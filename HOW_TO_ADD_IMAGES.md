# How to Add Images to Your InnerIcons Website

## Quick Guide: Adding Photos

### Step 1: Add Image Files

Put your images in the `images/` folder:

```
innericons-website/
├── images/
│   ├── logo.png
│   ├── hero-background.jpg
│   ├── product-1.png
│   ├── product-2.png
│   └── icon-set-preview.png
├── index.html
└── vercel.json
```

**Recommended formats:**
- **PNG** - for logos, icons, transparent images
- **JPG** - for photos, backgrounds
- **WebP** - for optimized web images (best performance)
- **SVG** - for vector graphics, icons

**Optimize before uploading:**
- Use https://tinypng.com/ to compress images
- Keep images under 500KB each for fast loading
- Use appropriate dimensions (don't upload 4000px images if you only need 800px)

### Step 2: Reference Images in HTML

Open `index.html` and add images using the `<img>` tag:

**Example 1: Logo in Header**
```html
<!-- Find the logo section (around line 245) -->
<a href="#" class="logo">
    <img src="images/logo.png" alt="InnerIcons Logo" width="32" height="32">
    <span>InnerIcons</span>
</a>
```

**Example 2: Hero Background Image**
```html
<!-- Add to hero section (around line 258) -->
<section class="hero" style="background-image: url('images/hero-background.jpg');">
    <div class="container">
        <h1>Hey creator!...</h1>
    </div>
</section>
```

**Example 3: Product Card Images**
```html
<!-- Replace emoji with actual product image (around line 393) -->
<div class="card">
    <div class="card-image">
        <img src="images/product-1.png" alt="Essential UI Icons" style="width: 100%; height: 100%; object-fit: cover;">
    </div>
    <div class="card-content">
        <h3 class="card-title">Essential UI Icons</h3>
        ...
    </div>
</div>
```

### Step 3: Commit and Push to GitHub

```bash
# Add your images
git add images/
git commit -m "Add product images and photos"
git push

# Vercel will automatically redeploy with your images! ✅
```

## Advanced: Using External Image Hosting

Instead of storing images in your repo, you can use:

### Option A: Cloudinary (Free tier: 25GB storage)
1. Upload images to https://cloudinary.com
2. Get the image URL
3. Use in HTML: `<img src="https://res.cloudinary.com/your-account/image.jpg">`

### Option B: Imgur (Free)
1. Upload to https://imgur.com
2. Right-click image → "Copy image address"
3. Use in HTML: `<img src="https://i.imgur.com/xyz123.jpg">`

### Option C: GitHub (Already using it!)
1. Images are already in your repo
2. Reference them with relative paths: `images/photo.jpg`
3. Best for small/medium sites (Vercel/GitHub have generous limits)

## Example: Complete Card with Image

```html
<div class="card">
    <div class="card-image">
        <img
            src="images/ui-icons-preview.png"
            alt="Essential UI Icons Preview"
            loading="lazy"
            style="width: 100%; height: 100%; object-fit: cover;"
        >
    </div>
    <div class="card-content">
        <h3 class="card-title">Essential UI Icons</h3>
        <p class="card-description">
            300+ essential interface icons covering navigation, actions, media, and more.
        </p>
        <div class="card-meta">
            <span class="tag">SVG</span>
            <span class="tag">PNG</span>
        </div>
    </div>
</div>
```

## CSS Tips for Images

**Make images responsive:**
```css
img {
    max-width: 100%;
    height: auto;
}
```

**Add rounded corners:**
```css
img {
    border-radius: 16px;
}
```

**Add subtle shadow:**
```css
img {
    box-shadow: 0 4px 16px rgba(0, 0, 0, 0.1);
}
```

**Lazy loading (improves performance):**
```html
<img src="images/photo.jpg" alt="Description" loading="lazy">
```

## File Size Limits

- **GitHub**: 100MB per file, 1GB per repo (plenty for a website)
- **Vercel**: No hard limit, but keep total site under 100MB for best performance
- **Recommended**: Keep individual images under 500KB

## Troubleshooting

**Image not showing:**
- Check file path is correct: `images/photo.jpg` (not `Images/photo.jpg`)
- Make sure you committed and pushed the images to GitHub
- Check browser console (F12) for 404 errors
- Verify image file name matches exactly (case-sensitive)

**Image too slow to load:**
- Compress with https://tinypng.com
- Convert to WebP format
- Use appropriate dimensions (resize before uploading)
- Add `loading="lazy"` attribute

**Image looks blurry:**
- Use 2x resolution for retina displays (e.g., 800px image displayed at 400px)
- Use PNG for graphics/icons instead of JPG
- Don't upscale small images

---

Need help adding specific images? Let me know what you want to add and I'll update the HTML for you!
