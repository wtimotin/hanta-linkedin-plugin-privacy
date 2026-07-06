# Hanta LinkedIn Plugin — Privacy Policy

**Effective date:** 6 July 2026  
**Extension:** Hanta LinkedIn Plugin, a Google Chrome extension using Manifest V3  
**Provider / data controller:** t-next GmbH, operator of Hanta ("Hanta", "we", "us")  
**Privacy contact:** info@t-next.de  
**Support:** https://hanta.atlassian.net/servicedesk/customer/portals

This policy covers the **Hanta LinkedIn Plugin browser extension only**. It explains what the extension reads from LinkedIn, what is stored locally in Chrome, and what is sent to Hanta when an authorized user saves data to Hanta CRM.

## Who this extension is for

The extension is intended for authorized Hanta users who want to capture LinkedIn profile and company information into their own Hanta CRM account. A Hanta account or Hanta API key is required for saving data to Hanta.

## What data the extension processes

The extension runs on LinkedIn pages and reads data from pages you actively view or explicitly capture. Depending on what LinkedIn makes visible to you, the extension may process:

### Person / profile data

- full name, first name, last name;
- LinkedIn profile URL and public identifier;
- headline, current position, current company, location;
- profile photo URL and, when saved, a base64 copy of the photo;
- about / summary text;
- experience entries, education entries, skills, top skills and languages;
- connection degree and mutual connections;
- contact information visible to you, such as email address, phone number, websites and structured contact-info entries;
- selected Hanta contact role, such as Contact, Candidate, Contact & Candidate, or Employee.

### Company data

- company name, official name and LinkedIn company URL;
- logo URL and, when saved, a base64 copy of the logo;
- tagline, description, website, industry, employee count, employee range and founded date;
- specialities, headquarters address and phone number when visible.

### Messaging data

If the user explicitly runs a messaging or chat capture feature, the extension may read the visible LinkedIn message thread, including message text, sender information and timestamps, so that the user can save the relevant conversation context to Hanta. The extension does not continuously monitor messages.

The extension does not read non-LinkedIn websites.

## Authentication data

To connect to Hanta, the extension may store a Hanta API key or OAuth token in Chrome extension storage (`chrome.storage.local`) on your device. This credential is used only to authorize requests to Hanta. It is not shared with LinkedIn and is not used for advertising.

## When data is sent to Hanta

The extension first extracts LinkedIn data locally in your browser and displays it in the Chrome side panel.

Data is sent to Hanta only in these cases:

- **Save or update:** when you click a save/update action, the selected profile or company data is sent to the Hanta backend at `https://supa.hanta.io/functions/v1`.
- **Presence check:** after you connect a valid Hanta API key, the extension may send only LinkedIn identifiers, such as profile URL, public identifier or company URL, to check whether the contact or company already exists in Hanta. The full captured record is not sent for this check.
- **Connected CRM integrations:** if your Hanta account is configured to forward saved records to a CRM integration, such as HubSpot, Hanta may transmit the saved record to that connected destination on your behalf.

Without a valid Hanta connection, the extension cannot save captured records to Hanta.

## Why we process this data

We process the data solely to provide the extension's core purpose:

- capture LinkedIn profile and company information into Hanta CRM;
- update existing Hanta CRM records;
- show whether a LinkedIn contact or company already exists in Hanta;
- support user-triggered CRM workflows and connected CRM integrations.

## What we do not do

We do not sell extension data.  
We do not use extension data for advertising or ad targeting.  
We do not use extension data to determine creditworthiness or for lending.  
We do not execute remote code in the extension.  
We do not use the extension to read non-LinkedIn websites.  

## Chrome Web Store Limited Use

The extension's use and transfer of user data is limited to providing and improving the Hanta LinkedIn Plugin's user-facing CRM capture functionality. We do not transfer user data to third parties except as necessary to provide the service, comply with law, protect against security threats, or when the user has connected a CRM integration through Hanta.

## Local storage and retention

The extension may store the following locally in Chrome extension storage:

- Hanta API key or OAuth token;
- current capture state and side-panel UI state;
- cached presence-check results, such as whether a contact or company exists in Hanta.

Captured records saved to Hanta are stored in the user's Hanta CRM account according to Hanta's product and account retention rules. Locally stored extension data can be removed by signing out, deleting the API key in the extension settings, clearing Chrome extension data, or uninstalling the extension.

## Data deletion and access requests

To request access, correction or deletion of data held in Hanta, contact us at info@t-next.de or use the Hanta support portal:

https://hanta.atlassian.net/servicedesk/customer/portals

If data has been forwarded to a connected third-party CRM, you may also need to delete or update it in that CRM.

## Permissions and why they are needed

- **`sidePanel`** — shows the Hanta capture UI next to LinkedIn.
- **`storage`** — stores the Hanta API key or session and keeps capture state across LinkedIn navigation and Manifest V3 service-worker restarts.
- **`identity`** — supports optional "Sign in with Hanta" OAuth login.
- **Host access to `https://www.linkedin.com/*` and `https://linkedin.com/*`** — lets the extension read the LinkedIn profile, company and user-triggered messaging pages the user views. Broad LinkedIn access is needed because LinkedIn is a single-page application and navigation can happen without a full page reload.
- **Host access to `https://media.licdn.com/*` and `https://*.licdn.com/*`** — lets the extension fetch LinkedIn profile photos and company logos as image bytes so they can be saved with the CRM record instead of relying on expiring LinkedIn CDN URLs. The extension does not inject content scripts into these media hosts.
- **Host access to `https://supa.hanta.io/*`** — lets the extension validate Hanta access, run presence checks and save captured records to Hanta.

## Security

Requests to Hanta use HTTPS. The extension validates backend responses before updating the side panel state. Untrusted LinkedIn page text is treated as plain text in the extension UI and is not inserted as executable HTML.

## Changes to this policy

We may update this policy from time to time. Material changes will be reflected by updating the effective date at the top of this document.

## Contact

t-next GmbH / Hanta  
Email: info@t-next.de  
Support: https://hanta.atlassian.net/servicedesk/customer/portals  
Website: https://www.hanta.io
