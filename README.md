# JApps

Five Android apps that keep your data on your phone, as files you can still read
if the apps disappear. No account, no company server, no telemetry.

The signed APKs are published under Releases. The source is not published here.

---

## JAuth - two-factor codes

Codes generated on the phone and kept there.

- Seeds are **encrypted with a key that cannot leave the device**, and the phone
  will not use that key until it has seen your fingerprint or PIN.
- **No Google Play Services.** QR scanning is ZXing and CameraX - no Firebase,
  no ML Kit, no Play dependency of any kind.
- **Imports from Google Authenticator, Aegis, 2FAS**, or any `otpauth://` list,
  so trying it does not mean re-enrolling thirty accounts. Google's transfer QR
  is read on-device and its contents listed for you to pick from.
- **Your codes are not trapped.** Export everything to a file whenever you want,
  or save an encrypted backup under a passphrase you choose. You can set up
  another authenticator from that export and delete JAuth.
- Free, and always will be.

## JCalendar - events as `.ics` files

One event, one `.ics` file, in storage only the app can touch. Each file is a
single `VEVENT` inside a `VCALENDAR` - the same way a CalDAV server stores one -
so a file copied off your backup server is byte-identical to the one on the
phone, and nothing is converted on the way out.

## JNotes - Markdown notes

Real `.md` files, openable in any editor on any computer years from now.
**Obsidian-compatible**: `[[Wikilinks]]` and `#tags` use the same syntax, so a
mirrored folder opens there and works. Live preview, tappable checklists that
write back into the file, attachments, full-text search.

Notes you would rather were encrypted go in a **vault**, unlocked by password or
fingerprint with an idle timeout you set. A vault note is encrypted on the device
and is never written to the backup mirror in readable form.

## JPhone - phone, messages and contacts

A replacement for Google Phone, Messages and Contacts. Three tabs.

Registers as **default phone app** (places calls through `TelecomManager`, draws
its own in-call screen - answer, decline, mute, speaker, hold, DTMF - including
over the lock screen) and **default SMS app** (single and multipart SMS with
delivery status, MMS with photos and voice notes).

Contacts are written out as `.vcf` and conversations as readable transcripts.

## JPhotos - gallery and editor

**Reads what is already on the phone.** Your pictures stay in the folders
Android already keeps them in - Camera, Screenshots, Downloads - and JPhotos
does not move or reorganise anything on its own. Uninstalling it leaves every
photo where it was.

**Nothing uploads by itself.** There is no background sync; every transfer is
one you started, on pictures you picked. Editing offers a copy by default -
overwriting the original is a separate, deliberate choice.

Android 14's "selected photos only" grant is supported, so you can hand over a
few pictures rather than the whole library and the app stays usable.

---

## What the five have in common

**The app owns the data, and the folder is a mirror.** What you create lives in
the app. If you switch backup on, a 1:1 copy is kept in a folder you choose - on
the device, or on your own FTP, SFTP or SMB server. The copy is a copy: deleting
the app does not take your backup folder with it, and nothing needs a server to
work.

There is no JApps server to point at, because there isn't one.

**One key unlocks all five.** Server backup is the single paid feature. A key is
bought once, arrives as text, and is checked entirely on the device - nothing is
sent anywhere and no account exists. That is not a convenience: an app that
argues it makes no network calls cannot then phone home to ask permission. Paste
a key into any one of the five and the other four pick it up on their next
launch.

**One theme.** Light, dark or system, across eight shared palettes. Every app
opens on Paper.


---

## Getting a key

The five apps are free to download and use. Server backup - mirroring your data
to your own FTP, SFTP or SMB server - is the one feature a key unlocks. Everything
else, including local folder backup, works without one.

If you want that feature, support the project and I will send you a key.

**Suggested: $20.** One key, all five apps, paid once - there is no subscription
and no second purchase. Any amount is welcome, and I will send a key either way.

| Chain | Address |
|---|---|
| Solana | `862YZXoRvaoTiP1AkQEEZ5FFGgPFsUhbEoRu4r44RhSe` |
| Ethereum | `0xF890c6A128920D145D47753D0b1159fA4Db2861d` |

Then email **jessymelanson1265@proton.me** with the transaction hash. I check the
chain, reply with a key, and that is the whole process. There is no checkout, no
account and no third party in the middle.

Transfers on both chains are irreversible - check the address character by
character, and send only native SOL or ETH, or standard tokens on those chains.

### How the key is checked

The key is a block of text. You paste it into any one of the five apps and the
other four pick it up on their next launch.

Verification happens **entirely on the device**, against a SHA-256 hash compiled
into the app. Nothing is transmitted, no licence server is contacted, and the app
works the same with no network at all. That is not a convenience - an app that
argues it makes no network calls cannot then phone home to ask permission.

What follows from that, stated plainly rather than discovered later:

- **A key works offline, forever.** It cannot be revoked remotely, because there
  is nothing to revoke it from.
- **It is not tied to a device or an account**, because neither is registered
  anywhere.
- **Keep it somewhere safe.** I can resend one from the email you used, but
  there is no account to recover it from.

Please do not share your key. The verification is offline by design, which means
the only thing keeping this sustainable is people not passing keys around.

---

## Verify what you downloaded

| File | SHA-256 |
|---|---|
| `JAuth-release.apk` | `e37197c7055ed034b3cd3ac2bfb3c051b3ee4d85ec5fc014154ec87f22e282af` |
| `JCalendar-release.apk` | `60dcca4c00ca326ac7241cd2ec07c97dd346c0f394c1cb34a604a9060a9b2185` |
| `JNotes-release.apk` | `f6d4c73c1cc826801f1ba74ae57b9eaf9bb175e161f62ea58668711055478568` |
| `JPhone-release.apk` | `fd8305bc41f4cd12ae7a623e88bfda4a5d2a6c0150258aa672c7f1fc39a08ddd` |
| `JPhotos-release.apk` | `3417347a0c993f50cab6d4e3556c1b0e14e31b23da1a5c07e6bcf3addf32e575` |

```bash
sha256sum JAuth-release.apk                    # Linux, macOS, git bash
certutil -hashfile JAuth-release.apk SHA256    # Windows
```

## Signing

All five are signed with one certificate. That is load-bearing rather than tidy:
each app answers activation queries only from callers whose signing certificate
matches its own, so separate keys would silently stop one key unlocking the
family.

```
CN=JApps, OU=JFamily, O=JApps, C=CA
753bf85dbbf2cd55862e494733ffe69a14eff96d9c0b8e0883fe347464c7a02f
```

```bash
apksigner verify --print-certs JAuth-release.apk
```

That prints `v1 scheme (JAR signing): false`. It is not missing - with
`minSdk 26`, apksigner only verifies the schemes that platform range uses. Add
`--min-sdk-version 21` and v1, v2 and v3 all verify.

## Requirements

Android 8.0 or later (minSdk 26), built against SDK 36.

