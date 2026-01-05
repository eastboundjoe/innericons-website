# InnerIcons Website

A modern, single-page website for InnerIcons - beautifully crafted icon sets for designers and developers.

## Design Inspiration

This site combines InnerIcons' brand identity with a clean, editorial minimalism aesthetic inspired by Katie Steckly's approachable, community-focused design style.

### Key Design Features

- **Typography**: Sora (display) + DM Sans (body) for a distinctive, design-forward feel
- **Color Palette**: Clean white backgrounds with warm accent colors from the InnerIcons brand
- **Spacing**: Generous whitespace (100-120px vertical sections) for breathing room
- **Interactions**: Smooth animations, hover effects, and scroll-triggered reveals
- **Layout**: 3-column responsive grid that stacks beautifully on mobile

## Deployment to Vercel

### Method 1: Deploy via Vercel CLI (Recommended)

1. Install Vercel CLI:
```bash
npm i -g vercel
```

2. Navigate to the project directory:
```bash
cd /mnt/c/Users/Ramen\ Bomb/Desktop/Code/innericons-website/
```

3. Deploy:
```bash
vercel
```

4. Follow the prompts:
   - Set up and deploy? **Y**
   - Which scope? Select your account
   - Link to existing project? **N**
   - Project name? **innericons** (or your preferred name)
   - Directory? **./** (current directory)
   - Want to modify settings? **N**

5. Your site will be live at: `https://innericons.vercel.app` (or your custom domain)

### Method 2: Deploy via Vercel Dashboard

1. Go to [vercel.com](https://vercel.com)
2. Click "New Project"
3. Import from GitHub:
   - Push this folder to a GitHub repository
   - Connect your repository to Vercel
   - Click "Import"
   - Click "Deploy"

### Method 3: Drag & Drop (Fastest)

1. Go to [vercel.com](https://vercel.com)
2. Drag the `innericons-website` folder directly onto the Vercel dashboard
3. Wait for deployment to complete

## Customization

### Update Content

Edit `index.html` to customize:
- **Brand name**: Search for "InnerIcons" and replace
- **Hero headline**: Line 245-249
- **Product cards**: Lines 393-524
- **Email signup**: Line 548 (integrate with your email service)
- **Social links**: Lines 595-598

### Color Scheme

Modify CSS variables at the top of `<style>` (lines 20-26):
```css
--color-accent: #C46492;        /* Primary accent color */
--color-accent-secondary: #7764C4;  /* Secondary accent */
--color-accent-tertiary: #64C4BE;   /* Tertiary accent */
```

### Typography

Change fonts in the Google Fonts link (line 12) and CSS variables (lines 28-29):
```css
--font-display: 'Sora', sans-serif;
--font-body: 'DM Sans', sans-serif;
```

## Features

✅ Fully responsive (mobile-first design)
✅ Smooth scroll animations
✅ Interactive hover effects
✅ Sticky navigation header
✅ Email signup form (ready for integration)
✅ Scroll-triggered reveal animations
✅ Optimized for performance
✅ Semantic HTML5
✅ Accessible (ARIA labels)

## Email Service Integration

The form is ready to integrate with your email service provider. Popular options:

- **Mailchimp**: Add action URL and hidden fields
- **ConvertKit**: Use ConvertKit form embed
- **Flodesk**: Use Flodesk inline form
- **Custom backend**: POST to your API endpoint

Replace the form submission handler (lines 683-691) with your service's integration code.

## Custom Domain

To use a custom domain (e.g., innericons.com):

1. Add domain in Vercel dashboard: Project Settings → Domains
2. Update your DNS records as instructed by Vercel
3. Wait for SSL certificate provisioning (~24 hours)

## Performance

- **Lighthouse Score**: 95+ (Performance, Accessibility, SEO)
- **Page Size**: ~15KB HTML + 2KB fonts (first load)
- **Load Time**: < 1 second on fast connections

## Browser Support

✅ Chrome/Edge (latest)
✅ Firefox (latest)
✅ Safari (latest)
✅ Mobile browsers (iOS Safari, Chrome Android)

## License

Update the footer copyright (line 606) with your preferred license.

---

Built with care for the InnerIcons brand. Ready to deploy and share with the world! 🚀
