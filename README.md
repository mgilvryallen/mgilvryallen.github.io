# M'Gilvry Allen's apps

The front page at https://mgilvryallen.github.io/, featuring the apps that live under it:
[Drone](https://github.com/mgilvryallen/drone), [Tunes](https://github.com/mgilvryallen/tunes),
[Theory](https://github.com/mgilvryallen/theory), [Little Guy](https://github.com/mgilvryallen/littleguy),
[Gas](https://github.com/mgilvryallen/gas) and [Soup](https://github.com/mgilvryallen/soup).

The list of apps is `apps.json`. To feature another app, add an entry there: its repo name
(`slug`), its `name`, a `color` (rust, ochre, woad, plum, teal or green), and a fallback sentence
about it (`about`). Two optional switches: `"hidden": true` keeps an app off this page while it's in
progress, and `"website": false` keeps it off the Projects page on
[mgilvryallen.com](https://mgilvryallen.com/projects.html#digital), which reads this same file.
That page shows `short` (a line for the website) if it's filled in, otherwise the app's description.

The apps describe themselves: each card's sentence is the `description` in that app's own
`manifest.webmanifest`, read when the page opens, so updating an app's manifest updates its card.
The `about` in `APPS` is only shown until then, or if the manifest can't be read. The icon comes from
the manifest too (its SVG entry, with any `?v=` an app adds so a new icon isn't stuck in a
browser's cache), and the fonts from the apps, so the page always matches them.

There's no service worker on this page on purpose: one at the site's root would take over every
app below it.
