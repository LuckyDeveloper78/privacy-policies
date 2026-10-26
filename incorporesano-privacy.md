# Privacy Policy for InCorporeSano

**Effective date: October 26, 2026** (replaces the version of October 25, 2026)

InCorporeSano ("the App", "we", "our") is a training-plan, coaching and route-planning application for runners and cyclists, available as a web app at `https://incorporesano.luckydev.be` and as an Android app (package `be.luckydev.incorporesano`). This policy explains which personal data the App processes, why, with which service providers, and what your rights are.

**Contact for all privacy matters:** `admin@luckydev.be`.

## 1. Data we process

### 1.1 Account
- Sign-in with Google (via Firebase Authentication) or with an email address and password.
- We store your display name, email address, whether the address is verified, your role in the App (runner, coach, admin), and your preferred language.
- Passwords are handled by Firebase Authentication only; we never see or store them.
- An account created with an email address and password must verify that address: Firebase Authentication sends a verification email on our behalf, and the App can be used once the link has been opened. An administrator may mark an address verified for a user they know.
- When an administrator archives an account, its sign-in is disabled on Firebase Authentication; it is enabled again if the account is restored.

### 1.2 Profile and biometric data (optional)
Year of birth, sex, height, weight, personal bests and recent best times. They are used to compute training paces and to personalise plans and the coach assistant.

### 1.3 Training data
Training sessions (planned and completed), recorded routes and GPS tracks attached to sessions, objectives (target races, target times), race plans, calendar availability, group membership, coach links and comments you post on sessions.

### 1.4 Coach assistant (chat) and its memory
When you use the coach assistant:
- Your messages and the assistant's answers are stored in your account (conversation history).
- The assistant keeps a written **memory** of you (goals, level, weekly volume, availability, equipment, **injury history and current physical restrictions**). This memory contains health-related information. You can read, edit and delete it at any time in the assistant's Memory panel.
- To answer, the assistant sends to an AI provider (section 3.4) the current conversation, this memory, your profile data of section 1.2 and your recent sessions. **Read section 3.4 before sharing anything you do not want an AI provider to receive.**

### 1.5 Location (optional)
If you allow the location permission, the App reads your current position to propose a start point for generated routes. You may also save a home or start location in your private profile. Location is used only for route generation and weather at the start point; it is never shared with other users.

### 1.6 Connected services (optional)
- **Garmin Connect**: see section 3.2.
- **Strava**: integration currently disabled (see section 3.3).

### 1.7 Technical data
- Our Garmin sync service keeps, for a short time and in memory only, request counters per user and per IP address to limit abuse, and writes error types (without personal content) to its logs.
- The App itself contains no analytics or advertising SDK and does not track you across other apps or sites.

### 1.8 Public race results
To predict finishing times and let users find and compare race performances, the App uses a dataset of **race results already published** by race organisers and timing companies (for example UTMB live results, RaceResult, UltraTiming): runner name, year of birth, gender, nationality, race, time and ranking. The data is used as published; it is not combined with your account data except to match your own results when you ask for them. Signed-in users consult this dataset only through the App's comparison and prediction screens (race history of a runner for coaches and administrators, race rankings for administrators, finishing-time estimates for everyone): the dataset itself stays on our server (3.5) and is never sent to or stored on your device; each query carries only the name searched and the target race. Since 25 October 2026 the App deletes any copy an earlier version had cached on the device. If you appear in it and object to this use, write to `admin@luckydev.be` (section 6).

## 2. Why we process your data and on which legal basis (GDPR)

| Purpose | Data | Legal basis |
|---|---|---|
| Provide the account and the App | 1.1, 1.3 | Performance of a contract (art. 6(1)(b)) |
| Personalised paces, plans and assistant | 1.2, 1.4 | Your consent (art. 6(1)(a) and, for health-related memory, art. 9(2)(a)); you withdraw it by deleting the data |
| Route generation and weather | 1.5 | Your consent (device permission) |
| Garmin / Strava sync | 1.6 | Your consent (you link the account) |
| Abuse prevention, security | 1.7 | Legitimate interest (art. 6(1)(f)) |
| Performance prediction and comparison on published results | 1.8 | Legitimate interest (art. 6(1)(f)) in analysing sporting results the organisers made public; right to object at any time |

## 3. Service providers (processors and third parties)

### 3.1 Google Firebase (hosting, database, authentication)
Your account, profile, training data, assistant memory and conversations are stored in Google Cloud Firestore, in Google's `nam5` multi-region (United States). Firebase App Check and reCAPTCHA Enterprise are used to protect the backend against abuse. See Google's privacy policy.

### 3.2 Garmin Connect (optional)
To link your Garmin account you enter your Garmin email and password in the App. They are sent once, over an encrypted connection, to our synchronisation service (section 3.5), which uses them to open a Garmin session and then **discards the password**. A Garmin multi-factor code, if requested, is handled the same way. The Garmin session tokens are stored on our server, never in the App. With those tokens we:
- read your recent activities (type, date, distance, durations, speeds, elevation, heart rate, cadence, training effect and load) to fill your training log, and
- send routes you generate in the App to your Garmin account as courses.

Disconnecting Garmin in the App deletes the stored tokens. Your Garmin email may be remembered on your device to prefill the form.

### 3.3 Strava (currently disabled)
The Strava integration is switched off. If it is re-enabled, linking will use Strava's OAuth authorisation; we will then receive your activities and store the OAuth tokens on our server. This policy will be updated before that happens.

### 3.4 Artificial-intelligence providers
The coach assistant and the plan generator send the data listed in section 1.4 to an AI model. Two modes exist:

- **Default mode (no key of your own): Google Gemini, free tier, through Firebase AI Logic.** On this free tier, Google's terms allow Google to use the submitted content, including through human review, to improve its products. Content sent in this mode should therefore be considered shared with Google. **If you do not want some information to be shared with Google, do not type it in the assistant in default mode, or use your own API key.**
- **Your own API key**: you may enter a personal API key for OpenAI, Anthropic (Claude), Google (Gemini) or DeepSeek. The conversation is then sent from your device directly to that provider under your own account and its terms; our servers do not relay it. The key is stored in your account on our server so that your devices can use it; you can remove it at any time in the App, which deletes it. We recommend a dedicated key with a spending limit.

### 3.5 Render (synchronisation service)
Our Garmin/Strava synchronisation service runs on Render.com. It processes your Garmin credentials once (3.2), your Garmin activities, the routes you push, and your Firebase identity token to authenticate the request; for administrators it also disables or re-enables the sign-in of archived accounts and marks email addresses verified (1.1). The same service holds the public race-results dataset (1.8) and answers the App's search, ranking and estimate queries; it receives the name searched, the target race and your identity token, and keeps no log of the queries beyond the provider's standard request logs.

### 3.6 Route generation and weather (OpenStreetMap ecosystem)
When you generate a route, the App sends the start point (your position or a saved location) and route parameters, directly from your device, to:
- **BRouter** (`brouter.de`) for routing,
- **Nominatim** (`nominatim.openstreetmap.org`) for address lookup,
- **Overpass API** (`overpass-api.de`) for map features,
- **Open-Meteo** for weather at the start point,
- OpenStreetMap tile servers to display the map.

These are public community services; requests carry your IP address and the coordinates sent. No account or identifier of yours is attached.

### 3.7 International transfers
Google (3.1, 3.4) and Render (3.5) store or process data in the United States. These transfers rely on the EU-US Data Privacy Framework where the provider is certified, and otherwise on the European Commission's standard contractual clauses.

## 4. Who can see your data inside the App

- **Other signed-in users** can see your display name, your role, whether a Garmin account is linked, the groups you belong to, your objectives (target race and time), and the comments you post. Registration is open, so treat these as visible to any user of the App.
- **Your coaches** (users linked to you as coach of your group) and **administrators** can additionally see your private profile (email, biometric data, personal bests) and your sessions.
- **Only you** can see your location, race planning, assistant memory, conversation history and API key. Administrators of the Firebase project can technically access all stored data, including API keys and Garmin tokens, for operation and support.

## 5. Storage, security and retention

- Data in transit is encrypted (HTTPS). Access to the database is governed by Firebase security rules enforcing the visibility described in section 4.
- The App keeps data on your device: interface state, a cached copy of your data for offline use, and your sign-in session. On Android, device backups to your Google account may include this local storage.
- **Retention**: your data is kept as long as your account exists. Assistant conversations and memory, Garmin tokens and API keys can be deleted by you at any time in the App. Garmin pending multi-factor state is held in memory for at most 10 minutes. Abuse counters are held in memory for at most one day. Service logs are kept for the hosting provider's default period, then deleted.
- No method of transmission or storage is completely secure; we apply reasonable measures and limit what we keep.

## 6. Your rights

Under the GDPR you may ask for access to, rectification, erasure or portability of your data, restriction of processing, and you may object to processing based on legitimate interest (sections 1.7 and 1.8). You may withdraw consent at any time without affecting prior processing. You may lodge a complaint with your supervisory authority (in Belgium: the Data Protection Authority, `autoriteprotectiondonnees.be`).

**Account deletion**: email `admin@luckydev.be` from your registered address, or use the form at `https://incorporesano.luckydev.be/account-deletion.html`. We delete your account, profile, sessions, routes, comments, group and coach links, race plans, assistant memory and conversations, API key, and Garmin/Strava tokens within 7 business days.

## 7. Age

The App has no minimum age. For users under 13, Belgian law requires a parent's consent for the processing based on consent in section 2 (profile, assistant, location, connected services); parents may contact us to exercise the rights of section 6 on their child's behalf.

## 8. Changes

We will post updates on this page with a new effective date and, for material changes, inform you in the App.

## 9. Contact

`admin@luckydev.be`
