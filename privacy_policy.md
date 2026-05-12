# Privacy Policy

**Last updated: May 12, 2026**

## Introduction

This Privacy Policy describes how Logfin ("we," "our," or the "App") collects, uses, stores, and protects your information when you use our mobile application. We are committed to protecting your privacy and being transparent about how your data is processed.

By using Logfin, you agree to the collection and use of information in accordance with this Privacy Policy.

## About Logfin

Logfin is a personal finance management application designed to help you track income and expenses, manage budgets, and gain insights into your spending habits. The App provides tools for manual transaction entry, automatic transaction detection from supported financial app notifications, AI-assisted text input, and receipt scanning.

## Information We Collect

### 1. Information You Provide Directly

When you register and use the App, we may collect:

- **Account Information:** Name, email address, and profile picture obtained through Google Sign-In authentication. We do not store your Google password.
- **Transaction Data:** Transaction details such as amount, merchant, category, date, notes, transaction type, and transaction items.
- **Budget Information:** Budget limits, categories, and related budget settings.
- **Settings Preferences:** App configuration, language, theme, notification preferences, and auto-detect settings.
- **Feedback Data:** Messages, logs, device/app information, and optional attachments you submit through the feedback feature.

### 2. Information Collected Automatically or With Permission

#### Camera Access

- **Purpose:** To scan receipts or transaction documents for automatic transaction entry.
- **Processing:** Receipt images may be sent securely to our backend and AI services for processing. AI analyzes the image to extract transaction information such as amount, merchant, date, and transaction type.
- **Storage:** Receipt images are not stored permanently in our database. They may temporarily exist during upload, processing, or device/server caching, and are discarded after processing.
- **AI Usage:** Computer vision AI analyzes receipt images only to identify and extract relevant transaction details.
- **Usage Limit:** Free users may scan up to 5 receipts. Additional scan quota may be available in a future paid tier.

#### Notification Access

- **Purpose:** To automatically detect transaction notifications from banking and e-wallet apps selected by you.
- **Scope:** The App only monitors supported banking and e-wallet applications that are explicitly listed and selected by you. The App does not monitor all installed apps.
- **Data Collected:** Notification text may include transaction amount, merchant or recipient name, date, time, and related transaction context.
- **User Control:** You can enable or disable notification reading at any time and select which supported apps to monitor.
- **Data Usage:** Notification data is used to help create transaction records in your expense history.
- **AI Processing:** Notification text may be processed using AI through our backend to extract transaction details because banking and e-wallet notification formats vary significantly.

#### Raw Notification Text and Debugging

Raw notification text may be stored in our database when necessary to support transaction detection, debugging, error analysis, and user-requested support. We use this information to understand whether AI parsing succeeded or failed and to improve the reliability of the auto-detect transaction feature.

We do not sell raw notification text, use it for advertising, or access it for unrelated purposes. Access is limited and used only when needed for support, debugging, service operation, or service improvement.

#### Notification Action Buttons

When you receive a supported transaction notification, Logfin may provide action buttons such as:

1. **Save:** AI extracts transaction details and saves the transaction.
2. **Edit:** AI extracts transaction details and opens an edit screen so you can review and modify the data before saving.

#### Device Information and Installed Apps

- **Installed Applications:** The App checks only for a predefined list of supported banking and e-wallet applications.
- **Purpose:** To display available supported financial apps in the notification settings menu so you can choose which apps to monitor.
- **Limitation:** The App does not request broad visibility of all apps installed on your device. It only checks for specific supported banking and e-wallet package names.

## How We Use Your Information

We use collected information to:

1. Create and manage your account.
2. Record and categorize income and expense transactions.
3. Provide transaction history, financial summaries, and spending insights.
4. Manage budgets and compare your spending against budget limits.
5. Sync data across devices and provide backup/restore functionality.
6. Automatically detect transactions from supported financial app notifications.
7. Process receipt scans and text input using AI to extract transaction information.
8. Provide notification history and auto-detect settings.
9. Improve reliability, debug issues, and respond to support requests.
10. Maintain security, prevent abuse, and operate the App.

Budgets are spending limits you set manually for each category. The App compares your actual expense transactions against those budget limits. Income transactions are not included in budget spending calculations.

## AI and Data Processing

Logfin uses Artificial Intelligence (AI) to simplify transaction data entry and improve accuracy. AI processing is routed through our backend service and may use different AI providers, including Google Gemini, Cerebras, Groq, or other providers we may integrate in the future.

AI is used in three key areas:

### 1. Receipt Scanning

- Receipt images may be sent securely to our backend and AI services for transaction extraction.
- **Data Extracted:** Amount, merchant name, date, transaction type, and other relevant transaction details.
- **Image Storage:** Receipt images are not stored permanently in our database. They may temporarily exist during upload or processing and are discarded after processing.

### 2. Text Input Processing

- When you use text input, AI processes your natural language input to extract transaction details.
- Example: "Lunch at McDonald's 50k" may be converted into a transaction with merchant, category, and amount.
- This helps you add transactions more quickly.

### 3. Notification Data Extraction

- AI processes notification text from supported banking and e-wallet apps you selected.
- AI helps extract transaction data more reliably than fixed pattern matching because notification formats vary significantly.
- Extracted data may include amount, merchant or recipient name, date/time, and transaction type.

### AI Processing Privacy

- AI is used only to extract transaction information and support Logfin features.
- Your data is not sold to third parties or used for advertising.
- We do not intentionally use your personal financial data to train public AI models.
- AI processing is performed through secure backend communication.
- Extracted data is used to create or suggest transaction entries in your account.

## Data Storage and Security

### Hybrid Storage Architecture

Logfin uses a combination of local and server storage.

**Local Storage on Your Device**

- Transaction data cache for offline access
- App settings and preferences
- Temporary data for quick access

**Server Storage**

- Account information such as name, email address, and profile picture
- Transaction history
- Budget configurations and categories
- Notification data needed for transaction detection, debugging, or support
- Feedback and support data you submit

This allows you to access your data across multiple devices, restore data when changing devices, and keep your financial records backed up.

### Security Measures

**Data Transmission**

- Data transmitted between your device and our servers uses SSL/TLS encryption.

**Server Security**

- Our backend database is hosted on PostgreSQL infrastructure.
- We use access controls, authentication protocols, and operational security practices to protect stored data.
- We limit access to user data to what is necessary for operating, debugging, and supporting the App.

**Local Security**

- Authentication tokens are stored using secure storage mechanisms on your device.
- Local app data is stored in the app’s private storage area.

## Permissions Required

### Required Permissions

1. **Internet Access:** Used for authentication, syncing data, AI processing, and communication with our backend.
2. **Camera:** Used to scan receipts for AI-assisted transaction extraction.
3. **Network State:** Used to detect connectivity for syncing and offline behavior.

### Optional Permissions for Auto-Detect Transaction

4. **Notification Access**
   - Used to read transaction notifications from supported banking and e-wallet apps you select.
   - You can grant or revoke this permission at any time.
   - Used exclusively for automatic transaction detection and recording.

5. **Battery Optimization Exemption**
   - Helps keep notification detection reliable.
   - Prevents Android from stopping the listener due to battery optimization.
   - You must manually grant this permission if you choose to use it.

6. **Auto-start Permission on Certain Devices**
   - On some devices from manufacturers such as Xiaomi, OPPO, Vivo, and Realme, the App may guide you to enable Auto-start permission.
   - This helps the notification listener restart if terminated by aggressive battery management.
   - This permission is optional and can be revoked through device settings.

### Important Permission Notes

- Notification monitoring permissions are only needed if you choose to use the auto-detect transaction feature.
- You can use core features such as manual entry, budgeting, and receipt scanning without enabling notification monitoring.
- Logfin does not automatically launch the full app when your device starts.
- You can disable notification monitoring at any time.

## Data Sharing and Third Parties

### We Do Not

- Sell your personal information.
- Share your transaction data with advertisers.
- Provide your data to data brokers.
- Use your financial data for advertising.

### We May Share Data Only When

- **Required by Law:** When necessary to comply with legal obligations.
- **Service Providers:** With trusted providers that help operate the App, such as hosting, database, authentication, AI processing, and email/support services.
- **With Your Consent:** When you explicitly authorize sharing.

### Authentication Services

We use Google Sign-In provided by Google LLC. When you sign in with Google, we receive your name, email address, and profile picture from your Google account. This data is governed by Google's Privacy Policy: https://policies.google.com/privacy.

### AI Providers

AI processing may be performed through providers such as Google Gemini, Cerebras, Groq, or other providers integrated through our backend. Data sent for AI processing is used to provide Logfin features such as receipt scanning, text input parsing, and notification transaction extraction.

## Data Retention

- **Account Data:** Stored for as long as you use the App, or until you request account deletion.
- **Transaction History:** Stored until you delete individual transactions or request account deletion.
- **Notification Data:** Notification text and parsing results may be retained when needed for transaction detection, debugging, support, or error analysis.
- **Categories and Budgets:** When deleted by you, categories and budgets may be deactivated and hidden from active use but retained where needed to preserve transaction history integrity.
- **Receipt Images:** Receipt images are not stored permanently in our database and are discarded after processing.
- **Feedback Data:** Stored as needed to respond to support requests and improve the App.
- **Account Deletion:** When you request account deletion, we will manually delete your account and associated data from our backend database using administrative database operations until an automated deletion feature is available.

## Your Rights and Choices

You have the right to:

1. **Access:** View your stored data in the App.
2. **Modify:** Edit transaction records, budgets, categories, and settings.
3. **Delete Transactions:** Delete individual transactions from your account.
4. **Control Notifications:** Enable or disable notification reading and choose which supported apps to monitor.
5. **Revoke Permissions:** Revoke camera, notification, battery, or auto-start permissions through the App or device settings.
6. **Opt Out:** Disable optional features such as auto-detect transaction.
7. **Request Account Deletion:** In-app account deletion is not yet available. To request deletion of your account and associated data, please contact us at logfin.help@gmail.com or submit a request through the in-app feedback feature. After verifying your request, we will manually delete your account and associated data from our backend database. We plan to provide an automated account deletion feature in a future update.

## Children's Privacy

Logfin is not intended for users under the age of 13. We do not knowingly collect personal information from children under 13. If we discover that we have collected information from a child under 13, we will promptly delete such information.

## International Data Transfers

If you use the App from outside Indonesia, your information may be transferred to, stored, and processed in Indonesia or other locations where our service providers operate. By using the App, you consent to this processing as described in this Privacy Policy.

## Changes to This Privacy Policy

We may update this Privacy Policy from time to time. We will notify users of changes by:

- Posting the updated Privacy Policy on this page
- Updating the "Last updated" date
- Providing in-app notice for significant changes when appropriate

You are advised to review this Privacy Policy periodically.

## Contact Us

If you have questions, concerns, or requests regarding this Privacy Policy or your personal data, please contact us at:

- **Email:** logfin.help@gmail.com
- **Address:** Sukapura, Dayeuhkolot District, Bandung Regency, West Java 40267
- **Support:** In-app feedback feature

## Consent

By using Logfin, you acknowledge that you have read and understood this Privacy Policy and agree to its terms.

---

## Summary of Key Privacy Points

- Logfin helps track income, expenses, budgets, and transaction history.
- Auto-detect transaction is optional and controlled by you.
- Notification access is used only for supported banking and e-wallet apps you select.
- The App checks only a predefined list of supported financial apps, not all installed apps.
- Receipt images are not stored permanently and are discarded after processing.
- Raw notification text may be retained when needed for transaction detection, debugging, support, and error analysis.
- AI processing may use providers such as Gemini, Cerebras, Groq, or other providers through our backend.
- Your data is not sold or used for advertising.
- Authentication tokens are stored securely on your device.
- Account deletion is currently handled manually after user request.
- You can disable optional permissions and features at any time.

---

This Privacy Policy is intended to clearly describe Logfin's privacy practices and support compliance with applicable privacy and platform requirements.
