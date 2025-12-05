# GitSync

## Integrations
|Name|Description|
|----|-----------|
|Akamai|Akamai provides security services deployed across a global edge network. This includes Web Application Firewall (WAF) capabilities identifying web-based attacks, Bot Management distinguishing between human and automated traffic, DDoS mitigation services absorbing malicious traffic floods, and API security protections. Akamai generates security event data reflecting threats detected and actions taken at the internet edge.|
|CSV|Integration designed around working with CSV files. CSV is a simple file format used to store tabular data, such as a spreadsheet or database.|
|CrowdStrike Falcon|CrowdStrike Falcon is the leader in next-generation endpoint protection, threat intelligence and incident response through cloud-based endpoint protection.|
|Darktrace|Darktrace empowers defenders to reduce risk and minimize cyber disruption. Its Self-Learning AI technology develops a deep and evolving understanding on your bespoke organization, allowing it to prevent, detect, and respond to unpredictable cyber-attacks across the entire digital environment – from cloud and email to endpoints and OT networks.|
|FileUtilities|A set of file utility actions created for Google SecOps Community to power up playbook capabilities.|
|FortiAnalyzer|FortiAnalyzer provides a solution to address current difficulties and strengthen security posture. As an integrated solution, FortiAnalyzer reduces the challenges of supporting multiple point products. It is also designed to include broad visibility and control of an organization’s entire digital attack surface to minimize risk.|
|Functions|A set of math and data manipulation actions created for Google SecOps Community to power up playbook capabilities.|
|GitSyncPlayground|Sync Google SecOps integrations, playbooks, and settings with a GitHub, BitBucket or GitLab instance|
|Gmail|Secure business email, and so much more - the latest Gmail makes it easier to stay on top of the work that matters. With secure, ad-free email as a foundation, you can also chat, make voice or video calls, and stay on top of project work with shared files and tasks - all right in Gmail.|
|Google Chronicle|Google SecOps enables you to examine the aggregated security information for your enterprise going back for months or longer. Use Google SecOps to search across all of the domains accessed from within your enterprise. To enable the Google API client to communicate with the Backstory API you will need Google Developer Service Account Credential, https://developers.google.com/identity/protocols/OAuth2#serviceaccount.|
|ServiceNow|An incident ticketing integration exchanges ticket data between your ServiceNow instance and Google SecOps system.|
|Splunk|Splunk captures, indexes, and correlates real-time data in a searchable repository from which it can generate graphs, reports, alerts, dashboards, and visualizations.|
|UrlScanIo|urlscan.io is a service to scan and analyse websites.|
|VirusTotalV3|VirusTotal was founded in 2004 as a free service that analyzes files and URLs for viruses, worms, trojans and other kinds of malicious content. Our goal is to make the internet a safer place through collaboration between members of the antivirus industry, researchers and end users of all kinds. Fortune 500 companies, governments and leading security companies are all part of the VirusTotal community, which has grown to over 500,000 registered users.This integration was created using the 3rd iteration of VT API.|


## Connectors
|Name|Description|Has Mappings|
|----|-----------|------------|
|Sample Integration - Simple Connector Example|This is an example of a simple connector. It's integrated with "api.vatcomply.com" service and provides all of the main design ideas necessary to build a stable connector. Dynamic List defines what rates should be returned for a given currency and expects input in the format "EUR" etc.|True|
|ServiceNow Connector|Fetching incidents from ServiceNow to Siemplify|True|
|Splunk Query Connector|The connector sends queries that are a part of the whitelist, retrieves results and builds a case based on the results.|True|


## Visual Families
|Name|Description|
|----|-----------|
|Playground Family 1|Playground Family 1|
|Playground Family 2|Playground Family 2|
|Playground Family 3|Playground Family 3|
|Remote Agent Family 1|Remote Agent Family 1|
|Remote Agent Family 2|Remote Agent Family 2|
|Remote Agent Family 3|Remote Agent Family 3|


## Jobs
|Name|Description|
|----|-----------|
|Google Chronicle Alerts Creator Job|This job will sync new SOAR alerts with Chronicle SIEM.Note: This job is only supported from Chronicle SOAR version 6.2.30 and higher.|
|Push Contents|Push all content of this platform to git|
|Sync Splunk ES Comments|This job will synchronize comments in Splunk ES events and Siemplify cases.|
|Sync Table Record Comments|This job will synchronize comments in ServiceNow table records and Siemplify cases.|

