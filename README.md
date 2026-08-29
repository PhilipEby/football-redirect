# playmaker.philipeby.com — permanent alias

Forwards every request to **football.philipeby.com**, preserving path, query
and fragment. `/sharing.html` lands on `/sharing.html`, not the front door.

This is permanent. The subdomain is never retired, so old bookmarks and the
links published in earlier builds of the app keep working indefinitely and
nobody has to update anything.

- `index.html` — forwards the root
- `404.html` — forwards every other path (GitHub Pages serves this for any
  unmatched request, which is what makes path preservation possible on a
  static host)
- `CNAME` — `playmaker.philipeby.com`

GitHub Pages allows one custom domain per repository, which is why this is
separate from the app repo. Serve from `main`, folder `/` (root).

A static host cannot issue a real HTTP 301. If the domain ever moves to
Cloudflare, replace this with a Redirect Rule for a true permanent redirect.
