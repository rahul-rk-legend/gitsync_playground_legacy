<p align="center"><img src="./Resources/Splunk.svg" 
     alt="Splunk" width="200"/></p>

# Splunk

Splunk captures, indexes, and correlates real-time data in a searchable repository from which it can generate graphs, reports, alerts, dashboards, and visualizations.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Server Address|None|True|None|{SCHEMA}://{IP}:8089|
|Username|None|False|String||
|Password|None|False|Password|*****|
|API Token|None|False|Password|*****|
|Verify SSL|None|False|Boolean|False|
|CA Certificate File|None|False|String||


#### Dependencies
| |
|-|
|chardet-5.2.0-py3-none-any.whl|
|rsa-4.9-py3-none-any.whl|
|urllib3-2.3.0-py3-none-any.whl|
|cachetools-5.5.1-py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|uritemplate-4.1.1-py2.py3-none-any.whl|
|httpcore-1.0.7-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|sniffio-1.3.1-py3-none-any.whl|
|idna-3.10-py3-none-any.whl|
|pyparsing-3.2.1-py3-none-any.whl|
|google_api_python_client-2.160.0-py2.py3-none-any.whl|
|httplib2-0.22.0-py3-none-any.whl|
|google_auth-2.38.0-py2.py3-none-any.whl|
|anyio-4.8.0-py3-none-any.whl|
|charset_normalizer-3.4.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|googleapis_common_protos-1.67.0-py2.py3-none-any.whl|
|TIPCommon-2.0.6-py2.py3-none-any.whl|
|protobuf-5.29.3-cp38-abi3-manylinux2014_x86_64.whl|
|google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|h11-0.14.0-py3-none-any.whl|
|pyasn1_modules-0.4.1-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|typing_extensions-4.12.2-py3-none-any.whl|
|google_api_core-2.24.1-py3-none-any.whl|
|certifi-2025.1.31-py3-none-any.whl|
|pycryptodome-3.21.0-cp36-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|proto_plus-1.26.0-py3-none-any.whl|
|pyasn1-0.6.1-py3-none-any.whl|


## Actions
#### Get Host Events
Get events related to hosts in Splunk.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Event Per Host Limit|Specify how many events to return per host.|True|String|100|
|Results From|Specify the start time for the events.|True|String|-24h|
|Results To|Specify the end time for the events.|True|String|now|
|Result fields|Specify a comma-separated list of fields that need to be returned.|False|String||
|Index|Specify what index should be used, when searching for events related to the host. If nothing is provided, action will not use index.|False|String||
|Host Key|Specify what key should be used to get information about host events. Default: host.|False|String|host|



##### JSON Results
```json
[{"Entity": "splunkagenttesting", "EntityResult": [{"_bkt": "main~26~FED9BC6A-E994-4572-86C7-54FE3B50738A", "_cd": "26:89795", "_indextime": "1613383846", "_raw": "type=CRYPTO_KEY_USER msg=audit(1613383843.429:3838): pid=21155 uid=0 auid=4294967295 ses=4294967295 msg='op=destroy kind=server fp=SHA256:c5:02:2b:73:57:14:86:31:c4:ae:7b:22:f2:bc:fe:6c:1f:de:a4:a8:b5:fc:cf:42:e5:42:d9:8d:fb:22:d8:ee direction=? spid=21155 suid=0  exe=\"/usr/sbin/sshd\" hostname=? addr=? terminal=? res=success'", "_serial": "0", "_si": ["splunkagenttesting", "main"], "_sourcetype": "linux_audit", "_subsecond": ".429", "_time": "2021-02-15 12:10:43.429 IST", "host": "splunkagenttesting", "index": "main", "linecount": "1", "source": "/var/log/audit/audit.log", "sourcetype": "linux_audit", "splunk_server": "splunkagenttesting"}, {"_bkt": "main~26~FED9BC6A-E994-4572-86C7-54FE3B50738A", "_cd": "26:89783", "_indextime": "1613383846", "_raw": "type=CRYPTO_KEY_USER msg=audit(1613383843.429:3837): pid=21155 uid=0 auid=4294967295 ses=4294967295 msg='op=destroy kind=server fp=SHA256:a3:22:d2:f6:3b:88:0e:b8:45:ca:28:d3:61:91:04:56:4c:34:72:64:d5:34:f1:b9:86:50:ba:26:70:82:40:e9 direction=? spid=21155 suid=0  exe=\"/usr/sbin/sshd\" hostname=? addr=? terminal=? res=success'", "_serial": "1", "_si": ["splunkagenttesting", "main"], "_sourcetype": "linux_audit", "_subsecond": ".429", "_time": "2021-02-15 12:10:43.429 IST", "host": "splunkagenttesting", "index": "main", "linecount": "1", "source": "/var/log/audit/audit.log", "sourcetype": "linux_audit", "splunk_server": "splunkagenttesting"}]}, {"Entity": "siemplify", "EntityResult": [{"_bkt": "main~26~FED9BC6A-E994-4572-86C7-54FE3B50738A", "_cd": "26:20080", "_indextime": "1613141733", "_raw": "Jan 26 10:20:03 siemplify systemd: Stopped target Multi-User System.", "_serial": "0", "_si": ["splunkagenttesting", "main"], "_sourcetype": "syslog", "_time": "2021-01-26 10:20:03.000 IST", "host": "siemplify", "index": "main", "linecount": "1", "source": "/var/log/messages-20210131", "sourcetype": "syslog", "splunk_server": "splunkagenttesting"}, {"_bkt": "main~26~FED9BC6A-E994-4572-86C7-54FE3B50738A", "_cd": "26:20076", "_indextime": "1613141733", "_raw": "Jan 26 10:20:03 siemplify systemd: Stopping Hostname Service...", "_serial": "1", "_si": ["splunkagenttesting", "main"], "_sourcetype": "syslog", "_time": "2021-01-26 10:20:03.000 IST", "host": "siemplify", "index": "main", "linecount": "1", "source": "/var/log/messages-20210131", "sourcetype": "syslog", "splunk_server": "splunkagenttesting"}]}]
```



#### Ping
Test connectivity to the Splunk with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Update Notable Events
Update notable events in Splunk ES. Note: This action is only supported for Splunk ES.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Notable Event IDs|Specify IDs of notable events. Example:1A082D7B-D5A1-4A2B-BB94-41C439BE3EB7@@notable@@cb87390ae72763679d3f6f8f097ebe2b,1D234D5B-1531-2D2B-BB94-41C439BE12B7@@notable@@cb87390ae72763679d3f6f8f097ebe2b|True|String||
|Status|Specify the new status for notable events.|False|List|Select One|
|Urgency|Specify the new urgency for the notable event.|False|List|Select One|
|New Owner|Specify the new owner of the notable event.|False|String||
|Comment|Specify comment for the notable event.|False|String||
|Disposition|Specify the disposition for the notable event.|False|List|Select One|



#### Submit Event
Submit event to Splunk
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Index|Specify the index, where the event should be created.|True|String|main|
|Event|Specify the raw event that needs to be submitted.|True|String||
|Host|Specify the host that is related to the event.|False|String||
|Source|Specify the source of the event. Example: www.|False|String||
|Sourcetype|Specify the source type of the event. Example: web_event|False|String||



##### JSON Results
```json
{"index":"default","bytes":70,"host":"dogo","source":"www","sourcetype":"web_event"}
```



#### SplunkQuery
Execute a query in Splunk. Note: Please exclude any quotes that are part of the query string.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Mode|Specify the mode for search execution.|False|List|Smart|
|Query|Specify the query that needs to be executed. Example: index="_internal". You can provide multiple queries in the same action. The format is [“query 1”, “query 2”].|True|String||
|Results count limit|Specify how many results to return. Note: this parameter appends the “head” key word to the provided query. Default is 100.|False|String|100|
|Results From|Specify the start time for the query. Default: -24h|False|String|-24h|
|Results To|Specify the end time for the query. Default: now.|False|String|now|
|Result fields|Specify a comma-separated list of fields that need to be returned. Note: this parameter appends "fields" key word to the provided query.|False|String||



##### JSON Results
```json
[{"chronicle_query_used": "index=\"main\" | head 1", "tag::eventtype": ["memory", "os", "oshost"], "date_zone": "120", "tag": ["memory", "os", "oshost"], "date_minute": "11", "index": "perfmon", "sourcetype": "Perfmon:Memory", "instance": "0", "eventtype": ["perfmon", "perfmon_memory", "perfmon_windows"], "_bkt": "perfmon~130~B6974FCF-0920-4FE2-8DFF-6E089EDB456B", "_cd": "130:170838", "splunk_server": "TEST_HOST", "date_second": "44", "linecount": "6", "date_wday": "sunday", "date_hour": "16", "dest": "TEST_HOST", "date_year": "2019", "object": "Memory", "Value": "14400", "punct": "//_::._+\\\\r=\\\\r=\\\\r=-_____()\\\\r=\\\\r=", "host": "TEST_HOST", "_sourcetype": "Perfmon:Memory", "_indextime": "1549203105", "collection": "Memory", "_kv": "1", "_eventtype_color": "none", "_si": ["TEST_HOST", "perfmon"], "src": "TEST_HOST", "Host": "TEST_HOST", "timestartpos": "0", "date_month": "february", "counter": "Long-Term Average Standby Cache Lifetime (s)", "_subsecond": ".917", "_time": "2019-02-03T16:11:44.917+02:00", "date_mday": "3", "source": "Perfmon:Memory", "timeendpos": "29", "_raw": "02/03/2019 16:11:44.917 +0200\\ncollection=Memory\\nobject=Memory\\ncounter=Long-Term Average Standby Cache Lifetime (s)\\ninstance=0\\nValue=14400", "_serial": "0"}, {"chronicle_query_used": "index=\"main\" | head 1", "tag::eventtype": ["memory", "os", "oshost"], "date_zone": "120", "tag": ["memory", "os", "oshost"], "date_minute": "11", "index": "perfmon", "sourcetype": "Perfmon:Memory", "instance": "0", "eventtype": ["perfmon", "perfmon_memory", "perfmon_windows"], "_bkt": "perfmon~130~B6974FCF-0920-4FE2-8DFF-6E089EDB456B", "_cd": "130:170832", "splunk_server": "TEST_HOST", "date_second": "44", "linecount": "6", "date_wday": "sunday", "date_hour": "16", "dest": "TEST_HOST", "date_year": "2019", "object": "Memory", "Value": "4124942336", "punct": "//_::._+\\\\r=\\\\r=\\\\r=____\\\\r=\\\\r=", "host": "TEST_HOST", "_sourcetype": "Perfmon:Memory", "_indextime": "1549203105", "collection": "Memory", "_kv": "1", "_eventtype_color": "none", "_si": ["TEST_HOST", "perfmon"], "src": "TEST_HOST", "Host": "TEST_HOST", "timestartpos": "0", "date_month": "february", "counter": "Standby Cache Normal Priority Bytes", "_subsecond": ".917", "_time": "2019-02-03T16:11:44.917+02:00", "date_mday": "3", "source": "Perfmon:Memory", "timeendpos": "29", "_raw": "02/03/2019 16:11:44.917 +0200\\ncollection=Memory\\nobject=Memory\\ncounter=Standby Cache Normal Priority Bytes\\ninstance=0\\nValue=4124942336", "_serial": "1"}]
```



#### SplunkCsvViewer
Deprecated. This action creates a CSV table based on the raw results.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Results|Raw results.|True|String||



#### Execute Entity Query
Execute an entity query in Splunk. Note: this action prepares the “Where” clause based on the entities. Check documentation for additional information.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Search Mode|Specify the mode for search execution.|False|List|Smart|
|Query|Specify the query that needs to be executed without the “Where” clause.  Example: index="_internal"|True|String||
|Results count limit|Specify how many results to return. Note: this parameter appends the "head" key word to the provided query. Default is 100.|False|String||
|Results from|Specify the start time for the query. Default: -24h|False|String|-24h|
|Results To|Specify the end time for the query. Default: now.|False|String|now|
|Result fields|Specify a comma-separated list of fields that need to be returned. Note: this parameter appends "fields" key word to the provided query.|False|String||
|IP Entity Key|Specify what key should be used with IP entities. Please refer to the action documentation for details.|False|String||
|Hostname Entity Key|Specify what key should be used with Hostname entities, when preparing the. Please refer to the action documentation for details.|False|String||
|File Hash Entity Key|Specify what key should be used with File Hash entities. Please refer to the action documentation for details.|False|String||
|User Entity Key|Specify what key should be used with User entities. Please refer to the action documentation for details.|False|String||
|URL Entity Key|Specify what key should be used with URL entities. Please refer to the action documentation for details.|False|String||
|Email Address Entity Key|Specify what key should be used with Email Address entities. Please refer to the action documentation for details.|False|String||
|Stop If Not Enough Entities|If enabled, action will not start execution, unless all of the entity types are available for the specified ".. Entity Keys". Example: if "IP Entity Key" and "File Hash Entity Key" are specified, but in the scope there are no file hashes then if this parameter is enabled, action will not execute the query.|False|Boolean|True|
|Cross Entity Operator|Specify what should be the logical operator used between different entity types.|True|List|OR|



##### JSON Results
```json
[{"_bkt": "_audit~10~FED9BC6A-E994-4572-86C7-xxxx", "_cd": "10:239434", "_indextime": "1613148388", "_kv": "1", "_raw": "Audit:[timestamp=02-12-2021 18:46:28.096, user=admin, action=search, info=granted , search_id='1613148xxx.393', search='search index=_* OR index=* | where (device_ip=\"10.0.x.x\") | head 3', autojoin='1', buckets=0, ttl=600, max_count=500000, maxtime=8640000, enable_lookups='1', extra_fields='*', apiStartTime='ZERO_TIME', apiEndTime='ZERO_TIME', savedsearch_name=\"\", app=\"search\", provenance=\"N/A\", mode=\"historical\"]", "_serial": "0", "_si": ["splunkagenttesting", "_audit"], "_sourcetype": "audittrail", "_subsecond": ".096213", "_time": "2021-02-12T18:46:28.096+02:00", "action": "search", "apiEndTime": "'ZERO_TIME'", "apiStartTime": "'ZERO_TIME'", "app": "search", "autojoin": "'1'", "buckets": "0", "device_ip": "10.0.x.x", "enable_lookups": "'1'", "extra_fields": "'*'", "host": "splunkagenttesting", "index": "_audit", "info": "granted", "linecount": "1", "max_count": "500000", "maxtime": "8640000", "mode": "historical", "provenance": "N/A", "savedsearch_name": "", "search": "'search index=_* OR index=* | where (device_ip=\"10.0.x.x\") | head 3'", "search_id": "'1613148xxx.393'", "source": "audittrail", "sourcetype": "audittrail", "splunk_server": "splunkagenttesting", "timestamp": "02-12-2021 18:46:28.096", "ttl": "600", "user": "admin"}, {"_bkt": "_audit~10~FED9BC6A-E994-4572-86C7-xxxx", "_cd": "10:238430", "_indextime": "1613148356", "_kv": "1", "_raw": "Audit:[timestamp=02-12-2021 18:45:56.996, user=admin, action=search, info=granted , search_id='1613148xxx.391', search='search index=_* OR index=* | where (device_ip=\"10.0.x.x\") | fields app | head 3', autojoin='1', buckets=0, ttl=600, max_count=500000, maxtime=8640000, enable_lookups='1', extra_fields='*', apiStartTime='ZERO_TIME', apiEndTime='ZERO_TIME', savedsearch_name=\"\", app=\"search\", provenance=\"N/A\", mode=\"historical\"]", "_serial": "1", "_si": ["splunkagenttesting", "_audit"], "_sourcetype": "audittrail", "_subsecond": ".996145", "_time": "2021-02-12T18:45:56.996+02:00", "action": "search", "apiEndTime": "'ZERO_TIME'", "apiStartTime": "'ZERO_TIME'", "app": "search", "autojoin": "'1'", "buckets": "0", "device_ip": "10.0.x.x", "enable_lookups": "'1'", "extra_fields": "'*'", "host": "splunkagenttesting", "index": "_audit", "info": "granted", "linecount": "1", "max_count": "500000", "maxtime": "8640000", "mode": "historical", "provenance": "N/A", "savedsearch_name": "", "search": "'search index=_* OR index=* | where (device_ip=\"10.0.x.x\") | fields app | head 3'", "search_id": "'1613148xxx.391'", "source": "audittrail", "sourcetype": "audittrail", "splunk_server": "splunkagenttesting", "timestamp": "02-12-2021 18:45:56.996", "ttl": "600", "user": "admin"}, {"_bkt": "_audit~10~FED9BC6A-E994-4572-86C7-xxxx", "_cd": "10:230413", "_indextime": "1613148106", "_kv": "1", "_raw": "Audit:[timestamp=02-12-2021 18:41:46.532, user=admin, action=search, info=completed, search_id='1613148xxx.382', total_run_time=1.45, event_count=25, result_count=25, available_count=25, scan_count=26861, drop_count=0, exec_time=1613148103, api_et=N/A, api_lt=N/A, search_et=N/A, search_lt=N/A, is_realtime=0, savedsearch_name=\"\", search_startup_time=\"197\", has_error_msg=false, fully_completed_search=true, acceleration_id=\"FED9BC6A-E994-4572-86C7-54FE3B50738A_search_admin_f92be55e186xxxx\", app=\"search\", provenance=\"N/A\", mode=\"historical\", searched_buckets=11, eliminated_buckets=0, considered_events=26861, total_slices=6622, decompressed_slices=2664, duration.command.search.index=171, invocations.command.search.index.bucketcache.hit=0, duration.command.search.index.bucketcache.hit=0, invocations.command.search.index.bucketcache.miss=0, duration.command.search.index.bucketcache.miss=0, invocations.command.search.index.bucketcache.error=0, duration.command.search.rawdata=744, invocations.command.search.rawdata.bucketcache.hit=0, duration.command.search.rawdata.bucketcache.hit=0, invocations.command.search.rawdata.bucketcache.miss=0, duration.command.search.rawdata.bucketcache.miss=0, invocations.command.search.rawdata.bucketcache.error=0, roles='admin+power+user', search='search index=_* OR index=* | where (device_ip=\"10.0.x.x\") | fields app | head 100']", "_serial": "2", "_si": ["splunkagenttesting", "_audit"], "_sourcetype": "audittrail", "_subsecond": ".532669", "_time": "2021-02-12T18:41:46.532+02:00", "acceleration_id": "FED9BC6A-E994-4572-86C7-54FE3B50738A_search_admin_f92be55e1865xxxx", "action": "search", "api_et": "N/A", "api_lt": "N/A", "app": "search", "available_count": "25", "considered_events": "26861", "decompressed_slices": "2664", "device_ip": "10.0.x.x", "drop_count": "0", "duration_command_search_index": "171", "duration_command_search_index_bucketcache_hit": "0", "duration_command_search_index_bucketcache_miss": "0", "duration_command_search_rawdata": "744", "duration_command_search_rawdata_bucketcache_hit": "0", "duration_command_search_rawdata_bucketcache_miss": "0", "eliminated_buckets": "0", "event_count": "25", "exec_time": "1613148103", "fully_completed_search": "true", "has_error_msg": "false", "host": "splunkagenttesting", "index": "_audit", "info": "completed", "invocations_command_search_index_bucketcache_error": "0", "invocations_command_search_index_bucketcache_hit": "0", "invocations_command_search_index_bucketcache_miss": "0", "invocations_command_search_rawdata_bucketcache_error": "0", "invocations_command_search_rawdata_bucketcache_hit": "0", "invocations_command_search_rawdata_bucketcache_miss": "0", "is_realtime": "0", "linecount": "1", "mode": "historical", "provenance": "N/A", "result_count": "25", "roles": "'admin+power+user'", "savedsearch_name": "", "scan_count": "26861", "search": "'search index=_* OR index=* | where (device_ip=\"10.0.x.x\") | fields app | head 100'", "search_et": "N/A", "search_id": "'1613148xxx.382'", "search_lt": "N/A", "search_startup_time": "197", "searched_buckets": "11", "source": "audittrail", "sourcetype": "audittrail", "splunk_server": "splunkagenttesting", "timestamp": "02-12-2021 18:41:46.532", "total_run_time": "1.45", "total_slices": "6622", "user": "admin"}]
```






## Jobs

#### Sync Splunk ES Comments
This job will synchronize comments in Splunk ES events and Siemplify cases.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Server Address|True|String|https://<ip>:8089|
|Username|False|String||
|Password|False|Password|*****|
|API Token|False|Password|*****|
|CA Certificate File|False|String||
|Verify SSL|False|Boolean||

#### Sync Splunk ES Closed Events
This job will synchronize closed Splunk ES notable events and Siemplify alerts.

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Server Address|True|String|https://<ip>:8089|
|Username|False|String||
|Password|False|Password|*****|
|API Token|False|Password|*****|
|Max Hours Backwards|False|String|24|
|CA Certificate File|False|String||
|Verify SSL|False|Boolean||



## Connectors
#### Splunk Pull Connector
Splunk Pull Connector

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Describes the name of the field where the product name is stored.|True|String|Product Name|
|EventClassId|Describes the name of the field where the event name is stored.|True|String|app|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|60|
|Server Address|IP Address of Splunk API Server.|True|String||
|Port|Port of the Splunk Instance.|True|Integer|8089|
|Username|Splunk account username.|False|String||
|Password|Splunk account password.|False|Password|*****|
|API Token|Splunk API Token. API token has priority over other authentication methods, when this field is not empty.|False|Password|*****|
|Time Frame|Time frame of alerts to fetch. Examples: 1m - from 1 minute ago 3h - from 3 hours ago 1d - from 24 hours ago (1 day) 1w - from 1 week ago.|False|String|1h|
|Alerts Count Limit|Limit the number of Alerts returned by the connector per 1 iteration.|False|Integer|100|
|Verify SSL|Whether to verify ssl certificate on connection or not.|False|Boolean|true|
|Environment Field Name|Describes the name of the field where the environment name is stored. If environment field isn't found, environment is "".|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return value unchanged. Used to allow the user to manipulate the environment field via regex logic. If regex pattern is null or empty, or the environment value is null, the final environment result is "".|False|String|.*|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|CA Certificate File|CA Certificate File|False|String||


#### Splunk Query Connector
The connector sends queries that are a part of the whitelist, retrieves results and builds a case based on the results.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|The field name used to determine the device product, e.g: device_product|True|String|device_product|
|EventClassId|The field name used to determine the event name (sub-type),  e.g: event_type_field_name|False|String|app|
|PythonProcessTimeout|The timeout limit (in seconds) for the python process running current script|True|String|60|
|Api Root|API root of the Splunk instance.|True|String|https://<ip>:8089|
|Username|Username of the Splunk account.|False|String||
|Password|Password of the Splunk account.|False|Password|*****|
|API Token|Splunk API Token. API token has priority over other authentication methods, when this field is not empty.|False|Password|*****|
|Verify SSL|Whether to verify ssl certificate on connection or not|False|Boolean|FALSE|
|Environment Field Name|Field which represent the environment in the event data.|False|String||
|Rule Generator Field|Field that represents the rule generator field.|True|String||
|Alert Name Field Name|Field which represent the alert name.|True|String||
|Events Count Limit Per Query|Max amount of events to fetch per query, e.g: 10|False|String|10|
|Max Days Backwards|Number of days before the first connector iteration to retrieve events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|String|1|
|Aggregate Events Query|If enabled, the connector will combine all events under one alert.|False|Boolean|FALSE|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|CA Certificate File|CA Certificate File|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the 'Environment Field Name' field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|


#### Splunk ES - Notable Events Connector
Ingest notable events from Splunk ES. Note: This connector only works with Splunk ES.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Notable Event Data Along Base Event|If enabled, connector will create Siemplify Events based on both Notable Event and Base Events together.|False|Boolean|false|
|Multivalue Fields|A comma-separated list of fields that contain multiple entities. If, for example, one field can contain two hostnames, we would need to split notable event into two Siemplify Events in order to do a correct mapping of entities.|False|String|asset, src, dest, ip|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|Product Name|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|app|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the 'Environment Field Name' field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field via regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|Rule Generator Field Name|The name of the field that will be used to map the rule generator value. Note: only information about notable event itself is used for mapping, events are disregarded. If invalid value is provided, connector will use "rule_name" as field.|False|String||
|Server Address|Server address of the Splunk instance.|True|String|https://<ip>:8089|
|Username|Username of the Splunk account.|False|String||
|Password|Password of the Splunk account.|False|Password|*****|
|API Token|Splunk API token. API token has priority over other authentication methods, when this field is not empty.|False|Password|*****|
|Lowest Urgency To Fetch|Lowest urgency that will be used to fetch notable events. Possible values: Informational Low Medium High Critical|True|String|Medium|
|Fetch Max Hours Backwards|Number of hours before the first connector iteration to retrieve notable events from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Padding Time|Amount of hours that will be used as a padding. If nothing is provided, this parameter is not going to be applied. Max 100 hours. Note: it's not safe to increase the padding period beyond 12 hours.|False|Integer||
|Only Drilldown Events|If enabled, the connector will only try to fetch drilldown events, without trying to fetch base events. Note: this parameter requires 'Extract Base Events' to be enabled.|False|Boolean|false|
|Max Notable Events To Fetch|How many notable events to process per one connector iteration.|False|Integer|50|
|Use whitelist as a blacklist|If enabled, whitelist will be used as a blacklist.|False|Boolean|false|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Splunk server is valid.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|
|Query Filter|Additional filter for the query that is sent to Splunk to get notable events. Value provided here will be appended to the WHERE clause of the query. Please refer to documentation portal for more information.|False|String||
|CA Certificate File|CA Certificate File|False|String||
|Extract Base Events|If enabled, connector will try to extract base events related to notable event using information about the job. In other case, connector will create a Siemplify Event based on the notable event. Note: that if parameter is set to True, but connector can't work with jobs, connector will use information about notable event as a fallback mechanism.|False|Boolean|true|
|Alert Name Source|Source for the alert name. Possible values: Search Name, Rule Name.|False|String|Search Name|




