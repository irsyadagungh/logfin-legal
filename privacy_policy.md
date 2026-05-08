# Privacy Policy

**Last updated: February 15, 2026**

## Introduction

This Privacy Policy describes how Logfin ("we," "our," or "the App") collects, uses, and protects your information when you use our mobile application. We are committed to protecting your privacy and ensuring the security of your personal information.

By using our App, you agree to the collection and use of information in accordance with this Privacy Policy.

## About Logfin

Logfin is a personal finance management application designed to help you track your income and expenses, manage budgets, and gain insights into your spending habits. The App provides tools for manual transaction entry, automatic transaction capture from notifications, and receipt scanning to simplify financial record-keeping.

## Information We Collect

### 1. Information You Provide Directly

When you register and use our App, we collect the following information:

- **Account Information:** Name, email address, and profile picture 
  obtained through Google Sign-In authentication. We do not store 
  your Google password — authentication is handled securely by Google.
- **Transaction Data**: Manually entered transaction details including amount, category, date, and notes
- **Budget Information**: Budget limits and categories you create
- **Settings Preferences**: App configuration and notification preferences

### 2. Information Collected Automatically

#### Camera Access
- **Purpose**: To scan receipts or transaction documents for automatic data entry
- **Data Retention**: Images captured through the camera are **NOT stored** on our servers or your device after processing
- **Processing**: Images are processed in real-time using AI to extract transaction information (amount, merchant, date)
- **AI Usage**: Computer vision AI analyzes the receipt image to identify and extract relevant transaction details
- **Future Consideration**: We may implement image storage in future versions if we identify a beneficial use case, and will update this policy accordingly

#### Notification Access
- **Purpose**: To automatically capture transaction notifications from banking and e-wallet apps you select
- **Scope**: Only reads notifications from apps you explicitly authorize (banking and e-wallet apps only)
- **Data Collected**: Transaction amount, merchant name, date, and time from notification text
- **User Control**: You can enable/disable notification reading at any time and select which specific apps to monitor
- **Data Usage**: Notification data is used solely for recording transactions in your expense history
- **AI Processing**: Notification text is processed using AI to extract transaction details (amount, merchant, date/time) because bank notification formats vary significantly. This is more reliable than traditional pattern matching methods.

**Notification Action Buttons**

When you receive a transaction notification, you can interact with it using action buttons:

1. **Save Button**: Automatically extracts transaction data from the notification using AI and saves it to your transaction history
2. **Edit Button**: Extracts transaction data using AI and opens the edit screen, allowing you to review and modify the details before saving

**Why AI is Used**: 
- Different banks and e-wallets use different notification formats
- AI can accurately extract transaction information regardless of format variations
- Traditional pattern matching (regex) would be complex, fragile, and difficult to maintain across multiple bank formats

**Notification Listener Service Requirements**

To ensure the notification listener works reliably and doesn't stop unexpectedly, the App implements several technical measures:

1. **Background Isolate**: The notification listener runs in a background isolate (separate execution thread) to ensure continuous operation without blocking the main app

2. **Sticky Service**: The notification listener automatically restarts if stopped by the system, ensuring continuous monitoring of your selected banking/e-wallet notifications

3. **Service Binding**: The App binds the notification listener service to keep it active and prevent the Android system from terminating it during memory cleanup

4. **Auto-restart on Termination**: If the Android system stops the notification listener service (due to memory pressure or other reasons), it will automatically restart itself - this is NOT the same as launching at boot

5. **Battery Optimization Exemption**: Prevents the system from stopping the notification listener to save battery, ensuring consistent transaction capture

**Important Clarifications**:
- **NO Boot Launch**: The App does NOT automatically launch when your device boots up or restarts
- **Auto-restart**: The service only restarts automatically if Android terminates it while the app is already running
- **NO Foreground Service**: We use background isolate technology instead of foreground services, so you won't see a persistent notification about the service running
- **User Control**: The notification listener only runs when you have explicitly enabled notification monitoring in the app settings

**Your Control**: 
- You can disable the notification listener feature at any time
- Disabling it will stop all automatic notification reading
- The service will only run if you have enabled notification monitoring in settings

#### Device Information
- **Installed Applications**: The App reads your installed applications list only to identify banking and e-wallet apps available for notification monitoring
- **Purpose**: To display available banking/e-wallet apps in the notification settings menu
- **Limitation**: We only detect and display banking and e-wallet applications

## How We Use Your Information

We use the collected information for the following purposes:

1. **Account Management**: To create and manage your user account across devices
2. **Income & Expense Tracking**: To record, categorize, and display your income and expense transactions
3. **Budget Management**: To help you set budget limits for different categories and monitor your spending against those budgets
4. **Financial Analytics**: To provide spending statistics, income vs. expense analysis, and financial insights
5. **Data Synchronization**: To sync your financial data across multiple devices using our secure servers
6. **Notification Processing**: To automatically capture and record transaction data from authorized banking/e-wallet app notifications
7. **App Functionality**: To provide core features including transaction history, category management, budget tracking, and settings customization

**Important Note**: Budgets are spending limits you set manually for each category. The App then compares your actual expense transactions in that category against your budget limit to show you how much you've spent versus your budget. Budget limits themselves are set by you, but the spending calculations use your expense transaction history filtered by category. Income transactions are not included in budget calculations.

## Data Storage and Security

### Hybrid Storage Architecture
Logfin uses a combination of local and server storage to provide you with the best experience:

**Local Storage (On Your Device)**
- Transaction data cache for offline access
- App settings and preferences
- Temporary data for quick access

**Server Storage (Cloud)**
- Your account information (name, email, encrypted password)
- Transaction history (income and expense records)
- Budget configurations and categories
- This allows you to:
  - Access your data across multiple devices
  - Restore your data if you change devices
  - Keep your financial records securely backed up

### Security Measures
We implement comprehensive security measures for both local and server storage:

**Data Encryption**
- All data transmitted between your device and our servers uses SSL/TLS encryption
- Passwords are hashed using industry-standard algorithms (never stored in plain text)
- Sensitive financial data is encrypted both in transit and at rest on our servers

**Server Security**
- Secure, encrypted database storage
- Regular security audits and updates
- Access controls and authentication protocols
- Data backup and disaster recovery systems

**Local Security**
- Encrypted local storage on your device
- Secure data caching mechanisms
- Automatic data synchronization with server

## Permissions Required

The App requires the following permissions:

### Required Permissions

1. **Internet Access**: For syncing your data with our secure servers and user authentication
2. **Camera**: To scan receipts for transaction data extraction with AI (images are not saved)
3. **Network State**: To detect internet connectivity for data synchronization

### Optional Permissions (For Notification Monitoring Feature)

4. **Notification Access**: To read transaction notifications from selected banking/e-wallet apps
   - You can grant or revoke this permission at any time
   - You control which apps' notifications are read
   - Used exclusively for automatic transaction recording
   - Notification text is processed by AI to extract transaction details

5. **Battery Optimization Exemption**: 
   - Ensures notification listener service runs continuously in the background
   - Prevents Android from stopping the service to save battery
   - Required for reliable automatic transaction capture
   - **User Action Required**: You'll be guided to manually exempt Logfin from battery optimization in device settings

**Important Notes**:
- Permissions 4-5 are ONLY needed if you choose to use the automatic notification monitoring feature
- You can use Logfin's core features (manual entry, receipt scanning, budgeting, text input with AI) without granting these permissions
- **No Boot Launch**: Logfin does NOT automatically launch when your device starts or reboots
- **Auto-restart**: The notification listener only auto-restarts if Android terminates it while the app is running (not at boot)
- **Background Processing**: We use background isolate technology instead of foreground services, so there's no persistent notification
- The notification listener service configurations (sticky service, binding, background isolate) are technical implementations that enhance reliability and don't require separate user permissions beyond those listed above

## Data Sharing and Third Parties

### We Do NOT:
- Sell your personal information to third parties
- Share your transaction data with advertisers
- Provide your data to data brokers
- Use your data for purposes other than providing App functionality

### We MAY Share Data Only When:
- **Required by Law**: When we have a good-faith belief that disclosure is necessary to comply with legal obligations
- **Service Providers**: With trusted third-party service providers who assist in operating our App (e.g., cloud hosting providers), under strict confidentiality agreements
- **With Your Consent**: When you explicitly authorize us to share specific information

### Authentication Services

We use Google Sign-In (provided by Google LLC) for user authentication. 
When you sign in with Google, we receive your name, email address, and 
profile picture from your Google account. This data is governed by 
Google's Privacy Policy (https://policies.google.com/privacy).

## AI and Data Processing

Logfin uses Artificial Intelligence (AI) to simplify transaction data entry and improve accuracy. AI is used in three key areas:

### 1. Receipt Scanning (Camera)
- When you scan a receipt with your camera, AI analyzes the image to extract transaction information
- **Data Extracted**: Amount, merchant name, date, transaction type
- **Image Storage**: Images are NOT stored - they are processed in real-time and immediately discarded after extraction
- **Processing**: May occur on-device or through secure AI services depending on the feature

### 2. Text Input Processing
- When you use the text input feature to add transactions, AI processes your natural language input
- **Example**: "Lunch at McDonald's 50k" → AI extracts: Category: Food, Merchant: McDonald's, Amount: 50,000
- **Purpose**: Allows you to quickly add transactions using conversational language instead of filling out forms

### 3. Notification Data Extraction
- AI processes notification text from your authorized banking/e-wallet apps
- **Why AI**: Bank notification formats vary significantly (different structures, languages, abbreviations)
- **Traditional methods** (regex/pattern matching) would be extremely complex and unreliable
- **AI advantage**: Accurately extracts transaction data regardless of bank-specific formatting
- **Data Extracted**: Transaction amount, merchant/recipient name, transaction date/time, transaction type
- **Triggered by**: 
  - Save button on notification: AI extracts data and saves automatically
  - Edit button on notification: AI extracts data and opens edit screen for your review

### AI Processing Privacy
- AI processing is used ONLY for extracting transaction information from the three sources above
- Your transaction descriptions and data are NOT used to train AI models
- We do not share your data with third-party AI services for training purposes
- AI processing is performed securely with data encryption
- Extracted data is only used to create transaction entries in your account

## Your Rights and Choices

You have the following rights regarding your data:

1. **Access**: View all your stored data within the App
2. **Modification**: Edit or update your transaction records, budgets, and account information
3. **Deletion**: Delete individual transactions or your entire account
4. **Export**: Export your transaction history and data
5. **Notification Control**: 
   - Enable or disable notification reading at any time
   - Select which apps' notifications to monitor
   - Revoke notification access permission entirely
6. **Opt-out**: Disable any optional features or data collection

## Data Retention

- **Account Data**: Stored on our servers until you delete your account
- **Transaction History**: Stored on our servers and synced to your device; retained until you manually delete entries or your account
- **Budget Data**: Stored on our servers until you delete them or your account
- **Camera Images**: Not stored anywhere - processed in real-time and immediately discarded after extracting transaction information
- **Notification Data**: Converted to transaction records and stored as part of your transaction history
- **Deleted Data**: When you delete transactions, budgets, or your account:
  - Removed from our servers within 30 days
  - May remain in encrypted backups for up to 90 days for disaster recovery purposes
  - Permanently and irrecoverably deleted after backup retention period

## Children's Privacy

Our App is not intended for users under the age of 13. We do not knowingly collect personal information from children under 13. If we discover that we have collected information from a child under 13, we will promptly delete such information.

## Changes to This Privacy Policy

We may update our Privacy Policy from time to time. We will notify you of any changes by:
- Posting the new Privacy Policy on this page
- Updating the "Last updated" date
- Sending an in-app notification for significant changes

You are advised to review this Privacy Policy periodically for any changes. Changes are effective when posted.

## International Data Transfers

If you use our App from outside Indonesia, please be aware that your information may be transferred to, stored, and processed in Indonesia where our servers are located. By using the App, you consent to this transfer.

## Contact Us

If you have any questions, concerns, or requests regarding this Privacy Policy or your personal data, please contact us at:

- **Email**: logfin.help@gmail.com
- **Address**: Sukapura, Dayeuhkolot District, Bandung Regency, West Java 40267
- **Support**: In-app support feedback feature

## Consent

By using our App, you acknowledge that you have read and understood this Privacy Policy and agree to its terms and conditions.

---

## Summary of Key Privacy Points

✓ Logfin tracks your income and expenses with budgeting tools  
✓ Budgets compare your expense spending against limits you set per category  
✓ Data is stored both locally (for offline access) and on secure servers (for sync and backup)  
✓ AI is used to extract transaction data from: receipt images, text input, and bank notifications  
✓ Scanned receipt images are NOT saved - only processed by AI for data extraction  
✓ You control which banking/e-wallet apps' notifications are monitored  
✓ Notification text is processed by AI (not regex) to handle varying bank formats  
✓ Save/Edit buttons on notifications trigger AI extraction of transaction details  
✓ Notification listener uses background isolate (not foreground service - no persistent notification)  
✓ Service auto-restarts only if terminated by Android (NOT at boot/startup)  
✓ App does NOT automatically launch when device boots  
✓ We do NOT sell or share your personal data with third parties  
✓ Your data is NOT used to train AI models  
✓ You can delete your data at any time  
✓ All data is encrypted in transit and at rest  
✓ You have full control over permissions and features  

---

*This Privacy Policy is compliant with Google Play Store requirements, GDPR principles, and general privacy best practices.*

---
