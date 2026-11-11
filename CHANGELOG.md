# Changelog

Dates are in Singapore time. The project is pre-1.0, so options may change between minor versions.

## 0.1.0 (11 Nov 2026)

The first tagged release. It is also part of [headless-kit](https://github.com/Sohwhat6420/headless-kit).

- Pulls public posts and comments for a subreddit over a date window, or one thread with its whole comment tree, from
  the Arctic Shift archive. No browser, no sign-in and no API key.
- Prints **one JSON line** on stdout saying what was written. Progress goes to stderr.
- A local `--grep` filter, de-duplication by id, and bodies cut to agent-sized lengths.
- Polite paging: 0.5 s between pages, waits out `429`s using `X-RateLimit-Reset`, identifies itself in the
  User-Agent, and has a page cap you set (`--max-pages`, default 30).
- An importable module as well as a CLI.
- 8 offline tests, run by CI on every push.

## Before 0.1.0

- **7 Nov 2026:** reshaped into an importable module with JSON-line output, `429` handling and tests. It also got a
  README with a measured run, notes on Arctic Shift's terms, CONTRIBUTING, issue templates and the MIT licence.
- **2 Nov 2026:** first written, in the monorepo it was extracted from. See [docs/HISTORY.md](docs/HISTORY.md).
