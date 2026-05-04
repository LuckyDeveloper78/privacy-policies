# Privacy Policy for InCorporeSano

**Effective Date: May 4, 2026**

InCorporeSano ("we," "our," or "the App") is committed to protecting your privacy. This Privacy Policy explains how we handle your information when you use our training plan, coaching, and fitness application.

## 1. Information We Collect and Process

**User Account Information:** When you create an account, we use third-party authentication services, such as Google Sign-In via Firebase Authentication. We collect your basic profile information (such as name and email address) provided by the identity provider.

**Biometric Data:** To generate accurate training plans tailored to your capabilities, we optionally collect and process fitness-related biometric data that you provide, including:
*   Year of Birth
*   Sex
*   Height
*   Weight

**Training and Performance Data:** We collect information about your training sessions, goals ("Objectives" such as race finishing, pacing targets, or target durations), calendar availability, and calculated athletic indicators (such as VMA and target interval paces).

## 2. Data Storage and Telemetry

**Database Storage:** The App utilizes a cloud database (Firebase Firestore) to securely store your user profile, biometric data, assigned coaches/groups, generated training plans, and recorded training sessions.

**Local Storage:** The App may use local storage on your device for caching interface states, storing offline changes to training plans, and handling user sessions securely.

**Telemetry and Logging:** To improve the application and understand usage patterns, we may log user interactions and error reports (such as authentication or generation failures). 

## 3. Third-Party Services

**Google Firebase:** We use Firebase for hosting our application (`incorporesano.luckydev.be`), secure database storage, User Authentication, and analytics. Please refer to Google's Privacy Policy regarding their data handling practices.

**Strava Integration:** When you choose to synchronize the App with your Strava account, we receive authorization (via OAuth) to access your training activities and performance data from Strava. We use this data strictly to analyze performance, provide feedback on completed sessions, and synchronize your training logs. Please review Strava’s Privacy Policy for more information on how they handle your data.

**AI Plan Generation:** We utilize Generative Artificial Intelligence functions (such as OpenAI/Google APIs) to help generate and parse automated, adaptive running plans based on the parameters and biometric data you provide. Any data sent to these APIs is utilized explicitly for generating training intervals and is securely processed.

## 4. Permissions Request

To function correctly, especially on mobile devices (Android App: `incorporesano.luckydeveloper.com`), the App requests the following permissions:

*   **Internet:** Required to synchronize your profile and training data with our backend, perform OAuth authorization with Strava, and utilize the AI Plan Generator.
*   **Deep Linking/OAuth interception:** Used natively to complete third-party authentication flows seamlessly.

## 5. Data Security

We employ standard security measures to protect your account via Firebase Authentication and secure data stored on our servers. Access to your personal biometric and training profile data is governed by our application's security rules. However, remember that no method of transmission over the internet or electronic storage is 100% secure.

## 6. Changes to This Policy

We may update our Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page.

## 7. Contact Us

If you have any questions about this Privacy Policy, please contact us at our provided contact domain or repository.
