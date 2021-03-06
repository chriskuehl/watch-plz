[![Build Status](https://travis-ci.org/asottile/watch-plz.svg?branch=master)](https://travis-ci.org/asottile/watch-plz)

watch-plz
=========

Ensure all of your repositories are watched.

### why

- My current employer also uses github
- They have lots of repositories
- I don't want to watch all of the repositories
- So I uncheck the `Automatically watch repositories` setting
- I then forget to watch my own repositories

### usage

Grab a token [here](https://github.com/settings/tokens/new).
`public_repository` should be sufficient for this token -- though if you want
to watch private repositories you'll need the full `repo` permission.

Modify `DONT_WATCH` in the `watch-plz` script.

```bash
GH_TOKEN=... ./watch-plz --dry-run
```

### how I use it

I use [travis-ci cron](https://docs.travis-ci.com/user/cron-jobs/) to run this
periodically.
