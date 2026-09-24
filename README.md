# JApps
Five Android apps that keep your data on your phone, as files you can still read
if the apps disappear. No account, no company server, no telemetry.

The signed APKs are published under Releases. The source is not published here.

<p align="center">
  <img src="images/jnotes.png" alt="JNotes showing a list of notes with tag filters" width="160">
  <img src="images/jcalendar.png" alt="JCalendar month view showing event titles in the day cells" width="160">
  <img src="images/jauth.png" alt="JAuth showing two factor codes counting down" width="160">
  <img src="images/jphone.png" alt="JPhone showing the contacts list" width="160">
  <img src="images/jphotos.png" alt="JPhotos showing a folder of photos as a grid" width="160">
</p>
<p align="center">
  <sub>JNotes &nbsp; &middot; &nbsp; JCalendar &nbsp; &middot; &nbsp; JAuth &nbsp; &middot; &nbsp; JPhone &nbsp; &middot; &nbsp; JPhotos</sub>
</p>

---

## JAuth - two-factor codes

Codes are generated on the phone and stay there. Secrets are encrypted with a
key that never leaves the device, and the phone will not use that key until it
has seen your fingerprint or PIN.

It imports from Google Authenticator, Aegis, 2FAS, or any `otpauth://` list, so
trying it does not mean re-enrolling every account by hand. You can export
everything to a file whenever you want, or save an encrypted backup under a
passphrase you choose, and set up a different authenticator from it.

No Google Play Services. Free.

## JCalendar - events as `.ics` files

Each event is a single `.ics` file, kept in storage only the app can reach. Any
calendar application can read them, and a file copied off your backup is the
same file that is on the phone. Month view shows event titles rather than dots.

## JNotes - Markdown notes

Plain `.md` files that open in any editor, on any computer, years from now.
Wikilinks and tags use the same syntax as Obsidian, so a mirrored folder opens
there and works. Live preview, tappable checklists that write back into the
file, attachments and full-text search.

Notes you would rather keep private go in a vault, unlocked by password or
fingerprint with an idle timeout you set. Vault notes are encrypted on the
device and are never written to the backup in readable form.

## JPhone - phone, messages and contacts

A replacement for the phone, messages and contacts apps, in three tabs. It
places and answers calls with its own in-call screen, including over the lock
screen, and handles SMS and MMS with photos and voice notes.

Contacts are written out as `.vcf` files and conversations as readable
transcripts.

## JPhotos - gallery and editor

Reads the folders Android already uses, such as Camera, Screenshots and
Downloads, and does not move or rename anything. Uninstalling it leaves every
photo where it was.

Nothing uploads on its own. Every transfer is one you start, on pictures you
picked, and editing saves a copy unless you choose to overwrite. Android 14's
"selected photos only" grant is supported, so you can hand over a few pictures
instead of the whole library.

---

## What the five have in common

Your data lives in the app. Switch backup on and a matching copy is kept in a
folder you choose, either on the device or on your own FTP, SFTP or SMB server.
The backup is a copy, so deleting an app leaves it alone. There is no JApps
server.

Server backup is the only paid feature, and one key covers all five. Paste it
into any one of the apps and the other four pick it up when they next start.

One theme across all five: light, dark or system, in eight shared palettes.
Every app opens on Paper.

<p align="center">
  <img src="images/theme-aurora.png" alt="The aurora palette" width="150">
  <img src="images/theme-camo.png" alt="The camo palette" width="150">
  <img src="images/theme-gears.png" alt="The gears palette" width="150">
  <img src="images/theme-orrery.png" alt="The orrery palette" width="150">
  <img src="images/theme-scope.png" alt="The scope palette" width="150">
  <img src="images/theme-sonar.png" alt="The sonar palette" width="150">
  <img src="images/theme-synthwave.png" alt="The synthwave palette" width="150">
  <img src="images/theme-terminal.png" alt="The terminal palette" width="150">
</p>
<p align="center">
  <sub>Aurora &nbsp; &middot; &nbsp; Camo &nbsp; &middot; &nbsp; Gears &nbsp; &middot; &nbsp; Orrery &nbsp; &middot; &nbsp; Scope &nbsp; &middot; &nbsp; Sonar &nbsp; &middot; &nbsp; Synthwave &nbsp; &middot; &nbsp; Terminal</sub>
</p>

---

## Install them

Install as many or as few as you want. They work on their own, and none of them
needs the others.

Android will not install an app from outside a store until you allow it once.

1. On the phone, open [Releases](../../releases) and download the ones you want.
   Each is a single `.apk` file.

2. Tap a downloaded file. Android will say it is not allowed to install unknown
   apps from this source.

3. Tap **Settings** in that message, turn on **Allow from this source**, then
   press back and tap **Install**. The remaining files install without asking
   again.

4. Open the app. Permissions are requested when they are needed, with the reason
   on screen.

You can turn that permission back off afterwards. It applies to the app you
downloaded with, usually your browser, and not to the phone as a whole. Updating
later is the same steps, and installing over the top keeps your data.

### JPhone needs one extra step

JPhone cannot place calls or send texts until you make it the default phone and
SMS app. It offers to do that the first time you open it. If you decline and
change your mind later, it is under Settings, then Apps, then Default apps, and
setting the old apps back is the same screen.

---

## Getting a key

The five apps are free to download and use. Server backup, which mirrors your
data to your own FTP, SFTP or SMB server, is the one feature a key unlocks.
Everything else, including local folder backup, works without one.

**Suggested: $25.** One key, all five apps, paid once. There is no subscription
and no second purchase. Any amount is welcome, and I will send a key either way.

| Chain | Address |
|---|---|
| Solana | `862YZXoRvaoTiP1AkQEEZ5FFGgPFsUhbEoRu4r44RhSe` |
| Ethereum | `0xF890c6A128920D145D47753D0b1159fA4Db2861d` |

Then email **jessymelanson1265@proton.me** with the transaction hash. I check the
chain and reply with a key. There is no checkout, no account and no third party
in the middle.

Transfers on both chains are irreversible. Check the address character by
character, and send only native SOL or ETH, or standard tokens on those chains.

### How the key is checked

The key is a block of text. Paste it into any one of the five apps and the other
four pick it up on their next launch.

It is verified on the device, against a SHA-256 hash compiled into the app.
Nothing is transmitted and no licence server is contacted, so the apps work the
same with no network at all. Three things follow from that:

- A key works offline and cannot be revoked remotely.
- It is not tied to a device or an account, because neither is registered
  anywhere.
- Keep it somewhere safe. I can resend one from the email you used, but there is
  no account to recover it from.

Please do not share your key. Verification is offline by design, so the only
thing keeping this sustainable is people not passing keys around.

---

## Verify what you downloaded

| File | Version | SHA-256 |
|---|---|---|
| `JAuth-release.apk` | 1.0.1 | `970abcb05a694fe7d8aa9dea30f10ba893f9692d33adc0a4fbe55b923c35f58b` |
| `JCalendar-release.apk` | 1.0.0 | `60dcca4c00ca326ac7241cd2ec07c97dd346c0f394c1cb34a604a9060a9b2185` |
| `JNotes-release.apk` | 1.0.0 | `f6d4c73c1cc826801f1ba74ae57b9eaf9bb175e161f62ea58668711055478568` |
| `JPhone-release.apk` | 1.0.1 | `1dd1c08c742c40be3f8fab5c76ab0d247467070d9cb2828132c7362dde4fac78` |
| `JPhotos-release.apk` | 1.0.0 | `3417347a0c993f50cab6d4e3556c1b0e14e31b23da1a5c07e6bcf3addf32e575` |

JAuth 1.0.1 and JPhone 1.0.1 each have their own release. The other three are in JApps 1.0.0.

```bash
sha256sum JAuth-release.apk                    # Linux, macOS, git bash
certutil -hashfile JAuth-release.apk SHA256    # Windows
```

## Signing

All five are signed with one certificate, which is what lets a single key
activate the whole family: each app accepts activation only from apps whose
signing certificate matches its own.

```
CN=JApps, OU=JFamily, O=JApps, C=CA
753bf85dbbf2cd55862e494733ffe69a14eff96d9c0b8e0883fe347464c7a02f
```

```bash
apksigner verify --print-certs JAuth-release.apk
```

This reports `v1 scheme (JAR signing): false`, which is expected at `minSdk 26`.
Pass `--min-sdk-version 21` and v1, v2 and v3 all verify.

## Requirements

Android 8.0 or later (minSdk 26), built against SDK 36.
