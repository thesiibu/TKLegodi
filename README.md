# Tshepo & Kelebogile — Save the Date RSVP

A single-page RSVP site matching the Save the Date invitation. No build step — it's one `index.html` file.

## 1. Connect Formspree (so RSVPs actually go somewhere)

1. Go to https://formspree.io and sign up (free tier is enough for a wedding).
2. Create a new form. Formspree gives you an endpoint like:
   `https://formspree.io/f/abc1234`
3. Open `index.html`, find this line near the top of the RSVP form:
   ```html
   <form id="rsvpForm" action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
   ```
   Replace `YOUR_FORM_ID` with your real endpoint.
4. Formspree will ask you to confirm your form the first time someone submits it (check your email) — send yourself a test RSVP after deploying to activate it.

Every RSVP will then arrive in your inbox, and you can also view/export all responses (as CSV) from your Formspree dashboard at any time — that's your guest list.

## 2. Put it on GitHub Pages

1. Create a new GitHub repository (e.g. `tshepo-kelebogile-wedding`).
2. Upload `index.html` to the root of the repo (drag-and-drop works fine on github.com).
3. Go to the repo's **Settings → Pages**.
4. Under "Build and deployment", set **Source: Deploy from a branch**, branch: `main`, folder: `/ (root)`.
5. Save. GitHub will give you a live URL after a minute or two, usually:
   `https://YOUR-USERNAME.github.io/tshepo-kelebogile-wedding/`

That URL is what you share on WhatsApp.

## 3. Optional — custom domain

If you'd rather share something like `rsvp.tshepoandkelebogile.com`, buy the domain from any registrar and point it at GitHub Pages (Settings → Pages → Custom domain). Not required — the default github.io link works fine.

## Notes

- This version has no built-in guest-list page on the site itself (unlike the Claude-hosted version) — your guest list lives in Formspree's dashboard/email instead, since a static GitHub Pages site has nowhere else to store submissions.
- If you'd rather have the guest list live in a Google Sheet instead of Formspree, let me know and I can rebuild the form for that instead.
