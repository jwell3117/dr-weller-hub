# Deployment notes

Replace the repository-root `index.html` with the included `index.html`.

If your Josh OS or Vercel route links directly to `chart-builder.html`, also replace that file with the included `chart-builder.html`.

Commit both replacements together. The two included HTML files are intentionally identical so either route opens the same current builder.

After Vercel deploys, hard-refresh the live page with Ctrl+Shift+R.
