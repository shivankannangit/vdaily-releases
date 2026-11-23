# V Daily

A Mac app for switching between several Google accounts in one window: Gmail, Google Calendar and
Google Drive for each account, each in its own separate session.

**[⬇ Download the latest version](https://github.com/shivankannangit/vdaily-releases/releases/latest)**
· Requires macOS 14 (Sonoma) or later · Runs natively on Apple silicon and Intel Macs

## Features

- **Switch accounts instantly.** Click an account in the sidebar or press ⌘1…⌘9. Pages keep running
  in the background, so nothing reloads when you switch.
- **Mail, Calendar and Drive** for every account (⇧⌘M, ⇧⌘C, ⇧⌘D).
- **Accounts stay separate.** Signing in or out of one account never affects another, and Google's
  sign-in pop-ups open inside the window.
- **Sidebar at a glance:** each account's profile picture, unread count and Google storage use.
  Collapse it to pictures only with ⌃⌘S.
- **Encrypted, with no extra password.** Your data's key is kept in your Mac's Keychain, so V Daily opens straight away.
  Press **Esc twice** to lock it while it's open.
- **Light, Dark or System** appearance for the app, and separately for Google's pages
  (View ▸ Page Theme).
- **Optional iCloud Drive sync** of your account list and settings between your Macs.

## Installing

1. Download the `.dmg` from the [latest release](https://github.com/shivankannangit/vdaily-releases/releases/latest).
2. Open it and drag **V Daily** onto **Applications**.
3. Open V Daily from Applications.

**The first time you open it,** macOS may say it can't verify V Daily. That's because V Daily isn't signed
with a paid Apple Developer certificate. Open **System Settings ▸ Privacy & Security**, scroll down and
click **Open Anyway** (or Control-click V Daily in Applications and choose **Open**). You only need to do
this once.

On first launch V Daily asks you to sign in to your Vcloud account (your Seimu account), which keeps your list of
accounts on every Mac you use. Then add your accounts with **⇧⌘N** and sign in with Google as usual.

## Updating

Choose **V Daily ▸ Check for Updates…**. If there's a newer version, V Daily offers to download it.
Quit V Daily, open the new DMG and drag V Daily onto Applications, then choose **Replace**. Your accounts
and settings are stored outside the app, so they're kept.

Versions are named by release date, e.g. `20261113`. A second release on the same day becomes
`20261113a`, and so on.

## Privacy and security

- **V Daily never sees your Google password.** You type it into Google's own sign-in page.
- **Everything V Daily saves is encrypted** (AES-256-GCM) in a single file. That covers your account
  list, your settings and the Google sign-in cookies that keep you signed in. Email addresses and profile
  pictures are held in memory only.
- The encryption key is kept in your Mac's Keychain, protected by your Mac's login. Press **Esc twice** to lock
  V Daily while it's open; Touch ID or your Mac's password unlocks it.
- Web data such as caches and page storage is kept in memory only and never written to disk.
- V Daily only connects to Google, plus GitHub when you check for updates. There's no analytics or tracking.

## Keyboard shortcuts

| Action | Shortcut |
|---|---|
| Switch to account 1–9 | ⌘1 … ⌘9 |
| Next / previous account | ⌃⇥ / ⌃⇧⇥ |
| Add account | ⇧⌘N |
| Mail / Calendar / Drive | ⇧⌘M / ⇧⌘C / ⇧⌘D |
| Back / Forward | ⌘[ / ⌘] |
| Home | ⇧⌘H |
| Reload | ⌘R |
| Zoom in / out / actual size | ⌘+ / ⌘− / ⌘0 |
| Collapse or expand sidebar | ⌃⌘S |

## Uninstalling

Use **V Daily ▸ Uninstall V Daily…**. Dragging the app to the Trash leaves its encrypted data behind. The
uninstaller asks for your password, then deletes V Daily's data and settings from this Mac and moves the
app to the Trash. It asks before deleting the iCloud Drive copy, since your other Macs may use it. Your
Google accounts themselves are not changed.

Already deleted the app? Remove what's left by running this in Terminal:

```sh
rm -rf ~/Library/"Application Support/V Daily"
defaults delete com.shivankannan.vdaily
```

If you used iCloud, also delete the **V Daily** folder in iCloud Drive.

## Other apps

- **[V Trio](https://github.com/shivankannangit/vtrio-releases):** preview a web page on desktop, tablet and
  mobile side by side.
- **[V Daw](https://github.com/shivankannangit/vdaw-releases):** play and practise your music, with a
  visualizer, markers, loops and Arturia MiniLab 3 support.

---

V Daily isn't affiliated with or endorsed by Google. Gmail, Google Calendar and Google Drive are
trademarks of Google LLC.
