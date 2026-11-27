# Security and data handling

How Cellar handles your data, for security reviews and questionnaires. Every
answer describes how the app actually works today.

| Question | Answer |
|---|---|
| Platform | Atlassian Forge. All code runs on Atlassian's infrastructure. |
| Does the app store end-user data? | Yes: spreadsheet contents and version history, in Forge SQL storage for the customer's site. |
| Where is data stored? | Inside Atlassian, following the site's data residency. No external storage. |
| Does the app send data outside Atlassian? | No. There are no egress permissions in the manifest. |
| Runs on Atlassian eligible? | Yes, confirmed by the Forge CLI on deploy. |
| Personal data processed | Atlassian account IDs of people who save versions. No names or emails. |
| Personal data reporting | Weekly report to Atlassian's personal data reporting API; account IDs of closed accounts are removed from version history. |
| Data read but not stored | Page edit permission for the current user; page content, only when a user imports a table from the page. |
| Scopes requested | `storage:app`, `read:confluence-content.permission`, `read:page:confluence`, `read:blogpost:confluence`, `report:personal-data` |
| Encryption | Provided by Atlassian Forge storage (at rest and in transit). |
| Access control | Editing requires Confluence page edit permission, checked on the server for every save and restore. Viewing follows page view permission. |
| Isolation between customers | Forge storage is isolated per installation. Within a site, each sheet is keyed to its page and macro by the server, never by client input. |
| Data retention | While installed. History thinning: all versions for 24h, hourly for 30 days, daily after. |
| Data deletion on uninstall | Handled by Forge's retention policy for uninstalled apps. |
| Analytics or tracking | None. |
| Third-party sub-processors | None besides Atlassian. |
| Logging | Errors are logged to Forge's app logs. Diagnostic logs record field names and types only, never sheet contents. |
| Vulnerability reporting | sebcyde@hotmail.com |
| Developer access to customer data | None. The developer cannot read customers' sheets. |
