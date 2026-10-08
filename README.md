# klmoxxx

Next.js website/app, deployed on Vercel. Edit from any device (Windows PC, phone) via Git.

## Run locally (Windows PC)

1. Install [Git](https://git-scm.com), [Node.js LTS](https://nodejs.org) and [VS Code](https://code.visualstudio.com).
2. Clone to a plain local folder (NOT inside OneDrive/Dropbox, which can corrupt `.git`):
   ```
   git clone https://github.com/67xaeioux67/klmoxxx.git
   cd klmoxxx
   npm install
   npm run dev
   ```
3. Open http://localhost:3000. The RSS feed is served at `/bloodline.xml`.

## Daily workflow (every device)

```
git pull                      # start of work
git switch -c my-change       # new branch per change
# edit files
git add -A && git commit -m "what changed"
git push -u origin my-change  # then open a PR and merge to main
```

- Always pull before starting and push before leaving a device.
- If a push is rejected: `git pull --rebase`, then push again.
- Never commit secrets. Put them in `.env.local` (git-ignored) and in Vercel's Environment Variables.

## Phone

Use the GitHub mobile app, github.dev (press `.` on the repo page), or a Claude Code session to make edits and open PRs.

## Deploy

Vercel builds every push: branches/PRs get a preview URL, `main` goes live.
