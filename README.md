# POW Survivor — Public Pick Log

This repo is the public record of picks for the **Pick of the Week** survivor pool at
[footballmn.com](https://footballmn.com). It exists so that nobody has to take the
website's word for it — not even the commissioner's.

## What gets published

A pick appears here once its game kicks off — the same moment it becomes visible in the
app, never before. Since games kick off in waves (Thursday night, Sunday early, Sunday
late, Sunday night, Monday night), each week's file grows across the week: every wave of
reveals lands as its own commit, usually within minutes of kickoff. The commit history
shows exactly which picks were public at each point. Unrevealed picks stay secret,
exactly as in the pool itself.

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

## Reading the data

The CSVs are plain text — click any week file to view it, or use the repo's history to
see exactly when each snapshot landed. Slot codes like `7B` mean week 7, second pick
(weeks later in the season require multiple picks).

Questions about the pool itself? See the [rules](https://footballmn.com/rules).
