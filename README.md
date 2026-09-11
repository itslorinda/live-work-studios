# Live-Work Studios — website

A free, static site for Live-Work Studios: design articles with affiliate product links, plus a spot to showcase projects.

## How to put this live on GitHub Pages (free)

1. **Create a repository.** On github.com, click the `+` in the top right → **New repository**. Name it something like `live-work-studios`. Keep it Public. Don't add a README (you already have one).

2. **Upload these files.** On the new repo's page, click **Add file → Upload files**, then drag in everything from this folder (`index.html`, `styles.css`, `README.md`, and the `articles` folder with `built-in-workshop.html` inside it). Commit the changes.

3. **Turn on Pages.** In the repo, go to **Settings → Pages**. Under "Build and deployment," set Source to **Deploy from a branch**, Branch to **main** and folder to **/ (root)**. Save.

4. **Wait about a minute**, then refresh that same Settings → Pages screen — it'll show your live URL, something like:
   `https://your-username.github.io/live-work-studios/`

That's it — no build step, no server, free hosting for as long as the repo stays public (or with GitHub Pro, private too).

## Adding a new article

1. Duplicate `articles/built-in-workshop.html`, rename it (e.g. `articles/sliding-wall.html`).
2. Update the `<title>`, the zone label (Create / Entertain / Stay), the heading, and the body copy.
3. Update the `.pick` blocks with your real affiliate links — swap the `href="#"` for your actual tracking URL.
4. Add a matching `<article class="article-card">` block to `index.html` under `#articles` pointing at the new file.
5. Upload the new/changed files to GitHub the same way as step 2 above (or use `git push` once you're comfortable with it).

## Affiliate links — a few notes

- Every link out to a product you earn commission on should keep `rel="sponsored nofollow"` (already on the `.buy` links) — this is the standard the FTC and search engines expect for paid/affiliate links.
- Keep the disclosure paragraph at the bottom of every article that contains affiliate links. This isn't optional — FTC guidelines require clear disclosure of affiliate relationships.
- Common free-to-join affiliate programs for a design/home-products niche: Amazon Associates, individual brand affiliate programs (many furniture/hardware brands run their own), and marketplaces like ShareASale or Awin that aggregate several brands under one account.

## Next steps worth considering

- A custom domain (e.g. `live-workstudios.com`) can be pointed at GitHub Pages for the cost of just the domain registration (~$12/yr) — everything else stays free.
- If you start publishing articles often enough that copy-pasting the HTML template gets tedious, migrating to Jekyll (built into GitHub Pages, no extra cost) automates the article list and templating. Ask me any time and I'll set that migration up.
