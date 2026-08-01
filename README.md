# Storiesbylity — website

This is a complete, self-contained website: one file (`index.html`) with everything built in. No build step, no dependencies to install.

## Get a real public link (free, ~2 minutes)

**Option A — Netlify Drop (easiest)**
1. Go to https://app.netlify.com/drop
2. Drag this whole folder onto the page.
3. Netlify gives you a live URL immediately, like `https://random-name-123.netlify.app`.
4. You can rename the site (and later connect a real domain like storiesbylity.com) from the site settings — free, no account required to start, though creating an account lets you edit it again later.

**Option B — GitHub Pages**
1. Create a new GitHub repository.
2. Upload `index.html` to it.
3. In the repo, go to Settings → Pages → set source to the `main` branch, root folder.
4. GitHub gives you a URL like `https://yourusername.github.io/your-repo-name`.

**Option C — Vercel**
1. Go to https://vercel.com/new
2. Import the folder or a GitHub repo containing it.
3. Deploy — you'll get a `https://your-project.vercel.app` link.

## Connecting your own domain (storiesbylity.com)

Once deployed on any of the above, buy the domain from a registrar (Namecheap, Google Domains successor Squarespace Domains, GoDaddy, etc. — typically $10–20/year) and follow that host's "custom domain" instructions in site settings. Netlify and Vercel both walk you through the DNS records step by step.

## Editing content

Everything is in `index.html`:
- Sample stories are in the `stories` array near the bottom, inside the `<script>` tag — edit `title`, `blurb`, `age`, and `pages` (each string in `pages` is one page of the reader).
- The email signup form currently doesn't send anywhere — connect it to a real service (Mailchimp, Kit/ConvertKit, or a lightweight form backend like Formspree) when you're ready to actually collect signups.
- Contact email is a placeholder (`hello@storiesbylity.com`) — swap in your real address.
