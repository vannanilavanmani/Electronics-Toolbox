# ⚡ Electronics Toolbox — Week 08 Deployment Assignment

**Live App URL:** `https://electronics-toolbox.vercel.app` *(replace with your actual URL after deploy)*

---

## 🔧 What It Does

An interactive web-based electronics reference tool with 5 calculators:

| Tool | Description |
|------|-------------|
| ⚡ Ohm's Law | Enter any 2 of V, I, R — auto-calculates the third + power |
| 💡 LED Resistor | Calculates current-limiting resistor with nearest E24 standard value |
| 🔀 Voltage Divider | Computes Vout, ratio, and current draw with live diagram |
| 🎨 Resistor Color Code | Decode 4-band resistors with visual color band preview |
| 🔋 Capacitor RC | Time constant, charge curve, and interactive charge slider |

**Stack:** Pure HTML + CSS + JavaScript — no framework, no backend, no dependencies.

---

## 🚀 Deployment Steps (Vercel)

### Method A — Vercel CLI (recommended)

```bash
# 1. Install Vercel CLI
npm install -g vercel

# 2. Clone / enter this folder
cd Week-08/

# 3. Deploy (first time — follow prompts)
vercel

# 4. For subsequent updates / redeploys
vercel --prod
```

### Method B — Vercel Dashboard (no CLI)

1. Go to [vercel.com](https://vercel.com) → **Add New Project**
2. Import your GitHub repo (push this folder to GitHub first)
3. Vercel auto-detects static site — click **Deploy**
4. Done! You get a `*.vercel.app` URL immediately

---

## ⚙️ Environment Variables / Secrets

This app is fully client-side — **no environment variables needed**.

If you extend it with a backend (e.g. a FastAPI for more complex calculations), you would add env vars like:

```bash
# In Vercel Dashboard → Settings → Environment Variables
API_URL=https://your-backend.railway.app
```

Or via CLI:
```bash
vercel env add API_URL
```

---

## 🔄 Rolling Updates (Redeploy)

```bash
# Make your code changes, then:
vercel --prod

# Vercel creates a new immutable deployment
# Previous URL still works until you promote the new one
# You can roll back in the Vercel dashboard → Deployments tab
```

---

## 📁 File Structure

```
Week-08/
├── index.html      ← entire app (HTML + CSS + JS in one file)
├── vercel.json     ← Vercel deployment config
└── README.md       ← this file
```

---

## 🗒️ Platform-Specific Notes (Vercel)

- **Free tier:** Unlimited static deploys, 100GB bandwidth/month
- **Auto HTTPS:** Vercel provisions SSL automatically
- **Custom domain:** Add in Dashboard → Domains (free with your own domain)
- **Preview URLs:** Every git push creates a unique preview URL (great for showing work-in-progress)
- **No build step needed:** Since this is plain HTML, no `npm install` or build command required — set Build Command to empty/none

---

## 🌐 Alternative PaaS Options

| Platform | How to deploy this app |
|----------|----------------------|
| **Netlify** | Drag-and-drop the folder at app.netlify.com |
| **GitHub Pages** | Push to repo → Settings → Pages → Deploy from branch |
| **Cloudflare Pages** | Connect GitHub repo, no build command needed |
| **Railway** | Would need a tiny Express server to serve the HTML |

---

## 👨‍💻 Author

**[Your Name]** — Week 08 Assignment  
Course: [Your Course Name]  
Submitted to: `Tutorials/Submissions/<Name>/Week-08/`
