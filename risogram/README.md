# risogram

a dark-mode portfolio layout with a fixed left-rail of four illustrated tiles in a riso-print palette — plum, peach, mustard, mint — pulled against deep midnight navy. each tile is a section (Studio, Work, Play, Hello) and carries its own hand-drawn SVG icon. main content scrolls to the right of the rail. responsive: in portrait / on mobile the rail collapses to a horizontal strip across the top. designed to feel like a darkroom with prints clipped to the wall.

**[view live →](https://demos.penjurupikiran.com/risogram/)**

---

## what it's good for

- a graphic designer / illustrator / studio portfolio
- a small one-person agency homepage
- any 4-section personal site where the nav itself can carry the visual identity (the tiles are the brand)
- riso-aesthetic sites that need to feel playful without being childish

## what it's not

- not a writing-heavy layout (the focus is the tiles + one short paragraph; if you want long-form text, [broadsheet](../broadsheet/) or [commonplace](../commonplace/) are better fits)
- not a build-step thing — single HTML file, inline CSS, no JS, system fonts, four inline SVG icons

---

## using it

1. copy `index.html` into your own project
2. open it in your editor — all layout + CSS + the four SVG icons are inline
3. swap the placeholder copy: search for `Tom Foolery` for the persona, `portomfolio` for the site name, and the section names (`Studio`, `Work`, `Play`, `Hello`)
4. swap or redraw the four SVG icons — each lives inside an `<a class="tile">` block and is around 20–30 lines of `<path>` / `<circle>` / `<rect>`. they're stylized geometric shapes you can edit by hand or replace wholesale
5. for additional pages, copy `index.html` to `studio.html` / `work.html` etc. and adapt the body content; this layout is built as a landing screen so subpages can be a different layout entirely

---

## customize

- **palette**: search the `<style>` block for `--plum`, `--peach`, `--mustard`, `--mint` — each tile reads from one variable. swap the hex codes to retune. there's a `*-deep` darker variant of each for hover / contrast. all 11 colors live in `:root`
- **fonts**: 100% system sans (`'Avenir Next', -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui, sans-serif`). swap the font-family in the `--sans` variable if you want something else. no Google Fonts dependency
- **tile count**: the grid is `grid-template-columns: repeat(4, 1fr)` — change to `repeat(3, 1fr)` for three sections, etc. each `<a class="tile">` block is independent, drop or duplicate freely
- **tile icons**: pure inline SVG, ~90×90 each, viewBox is `0 0 100 100`. use the palette colors directly in `fill="..."` and `stroke="..."` — they don't reference CSS variables since SVG presentation attributes don't pick up `:root` vars. swap the hex codes inside the SVG if you change the palette
- **icon palette inside each tile**: the icons mostly use `#1a0d22` (ink) and `#f7f1e3` (paper) plus small pulls of the *other* riso colors as accents — that's why they read as a family even though each tile is a different color

---

## inspiration

the structural skeleton — four large square tiles as nav, each illustrated, used as the entire home page — is a tribute to the portfolio-via-tile-grid pattern that some designer-portfolios use, where the navigation itself is the visual identity. palette (plum / peach / mustard / mint on cream) and the four custom SVG icons (desk lamp, portfolio stack, paper airplane, speech bubble) are entirely original and don't lift from any specific source.

---

## license

[CC BY 4.0](../LICENSE) — **attribution + linkback required.** Drop this somewhere visible on your site (the layout already includes one in the footer):

```html
<a href="https://penjurupikiran.com">layout by penjuru pikiran</a>
```
