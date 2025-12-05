## Google Chronicle Alerts Creator Job
This job will sync new SOAR alerts with Chronicle SIEM.
Note: This job is only supported from Chronicle SOAR version 6.2.30 and higher.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|ttps://test-backstory.sandbox.googleapis.com|
|Verify SSL|Boolean|False|true|
|User's Service Account|Password|False|*****|
|Workload Identity Email|Password|False|*****|

## Push Contents
Push all content of this platform to git


**Run Interval In Seconds:** 18000

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Commit|String|True|First Commit|
|Repo URL|String|False|https://github.com/rahul-rk-legend/gitsync_playground_legacy.git|
|Branch|String|False|main|
|Git Server Fingerprint|String|False||
|Commit Author|String|False|rahul-rk-legend <rkumbhar@google.com>|
|Commit Passwords|Boolean|False|false|
|Integrations|Boolean|False|false|
|Playbooks|Boolean|False|false|
|Jobs|Boolean|False|true|
|Connectors|Boolean|False|false|
|Integration Instances|Boolean|False|false|
|Visual Families|Boolean|False|false|
|Mappings|Boolean|False|false|
|Environments|Boolean|False|false|
|Dynamic Parameters|Boolean|False|false|
|Logo|Boolean|False|false|
|Case Tags|Boolean|False|false|
|Case Stages|Boolean|False|false|
|Case Title Settings|Boolean|False|false|
|Case Close Reasons|Boolean|False|false|
|Networks|Boolean|False|false|
|Domains|Boolean|False|false|
|Custom Lists|Boolean|False|false|
|Email Templates|Boolean|False|false|
|Blacklists|Boolean|False|false|
|SLA Records|Boolean|False|false|
|Simulated Cases|Boolean|False|false|

## Simple Job Example
This is an example of a simple job. It has 2 functions: if a case has a tag "Closed", it will close the case from the job, if a case has a tag "Currency", it will add a comment to the case.


**Run Interval In Seconds:** 18000

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://api.vatcomply.com|
|Verify SSL|Boolean|False|true|
|Password Field|Password|False|*****|


adding a readme add on## Sync Splunk ES Comments
This job will synchronize comments in Splunk ES events and Siemplify cases.


**Run Interval In Seconds:** 3600

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Server Address|String|True|https://lab:8089|
|Username|String|False|admin|
|CA Certificate File|String|False||
|Verify SSL|Boolean|False|true|
|Password|Password|False|*****|
|API Token|Password|False|*****|

## Sync Table Record Comments
This job will synchronize comments in ServiceNow table records and Siemplify cases.


**Run Interval In Seconds:** 18000

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Api Root|String|True|https://googlellcdemo3.service-now.com/api/now/v1/|
|Username|String|True|admin|
|Verify SSL|Boolean|False|false|
|Client ID|String|False||
|Use Oauth Authentication|Boolean|False|false|
|Table Name|String|True|incident|
|Password|Password|True|*****|
|Client Secret|Password|False|*****|
|Refresh Token|Password|False|*****|

