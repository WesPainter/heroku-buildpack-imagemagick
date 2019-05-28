heroku-buildpack-imagemagick-7
=================================

Forked to pull down the imagemagick-7 binaries.

## How it works
Rather than pulling down binary dependencies from a package manager and extracting them into place, this buildpack compiles Imagemagick from source the first time an app is built with it. The compiled binaries are cached for future builds, so this penalty is only incurred once.

This has the downside of a (potentially very long) deploy time for the first push, with the benefit of a less-fragile build product that's somewhat less likely to break due to platform and dependency shifts. Or at least, that's the hope!
