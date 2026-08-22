# Deploy This Site — Step by Step

## Files in this project
- `index.html` — Paint Calculator (home page)
- `wallpaper-calculator.html` — Wallpaper Calculator
- `paint-cost-calculator.html` — Paint Job Cost Estimator
- `about.html`, `privacy-policy.html`, `contact.html` — required pages for AdSense approval
- `styles.css` — shared design system used by every page

## Before you deploy — replace placeholders
Search each file for these and replace with your real info:
- `[Your Name]`, `[Your City/Country]` in about.html
- `hello@yourdomain.com` in contact.html and privacy-policy.html
- `YOUR_FORM_ID` in contact.html (get a free one at formspree.io if you want the contact form to actually email you)
- `paintcalc.com` in privacy-policy.html (your real domain once you have one)

## Step 1 — Put it on GitHub
1. Go to github.com/new, create a new repository (e.g. `paint-calculator`)
2. On your computer, download all files from this chat into one folder
3. In that folder, run:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/paint-calculator.git
   git push -u origin main
   ```
   (Or just drag-and-drop the files into GitHub's web upload page — no command line needed.)

## Step 2 — Deploy on Vercel
1. Go to vercel.com and sign up/log in with your GitHub account
2. Click "Add New Project"
3. Select your `paint-calculator` repo
4. Framework Preset: choose "Other" (this is a plain static site, no build step needed)
5. Click "Deploy"
6. In 1-2 minutes you'll get a live URL like `paint-calculator.vercel.app`

## Step 3 — (Optional) Custom domain
1. Buy a domain (Namecheap, Google Domains, etc.) — something short and relevant, e.g. `paintcalc.io`
2. In Vercel: Project → Settings → Domains → add your domain
3. Follow Vercel's DNS instructions at your domain registrar (usually just adding one A record and one CNAME)

## Step 4 — Get indexed by Google
1. Go to Google Search Console (search.google.com/search-console)
2. Add your property (URL prefix), verify ownership (Vercel makes this easy via DNS or HTML tag)
3. Submit your site — this fixes the "Technical Issues Block The Index" problem from the tutorial

## Step 5 — Apply for AdSense (only after you have real content + some traffic)
1. Make sure you have: this calculator + at least 2 more tools, About, Privacy Policy, Contact — all done here
2. Site should be live for a few weeks with some organic traffic before applying
3. Go to google.com/adsense, add your site, wait for review
4. Once approved, paste your AdSense code snippet just before `</head>` in every HTML file

## Before scaling this niche further
Before building more tools in this exact niche, re-run the validation prompt provided in chat
using real Ahrefs (or similar) data — confirm at least 2 of the top 5 ranking pages for your
target keyword have DR under 25. Paint/home-improvement calculators have some strong
incumbents (Sherwin-Williams, Behr, Home Depot, Lowe's), so pick your exact long-tail keyword
carefully rather than competing on broad terms like "paint calculator" alone.
