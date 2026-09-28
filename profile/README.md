<p align="center"><img src="https://raw.githubusercontent.com/finstats/finstats/main/web/assets/logo.svg" width="88" height="88" alt=""></p>
<h1 align="center">finstats</h1>

<p align="center">
  <b>See what your Jellyfin server is really doing.</b><br>
  Who is watching, what they watch, how it streams — and your year in review.<br>
  One small container. No database server. Set up in two minutes.
</p>

<p align="center">
  <a href="https://github.com/finstats/finstats"><b>Repository</b></a> ·
  <a href="https://github.com/finstats/finstats#get-started">Get started</a> ·
  <a href="https://github.com/finstats/finstats/releases/latest">Latest release</a> ·
  <a href="https://github.com/finstats/finstats/discussions">Discussions</a>
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/finstats/finstats/main/docs/screenshots/dashboard.png" alt="The finstats dashboard: two live streams, watch-time tiles and what is downloading" width="100%">
</p>

## What it answers

- **Who is watching right now?** Every stream as it happens: who, what, on which device and from where, and
  whether it plays directly or transcodes — and why.
- **Where does the effort go?** Peak concurrent streams, the apps that make your server transcode, how much
  leaves the house, and the titles nobody has ever pressed play on, sorted by the space they take.
- **What happened during a play?** Every pause, skip and subtitle switch, where people give up on a film, and
  which files never play at all.
- **Who watches together?** The people who press play on the same thing at the same time, and how much of
  their watching is in company.
- **Is that really them?** Every play and sign-in on a world map, with an alert when an account shows up
  somewhere it cannot be.
- **What is coming in?** Requests, releases and downloads from Sonarr, Radarr and Seerr — read, never changed.
- **How was your year?** A personal year in review for everyone, shareable as a set of story cards.

## Private by design

finstats only ever reads from Jellyfin, and people sign in with the Jellyfin account they already have. There
is no telemetry, and no font or script is loaded from the internet: it runs on your machine with its own built-in
database, using about 20 MB of memory. Every place it can reach out to is listed in its settings, so the promise is
one you can check. Each person sees their own statistics unless you give them more.

## Get started

You need Docker and a Jellyfin server (10.9 or newer).

```sh
docker run -d --name finstats --restart unless-stopped \
  -p 8080:8080 -e TZ=Europe/London -v "$PWD/data:/data" \
  ghcr.io/finstats/finstats:latest
```

Then open `http://your-server:8080` and point it at Jellyfin. Coming from Jellystat or Streamystats? Your history
imports in seconds — see the [README](https://github.com/finstats/finstats#moving-from-jellystat-or-streamystats).

## Get involved

Found a bug or have an idea? [Open an issue](https://github.com/finstats/finstats/issues/new/choose), or ask in
[Discussions](https://github.com/finstats/finstats/discussions). Want to help build it? Start with
[CONTRIBUTING.md](https://github.com/finstats/finstats/blob/main/CONTRIBUTING.md). Security problems go through
[private reporting](https://github.com/finstats/finstats/security/advisories/new), never an issue.

finstats is free software under the [GNU General Public License v3.0](https://github.com/finstats/finstats/blob/main/LICENSE).
