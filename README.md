# Security Portfolio

Personal security engineering portfolio built with Astro.

## Development

```bash
npm install
npm run dev
```

## Deploy to Netlify

### Option 1: Git-based deploy (recommended)

1. Push to GitHub:
   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git remote add origin git@github.com:Nancy-Chauhan/security-portfolio.git
   git push -u origin main
   ```

2. Go to [netlify.com](https://netlify.com) → Add new site → Import from Git

3. Select your repo, Netlify auto-detects settings from `netlify.toml`

4. Set custom domain:
   - Site settings → Domain management → Add custom domain
   - Enter: `security.nancychauhan.com`
   - Add DNS record where your domain is managed:
     ```
     CNAME  security  →  your-site-name.netlify.app
     ```

### Option 2: CLI deploy

```bash
npm install -g netlify-cli
netlify login
netlify init
netlify deploy --prod
```

## Commands

| Command           | Action                              |
| :---------------- | :---------------------------------- |
| `npm run dev`     | Start dev server at `localhost:4321`|
| `npm run build`   | Build for production to `./dist/`   |
| `npm run preview` | Preview production build locally    |

## Structure

```
src/
├── layouts/
│   └── Layout.astro      # Main layout with nav, footer, theme toggle
├── pages/
│   ├── index.astro       # Homepage
│   ├── projects.astro    # Projects listing
│   ├── blog.astro        # Blog (coming soon)
│   ├── til.astro         # Today I Learned
│   └── videos.astro      # Video embeds
└── styles/
    └── global.css        # Dark/light theme styles
```
