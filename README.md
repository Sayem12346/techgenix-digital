# Techgenix Digital — Website

Premium agency website built with React + Vite. Ready to deploy to Vercel or Netlify via GitHub.

---

## Bangla Deploy Guide (Mobile theke)

### Step 1: GitHub-e Repository Banano

1. [github.com](https://github.com) e login korun (account na thakle free banan)
2. Upper-right corner e **+** icon e tap korun → **New repository**
3. Repository name din: `techgenix-digital`
4. **Public** select korun, tarpor **Create repository**

### Step 2: Files Upload Korun

1. Notun repository page e **"uploading an existing file"** link e tap korun
2. Is ZIP file theke shob file gulo extract kore (ba file manager diye unzip kore) ekta ekta kore drag/select kore upload korun — **folder structure thik rakhben**:
   - `index.html`
   - `package.json`
   - `vite.config.js`
   - `.gitignore`
   - `src/main.jsx`
   - `src/TechgenixDigital.jsx`
3. Niche **Commit changes** button e tap korun

> Tip: GitHub mobile web theke ekbare puro folder upload na-o korte dite pare. Shekhetre GitHub mobile app use korun, ba ekta ekta file create kore content paste korun.

### Step 3: Vercel diye Deploy Korun

1. [vercel.com](https://vercel.com) e jan, **Continue with GitHub** diye login korun
2. **Add New Project** e tap korun
3. Apnar `techgenix-digital` repository select korun → **Import**
4. Vercel nijei bujhe nibe eta Vite project — kichu change korar dorkar nei
5. **Deploy** button e tap korun
6. 1-2 minute er moddhe live link pabe (jemon `techgenix-digital.vercel.app`)

### Netlify diye Deploy Korte Chaile

1. [netlify.com](https://netlify.com) e GitHub diye login korun
2. **Add new site** → **Import an existing project** → GitHub select korun
3. Repository select korun
4. Build command: `npm run build`, Publish directory: `dist` — eta automatic detect hoyer kotha
5. **Deploy site** e tap korun

### Custom Domain Add Korte Chaile

Vercel/Netlify dashboard er **Domains** section e giye apnar kena domain (jemon techgenixdigital.com) add korte parben — instructions ogulo nijeder site e dekhabe.

---

## English Quick Reference

```
techgenix-digital/
├── index.html
├── package.json
├── vite.config.js
├── .gitignore
└── src/
    ├── main.jsx
    └── TechgenixDigital.jsx
```

**Local test before deploying (optional, needs Node.js):**
```bash
npm install
npm run dev      # preview at localhost:5173
npm run build    # produces /dist for production
```

**Vercel:** Import the GitHub repo at vercel.com — it auto-detects Vite, no config needed. Build command `npm run build`, output directory `dist` (pre-filled automatically).

**Netlify:** Same flow at netlify.com — build command `npm run build`, publish directory `dist`.

### Notes
- All images (logo + 8 service photos) are embedded as base64 directly in `TechgenixDigital.jsx`, so there are no external image dependencies or broken-link risk.
- WhatsApp, phone, Facebook, YouTube, and email links are wired throughout (floating button, mobile bottom bar, hero, footer, final CTA).
- The contact form's "Submit Brief" button opens WhatsApp with the message pre-filled — there is no backend, so no data is stored anywhere.
- Testimonials and case-study percentages are placeholder content — replace with real client results before going live.
- For better long-term performance, consider moving the embedded base64 images to `/public` as separate files once the site is live and stable — this reduces the JavaScript bundle size. Ask if you'd like help with that conversion later.
