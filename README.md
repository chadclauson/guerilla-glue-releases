# Glue

A Windows desktop app with two tools: SMS Verify (automated phone verification) and Unsubscribe (bulk email unsubscribe + inbox cleanup).

This repository hosts Glue's Windows installers and its auto-update feed — it's where the app downloads updates from. There's no source code here, just built releases.

### Download & install

Open the Releases page.
Under the latest version, download Glue-Setup-<version>.exe.
Run it. Windows SmartScreen may say "Windows protected your PC / unknown publisher" — Glue isn't code-signed yet, so that prompt is expected. Click More info → Run anyway.
Launch Glue from the Start menu.
Requires Windows 10 or 11 (64-bit). There are no macOS or Linux builds.

### Updating
Glue keeps itself up to date from this feed:

In Glue, click Check for Updates (top bar).
When a newer version is available here, Glue downloads it with a progress bar and installs it once you confirm.
You'll see the same one-time "unknown publisher" prompt on each update.
Auto-update works from version 1.1.0 onward. If you're running an older copy that predates auto-update, download the latest installer from Releases and run it once by hand — every update after that is automatic.

Updating quits and relaunches the app. To avoid interrupting paid work, Glue won't install while an SMS-verify or Unsubscribe run is in progress — finish or stop the run first, then update.

### What's in each release
Glue-Setup-<version>.exe — the installer (this is the file you download).
latest.yml and *.blockmap — used by the in-app updater; you don't need to download these manually.
Changelog
Each version's notes live in its release description on the Releases page — the same text Glue shows you in the update prompt.

### A note on trust
Installers are currently unsigned, which is why Windows shows the "unknown publisher" warning. Download integrity is backed by GitHub + HTTPS and the checksums published in latest.yml. Only ever download Glue from this repository's Releases page.
