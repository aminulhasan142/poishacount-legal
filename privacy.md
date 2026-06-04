---
title: PoishaCount Privacy Policy
description: How PoishaCount collects, uses, stores, and lets you delete your data.
---

# PoishaCount Privacy Policy

**Effective date:** 4 June 2026  
**Last updated:** 4 June 2026

PoishaCount is a personal expense-tracking mobile application built by
**Aminul Hasan** (an individual developer; "we", "I", "us"). This privacy
policy explains, in plain language, what data the app collects, why, where
it lives, and how to delete it.

PoishaCount is built **offline-first**. By default, no data leaves your
device. Cloud features (back-up, multi-device sync) are strictly opt-in
and only activate after you choose to sign in.

---

## 1. The short version

| | |
|---|---|
| Without signing in | Nothing leaves your device. Your expenses, budgets, categories, and subscriptions stay in the app's local database (Hive) on your phone. |
| After signing in (Google) | Your data is mirrored to your private space in Firebase Firestore (`users/{your-uid}/**`), readable only by you, gated by Firestore security rules. Analytics is enabled in aggregate. |
| Want to delete everything | **Settings → Delete account** wipes Firestore data first, then your auth record, then local data on the device. Irreversible. |

---

## 2. What data we collect, and why

### 2.1 Data you enter yourself

- Expense entries (amount, currency, category, optional note, date)
- Budgets (overall and per-category amounts and periods)
- Subscriptions (name, amount, billing cycle, next billing date)
- Custom categories you create
- App preferences (theme, default currency, BDT-zero-decimals toggle)

**Where it lives:** on your device, in the encrypted-at-rest Hive database.
If you sign in, copies are mirrored to your Firestore document tree.

**Why we have it:** so the app can show you your data. We never read it,
analyze it, sell it, or share it.

### 2.2 Account data (only if you sign in)

If you choose to sign in with Google:

- Your Google account **email address** and **profile name** (shown in the
  app's nav bar as "Hi, {your first name}")
- Your **profile picture URL** (displayed as the avatar)
- A unique **Firebase Auth user ID** (UID) that we use to scope your data

We do not store your Google password. Authentication is handled by Google
and Firebase Auth; we only ever receive an opaque OAuth token after you
consent on Google's sign-in screen.

### 2.3 Anonymous usage analytics (Firebase Analytics)

When the app launches, Firebase Analytics records:

- **Session events:** app open, screen view, session start, session length
- **Tab usage:** which of Home / Statistics / Subscriptions / Settings you
  visit (no contents)
- **Device + locale signals:** device model, OS version, app version,
  language, country (derived from your IP address — never your precise
  location), and a Google-issued anonymous app instance ID

We **do not** collect: the contents of your expenses, your name, your
email (in analytics), your contacts, your photos, your microphone, your
location coordinates, or any unique device identifier we could use to
re-identify you across other apps.

Analytics events are processed by Google under their
[Privacy & Terms](https://policies.google.com/privacy).

### 2.4 Live exchange rates (network request)

The app fetches public exchange rates from `open.er-api.com` when refreshing
currency conversions. Only standard HTTP request metadata leaves your
device (e.g. your IP address visible to the rate provider). We do not send
any of your financial data with the request.

---

## 3. Where your data is stored

| Data | Location | Region |
|---|---|---|
| Local app data (Hive) | On your device only | Your device |
| Cloud-synced app data (signed-in users) | Firebase Firestore | `asia-southeast1` (Singapore) |
| Auth records | Firebase Authentication | Google data centres |
| Analytics events | Google Analytics for Firebase | Google data centres |

Google maintains industry-standard security practices for the services
above. Firestore data is encrypted at rest and in transit. The app's
Firestore security rules enforce that only you can read or write your own
documents (`users/{uid}/**`).

---

## 4. Who we share data with

**We do not sell or rent your data to anyone. Ever.**

We use the following sub-processors purely as infrastructure providers:

- **Google LLC / Firebase** — authentication, database, analytics
- **Open Exchange Rates API (`open.er-api.com`)** — currency rates only;
  receives no personal data, only the standard HTTP request

There are no advertising SDKs, no third-party trackers, no affiliate
networks, and no data-broker integrations in the app.

---

## 5. How long we keep your data

- **On-device data:** stays until you delete the app or use Settings →
  "Erase all data".
- **Cloud-synced data:** stays until you delete the entry in-app or use
  Settings → "Delete account", which permanently wipes
  `users/{your-uid}/**` and the auth record itself.
- **Analytics events:** retained by Google for the default Firebase
  retention window (14 months on the free Spark plan), then auto-deleted.

---

## 6. Your rights

You have the right to:

1. **Access** the data we hold about you — open the app; it's all visible.
2. **Correct** entries — every record in the app is editable.
3. **Delete** your data — Settings → "Delete account" (cloud + local) or
   uninstall the app + Settings → "Erase all data" (local only).
4. **Withdraw consent for analytics** — a future Settings toggle will let
   you call `setAnalyticsCollectionEnabled(false)`; until then, deleting
   the app stops collection.
5. **Export your data** — request a copy by emailing the address below.
   We will provide a JSON dump of your Firestore documents within 30 days.
6. **Object to processing** — contact us; we'll honour the request.

If you are in the European Economic Area, UK, or California, these rights
are guaranteed by GDPR / UK GDPR / CCPA. We honour them globally regardless.

---

## 7. Children

PoishaCount is intended for users **18 years and older**. We do not
knowingly collect data from children under 13 (or the equivalent minimum
age in your jurisdiction). If you believe a minor has signed in, contact
us and we will delete the account.

---

## 8. Security

- All network traffic uses HTTPS / TLS.
- Firestore security rules cryptographically prevent any user from reading
  another user's documents.
- Auth tokens are stored in the device's secure enclave (iOS Keychain /
  Android Keystore).
- The app does not transmit your data to any server other than the ones
  listed in section 4.

No system is perfectly secure. If we discover a breach affecting your
data, we will notify you via the app and your registered email within 72
hours of confirming it.

---

## 9. Changes to this policy

When we change this policy, we'll update the "Last updated" date at the
top and, for material changes, surface a notice inside the app the next
time you open it. Continued use after the effective date constitutes
acceptance of the new policy.

---

## 10. Contact

For privacy questions, data-deletion requests, or data-export requests:

**Aminul Hasan**  
📧 *Replace this line with your contact email before publishing.*  
GitHub: [@aminulhasan142](https://github.com/aminulhasan142)

We respond to privacy requests within 30 days, usually much faster.

---

*This policy is published in plain Markdown. The source file lives at
[github.com/aminulhasan142/poishacount-legal/blob/main/privacy.md](https://github.com/aminulhasan142/poishacount-legal/blob/main/privacy.md);
the rendered version you're reading is auto-deployed via GitHub Pages.*
