# Vmail

A Mac app for switching between several Google accounts in one window: Gmail, Google Calendar and
Google Drive for each account, each in its own separate session.

**[⬇ Download the latest version](https://github.com/shivankannangit/vmail-releases/releases/latest)**
· Requires macOS 14 (Sonoma) or later · Runs natively on Apple silicon and Intel Macs

## Features

- **Switch accounts instantly.** Click an account in the sidebar or press ⌘1…⌘9. Pages keep running
  in the background, so nothing reloads when you switch.
- **Mail, Calendar and Drive** for every account (⇧⌘M, ⇧⌘C, ⇧⌘D).
- **Accounts stay separate.** Signing in or out of one account never affects another, and Google's
  sign-in pop-ups open inside the window.
- **Sidebar at a glance:** each account's profile picture, unread count and Google storage use.
  Collapse it to pictures only with ⌃⌘S.
- **Locked and encrypted.** Vmail opens locked, unlocks with your password or Touch ID, and locks again
  when you press **Esc twice**.
- **Light, Dark or System** appearance for the app, and separately for Google's pages
  (View ▸ Page Theme).
- **Optional iCloud Drive sync** of your account list and settings between your Macs.

## Installing

1. Download the `.dmg` from the [latest release](https://github.com/shivankannangit/vmail-releases/releases/latest).
2. Open it and drag **Vmail** onto **Applications**.
3. Open Vmail from Applications.

**The first time you open it,** macOS may say it can't verify Vmail. That's because Vmail isn't signed
with a paid Apple Developer certificate. Open **System Settings ▸ Privacy & Security**, scroll down and
click **Open Anyway** (or Control-click Vmail in Applications and choose **Open**). You only need to do
this once.

On first launch Vmail asks you to:

- choose where to keep its data: **on this Mac** or in **iCloud Drive** (shared by your Macs);
- set a **password** and answer **three security questions** (they let you reset a forgotten password);
- optionally turn on **Touch ID**.

Then add your accounts with **⇧⌘N** and sign in with Google as usual.

## Updating

Choose **Vmail ▸ Check for Updates…**. If there's a newer version, Vmail offers to download it.
Quit Vmail, open the new DMG and drag Vmail onto Applications, then choose **Replace**. Your accounts
and settings are stored outside the app, so they're kept.

Versions are named by release date, e.g. `20261113`. A second release on the same day becomes
`20261113a`, and so on.

## Privacy and security

- **Vmail never sees your Google password.** You type it into Google's own sign-in page.
- **Everything Vmail saves is encrypted** (AES-256-GCM) in a single file. That covers your account
  list, your settings and the Google sign-in cookies that keep you signed in. Email addresses and profile
  pictures are held in memory only.
- The encryption key is protected by your Vmail password, by your security answers, and optionally by
  a Touch ID key in your Mac's Secure Enclave.
- Web data such as caches and page storage is kept in memory only and never written to disk.
- Vmail only connects to Google, plus GitHub when you check for updates. There's no analytics or tracking.

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
| Lock | Esc, Esc |

## Uninstalling

Use **Vmail ▸ Uninstall Vmail…**. Dragging the app to the Trash leaves its encrypted data behind. The
uninstaller asks for your password, then deletes Vmail's data and settings from this Mac and moves the
app to the Trash. It asks before deleting the iCloud Drive copy, since your other Macs may use it. Your
Google accounts themselves are not changed.

Already deleted the app? Remove what's left by running this in Terminal:

```sh
rm -rf ~/Library/"Application Support/Vmail"
defaults delete com.shivankannan.vmail
```

If you used iCloud, also delete the **Vmail** folder in iCloud Drive.

## Other apps

- **[Triview](https://github.com/shivankannangit/triview-releases):** preview a web page on desktop, tablet and
  mobile side by side.
- **[Vivvy DAW](https://github.com/shivankannangit/vivvy-releases):** play and practise your music, with a
  visualizer, markers, loops and Arturia MiniLab 3 support.

---

Vmail isn't affiliated with or endorsed by Google. Gmail, Google Calendar and Google Drive are
trademarks of Google LLC.
