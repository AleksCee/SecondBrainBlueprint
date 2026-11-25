# Weekly synthesis Prompt

Determine the current ISO week (YYYY-WW, Europe/Berlin). Find every /wiki file changed since that week's Monday 00:00 via `git log --since=<monday-00:00> -- wiki/`, not a trailing 7-day window — keeps the filename and the content in sync no matter which day this runs.

Write /wiki/weekly/YYYY-WW.md summarizing themes, decisions and open questions from those changes, with a relative markdown link to each source entry. If the weekly file already exists, update it — merge in new changes, do not delete or overwrite what's there.
