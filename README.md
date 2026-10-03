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

**[Download the APK for v0.1.0 →](https://github.com/quillmatick/vetIt/releases/download/v0.1.0/vetit-0.1.0-release.apk)**

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

**v0.1.0** — Android 8.0+. Newer versions will appear on this page and at the
releases link above.
