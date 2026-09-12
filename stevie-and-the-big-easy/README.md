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

The "Tell us about the date" form has no backend: it gathers the fields and
either hands them to the visitor's email app (`mailto:`) or copies them to the
clipboard. That works anywhere the page is hosted, including inside an Artifact.

On Netlify it can become a real form instead — add `data-netlify="true"` and a
`name` to the `<form>`, and submissions land in the Netlify dashboard with email
notification. Ask and I'll wire it up.

## The mailing list

"Join the list" currently points at the existing Kit signup at
music.steveheavenstone.com. If a band-specific list gets made, swap that one URL
in the booking sidebar.

## Still to confirm

- Band member names and instruments (the page credits only the bandleader).
- The **Stage & sound** figures are a sensible draft, not a real rider — check
  the stage sizes, power and input counts before sending this to a venue.
- Upcoming dates: there is no dates section yet. Add one when there's a run to list.
