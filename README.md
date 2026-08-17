# Bruna Weber — Personal Site

A single-page site: `index.html` (all CSS is inline — no build step, no dependencies to install).

## 1. Publish on GitHub Pages

1. Create a new GitHub repo (e.g. `brunaweber` or `bruna-weber-site`) — public.
2. Upload `index.html` to the root of the repo (drag-and-drop works fine on github.com, or `git push`).
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment," set **Source: Deploy from a branch**, branch `main`, folder `/ (root)`.
5. Save. Your site will be live at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

## 2. Add your custom domain (optional, ~$10–20/yr for the domain itself)

1. Buy a domain (Namecheap, Cloudflare, Google Domains, etc.) — e.g. `brunaweber.com`.
2. In the repo, **Settings → Pages → Custom domain**, enter your domain. GitHub will create a `CNAME` file automatically.
3. At your domain registrar, add the DNS records GitHub shows you (an `A` record set for apex domains, or a `CNAME` record for a `www` subdomain).
4. Check "Enforce HTTPS" once the certificate provisions (can take a few hours).

## 3. Turn on Google Analytics (GA4)

1. Create a GA4 property at [analytics.google.com](https://analytics.google.com) if you haven't already — you'll get a Measurement ID that looks like `G-XXXXXXXXXX`.
2. Open `index.html`, find the commented-out block near the top (search for `GOOGLE ANALYTICS 4`).
3. Uncomment it (remove the `<!--` and `-->`) and replace both instances of `G-XXXXXXXXXX` with your real Measurement ID.
4. Push the change. Traffic should start showing in GA4 within a few minutes (Realtime report is the fastest way to confirm it's working).

## 4. Turn on the contact form

1. Go to [formspree.io](https://formspree.io), sign up free, and create a new form using the email you want submissions sent to.
2. Formspree gives you a form ID / endpoint like `https://formspree.io/f/abc12345`.
3. Open `index.html`, find `<form action="https://formspree.io/f/YOUR_FORM_ID" ...>` near the bottom, and replace `YOUR_FORM_ID` with your real ID.
4. Push the change, then submit a test message on the live site to confirm it lands in your inbox. Formspree's free tier covers 50 submissions/month.

## What's left to personalize

- [ ] GA4 Measurement ID (see step 3 above)
- [ ] Formspree form ID (see step 4 above)
- [ ] Contact email inside Formspree's own dashboard (not in the code — you set this when you create the Formspree form)
- [ ] Custom domain, once purchased (see step 2 above)

Everything else — copy, pillars, background stats, links — is already filled in from your positioning doc, LinkedIn, and Substack.
