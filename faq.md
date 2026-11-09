---
layout: page
title: FAQ
permalink: /faq/
---

**Who can see the profiles?**
Everyone who can see the request in Jira Service Management. The app reads customers, organizations and requests with each user's own permissions, so people see only what Jira lets them see.

**Does the app need customer and organization details?**
For the detail fields, yes – they are a Jira Service Management feature an administrator sets up. Without them the app still shows names, e-mails, other requests and account health.

**Is customer data sent anywhere or stored by the app?**
No. Everything is read in your browser from your Jira site; exports and imports are created and read there. The app stores only its settings (field names, highlighted values, thresholds).

**What does the import change?**
Only the values of customer and organization detail fields that differ from the file, after you confirm the preview. It never creates or deletes organizations or customers, and you can undo the import.

**Which file formats can I import?**
The Excel (.xlsx) and CSV files of the Export tab, also after editing them in Excel, Google Sheets, LibreOffice or Numbers. CSV can use commas or semicolons. Files up to 10 MB.

**How is account health calculated?**
From the requests of the organization or customer: open ones, those created or resolved in the last 60–90 days, their SLA cycles and satisfaction ratings. See the [user guide]({{ '/guide/#account-health' | relative_url }}). Administrators can change the thresholds.

**How many organizations can it handle?**
The directory loads details only for the page you look at; exports and the health page read 25 organizations per request and show progress. Lists stop at 50 000 organizations and health at 20 000 requests, with a warning.

**Does it work in customer service (CSM) spaces?**
Yes – it reads the *Organizations* field of service spaces and the *Organization* field of customer service spaces.

**Are customers without an organization exported?**
No – Jira offers no way for apps to list them. They do appear on requests they raised.
