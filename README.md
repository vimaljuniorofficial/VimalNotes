# VimalNotes — Your Thoughts, Organized

A minimal, premium notes application built with React 19, TypeScript, Vite, and Tailwind CSS. Featuring pastel color cards, rich text editing, category organization, pinning, favorites, archiving, dark mode, and LocalStorage persistence.

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new)

---

## 🚀 Deploying to Vercel

This repository is already pre-configured for seamless deployment to Vercel.

### Method 1: Instant Deployment via Vercel CLI

1. Install the Vercel CLI (if not already installed):
   ```bash
   npm i -g vercel
   ```

2. Run the deployment command from the project root:
   ```bash
   vercel
   ```
   *Accept the default prompts — Vercel will automatically detect the **Vite** preset and use `dist` as the output directory.*

3. For a production deployment:
   ```bash
   vercel --prod
   ```

---

### Method 2: Git / GitHub CI/CD (Recommended)

1. Initialize Git and push this repository to GitHub:
   ```bash
   git init
   git add .
   git commit -m "feat: NoteSpace notes app"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/notespace.git
   git push -u origin main
   ```

2. Go to [vercel.com/new](https://vercel.com/new).
3. Import your `notespace` GitHub repository.
4. Vercel will detect:
   - **Framework Preset**: `Vite`
   - **Build Command**: `npm run build`
   - **Output Directory**: `dist`
5. Click **Deploy**. Your site will be live on an SSL `.vercel.app` domain in ~20 seconds!

---

## ⚙️ Configuration (`vercel.json`)

`vercel.json` is pre-configured with client-side SPA fallback routing so direct URLs and page refreshes work properly:

```json
{
  "framework": "vite",
  "buildCommand": "npm run build",
  "outputDirectory": "dist",
  "rewrites": [
    {
      "source": "/(.*)",
      "destination": "/index.html"
    }
  ]
}
```

---

## 🛠 Local Development

```bash
# Install dependencies
npm install

# Start local development server
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview
```

---

## ✨ Features

- **6 Pastel Color Palettes**: Sand, Rose, Sky, Mint, Lilac, Peach (with distinct dark-mode counterparts).
- **Categories**: Personal, Work, Study, Ideas, and Important.
- **Rich Text Editor**: Bold, italic, underline, bullet lists, numbered lists, and quotes.
- **Auto-Saving**: Continuous auto-save with saved status indicators.
- **Pinning & Favoriting**: Keep critical notes at the top.
- **Archiving & Trash**: Archive notes to clear space, restore them anytime.
- **Search & Sort**: Instant search by title or content, sort by newest, oldest, or title.
- **Export & Backup**: Export notes to JSON or import existing backups.
- **In-App Vercel Deployment Hub**: Copy CLI commands and inspect configurations directly inside the app.
