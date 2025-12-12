# 🚀 Deployment Guide

Complete guide to deploying your StartupFlow landing page to various platforms.

## GitHub Pages (Recommended)

### Step 1: Enable GitHub Pages

1. Visit: https://github.com/rahul700raj/tailwind-startup-landing/settings/pages
2. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
3. Click **Save**

### Step 2: Access Your Live Site

After 1-2 minutes, your site will be live at:

**🌐 https://rahul700raj.github.io/tailwind-startup-landing/**

---

## Alternative Deployment Options

### Option 1: Netlify

#### Method A: Drag & Drop (Fastest)
1. Go to [Netlify Drop](https://app.netlify.com/drop)
2. Drag your project folder
3. Get instant live link

#### Method B: Git Integration
1. Sign up at [Netlify](https://netlify.com)
2. Click "New site from Git"
3. Connect your GitHub repository
4. Configure build settings (none needed for static HTML)
5. Deploy automatically

**Netlify Features:**
- Automatic HTTPS
- Custom domains
- Form handling
- Continuous deployment

### Option 2: Vercel

```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
cd tailwind-startup-landing
vercel
```

Follow the prompts:
- Set up and deploy? **Y**
- Which scope? Select your account
- Link to existing project? **N**
- Project name? Press Enter
- Directory? Press Enter
- Override settings? **N**

**Vercel Features:**
- Edge network
- Automatic HTTPS
- Custom domains
- Analytics

### Option 3: Surge

```bash
# Install Surge
npm i -g surge

# Deploy
cd tailwind-startup-landing
surge
```

Choose a domain name (e.g., `my-startup-landing.surge.sh`)

**Surge Features:**
- Simple CLI
- Custom domains
- Free SSL

### Option 4: Firebase Hosting

```bash
# Install Firebase CLI
npm i -g firebase-tools

# Login
firebase login

# Initialize
firebase init hosting

# Deploy
firebase deploy
```

**Firebase Features:**
- Global CDN
- Custom domains
- SSL certificates
- Rollback support

---

## Custom Domain Setup

### For GitHub Pages

1. Add `CNAME` file to repository root:
```bash
echo "yourdomain.com" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

2. Configure DNS at your domain registrar:

**Option A: Apex Domain (yourdomain.com)**
Add A records:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**Option B: Subdomain (www.yourdomain.com)**
Add CNAME record:
```
rahul700raj.github.io
```

3. Enable HTTPS in repository settings (automatic after DNS propagation)

### For Netlify

1. Go to Site Settings → Domain Management
2. Click "Add custom domain"
3. Follow DNS configuration instructions
4. HTTPS is automatic

### For Vercel

1. Go to Project Settings → Domains
2. Add your domain
3. Configure DNS as instructed
4. HTTPS is automatic

---

## Pre-Deployment Checklist

### Content Review
- [ ] Update all placeholder text
- [ ] Replace company name and branding
- [ ] Add real testimonials
- [ ] Update pricing information
- [ ] Verify all links work
- [ ] Add real contact information

### Technical Checks
- [ ] Test on mobile devices
- [ ] Test on different browsers
- [ ] Verify smooth scrolling works
- [ ] Check all CTA buttons
- [ ] Test form submissions (if applicable)
- [ ] Optimize images (if added)

### SEO Optimization
- [ ] Add meta description
- [ ] Add Open Graph tags
- [ ] Add favicon
- [ ] Add sitemap.xml
- [ ] Add robots.txt

---

## Performance Optimization

### Before Deployment

1. **Optimize Images**
```html
<!-- Use WebP format -->
<img src="image.webp" alt="Description" loading="lazy">
```

2. **Minify HTML** (Optional)
Use online tools or build process to remove whitespace

3. **Add Meta Tags**
```html
<head>
    <meta name="description" content="Your landing page description">
    <meta property="og:title" content="StartupFlow">
    <meta property="og:description" content="Launch your product faster">
    <meta property="og:image" content="https://yourdomain.com/og-image.jpg">
    <meta name="twitter:card" content="summary_large_image">
</head>
```

4. **Add Favicon**
```html
<link rel="icon" type="image/png" href="favicon.png">
```

### After Deployment

1. **Test Performance**
   - [PageSpeed Insights](https://pagespeed.web.dev/)
   - [GTmetrix](https://gtmetrix.com/)
   - [WebPageTest](https://www.webpagetest.org/)

2. **Monitor Uptime**
   - [UptimeRobot](https://uptimerobot.com/)
   - [Pingdom](https://www.pingdom.com/)

---

## Environment-Specific Configuration

### Development
```bash
# Local server
python -m http.server 8000
# or
npx serve
# or
php -S localhost:8000
```

### Staging
Create a separate branch for staging:
```bash
git checkout -b staging
git push origin staging
```

Deploy staging branch to separate URL for testing.

### Production
Always deploy from `main` branch after thorough testing.

---

## Continuous Deployment

### GitHub Actions

Create `.github/workflows/deploy.yml`:

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [ main ]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      
      - name: Deploy to GitHub Pages
        uses: peaceiris/actions-gh-pages@v3
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./
```

This automatically deploys on every push to `main`.

---

## Troubleshooting

### Site Not Loading
- Wait 2-3 minutes after enabling Pages
- Check branch is set to `main`
- Verify `index.html` is in root directory
- Clear browser cache

### Custom Domain Not Working
- Wait for DNS propagation (up to 48 hours)
- Verify DNS records are correct
- Check CNAME file content
- Ensure HTTPS is enabled

### Styling Issues
- Ensure Tailwind CDN is loading
- Check browser console for errors
- Verify internet connection
- Try hard refresh (Ctrl+Shift+R)

### Mobile Display Issues
- Test on real devices
- Use browser dev tools mobile emulation
- Check viewport meta tag
- Verify responsive classes

---

## Post-Deployment Tasks

### Analytics Setup

**Google Analytics**
```html
<!-- Add before </head> -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

**Plausible Analytics** (Privacy-friendly)
```html
<script defer data-domain="yourdomain.com" src="https://plausible.io/js/script.js"></script>
```

### Form Integration

**Formspree**
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
  <!-- Your form fields -->
</form>
```

**Netlify Forms**
```html
<form name="contact" method="POST" data-netlify="true">
  <!-- Your form fields -->
</form>
```

---

## Security Best Practices

1. **HTTPS Only**: Always use HTTPS in production
2. **Content Security Policy**: Add CSP headers
3. **Regular Updates**: Keep dependencies updated
4. **Backup**: Regular backups of your code
5. **Monitoring**: Set up uptime monitoring

---

## Maintenance

### Regular Tasks
- [ ] Update content monthly
- [ ] Check broken links
- [ ] Monitor performance
- [ ] Review analytics
- [ ] Update testimonials
- [ ] Refresh pricing (if changed)

### Quarterly Tasks
- [ ] Full content audit
- [ ] SEO review
- [ ] Performance optimization
- [ ] Security audit
- [ ] Backup verification

---

## Support Resources

- **GitHub Pages**: [docs.github.com/pages](https://docs.github.com/pages)
- **Netlify**: [docs.netlify.com](https://docs.netlify.com)
- **Vercel**: [vercel.com/docs](https://vercel.com/docs)
- **Tailwind CSS**: [tailwindcss.com/docs](https://tailwindcss.com/docs)

---

**Happy Deploying! 🎉**

For issues, open a GitHub issue or contact support.