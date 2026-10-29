# Privacy Policy for KineCut

**Last updated:** October 29, 2026 (small, non-material additions: Section 1.15, Script to Video; Section 12, AI voices and the offline voice's use rules. Earlier: Section 1.12, the on-device Hindi, Hinglish and English voice packs; Section 1.13, Firebase Remote Config; Section 1.14, Flight Map online place search)
**Effective date:** October 11, 2026
**App name:** KineCut
**Package:** com.kinecut.app
**Publisher / Data Controller:** Yashwant Shila ("we", "our", "us")
**Contact:** punutype@gmail.com

This Privacy Policy explains what information KineCut ("the app") accesses, processes, and shares when you use it on your Android device. It applies to users worldwide and complies with the EU/UK GDPR, the California Consumer Privacy Act / CPRA, and India's Digital Personal Data Protection Act, 2023 (DPDP Act).

By installing or using KineCut, you confirm that you have read and accepted this Privacy Policy.

> **October 29, 2026 (not a material change):** added Section 1.15 for the new optional **Script to Video** tool. With the Gemini voice, the script you type is sent to Google's Gemini API with **your own** Gemini key (the same optional Gemini integration as Section 1.9); with the offline voice, the voice is made on your device and nothing is sent. Section 12 now also covers AI voices, including the use rules of the offline voice model. Nothing new is collected by us.
>
> **October 24, 2026 (not a material change):** added Section 1.14: Flight Map's optional "Search online" sends the place name you type to your phone's place-lookup service. Nothing new is collected by us.
>
> **October 19, 2026 (not a material change):** added Section 1.13: the app uses Google Firebase Remote Config to switch some features on or off without an update. Hindi, Hinglish and English no longer need an API key when their voice pack is downloaded (Section 1.12).
>
> **October 17, 2026 (not a material change):** added Section 1.12. If you download an optional Hindi, Hinglish or English voice pack from Google Play, that language's speech is turned into words on your device and that audio is not sent to anyone. Nothing new is collected or shared.
>
> **What changed in the October 4, 2026 version:** One material change:
>
> 1. **Crash and error reports (Google Firebase Crashlytics).** When the app crashes, or when something fails (for example an export or a transcription), KineCut now sends a **technical crash/error report** to us through **Google Firebase Crashlytics** so we can find and fix the problem. A report contains technical details only — what failed and where in the app, the error text, technical facts about the media format (for example "video, 1920x1080, 30 fps, AAC sound"), your device model and Android version, free storage and memory, and the app version. Before sending, the app removes API keys, e-mail addresses and your file names from the report. Reports **never** contain your media, audio, transcripts, captions, projects or exported videos. Like Firebase Analytics, this is only switched on after you accept this policy. See Section 1.11.
>
> Because this is a material change, we publish this update at least 7 days before the effective date, in line with Section 13. You will be asked to review and accept this updated policy again inside the app. Earlier changes (the optional Google Gemini integration in Section 1.9 and the export notification in Section 1.10) remain as described below.

---

## Plain-English summary

- We do not run any servers and we do not have user accounts. We never see your videos, audio, captions, or projects.
- Your media files are processed on your device. The only content leaving your device for the core feature is the **audio you choose to transcribe**, which is sent over HTTPS directly to **Groq's API** using **your own Groq API key**.
- **Optional Hindi, Hinglish and English voice packs:** if you download a free voice pack (from Google Play), Hindi, Hinglish or English speech is turned into words **on your device** and that audio is **not uploaded** anywhere. See Section 1.12.
- **Optional Google Gemini:** if you add your **own** Google Gemini API key, KineCut can also send your **audio** and your **transcript text** to **Google's Gemini API** under your own Google account, for sharper transcription and captions. This is **off by default** and only happens if you add a key. **If your Gemini key is on Google's free tier, Google may use your audio and text to improve Google's products and human reviewers may read them** — use a paid Gemini key, or skip Gemini, if you don't want that. See Section 1.9.
- **Optional Script to Video:** you type a script and KineCut makes a voice for it. With the **Gemini voice**, your script text is sent to **Google's Gemini API** with **your own** Gemini key (Section 1.15; the free-tier note above applies). With the **offline voice**, the voice is made **on your device** and your script is not sent anywhere. Voices are AI-generated: say so when you publish them (Section 12).
- The app exports videos using a short-lived **foreground service** and shows a **progress notification** so a long export keeps running when you switch away. On Android 13+ this needs **notification permission**. This is entirely on your device — no media or content is uploaded for it.
- We use **Google Firebase Analytics** to understand how the app is used at an aggregate level. This is automatic, standard Android telemetry; we do not link it to your name, email, or your media content.
- We use **Google Firebase Crashlytics** to receive **technical crash and error reports** (what failed, the error text, media-format facts, device model, app version) so we can fix problems. API keys, e-mail addresses and file names are removed first, and no media or content you create is ever included. See Section 1.11.
- We display **Google AdMob ads** (a full-screen ad shown before you export a video, which you may dismiss, and an occasional interstitial when you return to the Home screen). AdMob is operated by Google and uses your device's **advertising identifier** and ad-interaction data to serve and measure ads.
- In the EEA, UK, Switzerland and other regions where required, Google shows you a **consent form** (Google's User Messaging Platform) before personalized ads are served. You can change or withdraw this choice at any time.
- We do not sell your personal information for money. Where personalized ads are served, this may count as "sharing" for cross-context behavioural advertising under California law — you can opt out (see Sections 1.6 and 8).
- You can opt out of personalized ads, opt out of Firebase Analytics and Crashlytics, reset your advertising identifier, and clear all app data at any time (instructions below).

---

## 1. Information processed by the app

### 1.1 Media files (videos, audio) you select
KineCut accesses video and audio files **only** from the locations you explicitly pick through the Android system file picker. These files are read and processed locally on your device for the app's core features (Auto Captions and Kinetic Typography). We do **not** copy, upload, or retain your media on our infrastructure (we have none).

### 1.2 Your Groq API key
KineCut requires you to enter a Groq API key to use the AI transcription feature. This key:

- Is stored locally on your device using Android's `EncryptedSharedPreferences` with the `AES256_GCM` master-key scheme and `AES256_GCM` value encryption (`androidx.security:security-crypto`).
- Is never transmitted to us or to any party other than Groq's official API endpoints (`api.groq.com`).
- Is never shared with, reused for, or exposed to any other KineCut user. Each user supplies and uses only their own key.
- Is included in Android Auto Backup if you have backup enabled in your Google Account (see Section 6). To exclude it, disable Auto Backup for KineCut in Android Settings → Google → Backup.
- Can be cleared at any time through Settings → Apps → KineCut → Storage → Clear data, or by uninstalling the app.

### 1.3 Audio sent to Groq for transcription
When you press the "Generate Captions" or transcription button, KineCut extracts audio from the media file you selected and sends it over HTTPS (TLS) to Groq's API for speech-to-text processing. This transmission:

- Is initiated only by your explicit action.
- Uses your own Groq account and your own API key. Groq treats you, not us, as the customer for that request, and you remain responsible for activity associated with your account and API usage.
- Is governed by **Groq's Privacy Policy** (https://groq.com/privacy-policy/), Groq's Terms of Use, and Groq's Acceptable Use Policy (https://console.groq.com/docs/legal/ai-policy), which you accepted when you created your Groq account.
- Returns text transcripts back to your device. Groq states it does not use Inputs or Outputs to train its models.

Groq has confirmed that an application of this type — where each user supplies and uses their own Groq API key — is permitted under Groq's policies, provided the app and its users comply with Groq's Terms of Use and Acceptable Use Policy, keys are stored and handled securely, keys are not shared or reused between users, and usage does not attempt to bypass rate limits or platform restrictions. KineCut is designed to meet these requirements. KineCut does not relay your audio through any server we operate; your audio data does not pass through us.

### 1.4 Saved projects, captions, exports, settings
All caption projects, edited transcripts, exported videos, font/style preferences, and other in-app data are stored locally on your device in KineCut's private storage. We have no access to this data. Uninstalling the app or clearing app data removes it.

### 1.5 Firebase Analytics (Google) — automatic telemetry
KineCut integrates the **Google Firebase Analytics SDK** (`com.google.firebase:firebase-analytics`) to help us understand how the app is used in aggregate, fix crashes, and improve features. Firebase Analytics is operated by Google LLC and Google Ireland Ltd., and is governed by Google's Privacy Policy and Firebase's data-processing terms.

When you use KineCut, Firebase Analytics automatically collects, on Google's servers:

- **Pseudonymous identifiers**: Firebase Installation ID, App Instance ID. These reset when you reinstall the app or clear data.
- **Approximate location** derived from IP address (typically country-level). KineCut never requests precise GPS or network-based location.
- **Device and app information**: device model, manufacturer, brand, OS version, locale, app version, build, install time, first open time, time zone.
- **Usage events**: app opens, session start/end, session duration, screen views, foreground/background, crashes (`app_exception`), app update/clear-data events.
- **Network type** (Wi-Fi / mobile).

Firebase Analytics does **not** receive: your Groq API key, your media files, your audio, your transcripts, your caption projects, your exported videos, your name, your email, or any content you create.

Google may store this data on servers in the United States and other countries where Google operates. See:
- Firebase data privacy and security: https://firebase.google.com/support/privacy
- Google Privacy Policy: https://policies.google.com/privacy
- How Google uses data from sites or apps that use its services: https://policies.google.com/technologies/partner-sites

### 1.6 Google AdMob advertising
KineCut displays advertising through **Google AdMob** (Google Mobile Ads SDK, `com.google.android.gms:play-services-ads`). AdMob is operated by Google LLC and Google Ireland Ltd. and is governed by Google's Privacy Policy and the Google AdMob/AdSense terms.

**Where and how ads appear:**
- A **full-screen interstitial ad** shown before you export a video, in both the Kinetic Typography editor and Auto Captions. You may dismiss it, and the export still proceeds whether or not the ad is shown, dismissed, or fails to load.
- An occasional **full-screen interstitial ad** when you leave a feature and return to the Home screen. Both placements are frequency-capped (the two never stack back-to-back; the nav-back ad appears no more than roughly once every 3 minutes) to limit interruption.

**Data Google collects through AdMob:** To request, serve, frequency-cap, measure, and detect fraud/invalid activity for ads, the Google Mobile Ads SDK and Google may process:

- The **Android Advertising ID (AAID)** and, where applicable, an app-set ID. Because the Google Mobile Ads SDK is integrated, KineCut's app now declares the `com.google.android.gms.permission.AD_ID` permission (added automatically by the SDK), and the AAID is available to and used by AdMob. **This is a change from earlier versions of the app, which did not use the advertising ID.**
- IP address (used to derive approximate, typically country-level, location), device and OS information, ad-interaction data (ad views, clicks, time spent), and general app usage relevant to ad delivery.

**Personalized vs. non-personalized ads:** Depending on your region and your consent choice, ads may be **personalized** (selected using data about your interests/prior activity) or **non-personalized** (contextual only). In the EEA, UK, Switzerland and other regions where Google requires it, KineCut presents Google's **User Messaging Platform (UMP)** consent form before personalized ads are served, and respects your choice. Where a consent form is not required, ads may be personalized subject to your device-level ad settings; you can opt out of ad personalization at any time (see Section 8).

**AdMob does not receive:** your Groq API key, your media files, your audio, your transcripts, your caption projects, your exported videos, your name, or your email.

Google may store and process AdMob data in the United States and other countries where Google operates. See:
- How Google uses information from partner apps: https://policies.google.com/technologies/partner-sites
- Google Advertising / Ad technologies: https://policies.google.com/technologies/ads

### 1.7 Google Play Services (operating-system level)
KineCut runs on Android and uses Google Play Services where present (required for Firebase Analytics, Google AdMob, and standard Play distribution). Google Play Services is part of the Android operating system and is governed by Google's policies, not ours.

### 1.8 Your optional Google Gemini API key ("bring your own key")
KineCut includes an **optional** integration with Google's Gemini API. It is **disabled until you choose to enter your own Google Gemini API key** in the app's setup screen. If you do not add a key, the app runs entirely on the Groq path described above and **nothing is ever sent to Google Gemini**.

If you add a Gemini key:

- It is stored **locally on your device** using Android's `EncryptedSharedPreferences` with the `AES256_GCM` master-key scheme (key names encrypted with `AES256_SIV`, values with `AES256_GCM`, via `androidx.security:security-crypto`), in a storage file separate from your Groq key.
- It is **never transmitted to us or to any party other than Google's official Gemini API endpoint** (`generativelanguage.googleapis.com`), and is sent only in the request header that authenticates your own calls.
- It is **never shared with, reused for, or exposed to any other KineCut user.** Each user supplies and uses only their own key. We operate no server and never receive, log, or store your key.
- It is the credential of **your own** Google account. **You** are Google's customer for those API calls; you remain responsible for the activity, billing, quota, and terms associated with your Google/Gemini account.
- It is included in Android Auto Backup if you have backup enabled (see Section 6). To exclude it, disable Auto Backup for KineCut.
- Can be cleared at any time by clearing the field in setup, or via Settings → Apps → KineCut → Storage → Clear data, or by uninstalling the app.

### 1.9 Data sent to Google Gemini (only when you add a Gemini key)
When — and only when — you have added your own Gemini key, KineCut may send the following over HTTPS (TLS) directly to Google's Gemini API, initiated by your explicit action (pressing Generate / transcribe / export captions):

- **The audio you choose to transcribe or caption** (extracted from the media you selected), encoded and sent inline to Gemini for speech-to-text and caption-refinement.
- **The transcript text** produced from your audio, sent to Gemini for optional "smart-work" passes (choosing words to emphasise and where phrases break).

KineCut does **not** relay this through any server we operate; the data goes from your device straight to Google under your own API key. We never see it.

**How Google uses this data depends on your Gemini plan — please read this carefully:**

- **Free / unpaid Gemini tier (e.g. a key from Google AI Studio with no billing):** Under Google's *Gemini API Additional Terms of Service*, Google uses the content you submit and the responses generated **to provide, improve and develop Google's products, services and machine-learning technologies**, and **human reviewers may read, annotate and process your inputs and outputs** (Google states it disconnects this data from your Google account, API key and Cloud project before human review). **Do not send audio or text you consider sensitive, confidential, or personal on a free-tier key.**
- **Paid Gemini tier:** Google states it **does not** use your prompts or responses to improve its products, and processes them under Google's Data Processing Addendum.
- **EEA, UK and Switzerland:** Google's terms state that the "Paid Services" data rules apply to **all** Gemini API use in these regions (even free quota), and that API clients there may need to be on a paid plan. If you are in these regions, use a paid Gemini key.

This integration is governed by **Google's Gemini API Additional Terms of Service** (https://ai.google.dev/gemini-api/terms), the **Generative AI Prohibited Use Policy** (https://policies.google.com/terms/generative-ai/use-policy), and **Google's Privacy Policy** (https://policies.google.com/privacy), all of which you accept with Google when you create and use your Gemini API key. You are solely responsible for your use of your Gemini key and for ensuring your content and use comply with those Google policies and applicable law. Google receives your audio and transcript text for these calls; it does **not** receive your Groq API key, your saved projects, your exported videos, your name, or your email from KineCut.

### 1.10 Export notifications and the export foreground service
When you export a video, KineCut starts a short-lived **foreground service** that keeps the export running if you press Home or lock your phone, and shows a **progress notification** while the export is in progress. On Android 13 and above, showing this notification requires the `POST_NOTIFICATIONS` permission, which the system asks you to allow; if you deny it, the export still works, just without a visible progress notification. The service performs **no network activity and uploads nothing** — it only keeps the on-device export alive and reports progress. It stops automatically when the export finishes, fails, or is cancelled.

### 1.11 Firebase Crashlytics (Google) — crash and error reports
KineCut integrates the **Google Firebase Crashlytics SDK** (`com.google.firebase:firebase-crashlytics`) so we can find and fix crashes and failures. Firebase Crashlytics is operated by Google LLC and Google Ireland Ltd., and is governed by Google's Privacy Policy and Firebase's data-processing terms. It is **switched off until you accept this Privacy Policy** in the app, the same as Firebase Analytics.

A report is sent when the app crashes, or when a task fails and the app shows you an error (for example an export, a transcription, a translation or an audio-tool conversion). A report contains:

- **Crash / error details**: the error messages and the places in KineCut's code where the problem happened (a "stack trace"), a short code naming the feature and step that failed, and the app's own technical notes about recent problems it handled quietly (for example "used a lower export resolution").
- **Technical facts about the media being processed**: format and codec names, resolution, frame rate, duration, sound sample rate and channels, file extension and size. **Never** the media itself.
- **Device and app information**: device model and manufacturer, chip name, Android version, free storage and free memory at the time, app version, and whether the app was in the foreground.
- **Pseudonymous identifiers**: a Crashlytics installation ID and the Firebase installation ID (both reset when you reinstall the app or clear its data).

Before a report leaves your device, KineCut **removes API keys, e-mail addresses and your file names** from it (only the file extension, such as ".mp3", is kept). Crash reports created by Android itself when the app crashes are sent as Android creates them and may include file locations in rare cases. Crashlytics does **not** receive your Groq or Gemini API key, your media files, your audio, your transcripts or captions, your projects, your exported videos, your name or your email.

The app also lets **you** copy or share a problem report yourself ("Show details" → Copy / Share / Telegram). Nothing is sent that way unless you choose to send it.

See: Firebase data privacy and security: https://firebase.google.com/support/privacy

---

### 1.12 Offline Hindi, Hinglish and English voice packs (on-device speech recognition)
When you pick Hindi, Hinglish or English, KineCut can offer a free **voice pack** for that language (Hindi about 200 MB, Hinglish about 240 MB, sharing most of their files; English about 140 MB). It is downloaded **only if you tap Download**, and it comes from **Google Play**, like an app update (Google Play handles that download under Google's own policies; see Section 1.7).

Once the voice pack is on your device, Hindi, Hinglish or English speech is turned into words **entirely on your device**: for that step your audio is **not sent** to Groq, Google Gemini, us, or anyone else. If the voice pack is not downloaded, your phone cannot run it, or the on-device step fails, KineCut uses the normal online path described in Sections 1.3 and 1.9. Other AI features (for example smart highlights in Kinetic Typography) still use your own API keys as described above.

Firebase Analytics (Section 1.5) records only technical events about the voice pack, such as that it was offered or downloaded, and how long an on-device transcription took. It never receives your audio or the words.

To choose the language a tool starts on, KineCut reads your SIM card's country code (for example "in") **on your device**, without any permission. It is used only on your device and is **not sent** to us, Firebase or anyone else.

With a voice pack, Hindi, Hinglish and English need **no API key**. Other languages, and features such as caption translation, still need your own free Groq or Gemini key. Analytics also records which language you pick in a tool and, if you tap it, your vote for a language to get its own voice pack - never your audio or words.

### 1.13 Firebase Remote Config (Google) — app settings
KineCut uses the **Google Firebase Remote Config SDK** (`com.google.firebase:firebase-config`) to switch some features on or off and change small settings without an app update (for example, which language a new user's tool starts on). To fetch these settings the SDK sends Google a Firebase Installation ID and basic device and app information (app version, OS version, locale), like Firebase Analytics. It receives no media, audio, transcripts, keys or other content you create. Like Firebase Analytics, it only runs **after you accept this Privacy Policy**. Firebase Remote Config is operated by Google LLC and Google Ireland Ltd. under Google's Privacy Policy and Firebase's data-processing terms.

### 1.14 Flight Map: "Search online" for a place
Flight Map's place list works without internet. Only if you tap **Search online**, the place name you typed is sent to your phone's own place-lookup service (Google Play Services on most phones, see Section 1.7) to find it. We never receive what you typed, and Firebase Analytics only records whether a place was found.

### 1.15 Script to Video (optional): AI voices from the script you type
Script to Video turns a script you type into a voice, then opens the Kinetic Typography editor with every word of your script timed to that voice. You choose how the voice is made:

- **Gemini voice** (needs your own Gemini key, Section 1.8): when you tap **Make video**, the **script text you typed** is sent over HTTPS directly to **Google's Gemini API** (its text-to-speech models) with your key, and Google returns the voice. If one Gemini voice model is busy or out of its limit, KineCut sends the same request to the next Gemini voice model. Everything in Section 1.9 about how Google uses this data applies, including the free-tier note: **on a free Gemini key, Google may use your script to improve its products and human reviewers may read it.** Do not type anything sensitive on a free-tier key.
- **Offline voice:** a voice model (about 140 MB) is downloaded from **Google Play** only if you tap Download (see Sections 1.7 and 1.12). The voice is then made **entirely on your device**: your script is **not sent** to Google, us or anyone else.
- **Your phone's own voice** (only if you choose it, for example after a Gemini error): the script is given to your phone's text-to-speech engine (usually "Speech Services by Google"), which normally works on your device. That engine is part of your phone and works under its own policy.

To time each word, KineCut listens to the voice it just made **on your device** with the offline voice pack of Section 1.12 when you have it. If not, and you use the Gemini voice, the voice audio may be sent to Google's Gemini API with your key for speech-to-text (Section 1.9). As in Kinetic Typography, the words may also be sent to your own AI key's provider for the optional "smart-work" pass (choosing words to emphasise).

The voice is saved **on your device** as part of the Kinetic Typography project and is deleted when you delete that project. The script you are typing is kept on your device so it is still there when you come back. Firebase Analytics (Section 1.5) records only technical facts about each voice: which voice maker, model and voice name were used, the language, the script's length in letters, how long the voice is and how long it took, how the words were timed, and whether it worked. It **never** receives your script or the voice. Error reports (Section 1.11) never include your script either.

## 2. Information we do NOT collect

- We do not collect your name, email, phone number, postal address, or government identifiers.
- We do not require account registration or login with KineCut.
- We do not access your contacts, calendar, SMS, call logs, microphone (live), camera (live), or precise location.
- We do not have a backend; we cannot read your stored projects, exports, or API keys (Groq or the optional Gemini key).
- We do not enable the Gemini integration unless you add your own key; with no key, nothing is sent to Google Gemini. We never receive your Gemini key, your audio, or your transcripts — they go directly from your device to Google under your own account.
- We never receive the scripts you type in Script to Video or the voices made from them (Section 1.15).
- We do not sell your personal information for money.
- We do not use Firebase Authentication, Firebase Cloud Messaging, Google Sign-In, or any analytics or crash-reporting SDK other than Firebase Analytics (Section 1.5) and Firebase Crashlytics (Section 1.11) (plus Firebase Remote Config for app settings, Section 1.13), and no advertising SDK other than Google AdMob described in Section 1.6.

We **do** display Google AdMob ads, and AdMob's use of the advertising identifier to serve **personalized** ads may constitute "sharing" of personal information for cross-context behavioural advertising under the California CCPA/CPRA. We do not exchange personal information for money. See Sections 1.6 and 8 for how to opt out.

---

## 3. Permissions

KineCut requests only the permissions required for the features it offers:

| Permission | Purpose |
|---|---|
| `INTERNET` | Send audio to Groq's API for transcription; if you add a Gemini key, send audio/transcript text (and, for the Gemini voice in Script to Video, your script) to Google's Gemini API; let Firebase Analytics send aggregate telemetry; let Firebase Crashlytics send crash and error reports; let Google AdMob request and measure ads. |
| `ACCESS_NETWORK_STATE` | Let the ad and analytics SDKs check connectivity before making network requests. |
| `com.google.android.gms.permission.AD_ID` | Declared automatically by the Google Mobile Ads SDK. Allows access to the Android Advertising ID for ad serving, frequency capping, and fraud prevention. You can reset or delete this ID at any time (Section 8). |
| `READ_MEDIA_AUDIO` | Let you select audio files for Kinetic Typography (Android 13+). |
| `READ_EXTERNAL_STORAGE` (Android 12 and below only) | Let you select media on devices that don't yet expose granular media permissions. |
| `WRITE_EXTERNAL_STORAGE` (Android 9 and below only) | Save exported videos to your device gallery on legacy versions of Android. Not used on Android 10+ (we use scoped storage / MediaStore). |
| `FOREGROUND_SERVICE`, `FOREGROUND_SERVICE_DATA_SYNC` | Keep a video export running on your device if you leave the app or lock the phone mid-export. No network use. |
| `POST_NOTIFICATIONS` (Android 13+) | Show the export-progress notification while a video is being exported. You may deny it; export still works without the notification. |

Videos and images you add are chosen through the Android system picker, so KineCut never asks for access to your photo or video library and can only open the files you pick.

We do not request `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`, `RECORD_AUDIO`, `CAMERA`, `READ_CONTACTS`, or any "dangerous" runtime permission beyond the media permissions listed.

---

## 4. Legal bases for processing (EEA / UK users — GDPR Art. 6)

Where the GDPR or UK GDPR applies, we rely on the following lawful bases:

- **Contract / pre-contract steps (Art. 6(1)(b))** — to provide the app's core features that you actively requested (transcribing your selected audio, saving your project locally, and exporting your video, including the keep-alive export notification).
- **Consent (Art. 6(1)(a))** — for the **optional** Google Gemini integration: nothing is sent to Google Gemini unless you choose to add your own Gemini key, and you can remove it at any time. By adding a key you instruct us to send your audio and transcript text to Google under your own account, and you accept Google's Gemini API terms directly.
- **Legitimate interests (Art. 6(1)(f))** — for limited Firebase Analytics telemetry and Firebase Crashlytics crash/error reports used to maintain, debug, and improve the app, and for serving **non-personalized** ads and fraud prevention. We balance this against your privacy interests; analytics data is pseudonymous and aggregated, and error reports are technical and have keys, e-mail addresses and file names removed.
- **Consent (Art. 6(1)(a))** — for **personalized advertising** through Google AdMob, collected via Google's User Messaging Platform consent form where required, and for analytics where local law requires consent. You may withdraw consent at any time (see Section 8).

---

## 5. International transfers

KineCut is operated from India. Audio you transcribe is sent to Groq's infrastructure in the United States. If you add a Gemini key, your audio, transcript text and Script to Video scripts (Gemini voice) are sent to Google's Gemini API, processed by Google in the United States and other countries where Google operates. Firebase Analytics, Firebase Crashlytics and Google AdMob data are processed by Google on servers in the United States and other countries where Google operates.

For users in the EEA, UK and Switzerland, Groq and Google rely on the **EU Standard Contractual Clauses** and equivalent transfer mechanisms to lawfully transfer personal data outside those regions. KineCut is not party to these clauses; we rely on Groq's and Google's transfer frameworks for the third-party processing they perform. For the optional Gemini integration in the EEA, UK and Switzerland, Google's terms state that the paid-tier data protections apply to all Gemini API use and that a paid plan may be required; if you are in these regions and choose to use Gemini, use a paid Gemini key.

---

## 6. Android Auto Backup

KineCut declares `android:allowBackup="true"` in its manifest. If you have **Auto Backup** enabled in your Google Account (Settings → Google → Backup), Android may include KineCut's app data — including your locally saved projects and your encrypted Groq API key — in the encrypted backup uploaded to your personal Google Drive.

This backup is associated with **your** Google Account, end-to-end encrypted by Google, and never accessible to us. To opt out, disable Auto Backup for KineCut in your Android backup settings, or sign out of your Google Account before installing.

---

## 7. Data retention

- **On your device:** Saved projects, settings, and your encrypted Groq API key remain until you delete a project, clear app data, or uninstall the app.
- **Groq:** Per Groq's Privacy Policy, Groq does not use your audio or transcripts to train models and retains data only as needed to operate the service. Retention is governed by Groq.
- **Google Gemini (only if you use it):** Retention and use of any audio or text you send to Gemini are governed by Google's Gemini API terms and Privacy Policy. On the free tier, Google may retain and use it to improve Google's products (including human review); on the paid tier, Google states it does not use it to train its products. Remove your Gemini key to stop sending anything further; data already sent is handled under Google's policies and your Google account controls.
- **Firebase Analytics:** We retain analytics events for the maximum default period of **14 months**. Firebase Installation IDs may persist longer until you reinstall or clear data.
- **Firebase Crashlytics:** Google retains crash and error reports (stack traces, related technical details and the Crashlytics installation ID) for **90 days**, after which they are deleted.
- **Google AdMob:** Retention of advertising identifiers and ad-event data is governed by Google's policies. Resetting your advertising ID or opting out of ad personalization limits future use.

---

## 8. Your privacy rights

### 8.1 Rights available to all users
You can, at any time:

- **Stop the app from sending audio to Groq** by not pressing the transcription button.
- **Delete your Groq API key** from KineCut (Auto Captions screen → clear field, or Settings → Apps → KineCut → Storage → Clear data).
- **Delete your Google Gemini API key** (clear the Gemini field in setup, or Clear data) to disable the Gemini integration so nothing further is sent to Google Gemini. For Gemini data Google already holds, use your Google account and Gemini/Cloud privacy controls.
- **Change or withdraw your ads consent** through the in-app/Google "Privacy options" or consent form, where shown for your region.
- **Opt out of personalized ads** via Settings → Google → Ads (or "Ads" on your device) → "Opt out of Ads Personalisation"; ads then become non-personalized/contextual.
- **Reset or delete your Android Advertising ID** in Settings → Privacy → Ads (or "Ads" on your device).
- **Reset analytics and crash-report identifiers** by uninstalling and reinstalling the app, which generates a new Firebase Installation ID and Crashlytics installation ID.
- **Ask us to delete crash/error reports** linked to your app installation by contacting us (Section 9); otherwise Google deletes them automatically after 90 days (Section 7).
- **Limit Google's use of your data** through Google Account → Data & privacy (https://myaccount.google.com/data-and-privacy).

### 8.2 GDPR / UK GDPR rights (EEA, UK, Switzerland)
You have the rights to: access, rectification, erasure ("right to be forgotten"), restriction, data portability, objection (including to processing based on legitimate interests and to direct marketing/ad profiling), and withdrawal of consent at any time. You also have the right to lodge a complaint with your local supervisory authority (e.g. ICO in the UK, CNIL in France).

Because KineCut stores no personal data on our servers, we have nothing to access, export, or delete on your behalf for app-stored data — clearing app data on your device is the technical equivalent. For analytics, crash-report or advertising data Google holds about your app instance, please use Google's privacy and ad-consent controls referenced above, or contact us and we will raise a deletion request with Google on your behalf within 30 days.

### 8.3 California rights (CCPA / CPRA)
California residents have the rights to know, delete, correct, opt out of "sale" or "sharing", limit use of sensitive personal information, and not be discriminated against for exercising any right.

We **do not** sell personal information for money. We **do** use Google AdMob, and serving **personalized** ads may constitute "sharing" of personal information (your advertising identifier and ad-interaction data) for cross-context behavioural advertising. **To opt out of this "sharing,"** opt out of ad personalization via your device's Google Ads settings (Section 8.1), decline personalized ads in the consent form where shown, or reset/delete your advertising ID. Categories of personal information processed in the past 12 months are listed in Sections 1.3, 1.5, 1.6 and 1.11; they are processed for the purposes stated there and are not retained beyond Section 7. To exercise rights, contact us at the email below.

### 8.4 India (DPDP Act, 2023) rights
If you are in India, you have rights to: access information about your personal data, correction and erasure, grievance redressal, and nomination. We rely on **legitimate use** for performance of the app's core function and on your **consent** for Firebase Analytics, Firebase Crashlytics and for personalized advertising. You may withdraw consent through your device's privacy/ad settings, the ads consent form, or by uninstalling the app.

**Grievance Officer (DPDP Act §8(9)):**
Name: Yashwant Shila
Email: punutype@gmail.com
We will respond to grievances within the statutory timeline (currently 30 days under the DPDP Rules).

### 8.5 Children's privacy (COPPA, GDPR-K, DPDP §9)
KineCut is **not directed at children** and is rated for users 13 and over. It is not configured as a child-directed app, and we do not knowingly collect personal information from children under 13 (under 16 in some EEA jurisdictions; under 18 in India under the DPDP Act). Advertising shown through AdMob is general-audience and not directed to children. If you believe a child has used the app, please contact us and we will take reasonable steps to delete what we can identify.

If you are a parent or guardian and you discover your child has used KineCut with your Groq or Gemini API key, please remove your key(s) from the app and contact Groq and/or Google directly to handle any data your child may have submitted to their APIs.

---

## 9. How to exercise your rights or contact us

Email: **punutype@gmail.com**
Subject line: "KineCut Privacy — [your request type]"

Please tell us your country/state of residence and the right you wish to exercise. We will respond within 30 days, or sooner where required by law. We may need to verify your identity (for example by asking you to send the email from the device the app is installed on) to prevent fraudulent requests.

---

## 10. Security

- Your Groq API key and your optional Gemini API key are each encrypted at rest using AES-256 GCM via Android's `EncryptedSharedPreferences` (in separate storage files), are never shared or reused between users, and are never transmitted to anyone except the respective provider's official API (Groq, or Google's Gemini API).
- Network traffic to Groq, Google's Gemini API, Firebase, and Google AdMob uses HTTPS / TLS 1.2 or higher.
- We operate no servers, databases, or login systems, eliminating common attack surfaces (credential leaks, SQL injection, server breaches).
- No security measure is absolute. You are responsible for keeping your device, lock screen, Google Account, Groq account, and Gemini/Google AI Studio account secure. If you suspect your Groq API key has been exposed, regenerate it at https://console.groq.com/keys; if you suspect your Gemini key has been exposed, regenerate it at https://aistudio.google.com/apikey.

---

## 11. Third-party services and links

KineCut depends on the following third-party services. Their handling of your data is governed by their own policies, which we encourage you to review:

| Service | Role | Privacy policy |
|---|---|---|
| Groq, Inc. | AI speech-to-text transcription using your own API key | https://groq.com/privacy-policy/ |
| Google LLC (Gemini API) | OPTIONAL AI transcription, caption refinement and smart-work using **your own** Gemini API key (off unless you add a key) | https://ai.google.dev/gemini-api/terms ; https://policies.google.com/terms/generative-ai/use-policy ; https://policies.google.com/privacy |
| Google LLC / Firebase | App analytics (Firebase Analytics), crash/error reports (Firebase Crashlytics) and app settings (Firebase Remote Config) | https://firebase.google.com/support/privacy ; https://policies.google.com/privacy |
| Google AdMob (Google LLC) | In-app advertising (rewarded + interstitial), ad measurement and fraud prevention; consent via Google User Messaging Platform | https://policies.google.com/technologies/ads ; https://policies.google.com/privacy |
| Google Play Services | Required runtime layer for Firebase, AdMob and Play distribution | https://policies.google.com/privacy |

We are not responsible for the privacy practices of these third parties. Where this Privacy Policy makes statements about them, we have done so in good faith based on their published terms as of the "Last updated" date.

---

## 12. AI-generated content disclosure

Captions and transcripts produced by KineCut are generated by AI speech-to-text and language models operated by Groq and, if you enable it, by Google's Gemini API. AI output may contain errors, mis-transcriptions, or omissions. You are responsible for reviewing and correcting the output before publishing or relying on it for any consequential purpose. KineCut and its publisher are not liable for inaccuracies in AI-generated output.

You are responsible for ensuring that any media you transcribe with KineCut is content you have the legal right to use, and that your use complies with the policies of whichever provider you use:

- **Groq** — Groq's Acceptable Use Policy (https://console.groq.com/docs/legal/ai-policy).
- **Google Gemini (if you add a key)** — Google's Gemini API Additional Terms of Service (https://ai.google.dev/gemini-api/terms) and the Generative AI Prohibited Use Policy (https://policies.google.com/terms/generative-ai/use-policy). You enter your own Gemini key, you are Google's customer for those calls, and you are solely responsible for your use of the Gemini API through KineCut. Google's terms describe the Gemini API as intended for developers building for professional or business purposes; by adding your key you confirm you may use it on those terms.

**AI voices (Script to Video).** The voices made in Script to Video are generated by AI: by Google's Gemini API (under Google's terms listed above), by the offline voice model on your device, or by your phone's own text-to-speech engine. You are responsible for the scripts you type and for how you use the voices. **When you publish a video with an AI voice, clearly say that the voice is AI-generated** (for example "AI voice" in the caption or description). Do not use AI voices to impersonate a real person without their consent, to deceive, defame or harass anyone, or to spread false information meant to harm others.

**Offline voice use rules.** The offline voice uses the **Supertonic 3** model by Supertone Inc., licensed under the **BigScience Open RAIL-M License**. Its use-based restrictions (paragraph 5 and Attachment A of that licence) are part of these terms and you agree to follow them when you use the offline voice. In short, you may not use it: in a way that breaks any law; to exploit or harm minors; to make or spread verifiably false information meant to harm others; to make or spread personal information that can be used to harm someone; to publish its output without clearly saying it is machine generated; to defame, disparage or harass others; to impersonate others (for example deepfakes) without their consent; for fully automated decisions that harm a person's legal rights; to discriminate against or harm people or groups; to exploit the vulnerabilities of a group of people; to give medical advice or interpret medical results; or for the administration of justice, law enforcement, immigration or asylum processes (such as predicting crime). The complete licence and its full list of restrictions are in the app under **Open Source Licenses**; if this summary and the licence differ, the licence applies.

Do not use the app to process content you do not have rights to, to generate harassing, deceptive, infringing or unlawful material, to create non-consensual or deceptive media, to bypass rate limits or platform restrictions, or for any purpose prohibited by the applicable provider's policies or by law. KineCut does not itself send anything to any AI provider beyond the audio/text needed for the feature you trigger, and sends to Gemini only when you have added your own Gemini key.

---

## 13. Changes to this Policy

We may update this Privacy Policy from time to time. When we do, we will:

- Update the "Last updated" date at the top.
- For material changes (new categories of data collected, new third parties, new purposes), publish the updated policy at least 7 days before it takes effect, on this same page and on the KineCut Play Store listing.
- Continued use of the app after the effective date of an update constitutes acceptance of the updated policy.

A change-log of past versions is available on request.

---

## 14. Contact

**KineCut** — punutype@gmail.com
Publisher: Yashwant Shila
Country of operation: India
Application package: `com.kinecut.app`

If you cannot resolve a privacy concern with us, EEA users may complain to their local Data Protection Authority; UK users to the ICO (https://ico.org.uk/); Indian users to the Data Protection Board of India once constituted under the DPDP Act.
