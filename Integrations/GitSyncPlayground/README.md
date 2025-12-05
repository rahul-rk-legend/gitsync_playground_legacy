
# GitSyncPlayground

Sync Google SecOps integrations, playbooks, and settings with a GitHub, BitBucket or GitLab instance

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Repo URL|Repository URL. The URL must start with 'https' for HTTPS+Token or 'git@' for SSH+Cert.|True|String||
|Branch|Target branch|True|String||
|Git Server Fingerprint|SHA256 or MD5 fingerprint for secure Git server verification (optional). If provided, will enable secure host key verification. Format: 'SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8' or 'MD5:16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48'|False|String||
|Git Password/Token/SSH Key|Git Password/Token/SSH Key (Base64). RSA and Ed25519 are supported.|True|Password|*****|
|Git Username|Git Username|False|String||
|Commit Author|Commit Author. Must be in the following format: 'James Bond <james.bond@gmail.com>'|False|String||
|Siemplify Verify SSL|Siemplify Verify SSL|False|Boolean|true|
|Git Verify SSL|Git Verify SSL|False|Boolean|true|
|SOAR Username|Username with playbook edit permissions. Required if API Key fails due to permission limits.|False|String|None|
|SOAR Password|Password for SOAR Username.|False|Password|*****|


#### Dependencies
| |
|-|
|pycryptodome-3.23.0-cp37-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|urllib3-2.5.0-py3-none-any.whl|
|requests-2.32.5-py3-none-any.whl|
|cachetools-6.2.2-py3-none-any.whl|
|invoke-2.2.1-py3-none-any.whl|
|paramiko-4.0.0-py3-none-any.whl|
|google_api_python_client-2.187.0-py3-none-any.whl|
|EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cryptography-46.0.3-cp311-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1_modules-0.4.2-py3-none-any.whl|
|google_api_core-2.28.1-py3-none-any.whl|
|pyparsing-3.2.5-py3-none-any.whl|
|certifi-2025.11.12-py3-none-any.whl|
|pynacl-1.6.1-cp38-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|httplib2-0.31.0-py3-none-any.whl|
|jinja2-3.1.6-py3-none-any.whl|
|pycparser-2.23-py3-none-any.whl|
|charset_normalizer-3.4.4-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|TIPCommon-2.2.19-py2.py3-none-any.whl|
|typing_extensions-4.15.0-py3-none-any.whl|
|bcrypt-5.0.0-cp39-abi3-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|google_auth-2.43.0-py2.py3-none-any.whl|
|anyio-4.12.0-py3-none-any.whl|
|proto_plus-1.26.1-py3-none-any.whl|
|packaging-25.0-py3-none-any.whl|
|googleapis_common_protos-1.72.0-py3-none-any.whl|
|protobuf-6.33.1-py3-none-any.whl|
|idna-3.11-py3-none-any.whl|
|uritemplate-4.2.0-py3-none-any.whl|
|dulwich-0.24.1-py3-none-any.whl|
|h11-0.16.0-py3-none-any.whl|
|httpx-0.28.1-py3-none-any.whl|
|google_auth_httplib2-0.2.1-py3-none-any.whl|
|httpcore-1.0.9-py3-none-any.whl|
|rsa-4.9.1-py3-none-any.whl|
|markupsafe-3.0.3-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.manylinux_2_28_x86_64.whl|
|cffi-2.0.0-cp311-cp311-manylinux2014_x86_64.manylinux_2_17_x86_64.whl|
|pyasn1-0.6.1-py3-none-any.whl|


## Actions
#### Ping
Test connectivity to GitSync
Timeout - 600 Seconds






## Jobs

#### Push Content
Push all content of this platform to git

|Name|IsMandatory|Type|DefaultValue|
|----|-----------|----|------------|
|Commit|True|String||
|Repo URL|False|String|None|
|Branch|False|String|None|
|Git Server Fingerprint|False|String|None|
|Commit Author|False|String||
|Commit Passwords|False|Boolean|false|
|Integrations|False|Boolean|true|
|Playbooks|False|Boolean|true|
|Jobs|False|Boolean|true|
|Connectors|False|Boolean|true|
|Integration Instances|False|Boolean|true|
|Visual Families|False|Boolean|true|
|Mappings|False|Boolean|true|
|Environments|False|Boolean|true|
|Dynamic Parameters|False|Boolean|true|
|Logo|False|Boolean|true|
|Case Tags|False|Boolean|true|
|Case Stages|False|Boolean|true|
|Case Title Settings|False|Boolean|true|
|Case Close Reasons|False|Boolean|true|
|Networks|False|Boolean|true|
|Domains|False|Boolean|true|
|Custom Lists|False|Boolean|true|
|Email Templates|False|Boolean|true|
|Blacklists|False|Boolean|true|
|SLA Records|False|Boolean|true|
|Simulated Cases|False|Boolean|true|



