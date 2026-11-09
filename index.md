---
layout: page
title: Overview
permalink: /
---

**Customer Profiles for Jira Service Management** shows agents who they are helping – right on the request – and gives account managers a view of every customer organization: its details, its customers, its requests and its health. Organizations and customers can be exported to Excel and updated in bulk from an edited file.

Jira Service Management lets you add detail fields to customers and organizations (customer and organization details), but agents don't see them on the request, there is no list of organizations you can filter, and you can't export or bulk-edit them. Customer Profiles adds:

- **Customer profile on every request** – the reporter's details (phone, title, region…) and a card for each organization the request is shared with, with the fields you choose and important values highlighted as badges (for example *Customer Segment: Enterprise*).
- **Account health** – for every customer and organization: open requests, new requests in the last 30 days and the trend, SLA breaches in the last 30 days, satisfaction (CSAT) of the last 90 days and the oldest open request, rated **At risk / Watch / Healthy** with the reason. See all organizations on the Account health page, worst first.
- **Other requests** of the same customer and organization, with open and total counts.
- **Organization directory** – search by name, filter by any detail field ("Industry contains Finance", "Website is empty"), open a profile with all details, customers and requests.
- **Export to Excel or CSV** – one row per customer or per organization, with the organization and customer fields you choose and the request counts.
- **Import from Excel or CSV** – edit the exported file and import it back, or create organizations and add customers in bulk. You see every change before anything is written, problems are listed per row, and field changes can be undone.

## Safe by design
- All data is read and written **with the user's own permissions**, in the browser – agents see and change only what Jira lets them.
- The app stores only its settings (which fields to show, highlighted values, health thresholds) – **no customer data**. Exports and imports are processed in the browser.
- The app changes Jira only through the import, after the user confirms the preview: detail field values, and – when chosen – new organizations and customers added to organizations and service projects. It never deletes anything. **Runs on Atlassian.**

## Requirements
Jira Service Management Cloud. Detail fields need *customer and organization details* to be set up on the site (Jira Service Management settings); without them the app shows names, requests and account health.

Start with the [user guide]({{ '/guide/' | relative_url }}).
