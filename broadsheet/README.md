# broadsheet

a writer's personal-broadsheet layout — warm parchment paper, deep ink, rust accents. big multi-line serif title up top, an inverted callout strip for an opinion or quote, a marquee strip with location/edition/listening, and a two-column nav of "library" and "meta" sections.

**[view live →](https://demos.penjurupikiran.com/broadsheet/)**

---

## what it's good for

- a personal site for a writer / essayist / critic
- anywhere you want a strong masthead aesthetic without it feeling like a magazine homepage
- sites that publish slowly and want the slowness to read as deliberate (the "read with patience" pill, the marquee strip, the dark featured-quote section)
- single-author personal broadsheets in the henry-codes / kottke / waxy mode

## what it's not

- not a multi-author publication (the whole layout is shaped around one persona, one wordmark, one voice)
- not a feed (no infinite scroll, no chronological dump — the home page is curated)
- not a build-step thing — single HTML file, inline CSS, no JS, system fonts only

---

## using it

1. copy `index.html` into your own project
2. open it in your editor — all layout + CSS is inline
3. swap the placeholder copy for your own (search for `Esther` to find the persona, `vol. iii` for the version label, `Notes from / a long / paper trail.` for the hero title)
4. swap the illuminated capital `E` in the hero ornament for your own initial — search for `content: "E"` in the `<style>` block
5. for additional pages, copy `index.html` to `essays.html` / `about.html` etc. and adapt the body content; the masthead + nav is fine to keep identical across pages

---

## customize

- **palette**: search the `<style>` block for `--paper`, `--ink`, `--accent` — there are 9 CSS variables in `:root`. Swap the hex codes to retune the whole layout in one place
- **fonts**: body and display both use `Georgia, 'Iowan Old Style', 'Charter', Cambria, serif` (system serif). nav meta-labels and the marquee use the system sans (`-apple-system, ...`). swap either family for whatever you like — no Google Fonts dependency
- **callout strip** (the dark band up top): swap the copy for whatever opinion / quote / weather / status you want there. or remove the `<aside class="callout">` block entirely if it doesn't fit
- **hero title segments**: each `<span class="seg">` is a separate line so you can play with line-breaks visually rather than relying on word-wrap
- **marquee**: replace the spans with whatever stats fit your site (location, current reading, edition number, last-updated, etc.). The pulsing red dot is a CSS-only animation; it auto-disables for `prefers-reduced-motion`

---

## inspiration

the structural skeleton (callout strip + masthead + multi-segment display title + marquee bar + grouped two-column nav + dark featured-quote section) is a tribute to the broadsheet-style personal sites of writer-developers who treat their site like a printed publication. palette (parchment + deep ink + rust + jade) and fonts (system serif Georgia stack + system sans) are entirely original and don't lift from any specific source.

---

## license

[CC BY 4.0](../LICENSE) — **attribution + linkback required.** Drop this somewhere visible on your site (the layout already includes one in the footer):

```html
<a href="https://penjurupikiran.com">layout by penjuru pikiran</a>
```
