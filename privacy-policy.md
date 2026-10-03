# Privacy Policy

**Vet — the phishing message checker. Last updated 3 October 2026.**

## The short version

Vet has no accounts. There is nothing to sign up for and no way for us to identify you. We do
not run ads, we do not run analytics, and we do not build a profile of you.

When you check a message, Vet redacts personal details out of it *before* anything leaves your
device, and the redacted text is used once to produce a verdict and then discarded.

## What Vet reads

**On the Android app.** If you give Vet the default-SMS-app role, it can read your messages so
it can check them as they arrive. Vet never writes to, deletes from, or hides your inbox, and it
never sends anything on your behalf without you asking it to first.

**On the browser extension.** Vet reads the subject and a short snippet of the message you have
selected in Gmail, and only when you have explicitly asked it to.

**On the web app.** Vet reads only the text you paste into the box.

If you never grant a permission, the corresponding capability simply never runs.

## What Vet sends, and to whom

1. The text you asked to check, **after redaction**, is sent over HTTPS to the Vet API that
   powers this product.
2. That API forwards the redacted text to **OpenRouter**, which runs the language model that
   produces the verdict, and returns the verdict.
3. Nothing else is sent. There is no identifier, no device fingerprint, and no location.

The message text is never written to a log. The service records counts, timings and score
bands so we can see the service is healthy — never the content.

## What is stored, and where

**On your device or in your browser.** Check history, your draft, and your settings are stored
locally. Deleting the app or clearing site data removes them. This is on purpose: Vet has no
server-side history, so there is no copy for us to hand over.

**Rate-limit token.** To keep a small anonymous token that stops the daily free-check allowance
resetting every time the service restarts, Vet issues a signed token that your device or browser
keeps and sends back with each check. It contains nothing but a counter and a timestamp, it is
signed so it cannot be edited, and it cannot be linked to you.

## What we do not do

- No accounts, no sign-in, no email address
- No advertising, no analytics, no tracking pixels, no third-party scripts
- No selling or sharing of your data — there is none to share
- No background uploads: nothing is sent unless you press the button

## Children

Vet is not directed at children under 13 and collects no personal information from anyone.

## Your rights and choices

Because Vet does not hold identifiable data about you, there is generally nothing to access,
correct, export or erase — the data that exists is the history on your own device, which you can
delete at any time from within the app or your browser.

You can stop Vet reading anything at any time by revoking its permissions in your device
settings, or by unlinking a browser extension.

## Changes to this policy

If this policy changes materially, the updated version will be published at this same address
with a new date at the top.

## Contact

Questions are welcome at the project's issue tracker.