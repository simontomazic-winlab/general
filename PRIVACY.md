# Privacy Policy — Suspicious Email Reporter

_Last updated: September 2026_

**Suspicious Email Reporter** ("the add-on") is an internal Google Workspace add-on used within your organization to help employees identify potential phishing emails inside Gmail and report them to the security team. This policy explains what the add-on accesses and how that information is handled.

## Who this applies to

The add-on is a private, internal tool available only to users within your organization. It is not offered to the public.

## What the add-on accesses

When you open an email in Gmail, the add-on reads **only the message you currently have open** in order to run its automated checks. This includes the message headers, body, links, and attachment names. It uses this to display a risk assessment in the sidebar.

The add-on requests the following Google account permissions (OAuth scopes), each used solely for the purpose stated:

- **View your email messages and settings** (`gmail.readonly`) — to read the open message and its headers for analysis.
- **Send email as you** (`gmail.send`) — only when you click "Report to Security," to forward the reported message to the security mailbox.
- **Run as a Gmail add-on** (`gmail.addons.execute`) — to display the sidebar.
- **View your email address** (`userinfo.email`) — to record who submitted a report.
- **Connect to an external service** (`script.external_request`) — to perform the checks described below.

## How your information is used

- **On-device analysis:** Almost all checks run within Google Apps Script (Google's own infrastructure) and do not send your email anywhere.
- **Reporting:** When you click "Report to Security," the complete original message is emailed as an attachment to the **Security Team** for investigation, along with your address and an automated summary. This happens only when you choose to report.
- **Domain-age check:** The sender's domain name (not your email content) is sent to the public **RDAP** service (rdap.org) to check how recently the domain was registered.
- **Optional AI analysis (only if enabled by your administrator):** If the "Analyze with AI" feature is turned on, the sender, subject, detected signals, and a portion of the message body are sent to Google's **Gemini API** to produce an assessment. This runs only when a user clicks the button or files a report.
- **Optional link reputation (only if enabled by your administrator):** If configured, message links may be checked against Google **Safe Browsing**.

## Data retention

The add-on does not operate its own database. It temporarily caches non-sensitive lookup results (a sender's domain age and whether a sender is new to you) for up to about six hours using Google Apps Script's cache, purely to avoid repeated lookups. Reported messages are delivered to the security mailbox and retained there according to your organization's normal email retention practices.

## Data sharing

Your information is **not sold or shared** with third parties. Data leaves Google's environment only for the specific, limited checks listed above (RDAP, and — if enabled — the Gemini API and Safe Browsing), and only as needed to perform those checks.

## Your choices

Automated network checks (domain age) and AI analysis can be disabled by your administrator. Reporting is always user-initiated.

## Contact

Questions about this add-on or this policy: contact your **Security Team**.
