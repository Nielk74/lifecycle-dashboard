# Lifecycle dashboard

Three static mock-ups of a dashboard that follows a software release lifecycle:
`master`, the release branches cut from it, the TeamCity jobs that have to be
duplicated for each new branch, the DB scripts repository (`head.txt`, one per
release) and the packaging on JFrog.

Each option is a single HTML file with mock data and no backend. Open the file
in a browser.

| File | Idea |
|---|---|
| `board.html` | A status board. The release being prepared is a row of large steps at the top; below it, one column per version (`master`, the release in preparation, the live one) with the same rows in each: code, TeamCity jobs, DB scripts, JFrog artifacts and the environments running that version. Rows open for details, a filter shows problems only, and the open step and filter are kept in the URL. |
| `calendar.html` | A calendar. One time axis, one row per branch, and the checklist of the selected row underneath. |
| `subway.html` | A subway map. Each branch is a line, each preparation task a station, with supporting panels below. |

All three track `master`, the release being prepared and the last one shipped;
older releases are left out.

In all of them, ticking a checklist item or changing a status is saved in the
browser's local storage only. The mock data sits in one marked block at the top
of each file's script, which is the part to replace when real Bitbucket,
TeamCity and JFrog data is connected.
