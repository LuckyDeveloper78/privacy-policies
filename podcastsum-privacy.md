# Privacy Policy for PodCastSum

**Effective Date: March 14, 2026**

PodCastSum ("we," "our," or "the App") is committed to protecting your privacy. This Privacy Policy explains how we handle your information when you use our podcast summarization application.

## 1. Information We Collect and Process

**Gemini API Key:** You must provide your own Google Gemini API key to generate summaries. This key is stored securely and locally on your device using Android SharedPreferences and is used exclusively to communicate directly with Google's Gemini API. We do not transmit this key to our own servers.

**Podcast Audio and Metadata:** When you submit a podcast URL for summarization, the App downloads the audio file temporarily to your device. This audio file, along with the podcast metadata (title and episode name), is then transmitted to the Google Gemini API to generate the summary.

**User Notes:** You may optionally save personal notes related to specific podcast episodes within the App. These notes are stored locally on your device.

## 2. Data Storage and Telemetry

**Local Storage:** The App utilizes a local database (Room Database) to save your generated podcast summaries, associated metadata (such as episode titles, podcast titles, and URLs), and any personal notes you write. 

**Global Cache:** To increase efficiency and reduce redundant API calls for other users, the generated summaries and associated podcast metadata (URLs, podcast titles, and episode titles) are cached in our Firebase cloud database. 

**Telemetry and Logging:** To improve the application and understand usage patterns, we log user interactions (which podcast URL was summarized, the podcast title, and the episode title) to our Firebase backend. This interaction data is associated with an anonymous, randomly generated Unique Identifier (UUID) that is created when you first use the App. We do not collect identifiable information such as your name, email address, or device identifier.

## 3. Third-Party Services

**Google Gemini API:** The App relies on the Google Gemini API for transcription and summarization. By using the App, your downloaded podcast audio and the API key you provide will be sent to Google's servers. Please refer to Google's Privacy Policy regarding their data handling practices.

## 4. Permissions

To function correctly, the App requests the following permissions:

*   **Internet:** Required to download podcast audio files, scrape podcast metadata, communicate with the Gemini API, and access our Firebase backend.
*   **Access Network State:** Required to verify network connectivity before attempting downloads or API calls.

## 5. Data Security

The security of your locally stored data (including your Gemini API Key, summaries, and notes) depends on your device's security features. We employ standard measures to secure our Firebase backend where the global summary cache and anonymous interaction logs are stored, but remember that no method of transmission over the internet or electronic storage is 100% secure.

## 6. Changes to This Policy

We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page.

## 7. Contact Us

If you have any questions about this Privacy Policy, please contact us at: [Your Contact Email/GitHub Profile]

---
&copy; 2026 PodCastSum
