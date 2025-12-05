# Splunk Query Connector
The connector sends queries that are a part of the whitelist, retrieves results and builds a case based on the results.


Integration: Splunk

Integration Version: 59.0

Device Product Field: device_product

Event Name Field: app
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|60|
|Api Root|API root of the Splunk instance.|True|https://lab:8089|
|Username|Username of the Splunk account.|False|admin|
|Password|Password of the Splunk account.|False|***************|
|API Token|Splunk API Token. API token has priority over other authentication methods, when this field is not empty.|False||
|Verify SSL|Whether to verify ssl certificate on connection or not|False|false|
|Environment Field Name|Field which represent the environment in the event data.|False||
|Rule Generator Field|Field that represents the rule generator field.|True|Rule|
|Alert Name Field Name|Field which represent the alert name.|True|Alert|
|Events Count Limit Per Query|Max amount of events to fetch per query, e.g: 10|False|10|
|Max Days Backwards|Number of days before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|1|
|Aggregate Events Query|If enabled, the connector will combine all events under one alert.|False|false|
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False||
|CA Certificate File|CA Certificate File|False||
|Environment Regex Pattern|A regex pattern to run on the value found in the 'Environment Field Name' field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|

