# featherbomb

A personal browser start page — one self-contained `index.html` file, no build step,
no dependencies to install. Open it locally or serve it from GitHub Pages and it just
works.

**Live site:** https://anthorian.github.io/destination/

## What's on the page

- **Search rail** — quick-search boxes for Google, Google Maps, eBay, Amazon,
  YouTube, and Craigslist. Each submits a normal form (no JavaScript required for
  search to work) and opens results in the same tab.
- **Link sections** — Intel (news), Industry (design/tech), Humans (mail, social,
  AI tools), Electrotainment (gaming), Music, Local (Reston/DC), Hardware
  (Gadgetry, Photography, Thread, Badass), and Guitars — around 160 hand-picked
  links in total.
- **Suggested links** — every list also shows three grey, ✦-marked links drawn
  from a curated pool of about a dozen options per section. The pool reshuffles
  on every page load, so the mix of "suggested" links is different each time you
  open the page.
- **Animated hero** — a full-bleed color gradient with a small canvas-based
  particle system drifting across it. Colors and layout are randomized per load;
  the motion is a damped random walk, so it never repeats or visibly loops. It
  holds still automatically for anyone with "reduce motion" turned on.

## Tech notes

- Single HTML file (~35 KB): all CSS and JavaScript are inline, no external
  scripts except Google Fonts.
- Layout uses CSS Grid with `subgrid`, so sibling columns always line up even
  when the lists inside them are different lengths.
- No frameworks, no build tools — just modern HTML/CSS/JS.

## Updating the page

This repo has no CI/build step. To change anything (add a link, edit the
suggestion pools, tweak styling):

1. Edit `index.html` directly (either locally, or with GitHub's in-browser
   editor — click the pencil icon on the file).
2. Commit the change to `main`.
3. GitHub Pages rebuilds automatically, usually within a minute or two.

## Hosting

Pages is configured to deploy from the `main` branch, root folder
(Settings → Pages). No separate build is needed since `index.html` is served
as-is.
