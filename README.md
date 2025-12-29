# Backupnow

**NOTICE:** this script is no longer under development. To make really robust and efficient backups, I recommend using the [borg-go](https://github.com/AndrewDDavis/borg_go) scripts instead.

The `backupnow` script runs `rsync` to create a backup on a remote machine.

- This requires local and remote rsync binaries (Fink's is great, Ubuntu repos fine for local backups). For compiling, refer to [bombich](http://www.bombich.com/mactips/rsync.html).

- User config files go in `~/.backupnow`, root in `/usr/local/etc/backupnow`.  To run as root from a cron job requires `.bash_script_messages` in the `/root` directory.

## Usage

- The main script is called `backupnow`. To see the command-line options, run `backupnow -h`.

- The `backupprep` script is called from `backupnow`. It mounts the network share and disk image for backupnow.

- The `baklist` script may be run separately. It prepares files for backup that may be difficult to find otherwise, such as the list of installed applications on a Debian Linux system.

## Version History

- 1.4.1 -May 2011- new config syntax, code cleanup and robustness, email on error
- 1.4.0 -Apr 2011- deletes archives based on age rather than number
- 1.3.2 -Apr 2010- tweaks and bug fixes
- 1.3.1 -- generalize user, server, etc;  better sorting of archived files
- 1.3 -- delete old archive folders
- 1.2 -- error check added, specific handling of Music directory
