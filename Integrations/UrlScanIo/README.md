<p align="center"><img src="./Resources/UrlScanIo.svg" 
     alt="UrlScanIo" width="200"/></p>

# UrlScanIo

urlscan.io is a service to scan and analyse websites.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Api Key|None|True|Password|*****|
|Verify SSL|None|False|Boolean|false|


#### Dependencies
| |
|-|
|TIPCommon-1.0.10-py3-none-any.whl|
|charset_normalizer-3.3.2-py3-none-any.whl|
|chardet-5.2.0-py3-none-any.whl|
|certifi-2024.7.4-py3-none-any.whl|
|filelock-3.15.4-py3-none-any.whl|
|urllib3-2.2.2-py3-none-any.whl|
|requests-2.32.3-py3-none-any.whl|
|requests_file-2.1.0-py2.py3-none-any.whl|
|tldextract-5.1.2-py3-none-any.whl|
|idna-3.8-py3-none-any.whl|


## Actions
#### Url Check
Submit a URL to be scanned and get the scan details
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Visibility|Scans on urlscan.io have one of three visibility levels, make sure to use the appropriate level for your submission.|False|List|public|
|Threshold|Mark entity as suspicious if the score of verdicts is equal or above the given threshold. Default is 0, in this case, we consider every scanned url as suspicious.|False|String|0|
|Create Insight|If enabled, action will create an insight containing information about entities.|False|Boolean|true|
|Only Suspicious Insight|If enabled, action will only create insight for suspicious entities. Note: "Create Insight" parameter needs to be enabled.|False|Boolean|false|
|Add Screenshot To Insight|If enabled, action will add a screenshot of the website to the insight, if it’s available.|False|Boolean|false|



##### JSON Results
```json
[{"EntityResult": {"metatags":{"values": []},"usertags":{"values": []},"task": {"domURL": "https://urlscan.io/dom/7e9cb8cb-82ce-4ef7-881a-xxxx/", "screenshotURL": "https://urlscan.io/screenshots/7e9cb8cb-82ce-4ef7-881a-xxxx.png", "uuid": "7e9cb8cb-82ce-4ef7-881a-xxxx", "url": "http://domain-example.com/f1q7qxxxx.php", "visibility": "public", "source": "12a3ddafxxx", "time": "2019-01-31T15:19:55.267Z", "reportURL": "https://urlscan.io/result/7e9cb8cb-82ce-4ef7-881a-xxxx/", "userAgent": "Mozilla/5.0 (Macintosh; Intel Mac OS X 10_13_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/67.0.3396.87 Safari/537.36", "method": "api"}, "stats": {"malicious": 0, "uniqCountries": 1, "totalLinks": 3, "secureRequests": 14, "securePercentage": 93, "adBlocked": 0, "IPv6Percentage": 50}, "page": {"city": "Los Angeles", "domain": "domain-example.com", "asn": "AS22612", "url": "http://domain-example.com/f1q7qxxxx.php", "ip": "1.1.x.x", "asnname": "NAMECHEAP-NET - Namecheap, Inc., US", "server": "nginx", "country": "US", "ptr": ""}, "lists": {"linkDomains": ["www.namecheap.com", "ap.www.namecheap.com"], "countries": ["US"], "asns": ["22612"], "servers": ["cloudflare", "nginx"], "ips": ["1.1.x.x"], "urls": ["http://domain-example.com/f1q7qxxxx.php"], "domains": ["nc-img.com"], "hashes": ["f31c0889d28c7d713f237a8cea8cfbc5cb4cba63fad767666cce2bbcxxxxx"], "certificates": [{"subjectName": "nc-img.com", "validFrom": 1534204800, "validTo": 1565827199, "issuer": "COMODO RSA Domain Validation Secure Server CA"}]},  "verdicts": {"overall": {"score": 0,"categories": [],"brands": [],"tags": [],"malicious": false,"hasVerdicts": 0},"urlscan": {"score": 0,"categories": [],"brands": [],"tags": [],"detectionDetails": [],"malicious": false},"engines": {"score": 0,"malicious": [],"benign": [],"maliciousTotal": 0,"benignTotal": 0,"verdicts": [],"enginesTotal": 0},"community": {"score": 0,"votes": [],"votesTotal": 0,"votesMalicious": 0,"votesBenign": 0,"tags": [],"categories": []}}}, "Entity": "HTTP://domain-example.COM/F1Q7QXXXX.PHP"}]
```



#### Ping
Test Connectivity
Timeout - 600 Seconds



#### Search for Scans
 Search for urlscan.io existing scans by attributes such as domains, IPs, Autonomous System (AS) numbers, hashes, etc.  The action will find public scans performed by anyone as well as unlisted and private scans performed by you or your teams.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Max Scans|Number of scans to return per entity. Default: 100, Max: 10000 (depending on subscription)|False|String|100|



##### JSON Results
```json
[{"Entity": "0.0.x.x", "EntityResult": [{"indexedAt": "2020-12-21T18:06:51.758Z", "task": {"visibility": "public", "method": "automatic", "domain": "reserve.xxxx.ca", "time": "2020-12-21T18:06:21.677Z", "source": "certstream-suspicious", "uuid": "8baedb2c-040c-4b89-ba3f-xxxx", "url": "https://reserve.xxxx.ca"}, "stats": {"uniqIPs": 4, "consoleMsgs": 1, "uniqCountries": 2, "dataLength": 39187022, "encodedDataLength": 39202573, "requests": 11}, "page": {"country": "US", "server": "nginx/1.17.1", "city": "North Bergen", "domain": "reserve.billdion.ca", "ip": "104.248.xx.xx", "mimeType": "text/html", "asnname": "DIGITALOCEAN-ASN, US", "asn": "AS14061", "url": "https://reserve.xxxx.ca/", "status": "200"}, "_id": "8baedb2c-040c-4b89-ba3f-xxxx", "sort": [1608573981677, "8baedb2c-040c-4b89-ba3f-xxxx"], "result": "https://urlscan.io/api/v1/result/8baedb2c-040c-4b89-ba3f-xxxx/", "screenshot": "https://urlscan.io/screenshots/8baedb2c-040c-4b89-ba3f-xxxxx.png"}, {"indexedAt": "2020-12-20T18:19:30.042Z", "task": {"visibility": "public", "method": "automatic", "domain": "www.user-xxxx.nl", "time": "2020-12-20T18:19:13.755Z", "source": "certstream-suspicious", "uuid": "db4b87cf-37b4-4c9a-a0e2-xxxx", "url": "https://www.user-xxxx.nl"}, "stats": {"uniqIPs": 2, "consoleMsgs": 0, "uniqCountries": 1, "dataLength": 332, "encodedDataLength": 446, "requests": 2}, "page": {"country": "NL", "server": "nginx/1.6.2", "domain": "www.xxxx.nl", "ip": "2a01:7c8:aabc:2e:xxxx:ff:xxxx:1b7d", "mimeType": "text/html", "asnname": "TRANSIP-AS Amsterdam, the Netherlands, NL", "asn": "AS20857", "url": "http://www.xxxx.nl/", "status": "200"}, "_id": "db4b87cf-37b4-4c9a-a0e2-xxxx", "sort": [1608488353755, "db4b87cf-37b4-4c9a-a0e2-xxxx"], "result": "https://urlscan.io/api/v1/result/db4b87cf-37b4-4c9a-a0e2-xxxx/", "screenshot": "https://urlscan.io/screenshots/db4b87cf-37b4-4c9a-a0e2-xxxx.png"}, {"indexedAt": "2020-12-18T14:22:50.487Z", "task": {"visibility": "public", "method": "manual", "domain": "0.0.x.x", "time": "2020-12-18T14:22:34.806Z", "uuid": "e9bccb55-d818-4433-9640-xxxx", "url": "http://0.0.x.x:4100"}, "stats": {"uniqIPs": 0, "uniqCountries": 0, "dataLength": 0, "requests": 0}, "page": {"domain": "0.0.x.x", "url": "http://0.0.x.x:4100"}, "_id": "e9bccb55-d818-4433-9640-xxxx", "sort": [1608301354806, "e9bccb55-d818-4433-9640-xxxx"], "result": "https://urlscan.io/api/v1/result/e9bccb55-d818-4433-9640-xxxx/", "screenshot": "https://urlscan.io/screenshots/e9bccb55-d818-4433-9640-xxxx.png"}, {"indexedAt": "2020-12-18T14:21:30.743Z", "task": {"visibility": "public", "method": "manual", "domain": "0.0.x.x", "time": "2020-12-18T14:21:01.428Z", "uuid": "ceab2974-1fb2-4995-8d73-xxxx", "url": "http://0.0.x.x:3030"}, "stats": {"uniqIPs": 0, "uniqCountries": 0, "dataLength": 0, "requests": 0}, "page": {"domain": "0.0.x.x", "url": "http://0.0.x.x:3030"}, "_id": "ceab2974-1fb2-4995-8d73-xxxx", "sort": [1608301261428, "ceab2974-1fb2-4995-8d73-xxxx"], "result": "https://urlscan.io/api/v1/result/ceab2974-1fb2-4995-8d73-xxxx/", "screenshot": "https://urlscan.io/screenshots/ceab2974-1fb2-4995-8d73-xxxx.png"}]}]
```



#### Get Scan Full Details
Get Scan Full Details by scan ID
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Scan ID|Get scan report using the scan ID. Comma separated values.|True|String||



##### JSON Results
```json
[{"data":{"requests":[{"request":{"requestId":"2E282E5F97XXXXXXXXAA74A14B2C42","loaderId":"2E282E5F97XXXXXXXXAA74A14B2C42","documentURL":"http://145.112.368.158/bins/test.org","request":{"url":"http://145.112.368.158/bins/test.org","method":"GET","headers":{"Upgrade-Insecure-Requests":"1","User-Agent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.61 Safari/537.36"},"mixedContentType":"none","initialPriority":"VeryHigh","referrerPolicy":"no-referrer-when-downgrade"},"timestamp":19089897.282696,"wallTime":1607875822.141159,"initiator":{"type":"other"},"type":"Document","frameId":"B51D9A02BF27XXXXXXXXBA9C296F5DD","hasUserGesture":false},"response":{"encodedDataLength":0,"dataLength":0,"requestId":"2E282E5F97XXXXXXXXAA74A14B2C42","type":"Document","response":{"url":"http://145.112.368.158/bins/test.org","status":200,"statusText":"OK","headers":{"Date":"Sun, 13 Dec 2020 16:10:22 GMT","Server":"Apache/2.2.15 (CentOS)","Last-Modified":"Sun, 13 Dec 2020 15:17:50 GMT","ETag":"\"206ea-c48c-5b65a0762b76b\"","Accept-Ranges":"bytes","Content-Length":"50316","Connection":"close","Content-Type":"text/plain; charset=UTF-8"},"mimeType":"application/octet-stream","requestHeaders":{"Host":"145.112.368.158","Connection":"keep-alive","Pragma":"no-cache","Cache-Control":"no-cache","Upgrade-Insecure-Requests":"1","User-Agent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.61 Safari/537.36","Accept":"text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9","Accept-Encoding":"gzip, deflate","Accept-Language":"en-US"},"remoteIPAddress":"145.112.368.158","remotePort":80,"fromPrefetchCache":false,"encodedDataLength":273,"timing":{"requestTime":19089897.283066,"proxyStart":-1,"proxyEnd":-1,"dnsStart":0.318,"dnsEnd":0.322,"connectStart":0.322,"connectEnd":21.482,"sslStart":-1,"sslEnd":-1,"workerStart":-1,"workerReady":-1,"workerFetchStart":-1,"workerRespondWithSettled":-1,"sendStart":21.535,"sendEnd":21.578,"pushStart":0,"pushEnd":0,"receiveHeadersEnd":299.269},"responseTime":1607875822440.743,"protocol":"http/1.1","securityState":"insecure"},"failed":{"requestId":"2E282E5F97XXXXXXXXAA74A14B2C42","timestamp":19089897.583037,"type":"Document","errorText":"net::ERR_ABORTED","canceled":true},"asn":{"ip":"145.112.368.158","asn":"47869","country":"NL","registrar":"ripencc","date":"2008-09-09","description":"NETROUTING-AS, NL","route":"185.144.156.0/22","name":"NETROUTING-AS"},"geoip":{"range":[3113262080,3113263103],"country":"US","region":"FL","eu":"0","timezone":"America/New_York","city":"Miami","ll":[25.7806,-80.1826],"metro":528,"area":1000,"country_name":"United States"},"rdns":{"ip":"145.112.368.158","ptr":"8.8.8.8"}}}],"cookies":[],"console":[],"links":[],"timing":{"beginNavigation":"2020-12-13T16:10:22.140Z"},"globals":[]},"stats":{"resourceStats":[{"count":1,"size":0,"encodedSize":0,"latency":0,"countries":["US"],"ips":["145.112.368.158"],"type":"Document","compression":"NaN","percentage":null}],"protocolStats":[{"count":1,"size":0,"encodedSize":0,"ips":["145.112.368.158"],"countries":["US"],"securityState":{},"protocol":"http/1.1"}],"tlsStats":[{"count":1,"size":0,"encodedSize":0,"ips":["145.112.368.158"],"countries":["US"],"protocols":{},"securityState":"insecure"}],"serverStats":[{"count":1,"size":0,"encodedSize":0,"ips":["145.112.368.158"],"countries":["US"],"server":"Apache/2.2.15 (CentOS)"}],"domainStats":[{"count":1,"ips":["145.112.368.158"],"domain":"145.112.368.158","size":0,"encodedSize":0,"countries":["US"],"index":0,"initiators":[],"redirects":0}],"regDomainStats":[{"count":1,"ips":["145.112.368.158"],"regDomain":"158.181","size":0,"encodedSize":0,"countries":[],"index":0,"subDomains":[],"redirects":0}],"secureRequests":0,"securePercentage":0,"IPv6Percentage":0,"uniqCountries":1,"totalLinks":0,"malicious":0,"adBlocked":0,"ipStats":[{"requests":1,"domains":["145.112.368.158"],"ip":"145.112.368.158","asn":{"ip":"145.112.368.158","asn":"47869","country":"NL","registrar":"ripencc","date":"2008-09-09","description":"NETROUTING-AS, NL","route":"185.144.156.0/22","name":"NETROUTING-AS"},"dns":{},"geoip":{"range":[3113262080,3113263103],"country":"US","region":"FL","eu":"0","timezone":"America/New_York","city":"Miami","ll":[25.7806,-80.1826],"metro":528,"area":1000,"country_name":"United States"},"size":0,"encodedSize":0,"countries":["US"],"index":0,"ipv6":false,"redirects":0,"count":null,"rdns":{"ip":"145.112.368.158","ptr":"8.8.8.8"}}]},"meta":{"processors":{"wappa":{"state":"done","data":[{"app":"CentOS","confidence":[{"pattern":"headers server /CentOS/i","confidence":100}],"confidenceTotal":100,"icon":"CentOS.png","website":"http://centos.org","categories":[{"name":"Operating Systems","priority":6}]},{"app":"Apache","confidence":[{"pattern":"headers server /(?:Apache(?:$|\\\\/([\\\\d.]+)|[^/-])|(?:^|\\\\b)HTTPD)/i","confidence":100}],"confidenceTotal":100,"version":"2.2.15","icon":"Apache.svg","website":"http://apache.org","categories":[{"name":"Web Servers","priority":8}]}]},"geoip":{"state":"done","data":[{"ip":"145.112.368.158","geoip":{"range":[3113262080,3113263103],"country":"US","region":"FL","eu":"0","timezone":"America/New_York","city":"Miami","ll":[25.7806,-80.1826],"metro":528,"area":1000,"country_name":"United States"}}]},"asn":{"state":"done","data":[{"ip":"145.112.368.158","asn":"47869","country":"NL","registrar":"ripencc","date":"2008-09-09","description":"NETROUTING-AS, NL","route":"185.144.156.0/22","name":"NETROUTING-AS"}]},"rdns":{"state":"done","data":[{"ip":"145.112.368.158","ptr":"8.8.8.8"}]},"done":{"state":"done","data":{"state":"done"}}}},"task":{"uuid":"63e1af70-7412XXXXXXX34-9970e1149949","time":"2020-12-13T16:10:22.013Z","url":"http://145.112.368.158/bins/test.org","visibility":"public","options":{"useragent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.61 Safari/537.36"},"method":"automatic","source":"urlhaus","tags":[],"userAgent":"Mozilla/5.0 (Macintosh; Intel Mac OS X 10_14_5) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/83.0.4103.61 Safari/537.36","reportURL":"https://urlscan.io/result/63e1af70-7412XXXXXXX34-9970e1149949/","screenshotURL":"https://urlscan.io/screenshots/63e1af70-7412XXXXXXX34-9970e1149949.png","domURL":"https://urlscan.io/dom/63e1af70-7412XXXXXXX34-9970e1149949/"},"page":{"url":"http://145.112.368.158/bins/test.org","domain":"145.112.368.158","country":"US","city":"Miami","server":"Apache/2.2.15 (CentOS)","ip":"145.112.368.158","ptr":"8.8.8.8","asn":"AS47869","asnname":"NETROUTING-AS, NL"},"lists":{"ips":["145.112.368.158"],"countries":["US"],"asns":["47869"],"domains":["145.112.368.158"],"servers":["Apache/2.2.15 (CentOS)"],"urls":["http://145.112.368.158/bins/test.org"],"linkDomains":[],"certificates":[],"hashes":[]},"verdicts":{"overall":{"score":0,"categories":[],"brands":[],"tags":[],"malicious":false,"hasVerdicts":0},"urlscan":{"score":0,"categories":[],"brands":[],"tags":[],"detectionDetails":[],"malicious":false},"engines":{"score":0,"malicious":[],"benign":[],"maliciousTotal":0,"benignTotal":0,"verdicts":[],"enginesTotal":0},"community":{"score":0,"votes":[],"votesTotal":0,"votesMalicious":0,"votesBenign":0,"tags":[],"categories":[]}},"Effective URL":"http://145.112.368.158/bins/test.org"}]
```









