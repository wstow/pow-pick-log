# POW Survivor — Public Pick Log

This repo is the public record of picks for the **Pick of the Week** survivor pool at
[footballmn.com](https://footballmn.com). It exists so that nobody has to take the
website's word for it — not even the commissioner's.

## What gets published

- `seasons/<year>/week-NN.csv` — one file per week: entry, pick slot, team, and the
  timestamp the pick was submitted.
- `seasons/<year>/admin-changes.csv` — every time an admin changed a pick on someone's
  behalf: the entry, slot, old team → new team, when it happened, and whether the change
  came **after kickoff** (the pool allows rare commissioner corrections; this makes each
  one public). The reason for the change and who made it stay in the pool's internal
  audit log — this file records only *what* changed and *when*.
- `seasons/<year>/HEAD.md` — a summary page carrying the head hash of the site's
  internal tamper-evident audit chain.

A pick appears here once its game kicks off — the same moment it becomes visible in the
app, never before. Since games kick off in waves (Thursday night, Sunday early, Sunday
late, Sunday night, Monday night), each week's file grows across the week: every wave of
reveals lands as its own commit, usually within minutes of kickoff. The commit history
shows exactly which picks were public at each point. The same rule applies to admin
changes — one is listed only once the teams involved have kicked off. Unrevealed picks
stay secret, exactly as in the pool itself.

## Why this exists

Survivor pools live and die on trust that nobody quietly changed a pick after the games
started. The site already keeps an internal audit log, but that log lives in the same
database an insider could edit. This repo is the outside witness:

- Every snapshot is a real git commit, timestamped and content-addressed by GitHub.
- The latest commit hash is shown on the pool's home page, so every member's browser
  sees the same record this repo holds.
- Nothing here is ever hand-edited — commits come only from the pool server.

If a pick were altered after kickoff — by a member, or by an admin with database
access — it would contradict the history already published here for everyone to see.
Admin corrections aren't hidden either — every one is listed in `admin-changes.csv`,
timestamped and flagged when it happened after kickoff.

## Reading the data

The CSVs are plain text — click any week file to view it, or use the repo's history to
see exactly when each snapshot landed. Slot codes like `7B` mean week 7, second pick
(weeks later in the season require multiple picks).

Questions about the pool itself? See the [rules](https://footballmn.com/rules).
