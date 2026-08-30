# fleet-releases

The SideStore source for **Fleet** — one console for every Claude Code session
on your machine.

This repository holds three files and no code: the `.ipa`, the `apps.json`
manifest that tells SideStore a build exists, and the icon. Fleet itself is
private; this is public because **SideStore fetches a source anonymously**, with
no token and no session, so a manifest in a private repository returns 404 on
the phone.

## Add it to SideStore

Sources → **+** → paste:

```
https://raw.githubusercontent.com/12shamali12/fleet-releases/main/apps.json
```

The `.ipa` is **unsigned on purpose**. SideStore signs it on the device with your
own Apple ID, so nothing here carries a certificate. A free Apple ID's signature
expires after seven days and SideStore refreshes it in the background; a paid
developer account lasts a year.

## What updating means here

The app loads its interface from your own laptop's daemon, so a change to a
screen arrives the next time you open the app — no build, no reinstall. A new
`.ipa` is only needed when the native shell changes: the icon, permissions, or
the address it points at.
