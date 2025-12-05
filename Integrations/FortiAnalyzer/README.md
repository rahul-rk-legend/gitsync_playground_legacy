
# FortiAnalyzer

FortiAnalyzer provides a solution to address current difficulties and strengthen security posture. As an integrated solution, FortiAnalyzer reduces the challenges of supporting multiple point products. It is also designed to include broad visibility and control of an organization’s entire digital attack surface to minimize risk.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|API Root|API root of the FortiAnalyzer instance.|True|String|https://{ip_address}|
|Username|Username of the FortiAnalyzer account.|True|String||
|Password|Password of the FortiAnalyzer account.|True|Password|*****|
|Verify SSL|If enabled, verify the SSL certificate for the connection to the FortiAnalyzer is valid.|False|Boolean|true|


#### Dependencies
| |
|-|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|TIPCommon-1.0.12-py2.py3-none-any.whl|
|EnvironmentCommon-1.0.1-py2.py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|idna-3.7-py3-none-any.whl|


## Actions
#### Enrich Entities
Enrich entities using information from FortiAnalyzer. Supported entities: Hostname, IP Address.
Timeout - 600 Seconds



##### JSON Results
```json
[{"Entity":"172.xx.xxx.xxx","EntityResult":{"adm_pass":["xxxxxxx"],"adm_usr":"admin","app_ver":"","av_ver":"","beta":-1,"branch_pt":1255,"build":1255,"checksum":"","conf_status":0,"conn_mode":0,"conn_status":0,"db_status":0,"desc":"","dev_status":0,"eip":"","fap_cnt":0,"faz.full_act":0,"faz.perm":15,"faz.quota":0,"faz.used":0,"fex_cnt":0,"first_tunnel_up":0,"flags":2097152,"foslic_cpu":0,"foslic_dr_site":0,"foslic_inst_time":0,"foslic_last_sync":0,"foslic_ram":0,"foslic_type":0,"foslic_utm":0,"fsw_cnt":0,"ha_group_id":0,"ha_group_name":"","ha_mode":0,"ha_slave":null,"hdisk_size":0,"hostname":"","hw_rev_major":0,"hw_rev_minor":0,"hyperscale":0,"ip":"172.xx.xxx.xxx","ips_ext":0,"ips_ver":"","last_checked":1665664693,"last_resync":0,"latitude":"0.0","lic_flags":0,"lic_region":"","location_from":"","logdisk_size":0,"longitude":"0.0","maxvdom":10,"mgmt.__data[0]":0,"mgmt.__data[1]":0,"mgmt.__data[2]":0,"mgmt.__data[3]":0,"mgmt.__data[4]":0,"mgmt.__data[5]":0,"mgmt.__data[6]":0,"mgmt.__data[7]":0,"mgmt_if":"","mgmt_mode":2,"mgmt_uuid":"184xxxxxxx","mgt_vdom":"","module_sn":"","mr":2,"name":"FGVxxxxxxxxxx","node_flags":0,"nsxt_service_name":"","oid":181,"onboard_rule":null,"opts":0,"os_type":0,"os_ver":7,"patch":2,"platform_str":"FortiGate-VM64","prefer_img_ver":"","prio":0,"private_key":"","private_key_status":0,"psk":"","role":0,"sn":"FGVxxxxxxxxxx","source":2,"tab_status":"","tunnel_cookie":"","tunnel_ip":"","vdom":[{"comments":null,"devid":"FGVxxxxxxxxxx","ext_flags":0,"flags":0,"name":"root","node_flags":0,"oid":3,"opmode":1,"rtm_prof_id":0,"status":null,"tab_status":null,"vdom_type":1,"vpn_id":0}],"version":700,"vm_cpu":0,"vm_cpu_limit":0,"vm_lic_expire":0,"vm_mem":0,"vm_mem_limit":0,"vm_status":0}}]
```



#### Ping
Test connectivity to the FortiAnalyzer with parameters provided at the integration configuration page on the Marketplace tab.
Timeout - 600 Seconds



#### Update Alert
Update an alert in FortiAnalyzer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert that needs to be updated.|True|String||
|Acknowledge Status|Specify the acknowledgment status for alert.|False|List|Select One|
|Mark As Read|If enabled, the action marks the alert as read.|False|Boolean|false|
|Assign To|Specify to whom the alert needs to be assigned.|False|String||



##### JSON Results
```json
{"alerttime":"1665653864","logcount":"17","alertid":"202xxxxxxxxxxxxx","adom":"root","epid":"1","epname":"not implemented dev type","subject":"desc:Trim local db","euid":"1","euname":"N/A","devname":"fortianalyzer","logtype":"event","devtype":"FortiAnalyzer","devid":"FAZ-VMxxxxxxxxxx","vdom":"_self_locallog_","groupby1":"desc:Trim local db","triggername":"Local Device Event","tag":"Default,System,Local","eventtype":"event","severity":"medium","extrainfo":"{ \"msg\": \"Requested to trim database tables older than 60 days to enforce the retention policy of Adom FortiAuthenticator.\" }","ackflag":"no","readflag":"yes","filterkey":"337xxxxxxxxxxxxxx","firstlogtime":"1665653864","multiflag":"","lastlogtime":"1665653887","updatetime":"1665747977","filtercksum":"2072153473","filterid":"1","assignto":"api_user","ackby":"admin","acktime":"1665747892"}
```



#### Search Logs
Search logs in FortiAnalyzer. Note: Action is running as async, adjust the script timeout value in Siemplify IDE for action as needed.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Log Type|Specify the log type that needs to be searched.|False|List|Traffic|
|Case Sensitive Filter|If enabled, the filter is case sensitive.|False|Boolean|false|
|Query Filter|Specify the query filter for the search.|False|String||
|Device ID|Specify the ID of the device that needs to be searched. If nothing is provided, the action searches in All_Fortigate. Examples of values: All_FortiGate, All_FortiMail, All_FortiWeb, All_FortiManager, All_Syslog, All_FortiClient, All_FortiCache, All_FortiProxy, All_FortiAnalyzer, All_FortiSandbox, All_FortiAuthenticator, All_FortiDDoS.|False|String|All_Fortigate|
|Time Frame|Specify a time frame for the results. If "Custom" is selected, you also need to provide the "Start Time" parameter.|False|List|Last Month|
|Start Time|Specify the start time for the results. This parameter is mandatory, if "Custom" is selected for the "Time Frame" parameter. Format: ISO 8601|False|String||
|End Time|Specify the end time for the results. Format: ISO 8601. If nothing is provided and "Custom" is selected for the "Time Frame" parameter then this parameter uses current time.|False|String||
|Time Order|Specify the time ordering in the search.|False|List|DESC|
|Max Logs To Return|Specify the number of logs you want to return. Default: 20. Maximum: 1000.|False|String|20|



##### JSON Results
```json
{"sessionid":"1111","srcip":"1.1.1.1","dstip":"1.1.1.1","srcport":"11111","dstport":"443","trandisp":"noop","duration":"1","proto":"6","sentbyte":"216","rcvdbyte":"112","sentpkt":"4","rcvdpkt":"2","logid":"0001000014","service":"HTTPS","app":"HTTPS","appcat":"unscanned","srcintfrole":"undefined","dstintfrole":"undefined","eventtime":"1665752066921638736","srccountry":"Reserved","dstcountry":"Somewhere","srcintf":"root","dstintf":"port1","dstowner":"540","tz":"-0700","devid":"FGVMQWERKQ61YQD5","vd":"root","csf":"FortiNetFabric","dtime":"2022-10-14 05:54:27","itime_t":"1665752069","devname":"FGVMEV2YKQ61QWER"}
```



#### Add Comment To Alert
Add a comment to alert in FortiAnalyzer.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Alert ID|Specify the ID of the alert that needs to be updated.|True|String||
|Comment|Specify the comment for the alert.|True|String||



##### JSON Results
```json
{"jsonrpc":"2.0","id":"string","result":{"status":"done"}}
```









## Connectors
#### FortiAnalyzer - Alerts Connector
Pull information about alerts from FortiAnalyzer. Note: Dynamic list filter works with the "subject" parameter.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|siemplify_type|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|eventtype|
|Environment Field Name|Describes the name of the field where the environment name is stored. If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field. Default is .* to catch all and return the value unchanged. Used to allow the user to manipulate the environment field through regex logic. If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String|.*|
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|180|
|API Root|API root of the FortiAnalyzer instance.|True|String|https://{ip address}|
|Username|Username of the FortiAnalyzer account.|True|String||
|Password|Password of the FortiAnalyzer account.|True|Password|*****|
|Verify SSL|If enabled, verifies that the SSL certificate for the connection to the FortiAnalyzer server is valid.|False|Boolean|true|
|Lowest Severity To Fetch|The lowest severity that needs to be used to fetch alerts. Possible values: low, medium, high, critical. If nothing is specified, the connector ingests alerts with all severities.|False|String|Medium|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve alerts from. This parameter applies to the initial connector iteration after you enable the connector for the first time, or used as a fallback value in cases where connector's last run timestamp expires.|False|Integer|1|
|Max Alerts To Fetch|Number of alerts to process per one connector iteration. Default: 20.|False|Integer|20|
|Use dynamic list as a blacklist|If enabled, the dynamic list is used as a blacklist.|False|Boolean|false|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




