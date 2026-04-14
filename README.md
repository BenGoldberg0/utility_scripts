# just some scripts I wrote and use regularly

## gitstuff
run `gitstuff "<commit message>"`.

it runs  `git add .`,  `git commit -m "your message"`, and `git push`.

## gitundo
run `gitundo` to undo your last commit but keep the changes staged.

you can also pass a number, like `gitundo 3`, to undo multiple commits.

## gitfresh
run `gitfresh` from any branch.

it switches to main (or master), pulls latest, switches back to your branch, and rebases. it auto-stashes any uncommitted changes.

## extract
run `extract <file>` to extract any common archive format.

supports `.tar.gz`, `.zip`, `.7z`, `.rar`, `.bz2`, `.xz`, `.zst`, and more. you can pass multiple files at once.

## note
run `note "your thought here"` to save a timestamped note to `~/notes.md`.

run `note` with no arguments to open your notes in your editor. run `note -l` to see your last 10 notes.

## weather
run `weather` for a forecast of your current location, or `weather "new york"` for a specific city.

for zip codes, run `weather 90210`. for international postal codes, add a country code like `weather "SW1A 1AA" GB`. add `-s` for a one-line summary.
