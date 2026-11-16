# Lifecycle dashboard

Two static mock-ups of a dashboard that follows a software release lifecycle:
`master`, the release branches cut from it, the TeamCity jobs that have to be
duplicated for each new branch, the DB scripts repository (`head.txt`, one per
release) and the packaging on JFrog.

Each option is a single HTML file with mock data and no backend. Open the file
in a browser.

| File | Idea |
|---|---|
| `calendar.html` | A calendar. One time axis, one row per branch, and the checklist of the selected row underneath. Tracks `master`, the release being prepared and the last one shipped; older releases drop off. |
| `subway.html` | A subway map. Each branch is a line, each preparation task a station, with supporting panels below. |

In both, ticking a checklist item or changing a status is saved in the
browser's local storage only. The mock data sits in one marked block at the top
of each file's script, which is the part to replace when real Bitbucket,
TeamCity and JFrog data is connected.
