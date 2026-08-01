# Setting up your content editor (Decap CMS)

Your site now has an admin editor built in at `/admin` — a form where you can add stories, edit text, and upload cover images without touching code. But it needs to live in a GitHub repo connected to Netlify (not just a drag-and-drop upload) so it has somewhere to save changes.

If your site is currently on Netlify from dragging the folder in, you'll redo the hosting step once here — after that, publishing new stories is just filling in a form.

## Step 1 — Put the site on GitHub

1. Go to https://github.com and create a free account if you don't have one.
2. Click "New repository". Name it something like `storiesbylity-site`. Keep it **public** or **private**, either works.
3. Upload every file in this folder to that repo (drag-and-drop works on GitHub's web UI, or use GitHub Desktop if you prefer a visual app instead of the command line).

## Step 2 — Connect Netlify to the GitHub repo

1. In Netlify, go to **Add new site → Import an existing project**.
2. Choose GitHub, and select the `storiesbylity-site` repo.
3. Leave build settings blank (there's no build step — it's a static site) and click **Deploy**.
4. If you had an earlier site from drag-and-drop, you can delete that one once this new one is live, or keep both — just make sure you're editing the one connected to GitHub going forward.

## Step 3 — Turn on Identity and Git Gateway

This is what lets you log into `/admin` securely.

1. In your Netlify site, go to **Site configuration → Identity → Enable Identity**.
2. Under Identity settings, find **Registration** and set it to **Invite only** (so random people can't sign up).
3. Scroll to **Services → Git Gateway** and click **Enable Git Gateway**. This lets the CMS save your changes back to GitHub on your behalf.

## Step 4 — Invite yourself as an editor

1. Still under Identity, click **Invite users**, and enter your own email address.
2. Check your email for the invite, click the link — it'll take you to your live site and prompt you to set a password.
3. From now on, go to `yoursite.netlify.app/admin` (or your custom domain + `/admin`) and log in with that email and password.

## Using the editor day to day

- Go to `/admin` and log in.
- Click **Stories → Story shelf**.
- You'll see a list of stories with fields for title, author, age range, blurb, cover image, and pages — each page is one screen in the reader.
- Click **Add** under "Stories" to add a brand new story, or edit an existing one.
- Upload a cover image directly in the form — no need to touch a file yourself.
- Click **Publish** (top right) when you're done. Changes go live on your site within a minute or two, no re-uploading needed.

## If something doesn't work

- **Can't log in / no invite email** — check spam, and make sure Identity + Git Gateway are both enabled (Step 3).
- **Changes aren't showing on the site** — give it a minute; Netlify needs a moment to redeploy after Git Gateway commits the change.
- **"/admin" shows a blank page** — double-check the site was deployed from the GitHub repo (Step 2), not from a drag-and-drop folder, since drag-and-drop sites have no repo for the CMS to save into.
