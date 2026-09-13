# Stevie and the Big Easy — EPK

A self-contained one-page electronic press kit. No build step, no dependencies:
`index.html` carries its own CSS, and `img/` carries the photos and video stills.

**Live here:** https://steveheavenstone.github.io/ear-training/stevie-and-the-big-easy/

## To move it onto steveheavenstone.com

Copy this folder into the Netlify site as `big-easy/` (or point a
`bigeasy.` subdomain at it) and link it from the Bands page. Nothing in the
page depends on where it is served from — all asset paths are relative.

## The look

Mardi Gras after dark: purple / green / gold, a fleur-de-lis drawn as an inline
SVG symbol (reused for section marks and set-list bullets), and a French Quarter
wrought-iron grille repeated along each section divider. Type is Ultra for
display, Barlow Condensed for labels, Karla for body.

## Sources for the content

| Section | Where it came from |
|---|---|
| Promo artwork (`promo-art.jpg`) | the May 22 flyer in Canva, cropped above the date and venue block; full flyer kept as `flyer-may22-full.jpg` |
| Earlier promo artwork | `promo-art-2025-full.jpg`, from the band promo video |
| Video stills | the band's videos on youtube.com/@steveheavenstone |
| Bio | the band's own billing (Westside Blues & Jazz listing) and promo art |
| Set list | the chart folders in the "Stevie and the Big Easy" Drive folder |
| Photos | the press photos on steveheavenstone.com/media |

## The booking form

The "Tell us about the date" form is wired for **Netlify Forms**: the markup
carries `name="booking"`, `data-netlify="true"`, the hidden `form-name` field and
a `bot-field` honeypot, so Netlify picks it up at deploy time. The script posts
the fields plus a readable `summary` field, then resets and confirms.

It only posts on the real site — the host must be `steveheavenstone.com`,
a subdomain of it, or `*.netlify.app` (see `NETLIFY_HOSTS` in the script).
Anywhere else — a local file, an Artifact, a preview — the same button composes
the email in the visitor's mail app instead, so the form is never a dead end.

After the first deploy: Netlify -> Forms -> confirm **booking** is listed, then
add a notification so submissions reach an inbox (Forms -> Form notifications ->
Email notification). The free tier covers 100 submissions a month.

## The mailing list

"Join the list" points at the existing Kit signup at music.steveheavenstone.com.
For a band-only list, make a new form in Kit (Grow -> Landing Pages & Forms), tag
subscribers something like `stevie-big-easy`, and swap that one URL in the
booking sidebar.

## Still to confirm

- Band member names and instruments (the page credits only the bandleader).
- The **Stage & sound** figures are a sensible draft, not a real rider — check
  the stage sizes, power and input counts before sending this to a venue.
- Upcoming dates: there is no dates section yet. Add one when there's a run to list.
