Organic ($ORG)
================

A small, static marketing site for Organic ($ORG) — a community-driven Solana meme token. The site showcases the project's lore, memes, a Meme Fest page with a Weavely embed and an Instagram-style feed, and contact information for community interactions.

Contents
--------
- index.html — Main landing page: hero, how-to-buy guide, chart embed, meme gallery (with modal viewer), roadmap, FAQ.
- memefest.html — Dedicated Meme Fest page: Weavely embed and community feed with like/share UI.
- lore.html — Long-form lore and chaptered storytelling with a right-side chapter navigator.
- contact.html — Contact page with community email and a simple mailto form.
- assets/ — Image and media assets used by the pages.
- vercel.json — Vercel configuration for clean URLs and long-term caching for assets.

Project choices
---------------
- Static HTML/CSS with Tailwind CDN for styling (fast, minimal build requirements).
- Vanilla JavaScript for progressive enhancement: gallery renderers, modal gallery, like persistence (localStorage), smooth scrolling.
- No build step required — drop the files on any static host or deploy to Vercel (recommended).

Quick local preview
-------------------
You can preview the site locally with a simple static server. From the project root (PowerShell):

```powershell
# Python 3 built-in server
python -m http.server 8000
# Then open http://localhost:8000 in your browser
```

If you prefer Node and have http-server installed:

```powershell
npx http-server -c-1 . -p 8000
```

Deploying to Vercel
-------------------
This repository already includes a `vercel.json` with reasonable defaults (clean URLs and asset caching). To deploy:
1. Sign in to Vercel and import the GitHub repository.
2. Vercel will detect static output and deploy the repository as-is.
3. The `vercel.json` will be used to set headers and routing behavior.

Notes & next improvements
-------------------------
- Accessibility: add ARIA attributes and a focus trap for the modal for a better keyboard experience.
- Likes: currently persisted to localStorage (client-only). If you want global like counts, we should add a small serverless API or use a third-party backend.
- Visual QA: confirm the 3-up meme paging and arrow alignment across device sizes. I tuned padding and image min-widths, but additional tweaks may be needed for specific viewports.

Contributing
------------
- Please open issues or PRs on the GitHub repo for fixes and enhancements.
- Keep changes minimal for each PR (one feature or fix per PR).

Contact
-------
- Community email: organic_community@proton.me
- Discord: https://discord.gg/Npc5Gx6f2w
- X/Twitter: https://x.com/Organic_bonk

LICENSE
-------
This code is provided as-is for the Organic community. Add a license file if you want to clarify reuse terms.

Credits
-------
Built with Tailwind CSS (CDN), AOS for animations, and Feather icons.

---

If you'd like, I can also add a short CONTRIBUTING.md, add a license, or wire a GitHub Action to preview site changes automatically.