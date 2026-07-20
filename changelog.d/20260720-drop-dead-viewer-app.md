### Fixed

#### CI no longer fails on the removed viewer-app frontend

`coverage.yaml`, `nightly.yaml` and `release.yaml` still set up Node, pointed the
npm cache at `viewer-app/package-lock.json`, and ran `npm ci --prefix viewer-app`.
That directory was removed in f51ea46 ("Purge the angular for now") and no
`package.json` is tracked anywhere today, so `actions/setup-node` failed every
one of those jobs with "Some specified paths were not resolved, unable to cache
dependencies". The Node and npm steps are removed.
