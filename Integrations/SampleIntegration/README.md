
# SampleIntegration

This is an educational integration designed to showcase the most common design patterns, when working with actions, connectors and jobs.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API Root for the integration. In this case, we are integrating with "api.vatcomply.com" service.|True|String|https://api.vatcomply.com|
|Password Field|Example of API password field parameter. API doesn't require authentication, this parameter is just for showcase purpose.|False|Password|*****|
|Verify SSL|If selected, the integration validates the SSL certificate when connecting to API Service. Selected by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|TIPCommon-2.2.10-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|charset_normalizer-3.4.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|googleapis_common_protos-1.70.0-py3-none-any.whl|
|httplib2-0.30.0-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|google_api_python_client-2.179.0-py3-none-any.whl|
|cachetools-5.5.2-py3-none-any.whl|
|certifi-2025.8.3-py3-none-any.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|pyparsing-3.2.3-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|protobuf-6.32.0-py3-none-any.whl|
|google_auth-2.40.3-py2.py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|google_api_core-2.25.1-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|
|anyio-4.10.0-py3-none-any.whl|


## Actions
#### Enrich Entity Action Example
Example of action that works with entities and enriches them. This action runs on all Google SecOps entities provided in the parameter "Entity Type". This is NOT an Async action.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Entity Type|Defines what entities from the scope of the alert should be processed.|True|List|All Entities|



##### JSON Results
```json
[{"Entity": "him@abc.com", "EntityResult": {"enriched": "true", "timestamp": "1754418093881"}}, {"Entity": "192.105.72.1", "EntityResult": {"enriched": "true", "timestamp": "1754418093883"}}]
```



#### Ping
Use the Ping action to test the connectivity to API Service.
Timeout - 600 Seconds



#### Async Action Example
Example of an async action in Google SecOps. This action will not finish execution until timeout is reached or a case will have a tag provided in the "Case Tag To Wait For"
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Case IDs|Comma-separated list of cases that needs to be handled. If nothing is provided, action will use the case id from which the action was executed.|False|String|None|
|Case Tag To Wait For|Action will wait until a case will have the provided tag.|True|String|Async|



##### JSON Results
```json
[{"case_id": "1", "tags": ["Async"]}]
```



#### Simple Action Example
Example of a simple action in Google SecOps. This action is fetching data from "api.vatcomply.com" service based on the provided parameters. This is NOT an Async action. This action DOES NOT work with Google SecOps Entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Currencies String|Example of input via CSV values. Comma-separated list of currencies that need to be processed.|False|String|USD, EUR|
|Currencies DDL|Example of input via DDL. Action will check both "Currencies String" and "Currencies DDL" to understand what values to process.|False|List|Select One|
|Time Frame|Time frame for the results. If "Custom" is selected, you also need to provide "Start Time".|False|List|Today|
|Start Time|Start time for the results. This parameter is mandatory, if 'Custom' is selected for the 'Time Frame' parameter. Format: ISO 8601. Action will only extract the dates from the timestamp. The delta between 'Start Time' and 'End Time' can't be greater than 7 days.|False|String||
|End Time|End time for the results. Format: ISO 8601. If nothing is provided and 'Custom' is selected for the 'Time Frame' parameter then this parameter will use current time. Action will only extract the dates from the timestamp. The delta between 'Start Time' and 'End Time' can't be greater than 7 days.|False|String||
|Return JSON Result|Example of input via boolean. If enabled, action will return a JSON Result.|False|Boolean|true|



##### JSON Results
```json
[{"date": "2000-03-03", "exchange_rates": [{"base": "USD", "rates": {"EUR": 1.035303861683404, "USD": 1.0, "JPY": 107.8476032715602, "CYP": 0.5955481933947614, "CZK": 36.87752355316285, "DKK": 7.711357283362667, "EEK": 16.19898540221555, "GBP": 0.6332953721917383, "HUF": 265.60720571487735, "LTL": 4.001035303861683, "LVL": 0.5954032508541256, "MTL": 0.4235428098146806, "PLN": 4.125168236877524, "ROL": 18961.590226731547, "SEK": 8.769023708458434, "SIT": 209.5625841184388, "SKK": 43.26845429133451, "CHF": 1.6630085930220522, "ISK": 73.39269075473652, "NOK": 8.369396417848638, "TRL": 574745.8329019567, "AUD": 1.647479035096801, "CAD": 1.454705456051351, "HKD": 7.782379128274149, "KRW": 1119.9503054146392, "NZD": 2.0485557511129517, "SGD": 1.7232632777720263, "ZAR": 6.4730303344031475}}, {"base": "EUR", "rates": {"EUR": 1.0, "USD": 0.9659, "JPY": 104.17, "CYP": 0.57524, "CZK": 35.62, "DKK": 7.4484, "EEK": 15.6466, "GBP": 0.6117, "HUF": 256.55, "LTL": 3.8646, "LVL": 0.5751, "MTL": 0.4091, "PLN": 3.9845, "ROL": 18315.0, "SEK": 8.47, "SIT": 202.4165, "SKK": 41.793, "CHF": 1.6063, "ISK": 70.89, "NOK": 8.084, "TRL": 555147.0, "AUD": 1.5913, "CAD": 1.4051, "HKD": 7.517, "KRW": 1081.76, "NZD": 1.9787, "SGD": 1.6645, "ZAR": 6.2523}}]}]
```






## Jobs

#### Simple Job Example
This is an example of a simple job. It has 2 functions: if a case has a tag "Closed", it will close the case from the job, if a case has a tag "Currency", it will add a comment to the case.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|API Root|True|String|https://api.vatcomply.com|
|Password Field|False|Password|*****|
|Verify SSL|False|Boolean|true|



## Connectors
#### Sample Integration - Simple Connector Example
This is an example of a simple connector. It's integrated with "api.vatcomply.com" service and provides all of the main design ideas necessary to build a stable connector. Dynamic List defines what rates should be returned for a given currency and expects input in the format "EUR" etc.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|base|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|180|
|API Root|API Root for the integration. In this case, we are integrating with "api.vatcomply.com" service.|True|String|https://api.vatcomply.com|
|Password Field|Example of API password field parameter. API doesn't require authentication, this parameter is just for showcase purpose.|False|Password|*****|
|Currencies To Fetch|Connector will fetch exchange rates for the provided currencies.|False|String|USD, EUR|
|Create Alert Per Exchange Rate|If enabled, connector will create a separate Alert per each exchange rate.|False|Boolean|false|
|Alert Severity|Possible values: Critical, High, Medium, Low, Informational|False|String|Informational|
|Add Attachment|If enabled, connector will add JSON object to the alert.|False|Boolean|true|
|Max Days Backwards|Amount of days from where to fetch alerts. Max: 30.|True|Integer|30|
|Max Alerts To Fetch|This parameter dictates how many alerts (in this case, dates) will be processed per 1 connector iteration.|True|String|3|
|Use dynamic list as blocklist|If enabled, the dynamic list will be used as a blocklist.|False|Boolean|false|
|Disable Overflow|If enabled, connector will ignore the overflow mechanism.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the API Service server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|





adding a readme add on