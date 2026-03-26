# Privacy Policy for KineCut
**Last updated: March 26, 2026**

  This Privacy Policy describes how KineCut ("we", "our", or "the app")
  handles your information when you use our mobile application.

  ---

  ## 1. Information We Collect

  ### 1.1 Media Files
  KineCut accesses video and audio files that you explicitly select from
  your device. These files are used solely to provide the app's core
  features (Kinetic Typography and Auto Captions). We do not copy, store,
  or retain your media files beyond the current session.

  ### 1.2 API Key
  KineCut allows you to enter a Groq API key to enable AI-powered
  transcription. This key is:
  - Stored **locally on your device only**
  - Encrypted using **AES-256 encryption** via Android's
    EncryptedSharedPreferences
  - Never transmitted to us or any third party other than Groq's
    official API endpoint

  ### 1.3 Audio Data for Transcription
  When you use the Auto Captions or Kinetic Typography feature, the audio
  extracted from your selected media file is sent to the
  **Groq API** (groq.com) for transcription. This transmission:
  - Uses **HTTPS (TLS)** encrypted connection
  - Is governed by [Groq's Privacy Policy](https://groq.com/privacy-policy)
  - Is initiated only when you explicitly press the transcribe/generate button

  ---

  ## 2. Information We Do NOT Collect

  - We do **not** collect your name, email, or any personal identifiers
  - We do **not** require account registration
  - We do **not** use analytics or crash reporting SDKs
  - We do **not** serve advertisements
  - We do **not** track your location
  - We do **not** access your contacts, camera, or microphone directly
  - We do **not** have servers — KineCut has no backend of its own

  ---

  ## 3. Data Storage

  All data processed by KineCut (exported videos, caption projects,
  settings) is stored **locally on your device**. We have no access to
  this data. Uninstalling the app removes all locally stored app data.

  ---

  ## 4. Third-Party Services

  KineCut uses the following third-party service:

  | Service | Purpose | Privacy Policy |
  |---|---|---|
  | Groq API | AI speech-to-text transcription | https://groq.com/privacy-policy |

  We are not responsible for the privacy practices of Groq. Please review
  their privacy policy to understand how they handle audio data submitted
  for transcription.

  ---

  ## 5. Permissions

  KineCut requests the following Android permissions:

  | Permission | Reason |
  |---|---|
  | `READ_MEDIA_VIDEO` | Select video files for editing |
  | `READ_MEDIA_AUDIO` | Select audio files for Kinetic Typography |
  | `READ_MEDIA_IMAGES` | Access device storage on older Android versions |
  | `READ_EXTERNAL_STORAGE` | Access media on Android 12 and below |
  | `INTERNET` | Send audio to Groq API for transcription |

  We request only the minimum permissions necessary to provide
  the app's functionality.

  ---

  ## 6. Children's Privacy

  KineCut is not directed at children under the age of 13. We do not
  knowingly collect any personal information from children. If you believe
  a child has provided personal information through our app, please
  contact us and we will take steps to remove it.

  ---

  ## 7. Data Security

  We take data security seriously. Your Groq API key is protected with
  AES-256 encryption on your device. All communications with external
  APIs use HTTPS. Since we operate no backend servers, your data is never
  stored on our systems.

  ---

  ## 8. Your Rights

  Since KineCut stores no personal data on our servers, there is nothing
  for us to access, modify, or delete on your behalf. To remove all
  app data:

  - **Android:** Go to Settings → Apps → KineCut → Storage → Clear Data
  - Or simply **uninstall** the app

  ---

  ## 9. Changes to This Policy

  We may update this Privacy Policy from time to time. Changes will be
  posted on this page with an updated "Last updated" date. Continued use
  of the app after changes constitutes acceptance of the updated policy.

  ---

  ## 10. Contact Us

  If you have any questions about this Privacy Policy, please contact us:

  **Email:** punutype@gmail.com
  **App:** KineCut
  **Package:** com.kinecut.app
