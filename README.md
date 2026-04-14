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

## fwtmp
run `sudo fwtmp <port> [minutes] [protocol]` to temporarily open a firewall port that auto-closes. This is for firewalld.

`sudo fwtmp 3000` opens port 3000 for 5 minutes. `sudo fwtmp 3000 15` keeps it open for 15. defaults to tcp, pass `udp` as a third arg if needed.

## loginfails
run `sudo loginfails` to see failed SSH login attempts grouped by IP.

defaults to the last 24 hours. `sudo loginfails 7` looks back 7 days, `sudo loginfails --all` searches everything. works with journalctl, auth.log, and secure.
