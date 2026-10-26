# Privacy Policy

**Vet — the phishing message checker. Last updated 26 October 2026.**

## The short version

Vet has no accounts, sign-in, or email collection. We do not run ads, analytics, or tracking
pixels. When you ask Vet to analyze text, the app redacts personal details on your device and
sends the redacted text to the Vet API, which forwards it to OpenRouter for a verdict.

The Android app encrypts its private history databases with SQLCipher. The encryption key is
protected by Android Keystore. Browser history is kept in that browser's local storage and is
subject to the browser and device's protections.

## What Vet reads

**On the Android app.** A manual check reads the message you choose. If you enable Full Guard,
Android gives Vet the default-SMS-app role so it can process incoming SMS. Light Guard uses
notification access to read notifications from apps you select. These features are off until
you enable them and grant the required access.

If you enable overnight checking, Vet checks eligible, unchecked incoming messages from the
last 48 hours at the time you choose. It is capped at 10 checks per night and uses the same
free-check allowance as manual analysis.

**On the web app.** Vet reads only the text you paste into the box. It stores browser history
locally in that browser.

**On the browser extension.** The extension reads the subject and a short snippet of a Gmail
message only when you explicitly ask it to check that message. The extension is not part of the
Android APK release.

If you do not enable a feature or grant its permission, that capability does not run.

## Redaction and analysis

The Android app attempts to redact personal details on-device before analysis. For supported
manual checks, the personal-details review setting can show a preview of the redacted text and
let you hide additional text. Automatic Guard and overnight checks redact automatically and do
not show the review screen.

Automated detection is not perfect. Review the preview when it is available, and do not send
text you are not comfortable sharing. The text sent for a check is transmitted over HTTPS to the
Vet API. The API forwards the redacted text to OpenRouter, which routes it to the model that
produces the verdict. Message content is not written to Vet's application logs.

## Identifiers and service data

The app sends a random install token with analysis requests so Vet can enforce the free-check
limit. The API hashes install identifiers before logging them. A signed rate-limit token may
also be stored by the app or browser and sent with later checks; it contains rate-limit state,
not message text.

The service records operational counts, timings, status codes, and score bands. It does not log
message content. The API processes request content to return a verdict; it does not keep a
history of analyzed messages.

## Device linking

Linking a phone and browser is optional and starts only when you choose to pair them. The two
devices establish a shared encryption key. History sent between them is encrypted before it
reaches the relay. The relay handles ciphertext and does not receive the key or the message
text. Relay data is held temporarily in memory for the pairing/link and is removed when it is
acknowledged, unlinked, or expires. A service restart can end an active link.

## What is stored, and where

**Android app.** Vet's private check-history databases are encrypted with SQLCipher; their key
is protected by Android Keystore. The app migrates its private databases when they are opened.
Vet does not encrypt or replace the Android system's SMS/MMS provider database; Android and the
default messaging app manage that data.

**Web app and browser.** Settings and check history are stored locally in the browser. Clearing
the browser's site data removes them. Vet does not keep a server-side copy of this history.

**Service.** The Vet API processes redacted message text to return an analysis and does not
retain a message history. The pairing relay temporarily holds encrypted ciphertext as described
above.

Deleting the app or clearing browser site data removes the corresponding local Vet data.

## What we do not do

- No accounts, sign-in, email collection, advertising, analytics, or tracking pixels.
- No sale of message text or check history.
- No sending of analysis text unless you request a check or enable an opt-in Guard or overnight
  checking feature.
- No sending messages or contacting anyone on your behalf.

## Children

Vet is not directed at children under 13. It does not require an account, but users should not
submit information they do not have permission to share.

## Your choices

You can turn Guard and overnight checking off in the app and revoke SMS, notification, or other
permissions in Android settings. You can unlink a browser from the phone or clear the browser's
site data. Uninstalling Vet removes the app's private local data.

## Changes to this policy

If this policy changes materially, the updated version will be published at this same address
with a new date at the top.

## Contact

Questions are welcome at the project's issue tracker.
