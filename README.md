<img src="icon.png" width="96" alt="Vet">

# Vet

**A phishing message checker that reads the message and tells you plainly
whether it is a scam.**

Paste a text. Vet reads it, scores it from 0 to 100, marks the exact phrases
that gave it away, and gives you a short checklist of what to actually do
next. No account, no sign-up.

**[Privacy policy](privacy-policy.md)**

---

## Download

The app is not on the Play Store yet. Until it is, you can install it
directly.

**[Download the APK for v0.2.0 →](https://github.com/quillmatick/vetIt/releases/download/v0.2.0/vetit-0.2.0-release.apk)**

Older versions stay available on the [releases page](https://github.com/quillmatick/vetIt/releases).
v0.2.0 is signed with the same key as v0.1.0, so it installs over it and keeps your history and
settings.

<details>
<summary>How to install an APK on Android</summary>

1. Open the link above on your phone and download the file.
2. Android will warn you that the file came from outside the Play Store. This
   is expected — tap **Settings**, then **Allow from this source**.
3. Open the downloaded file and tap **Install**.

You may need to enable **Install unknown apps** for whichever app you used to
open the download (Chrome, Files, or your browser). It is a per-app setting
and you can turn it back off afterwards.

</details>

The APK is signed with a release key, so updates install over each other
cleanly once a newer version is published here.

**Requires Android 8.0 (API 26) or newer.**

---

## What it does

- **Scores a message 0–100** — how likely it is to be a scam.
- **Shows you the evidence** — the specific words and phrases triggered the
  score, highlighted in the original text.
- **Tells you what to do next** — a short verification checklist, not just a
  number.
- **Redacts before it sends** — phone numbers, account details and names are
  masked on your device before the text ever leaves it.
- **Works on messages you did not ask about** — with the optional SMS Guard, it
  can check incoming messages as they arrive.

There is also a [web version](https://vet-js1b.onrender.com) you can use
without installing anything.

---

## Privacy in brief

- **No account, no sign-up, no email address.** There is nothing that
  identifies you.
- **Your history stays on your device.** Vet has no server-side history, so
  there is no copy of it for anyone to hand over.
- **Messages are redacted before they are sent,** and the text used for a
  check is discarded afterwards.
- **No ads, no analytics, no trackers, no third-party scripts.**
- **The only thing sent** is the redacted text, the backend, and on to the
  model that produces the verdict. Nothing else.

The full detail is in the [privacy policy](privacy-policy.md).

---

## Two things worth knowing

**Guard is opt-in and off by default.** Nothing scans your messages until you
turn it on yourself, and you can see exactly what it does before you do.

**Vet cannot stop a scam on its own.** It tells you how a message looks and
what to check. The decision is still yours.

---

## Current version

**v0.2.0** — Android 8.0+. Newer versions will appear on this page and at the
releases link above.

### What changed in v0.2.0

Every one of these was reported by someone using v0.1.0.

- **Settings → Appearance now works.** It did nothing at all: the app was calling its theme
  with no arguments, so every control saved your choice, read it back correctly, and changed
  nothing. Dark and light now switch, and text size resizes the app.
- **Dark mode is readable everywhere**, not just on the tabs. The window background was pinned
  to a light colour and about fifteen screens paint no background of their own, so on a dark
  phone their text, icons and back arrow were almost invisible.
- **The back button navigates instead of closing the app.** There was no back stack, so back
  exited Vet from any screen that had a back arrow.
- **The Inbox no longer reads everything twice** when you open it.
- **Light Guard stopped billing a model call per notification.** Every notification posted was
  sent for scoring, with no dedup and no cap, so one busy conversation could use your whole
  daily allowance without you asking. A notification is now scored once, the day's budget is
  checked before anything is sent, and an over-long notification is refused on the device.

### Known limitations

Stated plainly, because a security tool should not oversell itself.

- **The Inbox is still slower than it should be on a phone with a long history.** It now reads
  half as much as before, but it still scans the message table. The proper fix uses Android's
  conversation view and is written up but not yet done — the obvious version of it empties the
  Inbox, which is why it needs care.
- **Vet cannot stop a scam on its own.** It tells you how a message looks and what to check. The
  decision is still yours.
- **Guard is opt-in and off by default.** Nothing scans your messages until you turn it on.

---

## Not on this page

- **The web app** works without installing anything:
  [vet-js1b.onrender.com](https://vet-js1b.onrender.com)
- **The browser extension** for Gmail is in progress and is **not** published here yet. It has
  unit tests but has never been run in a browser.
