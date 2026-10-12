# pAIssible Proof of Life

A disposable, safe test project. Needs a single static page at `public/index.html` that:
- says "pAIssible built and deployed this page."
- includes a short sentence noting it was created, built, tested, and deployed end-to-end by pAIssible
- shows a live timestamp

Also needs a GitHub Actions workflow at `.github/workflows/deploy.yml` that:
- builds the site (`npm run build`, which copies `public/index.html` to `dist/index.html`)
- deploys the `dist` directory to GitHub Pages using the official `actions/deploy-pages` flow
- can be triggered both by a push to the default branch and manually via `workflow_dispatch`
