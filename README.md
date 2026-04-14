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
run `sudo fwtmp <port> [minutes] [protocol]` to temporarily open a firewall port that auto-closes.

`sudo fwtmp 3000` opens port 3000 for 5 minutes. `sudo fwtmp 3000 15` keeps it open for 15. defaults to tcp, pass `udp` as a third arg if needed.

## loginfails
run `sudo loginfails` to see failed SSH login attempts grouped by IP.

defaults to the last 24 hours. `sudo loginfails 7` looks back 7 days, `sudo loginfails --all` searches everything. works with journalctl, auth.log, and secure.

## portdiff
run `sudo portdiff` to snapshot your open ports and compare against the last snapshot.

run it again later to see what's new or closed since last time. `sudo portdiff --show` lists current ports, `sudo portdiff --reset` clears saved snapshots.

## cronaudit
run `sudo cronaudit` to list every scheduled task on the system in one place.

covers user crontabs, /etc/crontab, /etc/cron.d/, cron.daily/hourly/weekly/monthly, at jobs, and systemd timers.

## snapstate
run `sudo snapstate` to capture a point-in-time snapshot of the system's security state.

saves ports, processes, connections, logins, firewall rules, cron jobs, SUID files, and more to a timestamped file. run `sudo snapstate --diff` to compare the last two snapshots.

## whowasin
run `sudo whowasin` to see a unified timeline of who accessed the machine and when.

combines `who`, `last`, `lastb`, and SSH auth logs into one view. defaults to 24 hours, `sudo whowasin 7` for 7 days, `sudo whowasin --current` for active sessions only.

## susprocess
run `sudo susprocess` to flag processes running from suspicious locations or states.

checks for processes in /tmp, /dev/shm, /var/tmp, deleted binaries still running, hidden directory paths, and root processes in user-writable directories.

## expiring
run `sudo expiring` to check for soon-to-expire SSL certs, user passwords, and old SSH keys.

defaults to 30 days. `sudo expiring 7` for things expiring within a week, `sudo expiring 90` for a wider check.
