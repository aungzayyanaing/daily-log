# daily-log

A plain Markdown daily log, kept in `daily-log.md`. A GitHub Actions workflow adds each day's entries automatically, so the log grows without manual editing.

## What it contains

- `daily-log.md` — the log. It starts with `# Daily Log`, followed by one line per entry in the format `- YYYY-MM-DD Daily log entry N`, for example `- 2026-11-12 Daily log entry 1`.
- `.github/workflows/daily-log.yml` — the automation that adds entries.
- `LICENSE` — MIT License.

## How it works

The `Daily Log` workflow runs every day at 17:00 UTC. It takes the date in the `Asia/Rangoon` timezone, checks whether that date already has an entry in `daily-log.md`, and if not, appends entries 1 through 10 for that date — each as a separate commit, with messages such as `Daily log 2026-11-12 entry 1` — then pushes to `main`. If the date already has an entry, the run does nothing.

## How to use it

- To read the log, open `daily-log.md`.
- To add a day's entries on demand, go to Actions > Daily Log > Run workflow.
- To add an entry by hand, append a line to `daily-log.md` in the same format and commit it.
- To change the schedule or the number of entries, edit `.github/workflows/daily-log.yml`.

## Scope

There is nothing to install, build, or run locally: this repository has no application code, dependencies, or tests. The entries are short placeholder lines with a date and a number; they do not contain journal text.

## License

MIT — see `LICENSE`.
