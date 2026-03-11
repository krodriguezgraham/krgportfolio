# Kassandra Rodriguez — Portfolio Site

Static portfolio site ready for Netlify deployment.

## Folder Structure

```
portfolio-site/
├── index.html
├── about.html
├── case-study-dialysate-generator.html
├── case-study-icu-sensor.html
├── case-study-learning-platform.html
├── case-study-movie-theater.html
├── case-study-rtl.html
├── netlify.toml
├── download-images.sh           ← Run this first!
└── images/
    ├── shared/
    │   ├── kassandra-about-photo.jpg
    │   ├── kassandra-photo.jpg
    │   └── kassandra-photo-2.JPG
    ├── case-study-movie-theater/
    │   ├── Affinity-Mapping.png
    │   ├── Competitive-Audit-1.png
    │   ├── Competitive-Audit-2.png
    │   ├── Competitive-Audit-3.png
    │   ├── Competitive-Audit-4.png
    │   ├── Vanessa-User-Journey-Map.png
    │   ├── Oliver-User-Journey-Map.png
    │   ├── Storyboard-Close-Up.png
    │   ├── Storyboard-Big-Picture.png
    │   ├── Low-Fi-1.png
    │   ├── Low-Fi-2.png
    │   ├── Screen-Shot-usability.png
    │   └── Sticker-Sheet.png
    ├── case-study-learning-platform/
    │   ├── RL-Affinity-Map.png
    │   ├── Competitive-Analysis.png
    │   ├── RL-Platform-User-Flow.png
    │   ├── 2X2-Matrix.png
    │   ├── Screen-Shot-wireframe.png
    │   └── Low-Fidelity-Wireframe.png
    └── case-study-rtl/
        ├── Facebook-2017-Arabic.png
        ├── Facebook-2017.png
        ├── iPhone-English.png
        ├── iPhone-Arabic.png
        ├── LTR.png
        └── RTL.png
```

> **Note:** `case-study-dialysate-generator.html` and `case-study-icu-sensor.html` 
> had no external images — they are ready to deploy as-is.

## Step 1 — Download Images

The case study images are currently hosted on Wixstatic. Run the download script 
from the root of this folder to pull them all locally:

```bash
chmod +x download-images.sh
./download-images.sh
```

This only needs to be done **once** before your first deploy.

## Step 2 — Deploy to Netlify

### Option A: Drag & Drop (Quickest)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the entire `portfolio-site` folder onto the deploy zone
3. Done — your site is live!

### Option B: Connect to Git (Recommended for ongoing updates)
1. Push this folder to a GitHub repo
2. In Netlify: **Add new site → Import an existing project → GitHub**
3. Select your repo, leave build settings blank (static site)
4. Click **Deploy site**

## Step 3 — Custom Domain

In Netlify: **Site settings → Domain management → Add custom domain**  
Enter `kassandrarodriguez.com` and follow the DNS instructions to point away from Wix.

**Wix DNS steps:**
1. Log in to Wix → Domains → Manage
2. Remove or disable the Wix nameservers / A records for `kassandrarodriguez.com`
3. Add Netlify's provided DNS records (or update nameservers to Netlify's)

Netlify will auto-provision an SSL certificate via Let's Encrypt within minutes.
