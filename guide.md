---
layout: page
title: User guide
permalink: /guide/
---

## Set up detail fields
Customer Profiles shows the native **customer and organization details** of Jira Service Management. A Jira administrator adds the fields (for example *Industry*, *Customer Segment*, *Phone*, *Region*) in Jira Service Management settings and agents fill them in on the customer or organization page – or in bulk with the [import](#import-from-excel-or-csv).

## The customer profile on a request
Every request has a **Customer profile** panel on the right, below the request details – expand it to see the profile. For a wider view, choose the *Apps* button below the request summary and select *Customer profile*: the panel is then shown below the description of that request.

- **Customer** – the reporter's name, e-mail and detail fields.
- **Organization** – one card for each organization the request is shared with, and *Open profile* to see the whole organization.
- **Badges** – values your administrator chose to highlight, for example *Customer Segment: Enterprise* or *Support plan: Premium*.
- **Account health** – *At risk*, *Watch* or *Healthy*, the reason, and the numbers behind it (see [account health](#account-health)).
- **Other requests** – the latest requests of the same customer and organization, with open and total counts and a link to all of them in Jira's search.

## Organizations
Open **Apps › Customer Profiles** in Jira.

- Search by name, or filter by a detail field: choose the field, *contains* or *is empty*, and the value (the field's options are suggested).
- The first three chosen fields are shown as columns; click an organization to open its **profile**: all detail fields, the customers (with their details on request), account health and the latest requests. The address of a profile can be bookmarked or shared.

## Account health
The **Account health** tab rates every organization from its requests:

| Measure | What counts |
|---|---|
| Open | Requests not in a *Done* status |
| New in 30 days | Requests created in the last 30 days, and the change against the 30 days before |
| SLA breaches in 30 days | SLA goals (any SLA, such as *Time to resolution*) breached in the last 30 days |
| CSAT | Average satisfaction rating (1–5) of the last 90 days and how many ratings |
| Oldest open | Days since the oldest open request was created |

By default an organization is **At risk** with 3 or more SLA breaches in 30 days or CSAT below 3, and to **Watch** with 1 breach, CSAT below 4, an open request older than 14 days, or 50 % more new requests than before (with at least 5 new requests). Administrators can change these thresholds. Click a column to sort, choose which organizations to show, and download the table to Excel or CSV.

## Export
On the **Export** tab choose:
1. **Rows** – one row per customer (organizations without customers get an empty row) or one row per organization with the number of customers.
2. **Columns** – organization fields, customer fields and the open and total requests of each organization.
3. **Organizations** – all, or by name and detail field value.
4. **Format** – Excel (.xlsx, with a bold header, a frozen first row and filters) or CSV (UTF-8).

Organizations or customers you can't see are skipped and listed in a message.

## Import from Excel or CSV
1. Export the organizations or customers with the fields you want to change.
2. Edit the values in Excel (or any spreadsheet). Keep the **Organization ID** column (or the organization name, if names are unique) and, for customer fields, the **E-mail** column. Columns are named like the export: *Organization: Industry*, *Customer: Phone*. Other columns are ignored.
3. On the **Import** tab choose the file and **Check the file**. The preview lists every change (now → new, and the rows of the file) and the problems per row – an organization that doesn't exist, a value that isn't an option of a select field, a customer who isn't in the organization, or different values for the same field in repeated rows.
4. **Apply** writes the changes with your permissions; each change gets ✓ or ✗. **Undo this import** puts the previous values back (until you leave the page), and **Download the change log** saves a CSV of what changed.

Empty cells leave the value as it is. Tick *Empty cells clear the value* to clear fields with empty cells. Multi-select values are separated by commas, as in the export. The import changes detail field values only; it never creates or deletes organizations or customers.

## Settings (Jira administrators)
On the **Request panel settings** tab:
- **Customer fields** and **organization fields** shown on requests and their order (or all fields, in the order set in Jira).
- **Highlighted values** – a field and a value, shown as a badge.
- **Account health** – on or off, and the thresholds.
- **Other requests** on or off.
- Whether only Jira administrators can **export** and **import**. (This hides the tabs for others; agents can still see and edit the same data in Jira.)
