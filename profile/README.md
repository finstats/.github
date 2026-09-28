<p align="center"><img src="https://raw.githubusercontent.com/finstats/finstats/main/web/assets/logo.svg" width="72" height="72" alt=""></p>
<h1 align="center">finstats</h1>
<p align="center"><b>Playback statistics for Jellyfin.</b></p>

finstats is a self-hosted companion to a Jellyfin media server. It watches what the server plays and turns it into
answers: who watches what, how it reaches them, what the library is really used for — and, once a year, each
person's year in review.

## Why it exists

Jellyfin tells you what is playing right now. It does not tell you that one app transcodes everything it touches,
that four people stream at once every Saturday, or that a third of the disk is films nobody has ever pressed play on.

The trackers that did answer those questions came with a database server of their own to run and look after.
finstats was made to be the small one: a single program with its own built-in database, set up in a couple of
minutes and then left alone. It only ever reads from Jellyfin, keeps everything on your own machine, and shows each
person their own statistics unless you decide otherwise.

**→ [finstats/finstats](https://github.com/finstats/finstats)** — what it shows, how to install it, and how to help.
