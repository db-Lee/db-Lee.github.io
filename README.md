# db-Lee.github.io

Personal homepage of Dong Bok Lee, served by GitHub Pages at https://db-lee.github.io/.

The site is a single static `index.html` (inline CSS, no build step) plus `photo.jpg`. `.nojekyll` makes Pages serve the files as-is. Any push to `main` goes live in a minute or two.

## How to update

**On github.com:** open `index.html`, click the pencil icon, edit, then **Commit changes**.

**Locally:**

```
sl pull --rebase
# edit index.html and check it in a browser
sl commit -m "Update homepage"
sl push --to main
```

## Where things are in `index.html`

| What | Search for |
|---|---|
| Header line under the name | `Currently a research intern` |
| About text and interests | `<section id="about"` |
| Experience / education entries (one `<li>` each) | `<section id="experience"` / `<section id="education"` |
| Publications, grouped by year | `<section id="publications"` |
| Footer date | `Last updated` |

To add a paper, copy an existing block and paste it at the top of its year. For a new year, copy a whole `<div class="year">` block and change the `<h3>`.

```html
<li class="pub">
  <p class="title"><a href="PAPER_URL">Paper Title</a></p>
  <p class="authors"><b>Dong Bok Lee</b>*, Coauthor A*, Coauthor B</p>
  <p class="meta"><span class="venue">ICLR 2027</span><a href="PAPER_URL">Paper</a><a href="CODE_URL">Code</a></p>
</li>
```

To change the photo, replace `photo.jpg` with an image of the same name.

The old CV site stays at https://db-lee.github.io/online-cv/ (repo `db-Lee/online-cv`).
