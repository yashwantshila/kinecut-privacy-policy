# Privacy Policy for KineCut

**Last updated:** May 9, 2026
**Effective date:** May 9, 2026
**App name:** KineCut
**Package:** com.kinecut.app
**Publisher / Data Controller:** Yashwant Shila ("we", "our", "us")
**Contact:** punutype@gmail.com

This Privacy Policy explains what information KineCut ("the app") accesses, processes, and shares when you use it on your Android device. It applies to users worldwide and complies with the EU/UK GDPR, the California Consumer Privacy Act / CPRA, and India's Digital Personal Data Protection Act, 2023 (DPDP Act).

By installing or using KineCut, you confirm that you have read and accepted this Privacy Policy.

---

## Plain-English summary

- We do not run any servers and we do not have user accounts. We never see your videos, audio, captions, or projects.
- Your media files are processed on your device. The only thing leaving your device for the core feature is the **audio you choose to transcribe**, which is sent over HTTPS directly to **Groq's API** using **your own Groq API key**.
- We use **Google Firebase Analytics** (a Google product) to understand how the app is used at an aggregate level (sessions, crashes, screen views, device/OS, country). This is automatic and standard Android SDK telemetry; we do not link it to your name, email, or your media content.
- We display no advertising. We do not sell or share your personal information.
- You can opt out of Firebase Analytics, reset your advertising identifiers, and clear all app data at any time (instructions below).

---

## 1. Information processed by the app

### 1.1 Media files (videos, audio) you select
KineCut accesses video and audio files **only** from the locations you explicitly pick through the Android system file picker. These files are read and processed locally on your device for the app's core features (Auto Captions and Kinetic Typography). We do **not** copy, upload, or retain your media on our infrastructure (we have none).

### 1.2 Your Groq API key
KineCut requires you to enter a Groq API key to use the AI transcription feature. This key:

- Is stored locally on your device using Android's `EncryptedSharedPreferences` with the `AES256_GCM` master-key scheme and `AES256_GCM` value encryption (`androidx.security:security-crypto`).
- Is never transmitted to us or to any party other than Groq's official API endpoints (`api.groq.com`).
- Is included in Android Auto Backup if you have backup enabled in your Google Account (see Section 6). To exclude it, disable Auto Backup for KineCut in Android Settings → Google → Backup.
- Can be cleared at any time through Settings → Apps → KineCut → Storage → Clear data, or by uninstalling the app.

### 1.3 Audio sent to Groq for transcription
When you press the "Generate Captions" or transcription button, KineCut extracts audio from the media file you selected and sends it over HTTPS (TLS) to Groq's API for speech-to-text processing. This transmission:

- Is initiated only by your explicit action.
- Uses your own Groq account and your own API key. Groq treats you, not us, as the customer for that request.
- Is governed by **Groq's Privacy Policy** (https://groq.com/privacy-policy/) and the Groq Services Agreement, which you accepted when you created your Groq account.
- Returns text transcripts back to your device. Groq states it does not use Inputs or Outputs to train its models (Groq Services Agreement, §4.2).

KineCut does not relay your audio through any server we operate. Your audio data does not pass through us.

### 1.4 Saved projects, captions, exports, settings
All caption projects, edited transcripts, exported videos, font/style preferences, and other in-app data are stored locally on your device in KineCut's private storage. We have no access to this data. Uninstalling the app or clearing app data removes it.

### 1.5 Firebase Analytics (Google) — automatic telemetry
KineCut integrates the **Google Firebase Analytics SDK** (`com.google.firebase:firebase-analytics`, BOM 33.7.0) to help us understand how the app is used in aggregate, fix crashes, and improve features. Firebase Analytics is operated by Google LLC and Google Ireland Ltd., and is governed by Google's Privacy Policy and Firebase's data-processing terms.

When you use KineCut, Firebase Analytics automatically collects, on Google's servers:

- **Pseudonymous identifiers**: Firebase Installation ID, App Instance ID. These reset when you reinstall the app or clear data.
- **Android Advertising ID (AAID)**: KineCut does **not** declare the `com.google.android.gms.permission.AD_ID` permission. As a result, on Android 13+ the AAID is reported as a zero-string and is not usable to identify you. On older Android versions Google may still receive it; you can reset or limit it from Settings → Privacy → Ads.
- **Approximate location** derived from IP address (typically country-level). KineCut never requests precise GPS or network-based location.
- **Device and app information**: device model, manufacturer, brand, OS version, locale, app version, build, install time, first open time, time zone.
- **Usage events**: app opens, session start/end, session duration, screen views, foreground/background, crashes (`app_exception`), app update/clear-data events.
- **Network type** (Wi-Fi / mobile, not your IP address as a stored identifier).

Firebase Analytics does **not** receive: your Groq API key, your media files, your audio, your transcripts, your caption projects, your exported videos, your name, your email, or any content you create.

Google may store this data on servers in the United States and other countries where Google operates. See Google's policies for retention details:
- Firebase data privacy and security: https://firebase.google.com/support/privacy
- Google Privacy Policy: https://policies.google.com/privacy
- How Google uses data from sites or apps that use its services: https://policies.google.com/technologies/partner-sites

### 1.6 Google Play Services (operating-system level)
KineCut runs on Android and uses Google Play Services where present (required for Firebase Analytics and standard Play distribution). Google Play Services is part of the Android operating system and is governed by Google's policies, not ours.

---

## 2. Information we do NOT collect

- We do not collect your name, email, phone number, postal address, or government identifiers.
- We do not require account registration or login with KineCut.
- We do not access your contacts, calendar, SMS, call logs, microphone (live), camera (live), or precise location.
- We do not display advertising and do not integrate any ad SDK.
- We do not sell or rent personal information to anyone.
- We do not "share" personal information for cross-context behavioural advertising as defined by the CCPA/CPRA.
- We do not have a backend; we cannot read your stored projects, exports, or API key.
- We do not use Firebase Crashlytics, Firebase Authentication, Firebase Cloud Messaging, AdMob, Google Sign-In, or any analytics SDK other than Firebase Analytics described in Section 1.5.

---

## 3. Permissions

KineCut requests only the permissions required for the features it offers:

| Permission | Purpose |
|---|---|
| `INTERNET` | Send audio to Groq's API for transcription; allow Firebase Analytics to send aggregate telemetry to Google. |
| `READ_MEDIA_VIDEO` | Let you select video files to caption or animate (Android 13+). |
| `READ_MEDIA_AUDIO` | Let you select audio files for Kinetic Typography (Android 13+). |
| `READ_MEDIA_IMAGES` | Let you select images for project assets on devices that grant media via this permission. |
| `READ_EXTERNAL_STORAGE` (Android 12 and below only) | Let you select media on devices that don't yet expose granular media permissions. |
| `WRITE_EXTERNAL_STORAGE` (Android 9 and below only) | Save exported videos to your device gallery on legacy versions of Android. Not used on Android 10+ (we use scoped storage / MediaStore). |

We do not request `ACCESS_FINE_LOCATION`, `ACCESS_COARSE_LOCATION`, `RECORD_AUDIO`, `CAMERA`, `READ_CONTACTS`, or any "dangerous" permission beyond those listed.

---

## 4. Legal bases for processing (EEA / UK users — GDPR Art. 6)

Where the GDPR or UK GDPR applies, we rely on the following lawful bases:

- **Contract / pre-contract steps (Art. 6(1)(b))** — to provide the app's core features that you actively requested (transcribing your selected audio, saving your project locally).
- **Legitimate interests (Art. 6(1)(f))** — for limited Firebase Analytics telemetry used to maintain, debug, and improve the app. We balance this against your privacy interests; the data is pseudonymous, aggregated, and not used for advertising. You may object at any time (see Section 8).
- **Consent (Art. 6(1)(a))** — where consent is required by local law for analytics on a mobile app, you provide it by continuing to use the app after viewing this notice. You may withdraw consent at any time by disabling analytics (Section 8) or uninstalling KineCut.

---

## 5. International transfers

KineCut is operated from India. Audio you transcribe is sent to Groq's infrastructure in the United States. Firebase Analytics data is processed by Google on servers in the United States and other countries where Google operates.

For users in the EEA, UK and Switzerland, Groq and Google rely on the **EU Standard Contractual Clauses** and equivalent transfer mechanisms to lawfully transfer personal data outside those regions. KineCut is not party to these clauses; we rely on Groq's and Google's transfer frameworks for the third-party processing they perform.

---

## 6. Android Auto Backup

KineCut declares `android:allowBackup="true"` in its manifest. If you have **Auto Backup** enabled in your Google Account (Settings → Google → Backup), Android may include KineCut's app data — including your locally saved projects and your encrypted Groq API key — in the encrypted backup uploaded to your personal Google Drive.

This backup is associated with **your** Google Account, end-to-end encrypted by Google, and never accessible to us. To opt out, disable Auto Backup for KineCut in your Android backup settings, or sign out of your Google Account before installing.

---

## 7. Data retention

- **On your device:** Saved projects, settings, and your encrypted Groq API key remain until you delete a project, clear app data, or uninstall the app.
- **Groq:** Per Groq's Privacy Policy, Groq does not use your audio or transcripts to train models and retains data only as needed to operate the service. Retention is governed by Groq.
- **Firebase Analytics:** We retain analytics events for the maximum default period of **14 months**. Firebase Installation IDs may persist longer until you reinstall or clear data.

---

## 8. Your privacy rights

### 8.1 Rights available to all users
You can, at any time:

- **Stop the app from sending audio to Groq** by not pressing the transcription button.
- **Delete your Groq API key** from KineCut (Auto Captions screen → clear field, or Settings → Apps → KineCut → Storage → Clear data).
- **Reset analytics identifiers** by uninstalling and reinstalling the app, which generates a new Firebase Installation ID.
- **Reset or delete your Android Advertising ID** in Settings → Privacy → Ads (or "Ads" on your device).
- **Limit Google's use of your data** through Google Account → Data & privacy → My Activity controls (https://myaccount.google.com/data-and-privacy).

### 8.2 GDPR / UK GDPR rights (EEA, UK, Switzerland)
You have the rights to: access, rectification, erasure ("right to be forgotten"), restriction, data portability, objection (including to processing based on legitimate interests), and withdrawal of consent at any time. You also have the right to lodge a complaint with your local supervisory authority (e.g. ICO in the UK, CNIL in France).

Because KineCut stores no personal data on our servers, we have nothing to access, export, or delete on your behalf for app-stored data — clearing app data on your device is the technical equivalent. For analytics data Google holds about your app instance, please use Google's privacy controls referenced above, or contact us and we will raise a deletion request with Google on your behalf within 30 days.

### 8.3 California rights (CCPA / CPRA)
California residents have the rights to know, delete, correct, opt out of "sale" or "sharing", limit use of sensitive personal information, and not be discriminated against for exercising any right. We **do not** sell or share personal information for cross-context behavioural advertising. Categories of personal information processed in the past 12 months are listed in Sections 1.3 and 1.5; they are processed for the purposes stated there and are not retained beyond Section 7. To exercise rights, contact us at the email below.

### 8.4 India (DPDP Act, 2023) rights
If you are in India, you have rights to: access information about your personal data, correction and erasure, grievance redressal, and nomination. We rely on **legitimate use** for performance of the app's core function and on your **consent** for Firebase Analytics. You may withdraw consent by disabling analytics through your device's privacy settings or by uninstalling the app.

**Grievance Officer (DPDP Act §8(9)):**
Name: Yashwant Shila
Email: punutype@gmail.com
We will respond to grievances within the statutory timeline (currently 30 days under the DPDP Rules).

### 8.5 Children's privacy (COPPA, GDPR-K, DPDP §9)
KineCut is **not directed at children** and is rated for users 13 and over. We do not knowingly collect personal information from children under 13 (under 16 in some EEA jurisdictions; under 18 in India under the DPDP Act). If you believe a child has used the app, please contact us and we will take reasonable steps to delete what we can identify.

If you are a parent or guardian and you discover your child has used KineCut with your Groq API key, please remove your key from the app and contact Groq directly to handle any data your child may have submitted to Groq's API.

---

## 9. How to exercise your rights or contact us

Email: **punutype@gmail.com**
Subject line: "KineCut Privacy — [your request type]"

Please tell us your country/state of residence and the right you wish to exercise. We will respond within 30 days, or sooner where required by law. We may need to verify your identity (for example by asking you to send the email from the device the app is installed on) to prevent fraudulent requests.

---

## 10. Security

- Your Groq API key is encrypted at rest using AES-256 GCM via Android's `EncryptedSharedPreferences`.
- Network traffic to Groq and Firebase uses HTTPS / TLS 1.2 or higher.
- We operate no servers, databases, or login systems, eliminating common attack surfaces (credential leaks, SQL injection, server breaches).
- No security measure is absolute. You are responsible for keeping your device, lock screen, Google Account, and Groq account secure. If you suspect your Groq API key has been exposed, regenerate it at https://console.groq.com/keys.

---

## 11. Third-party services and links

KineCut depends on the following third-party services. Their handling of your data is governed by their own policies, which we encourage you to review:

| Service | Role | Privacy policy |
|---|---|---|
| Groq, Inc. | AI speech-to-text transcription using your own API key | https://groq.com/privacy-policy/ |
| Google LLC / Firebase | App analytics (Firebase Analytics) | https://firebase.google.com/support/privacy ; https://policies.google.com/privacy |
| Google Play Services | Required runtime layer for Firebase and Play distribution | https://policies.google.com/privacy |

We are not responsible for the privacy practices of these third parties. Where this Privacy Policy makes statements about them, we have done so in good faith based on their published terms as of the "Last updated" date.

---

## 12. AI-generated content disclosure

Captions and transcripts produced by KineCut are generated by an AI speech-to-text model operated by Groq. AI output may contain errors, mis-transcriptions, or omissions. You are responsible for reviewing and correcting the output before publishing or relying on it for any consequential purpose. KineCut and its publisher are not liable for inaccuracies in AI-generated output.

You are responsible for ensuring that any media you transcribe with KineCut is content you have the legal right to use, and that your use complies with Groq's Acceptable Use Policy (https://console.groq.com/docs/legal/ai-policy). Do not use the app to transcribe content you do not have rights to, to generate harassing or unlawful material, or for any purpose prohibited by Groq's policies or applicable law.

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
