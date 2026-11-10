# Explain4me Status

Status page for [Explain4me](https://explain4me.com), built with
[Upptime](https://github.com/upptime/upptime): GitHub Actions checks every
component every 5 minutes and GitHub Pages publishes the page, so it stays up
even when the app's own infrastructure (Google Cloud) is down.

Components and the URL each one checks are in [`.upptimerc.yml`](.upptimerc.yml).

The page itself is [`index.html`](index.html), a single file with Explain4me's
branding (EN/ES, light/dark) that reads the data Upptime commits to
`history/` (`summary.json` and one `.yml` per component). GitHub Pages serves
it from `master`; Upptime's own Static Site CI is disabled.
The per-platform checks (`/api/health/<platform>`) fail when that platform
hasn't updated metrics in the last 12 hours.

Status page: https://status.explain4me.com
