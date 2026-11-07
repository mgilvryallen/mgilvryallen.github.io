# M'Gilvry Allen's apps

The front page at https://mgilvryallen.github.io/, featuring the apps that live under it:
[Drone](https://github.com/mgilvryallen/drone), [Tunes](https://github.com/mgilvryallen/tunes),
[Theory](https://github.com/mgilvryallen/theory), [Little Guy](https://github.com/mgilvryallen/littleguy),
[Gas](https://github.com/mgilvryallen/gas) and [Soup](https://github.com/mgilvryallen/soup).

Everything is in `index.html`. To feature another app, add a line to the `APPS` list there: its
repo name, its name, a color, and a fallback sentence about it. Add `hidden: true` to keep one off
the page while it's in progress.

The apps describe themselves: each card's sentence is the `description` in that app's own
`manifest.webmanifest`, read when the page opens, so updating an app's manifest updates its card.
The `about` in `APPS` is only shown until then, or if the manifest can't be read. The icon comes from
the manifest too (its SVG entry, with any `?v=` an app adds so a new icon isn't stuck in a
browser's cache), and the fonts from the apps, so the page always matches them.

There's no service worker on this page on purpose: one at the site's root would take over every
app below it.
