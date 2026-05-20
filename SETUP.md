# Setup — how to make your profile README go live

Your GitHub profile README lives in a **special repo** with the same name as your username. Follow these steps once.

## 1. Create the special repo

1. Go to https://github.com/new
2. Repository name: **`PedroCnm`** (must match your username exactly, case-sensitive)
3. Set it to **Public**
4. Check **"Add a README file"**
5. Click **Create repository**

GitHub will show a green hint "PedroCnm/PedroCnm is a ✨ special ✨ repository" — that's how you know it worked.

## 2. Push the files in this folder

From the `PedroCnm/` folder (this one):

```bash
cd PedroCnm
git init
git branch -M main
git remote add origin https://github.com/PedroCnm/PedroCnm.git
git add README.md .github/workflows/snake.yml
git commit -m "feat: initial profile README + snake workflow"
git push -u origin main --force
```

> `--force` is fine here because the repo only has the auto-generated README from step 1.

## 3. Enable the snake animation

After the first push, the workflow runs automatically and creates an `output` branch with the SVG. If it doesn't fire on its own:

1. Go to https://github.com/PedroCnm/PedroCnm/actions
2. Click **"Generate Snake"** in the left sidebar
3. Click **"Run workflow"** → **Run workflow**

Wait ~30 seconds, refresh your profile at https://github.com/PedroCnm — the snake should now be eating your contribution graph.

If the action fails with a permissions error, go to:

**Settings → Actions → General → Workflow permissions** → select **"Read and write permissions"** → Save.

Then re-run the workflow.

## 4. Future updates

Just edit `README.md` and push to `main`. The snake refreshes itself daily at 03:17 UTC, or manually via "Run workflow" anytime.

## Optional polish

- **Pin repos:** on your profile, click "Customize your pins" and pin 6 repos you want to showcase. Good candidates: `creator-studio-ai-2`, anything Airflow/dbt-related, side projects.
- **Add a profile photo + bio** in https://github.com/settings/profile if you haven't yet — the README looks much better next to a real avatar.
- **Sponsor / Hireable toggle:** in profile settings, flipping "Available for hire" adds a subtle badge that recruiters filter by.

That's it. Welcome to ✨ profile README ✨ club.
