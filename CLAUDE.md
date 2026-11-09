# The front page

Each app's card shows the `description` from that app's `manifest.webmanifest`, read live. When an
app changes, update its manifest description in the app's own repo (each app's CLAUDE.md says so);
keep the fallback `about` in `apps.json` here roughly in step. A new app needs an entry in `apps.json`
and a mention in the README's list of apps.

`apps.json` is also read by Gordon's Netlify site (mgilvryallen.com/projects.html, Building →
Digital), so changing it changes that page too, without a Netlify deploy. Fields: `slug`, `name`,
`color` (rust/ochre/woad/plum/teal/green), `about` (fallback description), `short` (Gordon's own
one-liner for his website; blank means use the manifest description), `hidden: true` (off this
page), `website: false` (off mgilvryallen.com; on by default). Keep it valid JSON: a stray comma
empties both pages' app lists. Don't rename the fields: the website's code reads them.
