# Kickstand Design Company — website

A free, static site: five main pages, a set of affiliate-linked articles, and two product stores (art and lamps).

## Site map

- `index.html` — homepage
- `what-we-do.html` — About
- `floor-plans.html` — house/building designs (currently shows "Floor plans in progress")
- `articles.html` — index of design articles (affiliate links live inside each article)
- `articles/built-in-workshop.html` — sample article
- `art-store.html` — original art for sale (currently shows "Art designs in progress") — **not linked in navigation yet**, only reachable by its direct URL
- `lamp-store.html` — lamps for sale (currently shows "Lighting designs in progress") — **not linked in navigation yet**, only reachable by its direct URL
- `styles.css` — shared styling for every page

## Publishing to GitHub Pages (free)

1. **Create a repository** on github.com, or reuse an existing one.
2. **Upload all the files listed above**, keeping the `articles` folder as an actual subfolder — open it locally and drag its *contents* in, not the outer folder itself, or use "Create new file" and type `articles/built-in-workshop.html` as the filename to create the folder automatically.
3. In the repo, go to **Settings → Pages**. Set Source to **Deploy from a branch**, Branch to **main**, folder to **/ (root)**. Save.
4. Wait about a minute, refresh that screen, and your live URL will appear.

## Editing content later

- **Small tweaks** (a sentence, a price, a link): open the file on GitHub, click the pencil icon top-right, edit directly, scroll down and commit.
- **Bigger changes** (new product, new article, new page): easiest to come back and ask for the file to be rebuilt, then re-upload it the same way.

## Making a store public

When a store is ready, add its line back inside the `<nav class="site-nav">` block on every page (`index.html`, `what-we-do.html`, `floor-plans.html`, `articles.html`, `art-store.html`, `lamp-store.html`, and `articles/built-in-workshop.html`, where it needs `../` in front of the filename instead):

```html
<a href="art-store.html">Art Store</a>
<a href="lamp-store.html">Lamp Store</a>
```

Place each wherever you want it to sit in the menu order. You'll also want to add the matching card back to the "Explore Kickstand" section on `index.html`.

## Setting up the stores

Each store's "Buy" button is meant to link out to a **Stripe Payment Link** — free to set up, no monthly fee (Stripe takes roughly 2.9% + 30¢ per sale).

**To set one up per piece/lamp:**
1. Create a free Stripe account at stripe.com
2. In the Stripe dashboard, go to **Payment Links → New**
3. Add the product name, price, and a photo
4. Stripe gives you a checkout URL (e.g. `https://buy.stripe.com/xxxxx`)
5. Paste that URL into the product's buy button once the product card is built

## Adding a new article

1. Duplicate `articles/built-in-workshop.html`, rename it
2. Update the title, category label (Create/Entertain/Stay), heading, and body
3. Update the `.pick` blocks with real affiliate links, keeping `rel="sponsored nofollow"`
4. Add a matching `<article class="card">` block to `articles.html`
5. Keep the disclosure paragraph — FTC guidelines require clear disclosure on affiliate content

## Notes

- Fonts are Plus Jakarta Sans (headings) and Inter (body), both free via Google Fonts — close matches to the Söhne/Inter pairing from the brand board without the licensing cost of Söhne.
- Any photo you add should go in an `images` folder alongside the HTML, referenced like `<img src="images/photo-name.jpg" alt="description">`.

