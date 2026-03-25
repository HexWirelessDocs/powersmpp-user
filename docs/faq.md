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
    Navigate to your Power SMPP instance URL provided by your administrator. Enter your **Username** and **Password** to access the user dashboard. If you have forgotten your credentials, contact your system administrator for a reset.

??? question "What does the dashboard show?"
    The dashboard (iText Hub) provides a real-time overview of your messaging activity, including **SMS Sent Today**, **Delivered Today**, **SMS Sent Yesterday**, and **Delivered Yesterday**. It also displays traffic monitoring charts for both MT (outgoing) and MO (incoming) messages. See [Dashboard](user/dashboard/dashboard.md) for more details.

??? question "How do I change my password?"
    Go to **Settings > Change Password**. Enter your current password, then type and confirm your new password. Click **Save** to update. Regular password changes are recommended for security. See [Change Password](user/settings/changepassword.md).

---

## Sending SMS

??? question "How do I compose and send an SMS campaign?"
    Go to **SMS MT > Compose SMS**. Enter a campaign name, select a Sender ID, add recipients (from groups, file upload, or manual entry), compose your message, and click **Send**. You can also preview the cost before sending. See [Compose SMS](user/smsmt/compose.md).

??? question "How do I send SMS from an Excel file?"
    Go to **SMS MT > SMS From Excel**. Upload an Excel (.xls/.xlsx) or CSV file containing phone numbers and optional message variables. Map the columns to the required fields, compose your message with placeholders, and send. See [SMS From Excel](user/smsmt/smsfromexcel.md).

??? question "What contact formats are supported for upload?"
    Power SMPP supports **Excel (.xls, .xlsx)** and **CSV** file formats for contact uploads. The file should contain phone numbers in international format (with country code). Additional columns can be used for personalized message variables.

??? question "What is Flash SMS?"
    Flash SMS is a special type of message that appears directly on the recipient's screen without being stored in the inbox. It is useful for urgent notifications. You can enable this option while composing an SMS by selecting the **Flash SMS** checkbox.

??? question "How does Unicode/special character detection work?"
    Power SMPP automatically detects when your message contains Unicode characters (e.g., non-Latin scripts, emojis). When Unicode is detected, the system switches to Unicode encoding, which reduces the character limit per SMS segment from 160 to 70 characters.

??? question "What is the character limit per SMS?"
    For standard GSM characters (English letters, numbers, basic symbols), the limit is **160 characters** per SMS. For Unicode messages (non-Latin scripts, special characters), the limit is **70 characters** per SMS. Messages exceeding these limits are split into multiple segments (concatenated SMS).

??? question "How do I schedule a campaign for later?"
    While composing your SMS, select the **Schedule** option instead of sending immediately. Choose your desired date, time, and timezone. The campaign will be queued and sent automatically at the scheduled time. You can manage scheduled campaigns from [My Schedules](user/report/schedule.md).

---

## Sender ID & Templates

??? question "How do I request a new Sender ID?"
    Go to **SMS MT > Manage Sender ID** and click **Add New**. Enter the desired Sender ID (alphanumeric or numeric) and submit the request. Your administrator will review and approve it. Once approved, the Sender ID becomes available for use in campaigns. See [Manage Sender ID](user/smsmt/managesenderid.md).

??? question "How do I create and manage message templates?"
    Go to **SMS MT > Manage Template**. Click **Add Template**, provide a name, and compose the template content. You can include dynamic placeholders for personalization. Templates must be approved before use. See [Manage Template](user/smsmt/managetemplate.md).

??? question "What is DLT and why is template approval required?"
    DLT (Distributed Ledger Technology) is a regulatory framework mandated by TRAI (Telecom Regulatory Authority of India) for A2P messaging. All Sender IDs and message templates must be registered and approved on the DLT platform before they can be used for sending SMS in India. This ensures compliance and reduces spam.

---

## Contacts

??? question "How do I create contact groups?"
    Go to **Contacts > Manage Groups**. Click **Add Group**, enter a group name, and save. You can then add contacts to the group manually or via file import. Groups make it easy to send campaigns to predefined sets of recipients. See [Manage Groups](user/contacts/managegroups.md).

??? question "How do I import/export contacts?"
    To **import**, go to **Contacts > Import Contacts**, upload an Excel/CSV file, map columns, and select the target group. To **export**, go to **Contacts > Export Contacts**, select the group, and download. See [Import Contacts](user/contacts/importcontacts.md) and [Export Contacts](user/contacts/exportcontacts.md).

---

## Reports

??? question "How do I view campaign reports?"
    Go to **Report > Campaign Report**. You can switch between **Campaign View** (summary per campaign) and **List View** (individual message DLR details). Filter by date range to find specific campaigns. See [Campaign Report](user/report/campaign.md).

??? question "What do DLR statuses mean (Delivered, Failed, Pending)?"
    - **Delivered**: The message was successfully delivered to the recipient's handset.
    - **Failed**: The message could not be delivered (invalid number, network issue, or blocked).
    - **Pending**: The message has been sent but a delivery confirmation has not yet been received from the operator.
    - **Queued**: The message is waiting to be processed and sent.

??? question "How do I download reports in Excel format?"
    Go to **Report > Download Report**. Select the date range and report type, then click **Download**. Reports are exported in Excel (.xls) format with detailed message-level data including status, timestamps, and costs. See [Download Report](user/report/downloadreport.md).

??? question "Can I resend failed messages?"
    Yes. Open the campaign in **Campaign Report**, go to the **Resend** tab, and select the failed or pending messages to resend. Note: resending is only available for executed campaigns, not those still in queue.

??? question "How do I stop a running campaign?"
    In **Campaign Report**, find the active campaign and click the **Stop** button. This will halt the campaign immediately. Messages already sent cannot be recalled, but remaining queued messages will be cancelled.

---

## WhatsApp

??? question "How do I connect my WhatsApp Business account?"
    You need a verified Facebook Business account linked to a WhatsApp Business Profile. Your administrator will configure the WhatsApp connector in Power SMPP. Once connected, you can start sending campaigns. See [Getting Started](plugins/whatsapp/whatsappuser/overview.md).

??? question "How do I create a WhatsApp campaign?"
    Go to **WhatsApp > Campaign**. Select a sender name, add recipients (manual entry, Excel/CSV upload, or existing groups), choose a pre-approved template, customize dynamic variables (e.g., {{1}}), and send or schedule. See [Campaign](plugins/whatsapp/whatsappuser/campaign.md).

??? question "What are WhatsApp message templates and why do they need approval?"
    WhatsApp message templates are pre-defined message formats required by Meta (Facebook) for business-initiated conversations. Templates must be submitted for approval to ensure they comply with WhatsApp's commerce and business policies. Only approved templates can be used in campaigns. See [Template](plugins/whatsapp/whatsappuser/template.md).

??? question "How do I use Team Inbox for customer support?"
    Team Inbox allows your support agents to manage WhatsApp conversations in real-time. Agents can view incoming messages, respond to customers, and transfer conversations between team members. See [Team Inbox](plugins/whatsapp/whatsappuser/teaminbox.md).

??? question "How do I set up advanced routing rules?"
    Go to **WhatsApp > Advanced Routing Rules** to define how incoming messages are routed to specific agents or teams based on keywords, message content, or other criteria. See [Advanced Routing](plugins/whatsapp/whatsappuser/advancerouting.md).

??? question "How do I manage WhatsApp flows?"
    Go to **WhatsApp > Manage Flow** to create automated conversation flows using a visual builder. Flows can handle common queries, collect information, and route conversations to human agents when needed. See [Manage Flow](plugins/whatsapp/whatsappuser/manageflow.md).

---

## Developer API

??? question "How do I access the API documentation?"
    Go to **Developer API > API Document** to view the complete API reference with endpoints, parameters, and example requests. See [API Document](user/apidocument/document.md).

??? question "How do I generate API credentials?"
    API credentials are provisioned by your administrator when enabling HTTP API access for your account. Once enabled, you will receive a **Username** and **API Key** to authenticate your API requests. See [Developer API](user/apidocument/developerapi.md).

??? question "What API endpoints are available?"
    Power SMPP provides REST APIs for sending SMS, checking delivery status, managing contacts, and retrieving reports. All endpoints accept standard HTTP methods and return JSON responses. Refer to the [API Document](user/apidocument/document.md) for the full endpoint list.

---

## Account & Billing

??? question "How do I view my rate plan?"
    Go to **Application Bar > My Rate Plan** to see your current pricing per country and network. Rate plans are configured by your administrator and determine the cost per message for each destination. See [My Rate Plan](user/applicationbar/rateplan.md).

??? question "How do I check my transaction history?"
    Go to **Application Bar > My Transactions** to view your credit usage, top-ups, and deductions. You can filter by date range to find specific transactions. See [My Transactions](user/applicationbar/transaction.md).

??? question "How do I set up webhooks for real-time notifications?"
    Go to **Application Bar > WebHooks** to configure HTTP callback URLs. Webhooks allow you to receive real-time DLR status updates and MO (incoming message) notifications directly to your application. See [WebHooks](user/applicationbar/webhook.md).
