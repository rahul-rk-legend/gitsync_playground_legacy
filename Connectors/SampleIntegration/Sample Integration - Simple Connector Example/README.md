# Sample Integration - Simple Connector Example
This is an example of a simple connector. It's integrated with "api.vatcomply.com" service and provides all of the main design ideas necessary to build a stable connector. Dynamic List defines what rates should be returned for a given currency and expects input in the format "EUR" etc.


Integration: SampleIntegration

Integration Version: 1.0

Device Product Field: Product Name

Event Name Field: base
### Parameters
|Name|Description|Is Mandatory|Value|
|----|-----------|------------|-----|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|.*|
|Script Timeout (Seconds)|The timeout limit (in seconds) for the python process running current script|True|180|
|API Root|API Root for the integration. In this case, we are integrating with "api.vatcomply.com" service.|True|https://api.vatcomply.com|
|Password Field|Example of API password field parameter. API doesn't require authentication, this parameter is just for showcase purpose.|False||
|Currencies To Fetch|Connector will fetch exchange rates for the provided currencies.|False|USD, EUR|
|Create Alert Per Exchange Rate|If enabled, connector will create a separate Alert per each exchange rate.|False|false|
|Alert Severity|Possible values: Critical, High, Medium, Low, Informational|False|Informational|
|Add Attachment|If enabled, connector will add JSON object to the alert.|False|true|
|Max Days Backwards|Amount of days from where to fetch alerts. Max: 30.|True|30|
|Max Alerts To Fetch|This parameter dictates how many alerts (in this case, dates) will be processed per 1 connector iteration.|True|3|
|Use dynamic list as blocklist|If enabled, the dynamic list will be used as a blocklist.|False|false|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the API Service server is valid.|False|true|
|Proxy Server Address|The address of the proxy server to use.|False||
|Proxy Username|The proxy username to authenticate with.|False||
|Proxy Password|The proxy password to authenticate with.|False||


adding a readme add on