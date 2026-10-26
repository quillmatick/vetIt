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

**[Download the APK for v0.3.0 →](https://github.com/quillmatick/vetIt/releases/download/v0.3.0/vetit-0.3.0-release.apk)**

Older versions stay available on the [releases page](https://github.com/quillmatick/vetIt/releases).
v0.3.0 is signed with the same key as v0.1.0 and v0.2.0, so it installs over them and keeps
your history and settings.

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
- **Redacts personal details on your device** before sending text for analysis.
  For supported manual checks, the review setting shows what will be sent and
  lets you hide additional text. Automatic Guard checks redact without a review
  screen; detection is not perfect, so do not send anything you are not
  comfortable sharing.
- **Checks only what you choose** — opening an Inbox conversation does not spend
  checks. Tap an individual message to check it or copy it. Optional overnight
  checking is available in Settings and is capped.
- **Optional SMS Guard** can help check incoming messages. Full Guard requires
  Vet to be the default SMS app; Light Guard uses notification access.
- **Encrypted device linking** lets you transfer selected check history between
  your phone and browser; the relay receives ciphertext, not the encryption key.

There is also a [web version](https://vet-js1b.onrender.com) you can use
without installing anything.

---

## Privacy in brief

- **No account, sign-up, or email address.** The app uses a random install token
  for its free-check limit; it is not a device fingerprint.
- **Check history is stored locally.** The Android app encrypts its private
  history databases; browser history stays in that browser's local storage.
- **Message text is redacted on-device before analysis.** The API forwards the
  redacted text to the model provider and does not log message content.
- **Device-link relay data is encrypted ciphertext.** The paired devices hold
  the key; the relay does not.
- **No ads, no analytics, no trackers, no third-party scripts.**
- A random install token and rate-limit token are also sent to enforce the
  anonymous free-check allowance.

The full detail is in the [privacy policy](privacy-policy.md).

---

## Two things worth knowing

**Guard and overnight checking are opt-in.** They do not run until you enable
them. Guard checks can send redacted message text for analysis; overnight
checking uses your network connection and available daily check allowance.

**Vet cannot stop a scam on its own.** It tells you how a message looks and
what to check. The decision is still yours.

---

## Current version

**v0.3.0** — Android 8.0+. Newer versions will appear on this page and at the
releases link above.

### What changed in v0.3.0

This release addresses the reported Android issues and completes the linked-device service.

- **Linked devices can now pair.** The pairing relay is live; history transfers are encrypted
  between the paired phone and browser.
- **Personal-detail protection is clearer and more useful.** Manual checks can show a redacted
  preview for review and let you hide additional text before sending.
- **Inbox checks are on demand.** Opening a conversation no longer checks every message. Check
  one message at a time, or opt in to capped overnight checks in Settings.
- **Guard setup explains Android permissions.** Full Guard and Light Guard have clearer
  permission guidance, notification-access status, and notification permission handling.
- **Private Android history databases are encrypted at rest** with SQLCipher and a key protected
  by Android Keystore. Existing private history is migrated when the app opens it.
- **Improved device pairing and history sync** with expiry handling and bounded transfers.

### Known limitations

Stated plainly, because a security tool should not oversell itself.

- **Automated redaction can miss personal details.** Review the preview for manual checks and
  hide anything you do not want to send. Automatic Guard and overnight checks do not show that
  review screen.
- **The Android app encrypts its own private history databases.** SMS/MMS messages in Android's
  system messaging provider are managed by Android and are not Vet's SQLCipher databases.
- **The free analysis allowance is limited.** Optional overnight checks use that allowance;
  they are capped to preserve part of it for manual checks.
- **Vet cannot stop a scam on its own.** It tells you how a message looks and what to check. The
  decision is still yours.
- **Guard is opt-in and off by default.** Full Guard needs the default-SMS role; Light Guard
  needs notification access.

---

## Not on this page

- **The web app** works without installing anything:
  [vet-js1b.onrender.com](https://vet-js1b.onrender.com)
- **The browser extension** for Gmail is not part of this Android release.
