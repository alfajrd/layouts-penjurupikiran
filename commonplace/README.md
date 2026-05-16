# commonplace

a small notebook on the open web — fixed-width, two-column, warm-cream paper with a deep burgundy sidebar and brass accents. for personal sites in the slow / commonplace-book mode: short notes in the middle, a "now" block + links on the side, a chronological log down the page.

**[view live →](https://demos.penjurupikiran.com/commonplace/)** · _(once you've published a demo)_

---

## what it's good for

- a personal site that wants to feel like a kept notebook, not a feed
- a link log + reading log + occasional essay
- a "now" page with an `/about` and not much else
- anywhere the early-2000s personal-website mood fits — fixed width, hand-typeset, low chrome

## what it's not

- not responsive (deliberately — fluid-width breaks the era it's referencing). there's a horizontal scrollbar below 980px and that's the intended fallback. instructions for a fluid variant are in the `<style>` block comment if you want one
- not a build-step thing — single HTML file, inline CSS, system fonts only

---

## using it

1. copy `index.html` into your own project
2. open it in your editor — all layout + CSS is inline
3. swap the placeholder copy for your own
4. for additional pages, copy `index.html` to `notes.html` / `essays.html` / etc., update the nav `<a class="selected">` to point at the current page on each one
5. host it wherever — nekoweb, neocities, github pages, cloudflare pages, any static host

---

## customize

- **palette**: search the `<style>` block for `--paper`, `--ink`, `--bar`, `--plot` — there are about eight CSS variables in `:root` and the rest of the styles read from them. swap the hex codes to retune the whole layout
- **fonts**: body is `Georgia, Charter, Cambria, serif` (system fonts everywhere — no Google Fonts dependency). nav, labels, and the meta line use the system sans (`-apple-system, ...`). swap either family for whatever you like
- **structure**: the header + tab nav + main column + sidebar + footer are five blocks in HTML order. rearrange or drop any of them
- **fixed width**: change `width: 980px` in `header`, `#menubar`, `#frame`, and `footer` to a `max-width` and remove the explicit pixel widths on `#maincont` (`620px`) and `#auxcont` (`280px`) for a fluid variant

---

## inspiration

the structural skeleton — fixed page, gray tab-style nav, a brightly colored aside on the right — is a tribute to the late-90s / early-2000s personal-site mode that knowledge-management folks were keeping when blogs were still novel. the palette and fonts here are entirely original (warm cream + terracotta, system serif body) and don't lift from any specific existing site.

---

## license

[CC BY 4.0](../LICENSE) — **attribution + linkback required.** Drop this somewhere visible on your site (footer is fine, the layout already includes one):

```html
<a href="https://penjurupikiran.com">layout by penjuru pikiran</a>
```
