# M'Gilvry Allen's apps

The front page at https://mgilvryallen.github.io/, featuring the apps that live under it:
[Drone](https://github.com/mgilvryallen/drone), [Tunes](https://github.com/mgilvryallen/tunes),
[Little Guy](https://github.com/mgilvryallen/littleguy), [Gas](https://github.com/mgilvryallen/gas)
and [Soup](https://github.com/mgilvryallen/soup).

Everything is in `index.html`. To feature another app, add a line to the `APPS` list there: its
repo name, its name, a sentence about it, and a color. Add `hidden: true` to keep one off the
page while it's in progress (Little Guy, for now). The icon and fonts come from the apps
themselves, so the page always matches them.

There's no service worker on this page on purpose: one at the site's root would take over every
app below it.
