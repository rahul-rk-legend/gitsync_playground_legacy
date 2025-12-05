# ServiceNow Connector
Fetching incidents from ServiceNow to Siemplify


Integration: ServiceNow

Integration Version: 59.0

Device Product Field: Product Name

Event Name Field: sys_class_name
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|false|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|60|
|Rule Generator|The field name used to determine the rule generator.|False||
|Api Root|https://{dev-instance}.service-now.com/api/now/v1/|True|https://googlellcdemo3.service-now.com/api/now/v1/|
|Incident Table|This parameter is defining what API root ServiceNow integration is going to use for actions that revolve around incidents. By default the integration uses the “table/incident” path. |False|incident|
|Username|Username|True|admin|
|Password|Password|True|***************|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the ServiceNow server is valid.|False|false|
|Client ID|Client ID of Service Now application. Required for Oauth authentication.|False||
|Client Secret|Client Secret of Service Now application. Required for Oauth authentication.|False||
|Refresh Token|Refresh token for Service Now application. Required for Oauth authentication.|False||
|Assignment Group|Name of the assignment group for which you want to ingest records.|False||
|Use Oauth Authentication|If enabled, integration will use Oauth authentication. Parameters “Client ID“, “Client Secret“ and “Refresh Token“ are mandatory.|False|false|
|Days Backwards|Fetch incidents from 'x' days backwards. e.g. 3|False|5|
|Max Incidents Per Cycle|Fetch max 'x' incidents. e.g. 10|False|10|
|Server Time Zone|The timezone configured in the server, ex. UTC, Asia/Jerusalem etc.|False|UTC|
|Environments Whitelist|The environments (domains) to ingest into Siemplify, comma separated list (env1,env2)|False||
|Table Name|The table to fetch from. e.g. incident|False||
|Event Name|The name of the event in Siemplify. e.g. ServiceNowEvent|False||
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False||
|Get User Information|If enabled, connector will additionally retrieve information about the users related to the incident.|False|false|

