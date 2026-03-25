---
tags:
  - FAQ
  - Help
---

# Frequently Asked Questions

Find quick answers to common questions about Power SMPP.

---

## Getting Started

??? question "How do I log in to the user panel?"
    Navigate to your Power SMPP instance URL provided by your administrator. Enter your **Username** and **Password** to access the iText Hub user dashboard.

    If you have forgotten your credentials, contact your system administrator for a password reset. For security, it is recommended to change your password after your first login via **Settings > Change Password**.

??? question "What does the dashboard show?"
    The dashboard (iText Hub) provides a real-time overview of your messaging activity with four key metrics:

    - **SMS Sent Today** — Total SMS messages sent from all interfaces on the current day
    - **Delivered Today** — Total SMS messages successfully delivered on the current day
    - **SMS Sent Yesterday** — Messages sent on the previous day
    - **Delivered Yesterday** — Messages delivered on the previous day

    It also displays interactive traffic monitoring charts for both **MT (Mobile Terminated / outgoing)** and **MO (Mobile Originated / incoming)** messages. From the dashboard, you can quickly access campaign creation, contact management, traffic viewing, report downloads, and profile settings. See [Dashboard](user/dashboard/dashboard.md) for more details.

??? question "How do I change my password?"
    1. Go to **Settings > Change Password**
    2. Enter your **current password** for verification
    3. Enter your **new password** (must meet security requirements set by your admin)
    4. **Confirm** the new password
    5. Click **Save**

    Regular password updates are recommended to maintain account security and align with best practices. Your administrator may also enforce a password change policy requiring periodic updates. See [Change Password](user/settings/changepassword.md).

??? question "How do I update my profile information?"
    Go to **Settings > My Profile** where you can update the following fields:

    - **First Name** — Referenced by your parent account for invoicing
    - **Mobile Number** — Used for account communications and verification
    - **Country Code** — Can be auto-appended to campaign numbers via the "Auto-add country code" option
    - **Email ID** — Used for communications, alerts, OTP, and notification delivery
    - **Country / State** — For billing and reference purposes
    - **Timezone** — Affects all date/time displays across the platform, including campaign scheduling and reports

    Click **Save** after making changes. See [My Profile](user/settings/myprofile.md).

??? question "What timezone does the platform use?"
    The platform uses the timezone configured in your **My Profile** settings. This timezone affects:

    - Dashboard metrics display
    - Campaign scheduling
    - Report date/time stamps
    - Message count reports

    Always verify your timezone is correct before scheduling campaigns to ensure they are sent at the intended time for your recipients.

??? question "What is the difference between MT and MO messages?"
    - **MT (Mobile Terminated)** — Messages sent **to** a mobile handset. These are your outbound/outgoing messages (e.g., campaigns, notifications, OTPs).
    - **MO (Mobile Originated)** — Messages sent **from** a mobile handset. These are inbound/incoming messages received from your recipients (e.g., replies, opt-out requests).

    Both MT and MO traffic are displayed on your dashboard charts.

---

## Sending SMS

??? question "How do I compose and send an SMS campaign?"
    Follow these steps to create and send an SMS campaign:

    1. Click **SMS MT** to open the Compose SMS page
    2. Enter a **Campaign Name** (auto-generated with prefix "Camp_" and date-time, or enter a custom name)
    3. Select a **Sender ID** from the approved list (or enter a dynamic one if "Open Sender ID" is enabled by your admin)
    4. **Add recipients** using one of four methods:
        - **Stored Groups** — Select from pre-created contact groups
        - **Local File** — Upload an Excel/CSV file with phone numbers
        - **Manual Entry** — Type numbers directly (comma-separated with country code, no + symbol)
        - **Copy-Paste** — Paste numbers from another source
    5. **Compose your message** in the text box (or select from drafts/templates)
    6. Optionally enable **Flash SMS** for instant screen display
    7. The system **auto-detects Unicode** if special characters are used
    8. Choose to **Send Now** or **Schedule** for later
    9. Click **Send SMS** — a cost preview is displayed before final confirmation

    !!! tip
        Always test your message content on a few numbers before running large-scale campaigns, as character counters are approximate due to browser/encoding variations.

    See [Compose SMS](user/smsmt/compose.md) for the full guide.

??? question "How do I send personalized SMS from an Excel file?"
    The SMS From Excel feature lets you send personalized messages using data from your spreadsheet:

    1. Open the **SMS From Excel** tab
    2. Download the **sample file** via "View Sample" tab to see the required format
    3. Prepare your Excel file with mobile numbers in one column and personalization data (names, amounts, dates, etc.) in other columns
    4. **Upload** the Excel file — the top 5 rows are displayed for verification
    5. **Select the column** containing mobile numbers
    6. Enter a **Sender ID**
    7. Compose your message and click **"Insert Placeholder"** to add dynamic variables from your spreadsheet columns (e.g., `{name}`, `{amount}`)
    8. Click **Preview** to see the top 5 personalized messages with character counts
    9. Choose to **Schedule** or **Send Now**
    10. Review the **final preview screen** showing country-wise cost breakdown
    11. Click **Send**

    This is ideal for personalized content like appointment reminders, order confirmations, or payment notifications. See [SMS From Excel](user/smsmt/smsfromexcel.md).

??? question "What file formats are supported for contact uploads?"
    Power SMPP supports the following file formats for contact uploads:

    | Format | Extension | Use Case |
    |--------|-----------|----------|
    | Excel | .xls, .xlsx | Most common, supports multiple columns |
    | CSV | .csv | Lightweight, universal compatibility |
    | Text | .txt | Simple number lists |

    **Requirements:**

    - Phone numbers should include the **country code** (e.g., 919909945175, not +919909945175)
    - Do **not** use the `+` symbol before the country code
    - Additional columns can contain personalization data (names, amounts, etc.)
    - The system auto-detects columns after upload

??? question "What is Flash SMS and when should I use it?"
    Flash SMS is a special message type that **appears directly on the recipient's screen immediately** without being stored in their inbox. The message is displayed as a popup overlay on the handset.

    **When to use Flash SMS:**

    - Urgent alerts and emergency notifications
    - Time-sensitive information that requires immediate attention
    - OTP codes that don't need to be saved
    - Critical system notifications

    **How to enable:** Check the **Flash SMS** checkbox while composing your message in the Compose SMS page. Note that Flash SMS behavior may vary depending on the recipient's handset and carrier.

??? question "How does Unicode/special character detection work?"
    Power SMPP **automatically detects** when your message contains Unicode characters. Here's how it works:

    - **GSM 7-bit encoding** (default): Supports standard English letters, numbers, and basic symbols. Limit: **160 characters** per SMS segment.
    - **Unicode encoding** (auto-detected): Activated when non-Latin scripts (Arabic, Hindi, Chinese, etc.), emojis, or special characters are detected. Limit: **70 characters** per SMS segment.

    **Important:** When Unicode is detected, the character counter updates automatically. A single emoji or special character will switch the entire message to Unicode encoding, reducing the available characters per segment.

    !!! warning
        The message and character counters displayed are **indicative only** due to browser and encoding variations. Always test on a small batch before large campaigns.

??? question "What is the character limit per SMS and how does concatenation work?"
    **Character limits per SMS segment:**

    | Encoding | Single SMS | Concatenated SMS (per segment) |
    |----------|-----------|-------------------------------|
    | GSM 7-bit (standard) | 160 characters | 153 characters |
    | Unicode | 70 characters | 67 characters |

    When a message exceeds the single SMS limit, it is automatically split into **concatenated (multi-part) SMS**. Each additional segment uses slightly fewer characters (153 or 67) because some bytes are reserved for the concatenation header that tells the handset how to reassemble the parts.

    **Example:** A 320-character GSM message = 3 SMS segments (153 + 153 + 14 characters). You are billed per segment.

??? question "How do I schedule a campaign for later?"
    1. While composing your SMS (Compose SMS or SMS From Excel), select the **Schedule** option
    2. Choose your desired **date and time**
    3. Select the correct **timezone** (defaults to your profile timezone)
    4. Complete the rest of the campaign setup and click **Send**
    5. The campaign will be queued and sent automatically at the scheduled time

    **Managing scheduled campaigns:**

    - Go to **Report > My Schedules** to view all scheduled campaigns
    - You can **reschedule** a pending campaign by clicking the **Edit** button in the Action tab
    - Always verify the selected timezone matches your intended delivery time

    See [My Schedules](user/report/schedule.md).

??? question "What is the difference between Drafts and Templates?"
    | Feature | Drafts | Templates |
    |---------|--------|-----------|
    | **Editability** | Fully editable — you can modify the entire content | Only placeholders can be modified; static content is locked |
    | **Approval** | No approval required | May require admin approval before use |
    | **Use case** | Saving work-in-progress messages | Reusable, approved message formats |
    | **Compliance** | No compliance enforcement | DLT-compliant (for India) |

    **Drafts** are ideal for saving messages you're still working on. **Templates** are ideal for standardized, pre-approved messages that must maintain consistent formatting.

    !!! warning "API Users"
        When using templates via API, ensure exact spacing, commas, and punctuation match the approved template. Any discrepancy in formatting may result in the template being rejected as invalid.

??? question "Can I add a country code automatically to all numbers?"
    Yes. There are two ways:

    1. **During campaign composition** — Check the **"Auto-add country code"** checkbox when adding recipients. The system will prepend the configured country code to all numbers.
    2. **In your profile** — Go to **Settings > My Profile** and configure your default **Country Code**. This setting is used when the auto-add option is enabled.

    This is useful when your contact list contains local numbers without the country prefix.

---

## Sender ID & Templates

??? question "How do I request a new Sender ID?"
    1. Go to **SMS MT > Manage Sender ID**
    2. Click the **"Add Sender ID"** tab
    3. A configuration popup appears — enter the desired Sender ID details following your admin's guidelines
    4. Click **Save**
    5. The Sender ID enters a **pending approval** state
    6. Your administrator reviews and approves/rejects the request
    7. Once approved, the Sender ID appears in your dropdown when composing campaigns

    You can view the **approval status** of all your Sender IDs in the Manage Sender ID list. If your account has **"Open Sender ID"** enabled by the admin, you can skip this step and type any Sender ID directly when composing. See [Manage Sender ID](user/smsmt/managesenderid.md).

??? question "How do I create and manage message templates?"
    1. Go to **SMS MT > Manage Template**
    2. Click the **"Add Template"** tab
    3. Enter the template name and compose the content
    4. Click **"Insert Placeholder"** to add dynamic variables for personalization (e.g., `{name}`, `{amount}`)
    5. Click **Save** — the template may require admin approval

    **After approval:**

    - **Static content** (everything except placeholders) is locked and cannot be changed
    - Only **placeholder values** can be modified when using the template in campaigns
    - You can view approval status for all templates in the list view

    !!! warning "Important for API Users"
        When sending via API using templates, ensure **exact** spacing, commas, punctuation, and formatting match the approved template. Even a minor discrepancy may cause the template to be treated as invalid and the message may be rejected.

    If your account has **"Open Template"** enabled, you can skip template configuration. See [Manage Template](user/smsmt/managetemplate.md).

??? question "What is DLT and why is template/Sender ID approval required?"
    **DLT (Distributed Ledger Technology)** is a regulatory framework mandated by **TRAI (Telecom Regulatory Authority of India)** for all Application-to-Person (A2P) messaging in India.

    **Key requirements:**

    - All **Sender IDs** must be registered on the DLT platform
    - All **message templates** must be pre-approved on DLT before use
    - Messages that don't match approved templates may be blocked by operators
    - This applies to all commercial and transactional SMS sent in India

    **Why it exists:**

    - Reduces unsolicited commercial communications (spam)
    - Protects consumers from fraudulent messages
    - Creates an auditable trail for all A2P messaging
    - Ensures regulatory compliance for telecom operators

    If you operate outside India, DLT may not apply, but your admin may still enforce template approval for quality control.

??? question "What happens if my Sender ID or template is rejected?"
    If your Sender ID or template is rejected by your administrator:

    - The status will show as **Rejected** in the respective management page
    - You will need to create a **new request** with corrected details
    - Common rejection reasons include: non-compliant content, incorrect formatting, duplicate entries, or policy violations
    - Contact your administrator for specific rejection reasons and guidelines

---

## Contacts

??? question "How do I create and manage contact groups?"
    **Creating a group:**

    1. Go to **Contacts > Manage Groups**
    2. Click **Add Group**
    3. Enter a group name and save

    **Managing existing groups — available actions:**

    | Action | Description |
    |--------|-------------|
    | **Edit Group Name** | Rename an existing group |
    | **Bulk Import Contacts** | Add multiple contacts at once from a file |
    | **Empty Group** | Remove all contacts but keep the group |
    | **Delete Group** | Permanently remove the group and all contacts |

    Groups make it easy to organize recipients and quickly select them when composing campaigns. See [Manage Groups](user/contacts/managegroups.md).

??? question "How do I import contacts?"
    Power SMPP offers **three import methods**:

    **Method 1: Import From a File**

    - Best for large datasets
    - Supports **.xls**, **.csv**, and **.txt** formats
    - Select the target group, upload the file, and confirm

    **Method 2: Copy and Paste**

    - Quick and flexible
    - Copy contacts directly from an Excel sheet or other source
    - Paste into the input area

    **Method 3: Manual Entry**

    - Add contacts one by one
    - Best for small numbers of contacts

    **Steps:**

    1. Select the **target group** from the dropdown
    2. Choose your import method
    3. Add your contacts
    4. Click **Done** to confirm the import

    See [Import Contacts](user/contacts/importcontacts.md).

??? question "How do I export contacts?"
    1. Go to **Contacts > Export Contacts**
    2. Select the **group(s)** you want to export using checkboxes
    3. Click **Export**
    4. Choose your preferred format:
        - **.xls** — Excel format
        - **.csv** — Comma-separated values
        - **.txt** — Plain text
    5. Download the exported file

    !!! tip
        Export only the groups you need for manageable file sizes. Use exports for backup purposes or migrating contacts between systems.

    See [Export Contacts](user/contacts/exportcontacts.md).

---

## Reports

??? question "How do I view campaign reports?"
    Go to **Report > Campaign Report** where you have multiple views:

    **Campaign View:**

    - Consolidated list of all campaigns
    - Shows campaign status, delivery rates, execution dates, and key statistics
    - Click on a campaign to drill down into details

    **List View:**

    - DLR (Delivery Receipt) report with message-level detail
    - Shows individual message delivery status

    **Campaign Status:**

    - Real-time message queue tracking
    - View completed and pending deliveries

    **Actions Tab:**

    - Delivered message count
    - Pending message count
    - Failed message count
    - Other status categories

    Filter by **date range** to find specific campaigns. See [Campaign Report](user/report/campaign.md).

??? question "What do DLR statuses mean?"
    DLR (Delivery Report) statuses indicate the delivery outcome of each message:

    | Status | Meaning | Action |
    |--------|---------|--------|
    | **Delivered** | Message successfully delivered to the recipient's handset | No action needed |
    | **Failed** | Message could not be delivered (invalid number, network issue, blocked, or DND) | Check the number validity; consider removing from list |
    | **Pending** | Message sent to the operator but delivery confirmation not yet received | Wait — status may update; some operators delay DLRs |
    | **Queued** | Message is waiting in the system to be processed and sent | Wait for processing |
    | **Rejected** | Message was rejected by the operator or gateway | Check template compliance, sender ID, or content restrictions |

    !!! tip
        Use the **Message Count** report to get a status-wise summary over a date range, and use **Download Report** for detailed Excel exports.

??? question "How do I view message count reports?"
    1. Go to **Report > Message Count**
    2. Select a **date range** or specific **month**
    3. View message counts broken down by status (Delivered, Pending, Failed, etc.)
    4. Click the **hyperlink** on a month to drill down into a **day-by-day breakdown**

    The report displays counts according to your configured timezone. Use date range and status filters together for targeted traffic analysis. See [Message Count](user/report/messagecount.md).

??? question "How do I download reports in Excel format?"
    1. Go to **Report > Download Report**
    2. View the list of **previously requested reports** (if any)
    3. Click **Request Report** to generate a new report
    4. The report enters **Pending** status while the system fetches the data
    5. Once processing is complete, the status changes to **Ready**
    6. Click the report to **download** in Excel (.xls) format

    Reports include detailed message-level data: recipient number, status, timestamps, cost, sender ID, and more. See [Download Report](user/report/downloadreport.md).

??? question "Can I resend failed messages from a campaign?"
    Yes, but with conditions:

    1. Open the campaign in **Campaign Report**
    2. Go to the **Resend** tab
    3. Select the failed or pending messages to resend

    **Resend eligibility rules:**

    | Scenario | Resend Available? |
    |----------|-------------------|
    | Executed campaign (completed) | Yes |
    | Campaign still in queue | No |
    | Long messages still processing | No |

    !!! tip
        Download the report **before resending** to validate your target list and avoid duplicate deliveries to numbers that may have already received the message.

??? question "How do I stop a running campaign?"
    1. Go to **Report > Campaign Report**
    2. Find the active campaign
    3. Click the **Stop** button

    **Important:**

    - Messages **already sent** cannot be recalled
    - Only **remaining queued messages** will be cancelled
    - This action is immediate and cannot be undone
    - Use this when you discover an error in your campaign content or need to halt delivery urgently

??? question "How do I reschedule a pending campaign?"
    1. Go to **Report > My Schedules**
    2. Find the campaign you want to reschedule
    3. Click the **Edit** button in the Action tab
    4. Select the new **timezone**
    5. Set the new **schedule date and time**
    6. Click **Save**

    Always verify the selected timezone to ensure the campaign sends at the correct local time for your recipients. See [My Schedules](user/report/schedule.md).

---

## WhatsApp

??? question "How do I connect my WhatsApp Business account?"
    **Prerequisites:**

    - A verified **Facebook Business** account
    - A **WhatsApp Business Profile** linked to your Facebook account

    **Steps:**

    1. Navigate to the WhatsApp section
    2. Click **"Connect using Facebook"**
    3. A dialogue box appears — register your Facebook account with iTextPro
    4. Create or link your **WhatsApp Business Profile** (this acts as the bridge between Meta and iTextPro)
    5. Configure WhatsApp messaging settings within iTextPro

    Once connected, you can start creating templates, campaigns, and use Team Inbox for customer support. See [Getting Started](plugins/whatsapp/whatsappuser/overview.md).

??? question "How do I create a WhatsApp campaign?"
    1. Click the **Campaign** button in the WhatsApp section
    2. **Select Sender Name** from the dropdown (defaults to the connector's name)
    3. **Add recipients** using one of three methods:
        - **Manual Entry** — Type mobile numbers directly
        - **Import Contacts** — Upload an Excel/CSV file
        - **Use Existing Groups** — Select pre-created contact groups
    4. Click **"Select Template"** and choose a pre-approved template
    5. **Customize the message:**
        - Modify the header if needed
        - Replace dynamic variables ({{1}}, {{2}}, etc.) with actual values
        - A **real-time preview** appears on the right side
    6. Choose to **Schedule** (check the box and set date/time) or **Send Now**
    7. Click **Send**

    Only **Meta-approved templates** can be used, ensuring regulatory compliance. See [Campaign](plugins/whatsapp/whatsappuser/campaign.md).

??? question "What are WhatsApp template categories and how do I create one?"
    WhatsApp templates are categorized by Meta into three types:

    | Category | Purpose | Examples |
    |----------|---------|---------|
    | **Marketing** | Promotional messages to multiple recipients | Offers, product launches, newsletters |
    | **Utility** | Timely updates related to purchases/customer journey | Order confirmations, shipping updates, appointment reminders |
    | **Authentication** | OTP and verification messages | Login codes, account verification |

    **Creating a template:**

    1. Go to **WhatsApp > Template**
    2. Select the **category** (Marketing, Utility, or Authentication)
    3. Select the **language** (Meta supports multiple languages)
    4. **Add Header** (optional): None, Text, or Media (image, video, document, location)
    5. **Add Body**: Main message content with variables via the Variable button (format: {{1}}, {{2}}, {{3}})
    6. Provide **examples** for each variable (helps Meta understand and approve faster)
    7. **Add Footer** (optional): Brand text or disclaimer
    8. **Add Buttons** (optional):
        - **Opt-Out Button** — Unsubscribe option
        - **CTA Buttons** — Visit Website (up to 2) or Call Phone Number
    9. Click **Save as Draft** (edit later) or **Save and Submit** for Meta approval

    Approval usually takes a **few seconds**. Once approved, you can preview, edit (requires re-approval), delete, or directly launch a campaign from the template. See [Template](plugins/whatsapp/whatsappuser/template.md).

??? question "How do I use Team Inbox for customer support?"
    Team Inbox is a centralized platform for managing WhatsApp conversations:

    **For Admins:**

    - Full visibility into **all chats** (both human agent and chatbot conversations)
    - **Instant takeover** of any ongoing conversation for quick issue resolution
    - Search and filter conversations

    **For Agents:**

    - Unique login credentials for each agent
    - Access limited to **assigned chats** only
    - Respond to customers in real-time

    **Key features:**

    - Centralized monitoring of all WhatsApp interactions in one place
    - Admin takeover capability for escalated issues
    - Secure access with unique logins ensuring privacy and data protection
    - Search and filter for quick conversation lookup

    See [Team Inbox](plugins/whatsapp/whatsappuser/teaminbox.md).

??? question "How do I create and manage agent accounts?"
    Agent accounts provide individual login access for your support team members:

    1. Go to **WhatsApp > Team with Agent Accounts**
    2. Click **Add New Agent**
    3. Fill in the required details
    4. Click **Save** — the agent account is instantly created

    **Benefits of individual agent accounts:**

    - **Enhanced Team Management** — Create specialized groups for different topics or customer segments
    - **Improved Security** — Restrict access to authorized agents only
    - **Increased Accountability** — Monitor individual agent performance and response times
    - **Flexible Shift Scheduling** — Separate accounts for different shifts or time zones

    See [Team Agent](plugins/whatsapp/whatsappuser/teamagent.md).

??? question "How do I set up advanced routing rules for WhatsApp?"
    Advanced routing automatically directs incoming WhatsApp messages to the right agent or chatbot:

    1. Go to **WhatsApp > Advanced Routing Rules**
    2. Click **"Add New Rule"**
    3. Configure the rule with these parameters:

    | Parameter | Description |
    |-----------|-------------|
    | **Rule Name** | Clear, descriptive name for easy identification |
    | **Scope - Connector** | Select the specific webchat connector |
    | **Scope - Time Frame** | Set when the rule is active |
    | **Logic - Payload Type** | Route by content type (text, image, etc.) |
    | **Logic - Payload Text** | Route by specific keywords or phrases |
    | **Logic - Payload Caption** | Route by image/video caption |
    | **Logic - Sender Info** | Route by sender details (name, phone) |
    | **Logical Operators** | Combine conditions with AND/OR logic |
    | **Fulfillment** | Route to a specific **Agent** or **Bot** |

    See [Advanced Routing](plugins/whatsapp/whatsappuser/advancerouting.md) and [Rule Configuration](plugins/whatsapp/whatsappuser/ruleconfiguration.md).

??? question "How do I create automated chatbot flows?"
    1. Go to **WhatsApp > Manage Flow**
    2. Choose: **Use a Pre-built Template** (quick setup) or **Build from Scratch** (fully custom)
    3. Configure the **Bot Trigger** — a specific text/phrase that activates the chatbot
    4. Set the **Retry Mechanism** for failed trigger attempts
    5. Configure **Idle Timeout** for automatic follow-up when the user stops responding

    **Available flow building blocks:**

    | Block | Description |
    |-------|-------------|
    | **Send Message** | Send a text message to the user |
    | **Collect Input** | Display a prompt and capture the user's response in a variable |
    | **Option** | Present up to 3 options (Meta limit) with optional image; flow continues based on selection |
    | **Branch** | Create conditional paths based on previously collected inputs |
    | **Send Attachment** | Send documents, photos, or videos |

    Combine these blocks to create automated conversations that handle FAQs, collect information, qualify leads, and route to human agents when needed. See [Manage Flow](plugins/whatsapp/whatsappuser/manageflow.md).

??? question "How do I monitor WhatsApp communication logs?"
    Go to **WhatsApp > Monitoring** to view detailed transaction records:

    - Every interaction between your application and Meta (WhatsApp) is logged
    - Both **requests** and **responses** are recorded
    - Useful for troubleshooting delivery issues and diagnosing technical problems

    !!! warning
        Monitoring logs are retained for the **last 3 days** only. Check logs promptly if you need to investigate an issue.

    See [Monitoring](plugins/whatsapp/whatsappuser/monitoring.md).

??? question "How do I view WhatsApp campaign reports?"
    Go to **WhatsApp > Reports** for multiple report types:

    **Campaign Report:**

    - **Campaign View** — Overview showing campaign name, sender, content, total messages, status, and cost
    - **List View** — Message-level details including recipient number, template used, submission date, delivery date, status, and error codes

    **Message Count Report:**

    - Quick overview of total messages sent within a selected date range

    **My Schedule:**

    - View all scheduled WhatsApp campaigns with status and message counts

    **Download Report:**

    - Export detailed WhatsApp campaign reports for offline analysis
    - Separate from SMS reports for better organization

    See [Campaign Report](plugins/whatsapp/whatsappuser/reports/campaignreport.md).

---

## Developer API

??? question "How do I access the API documentation?"
    1. Go to **Developer API > API Document**
    2. Click **View API Document**
    3. The system redirects to the **Swagger** interactive API tool
    4. Browse endpoints, view request/response formats, and test API calls directly

    The documentation includes request payload formats, response structures, authentication details, error handling, and integration best practices. See [API Document](user/apidocument/document.md).

??? question "How do I generate API credentials and get started?"
    API access is provisioned by your administrator:

    1. Your admin enables **HTTP API access** for your account
    2. You receive a **Username** and **API Key** for authentication
    3. Go to **Developer API > Developer API** to view your credentials
    4. Click **View API Document** to access the Swagger tool for testing

    Use these credentials in the authorization header of your API requests. The Swagger tool allows you to test all API endpoints interactively before integrating into your application. See [Developer API](user/apidocument/developerapi.md).

??? question "What API endpoints are available?"
    Power SMPP provides comprehensive REST APIs for:

    - **Sending SMS** — Single and bulk message submission
    - **Checking Delivery Status** — Query DLR status for sent messages
    - **Managing Contacts** — Create, update, and delete contacts/groups
    - **Retrieving Reports** — Pull campaign and message reports programmatically

    All endpoints accept standard **HTTP methods** (GET, POST) and return **JSON responses**. The complete endpoint list with parameters, examples, and response codes is available in the [API Document](user/apidocument/document.md).

??? question "Can I integrate Power SMPP with my own application?"
    Yes. Power SMPP supports third-party integration through:

    - **REST API** — Full-featured HTTP API for programmatic access
    - **Webhooks** — Real-time callbacks for DLR and MO notifications
    - **SMPP Protocol** — Direct SMPP v3.4 connectivity for high-volume integrations (configured by admin)

    The Swagger documentation provides request/response examples and best practices for seamless integration. Contact your administrator for SMPP connection details.

---

## Account & Billing

??? question "How do I view my rate plan?"
    Go to **Application Bar > My Rate Plan** to see your current pricing:

    - Prices are displayed per **country** and **network**
    - Rates are set by your parent account/administrator
    - These determine the **cost per message** for each destination
    - Use this to estimate campaign costs before sending

    The cost preview shown during campaign composition uses these rates. See [My Rate Plan](user/applicationbar/rateplan.md).

??? question "What is the difference between Prepaid and Postpaid billing?"
    | Feature | Prepaid | Postpaid |
    |---------|---------|----------|
    | **Balance** | Must have sufficient credits before sending | Billed after consumption |
    | **Credit Check** | System checks balance before processing | No pre-check required |
    | **Overspending** | Not possible — campaign stops when credits run out | Possible — tracked for invoicing |
    | **Use Case** | Most common for end users | Typically for trusted/enterprise accounts |

    Your billing mode is configured by your administrator. Check **Application Bar > My Transactions** to view your current balance and transaction history.

??? question "How do I check my transaction history?"
    Go to **Application Bar > My Transactions** to view:

    - Complete transaction history between your account and parent account
    - Credit additions (top-ups)
    - Credit deductions (campaign costs)
    - Full audit trail for transparency

    This helps you track spending, verify top-ups, and manage your messaging budget. See [My Transactions](user/applicationbar/transaction.md).

??? question "How do I set up webhooks for real-time notifications?"
    Webhooks push real-time DLR and MO notifications to your application:

    1. Go to **Application Bar > WebHooks**
    2. Click **"Add New Webhook"**
    3. Configure the webhook:

    | Field | Description |
    |-------|-------------|
    | **Friendly Name** | A descriptive name for the webhook |
    | **Endpoint Base URL** | Your server's callback URL |
    | **Method** | GET or POST |
    | **Handler** | MO (incoming messages) or DLR (delivery receipts) |

    **Technical requirements:**

    - Your endpoint must return **HTTP 200 OK** within the timeout
    - Default timeout is **10 seconds**
    - If your server doesn't respond in time, the notification may be retried or dropped

    See [WebHooks](user/applicationbar/webhook.md).

??? question "How do I configure notification emails?"
    Go to **Application Bar > Notification Emails** to set up email alerts:

    - By default, notifications are sent to your **registered email** address
    - You can add **additional stakeholder email addresses** to receive alerts
    - Configure which **events** trigger email notifications

    Email notifications are used for account communications, campaign alerts, OTP delivery, and system notifications. See [Notification Email](user/applicationbar/notificationemail.md).

---

## Troubleshooting

??? question "Why are my messages showing as 'Pending' for a long time?"
    Several reasons can cause prolonged pending status:

    - **Operator delays** — Some mobile operators take longer to return delivery confirmations
    - **Recipient phone off** — The message is queued at the operator until the phone is reachable
    - **Network congestion** — High traffic periods may delay DLR processing
    - **Gateway issues** — The upstream gateway may be experiencing delays

    **What to do:** Wait for a reasonable period (varies by country/operator). If messages remain pending after 24-48 hours, they are unlikely to be delivered. Check with your administrator if the issue persists.

??? question "Why was my message rejected or failed?"
    Common reasons for message failure:

    | Reason | Solution |
    |--------|----------|
    | Invalid phone number | Verify the number format includes correct country code |
    | DND/Do Not Disturb | Recipient has opted out of commercial messages |
    | Template mismatch | Ensure message matches the approved template exactly |
    | Sender ID not approved | Use an approved Sender ID or request approval |
    | Insufficient credits | Top up your account balance (prepaid) |
    | Blacklisted number | Check with your administrator |
    | Content blocked | Review message content for restricted keywords |

??? question "Why does my campaign cost differ from what I expected?"
    Campaign costs depend on:

    - **Number of recipients** — Each unique number is charged
    - **Message segments** — Long messages are split into multiple segments, each billed separately
    - **Unicode vs GSM** — Unicode messages have lower character limits, resulting in more segments
    - **Destination rates** — Different countries/networks have different per-message costs
    - **DLR compensation** — Some configurations may adjust costs based on delivery status

    Always check the **cost preview** before confirming a campaign, and review your [Rate Plan](user/applicationbar/rateplan.md) for destination-specific pricing.

??? question "I forgot my password. How do I reset it?"
    Password resets are managed by your **system administrator**. Contact them directly to request a reset. Once reset, log in with the temporary password and immediately change it via **Settings > Change Password**.

    Your admin may also have a self-service password reset option configured — check with them for the specific process.
