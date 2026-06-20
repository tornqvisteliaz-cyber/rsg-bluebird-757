# RSG Bluebird 757 — Website

A modern, fully functional remake of the original Bluebird 757 flight simulation website, rebranded for **RSG** (the developer).

## Features

- **Beautiful hero section** with the original plane photography
- **Dynamic Announcements** powered by `localStorage` — new posts appear instantly on the public site
- **Admin Login** protected page at `/login.html`
  - Email: `Tornqvisteliaz@gmail.com`
  - Password: `rsgbluebird` (demo)
- **Admin Dashboard** (`/admin.html`) where you can:
  - Create and publish new announcements
  - Delete existing announcements
  - See live stats
- Fully responsive + mobile menu
- Contact form (demo)
- Job openings with fake apply flow
- 787 development section using the original imagery
- Ready for **Vercel** static deployment + **GitHub**

## How to Deploy on Vercel + GitHub

### 1. Push to GitHub

```bash
cd rsg-website
git init
git add .
git commit -m "Initial RSG website"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/rsg-bluebird.git
git push -u origin main
```

### 2. Deploy on Vercel (recommended)

1. Go to [vercel.com](https://vercel.com) and sign in with GitHub
2. Click **"Add New Project"**
3. Import your `rsg-bluebird` repository
4. Framework Preset: **Other** (or leave blank — it's static HTML)
5. Root Directory: leave as `/`
6. Click **Deploy**

Vercel will give you a beautiful `*.vercel.app` URL instantly. Every push to `main` will auto-deploy.

### 3. (Optional) Real Backend Upgrade Path

The current version uses browser `localStorage` (works great for personal/demo use).

For a production version with **persistent shared announcements** and proper auth:

- Migrate to **Next.js 15** + Tailwind
- Use **Vercel KV** or **Postgres** to store announcements
- Add **NextAuth.js** or **Clerk** for secure login (magic links or password)
- Protect `/api/announcements` routes so only the verified email can POST

I can help you upgrade to that full-stack version whenever you're ready.

## Local Development

Just open `index.html` in any browser. No build step needed.

To test the full flow:
1. Open `index.html`
2. Go to **Admin Login**
3. Use `Tornqvisteliaz@gmail.com` + `rsgbluebird`
4. You'll be taken to the admin dashboard where you can post announcements
5. Refresh `index.html` — your new announcements will appear!

## Tech Stack

- Pure HTML + Tailwind CSS (via CDN)
- Vanilla JavaScript
- Font Awesome 6
- Zero dependencies / zero build step
- 100% deployable on Vercel, Netlify, GitHub Pages, etc.

## Credits

Original design & photography inspired by the Bluebird 757 project.
Remade & extended for RSG by Grok.

Enjoy building the future of flight simulation! ✈️

— RSG Team