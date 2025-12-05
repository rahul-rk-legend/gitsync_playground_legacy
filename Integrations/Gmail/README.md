
# Gmail

Secure business email, and so much more - the latest Gmail makes it easier to stay on top of the work that matters. With secure, ad-free email as a foundation, you can also chat, make voice or video calls, and stay on top of project work with shared files and tasks - all right in Gmail.

Python Version - 3
#### Parameters
|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Service Account Json File Content|The content of the service account key JSON file. You can configure either this parameter, or the Workload Identity Email parameter. To configure this parameter, provide the full content of the service account key JSON file that you have downloaded when creating a service account.|False|Password|*****|
|Workload Identity Email|The client email address of your service account.You can configure either this parameter or the Service Account JSON File Content parameter. To impersonate service accounts with workloads, grant the Service Account Token Creator role to your Google SecOps service account.|False|String||
|Default Mailbox|A default mailbox to use in the integration.|True|String||
|Verify SSL|If selected, the integration verifies that the SSL certificate for connecting to Gmail is valid. Selected by default.|False|Boolean|true|


#### Dependencies
| |
|-|
|cross/google_auth-2.32.0-py2.py3-none-any.whl|
|cross/rsa-4.9-py3-none-any.whl|
|cross/anyio-4.4.0-py3-none-any.whl|
|cross/EnvironmentCommon-1.0.2-py2.py3-none-any.whl|
|cross/httpx-0.27.2-py3-none-any.whl|
|cross/certifi-2024.7.4-py3-none-any.whl|
|cross/pyparsing-3.1.2-py3-none-any.whl|
|cross/uritemplate-4.1.1-py2.py3-none-any.whl|
|cross/TIPCommon-2.2.2-py2.py3-none-any.whl|
|cross/urllib3-2.2.2-py3-none-any.whl|
|cross/protobuf-5.27.2-cp38-abi3-manylinux2014_x86_64.whl|
|cross/annotated_types-0.7.0-py3-none-any.whl|
|cross/requests-2.32.3-py3-none-any.whl|
|cross/sniffio-1.3.1-py3-none-any.whl|
|cross/pyasn1_modules-0.4.0-py3-none-any.whl|
|cross/yarl-1.9.4-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/httplib2-0.22.0-py3-none-any.whl|
|cross/beautifulsoup4-4.12.3-py3-none-any.whl|
|cross/pydantic_core-2.20.1-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/soupsieve-2.6-py3-none-any.whl|
|cross/proto_plus-1.24.0-py3-none-any.whl|
|cross/idna-3.7-py3-none-any.whl|
|cross/pyasn1-0.6.0-py2.py3-none-any.whl|
|cross/google_api_python_client-2.137.0-py2.py3-none-any.whl|
|cross/google_api_core-2.19.1-py3-none-any.whl|
|cross/pycryptodome-3.20.0-cp35-abi3-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/charset_normalizer-3.3.2-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/cachetools-5.4.0-py3-none-any.whl|
|cross/attrs-23.2.0-py3-none-any.whl|
|cross/google_auth_httplib2-0.2.0-py2.py3-none-any.whl|
|cross/googleapis_common_protos-1.63.2-py2.py3-none-any.whl|
|cross/multidict-6.0.5-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/h11-0.14.0-py3-none-any.whl|
|cross/siemplify_html2text-2020.1.16-py3-none-any.whl|
|cross/typing_extensions-4.12.2-py3-none-any.whl|
|cross/httpcore-1.0.5-py3-none-any.whl|
|cross/aiohttp-3.9.5-cp311-cp311-manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/aiosignal-1.3.1-py3-none-any.whl|
|cross/frozenlist-1.4.1-cp311-cp311-manylinux_2_5_x86_64.manylinux1_x86_64.manylinux_2_17_x86_64.manylinux2014_x86_64.whl|
|cross/pydantic-2.8.2-py3-none-any.whl|


## Actions
#### Remove Email Label
Use the Remove Email Label action to remove a label from the specified email. Adjust the action timeout in the Google SecOps IDE accordingly. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Labels Filter|A filter condition that specifies the email labels to search for. This parameter accepts multiple values as a comma-separated string. You can search for emails with specific labels, such as label1, label2. To search for emails that don’t possess the specific label, use the following format: -label1. You can configure this parameter to search for emails with and without specific labels in one string, such as label1, -label2, label3.|False|String|Inbox|
|Internet Message ID|An internet message ID of the email to search for. This parameter accepts multiple values as a comma-separated string. If you provide the internet message ID, the action ignores the Labels Filter, Subject Filter, Sender Filter, and Time Frame (minutes) parameters.|False|String||
|Subject Filter|A filter condition that specifies the email subject to search for. This filter uses the “contains” logic and requires you to specify search items in full words. This filter doesn’t support partial matches.|False|String||
|Sender Filter|A filter condition that specifies the email sender to search for. This filter uses the “equals” logic.|False|String||
|Time Frame (minutes)|A filter condition that specifies the timeframe in minutes to search for emails.|False|String|60|
|Email Status|A status of the email to search for.|False|List|Both Read & Unread Messages|
|Label|A label to remove from an email. This parameter accepts multiple values as a comma-separated list.|True|String||



##### JSON Results
```json

```



#### Wait For Thread Reply
Use the Wait For Thread Reply action to wait for the user's reply based on an email sent using the Send Email action. This action is asynchronous. Adjust the action timeout in the Google SecOps IDE accordingly. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to wait for a reply in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Internet Message ID|The internet message ID of an email for the action to wait for. If the message was sent using the Send Email action, configure this parameter using the following placeholder: SendEmail.JSONResult|message_id. To retrieve an internet message ID, use the Search for Emails action.|True|String||
|Wait for All Recipients to Reply|If selected, the action waits for responses from all recipients until reaching timeout. Not selected by default.|False|Boolean|false|
|Fetch Response Attachments|If selected and the recipient reply contains attachments, the action retrieves email attachments and adds them as an attachment to the Case Wall in Google SecOps. Not selected by default.|False|Boolean|false|



##### JSON Results
```json
[{"Entity":"xxx@domain.com","EntityResult":{"id":"1929ea7cbb127b4f","thread_id":"1929ea6e77884359","label_ids":["UNREAD","IMPORTANT","CATEGORY_PERSONAL","INBOX"],"snippet":"Here we go again On Fri, Oct 18, 2024 at 10:03 AM &lt;yyy@domain.com&gt; wrote: 2024-10-18 09:02:09 UTC+01Test Thread Reply","history_id":"220339","internal_date":1729238629000,"message_id":"<CAFkrbWr_giG77GNkNPjFDBKBq0z8jVuh3-kQ_zEUKgMftG3j9Q@mail.gmail.com>","subject":"Re: Test Thread Reply","headers":{"delivered-to":"yyy@domain.com","received":["by 2002:a17:906:5ace:b0:a9a:343:8359 with SMTP id x14csp680914ejs;        Fri, 18 Oct 2024 01:04:09 -0700 (PDT)","from mta-8a969f.us.email.fireeyecloud.com (mta-8a969f.us.email.fireeyecloud.com. [34.223.36.10])        by mx.google.com with ESMTPS id d9443c01a7336-20e5a71df00si12367765ad.15.2024.10.18.01.04.09        for <yyy@domain.com>        (version=TLS1_3 cipher=TLS_AES_256_GCM_SHA384 bits=256/256);        Fri, 18 Oct 2024 01:04:09 -0700 (PDT)","from [127.0.0.1] ([127.0.0.1:22606] helo=smtp-injection-worker) by prd08-usw2-01 (envelope-from <xxx@domain.com>) (ecelerity 4.7.0.20111 r(msys-ecelerity:tags/4.7.0-ga^0)) with ESMTP id 5D/22-02501-97612176; Fri, 18 Oct 2024 08:04:09 +0000","from mail-yb1-f172.google.com (mail-yb1-f172.google.com [209.85.219.172]) by prd08-usw2-18 (envelope-from <xxx@domain.com>) FireEye ETP with ESMTPS (cipher=TLS_AES_128_GCM_SHA256) id 3yWgury-62026-08g51CE246854761217623602d2; batch_id 51/CE-24685-47612176; Fri, 18 Oct 2024 08:04:05 +0000 (UTC)","by mail-yb1-f172.google.com with SMTP id 3f1490d57ef6-e292926104bso1655513276.0        for <yyy@domain.com>; Fri, 18 Oct 2024 01:04:04 -0700 (PDT)"],"x-google-smtp-source":"AGHT+IGgg56MVu6USqfl7GxqmFGLGUiRSfSHqruUf7IZ0PCqqnQYxWX8SWOkZgOLpMpulvmUoQMw","x-received":["by 2002:a17:902:da88:b0:20b:9e14:c138 with SMTP id d9443c01a7336-20e5a7662f1mr19628455ad.23.1729238649556;        Fri, 18 Oct 2024 01:04:09 -0700 (PDT)","by 2002:a05:690c:6609:b0:6dd:c679:f108 with SMTP id 00721157ae682-6e5bfbed526mr13995077b3.5.1729238641604; Fri, 18 Oct 2024 01:04:01 -0700 (PDT)"],"arc-seal":"i=1; a=rsa-sha256; t=1729238649; cv=none;        d=google.com; s=arc-20240605;        b=lb9VvKhc8TP9jhyO5X7mZ1uimN/L7rQHYBatrexHMymmFhFyB2c73+JAfy4eiQbUar         IS0+rxIrsQNd9qEsm4k5cJqasLyvrfRoO0IqOTM0DFGFRJmEzhxb4mGVB7fS7WrHUitl         4Gi1uMVwkRFVsoGIGLAmbKQ80VhXWlsgOya+OJsmOW7yYDd9+z63m1uyHItYX/hlZCcZ         xwKxra2oSW3eiEZcoLv8gJr+B3B6U6lsYXHoj9l78SHF36GE7lvMQDElIhowT2vbX53B         14oa5UO9CcayTDmfhy5QfhMkcErhxM5X66S7zocbQquzsREb0LHgCFHnbLaxUfKLMF7I         CDAA==","arc-message-signature":"i=1; a=rsa-sha256; c=relaxed/relaxed; d=google.com; s=arc-20240605;        h=to:subject:message-id:date:from:reply-to:in-reply-to:references         :mime-version:dkim-signature;        bh=kMphU6oi06M0ZCkCip6kdLRxXNQkZDYyIX+n96oYBcs=;        fh=T6FkELcvpAH6I3xvEnQ5AiwAiU2r5nRZKl7LC76j5mE=;        b=I6gzkdFkvEviSIPCPbzLW6/dFKIYtKkFg2F92Oq7avbiPlX54aIiFuAlCxMZhzDuIB         IoIJo/A4uOYOw/fAZjUFWU0OI9sqHSE/8QO6pflyARFxPowQH/EY+IsHTxgmgCzAY+t1         ThazWM16ptZrI7l9So04LW3uLXvhc0eMLJxE85wByYnst6xSYV1GoPQcbnyfv4NRu+VD         FkbR+niG2cYy6s4KOqmRcXjVkXjFPwS9hhVujmq9Gz2aE07EQyqc/d0n7nj51Aidmw0H         LZkGen1Fg7j0PSNo0Bd9IJbFGTzc0ciObw2ZLZbg1XVB8YvWr3ZVA0o3tJylh3Z/9Zhx         lcDQ==;        dara=google.com","arc-authentication-results":"i=1; mx.google.com;       dkim=pass header.i=@google.com header.s=20230601 header.b=\"held/nE6\";       spf=pass (google.com: domain of xxx@domain.com designates 209.85.219.172 as permitted sender) smtp.mailfrom=xxx@domain.com;       dara=pass header.i=@smplylab.com","return-path":["<xxx@domain.com>","<xxx@domain.com>"],"received-spf":"pass (google.com: domain of xxx@domain.com designates 209.85.219.172 as permitted sender) client-ip=209.85.219.172;","authentication-results":["mx.google.com;       dkim=pass header.i=@google.com header.s=20230601 header.b=\"held/nE6\";       spf=pass (google.com: domain of xxx@domain.com designates 209.85.219.172 as permitted sender) smtp.mailfrom=xxx@domain.com;       dara=pass header.i=@smplylab.com","mta-643920.us.email.fireeyecloud.com; dmarc=pass (p=reject; dis=none) header.from=xwf.google.com"],"x-fe-etp-sender-ip":"209.85.219.172","x-fe-etp-connecting-ip":"209.85.219.172","dkim-signature":"v=1; a=rsa-sha256; c=relaxed/relaxed;        d=google.com; s=20230601; t=1729238643; x=1729843443; darn=smplylab.com;        h=to:subject:message-id:date:from:reply-to:in-reply-to:references         :mime-version:from:to:cc:subject:date:message-id:reply-to;        bh=kMphU6oi06M0ZCkCip6kdLRxXNQkZDYyIX+n96oYBcs=;        b=held/nE6bTEerFdWefmEIIHXQ1BnPaIU7NhEwx4y2Rz00cSVJGUMGJKx6g7rlxVkko         yPuVzpz9pPY1vMrzw8dofVwDYVO3Kehr9sfUf5kerzOYhnDefKAj5JkPcuJ1ore/LeOm         6lBQyQawE2xBRMC3y2CSIb1RmpOkN7ateO6p3cLXtu+1bsXJKbXM7GcbImr1mcjAobzP         PZe+7dcZFV922qUKpYWnkjgeG4FOl1HOjA4f7R7XU3cOlkRwnNbfMt4rD5xe6hYWqeMb         3pEzH5LZxbURKUj2XNLFL2NR6fa6Ogtqko7tbhR4EgNBVhdrqRtj+c9kuyx+NNXdFgY7         ohEw==","x-google-dkim-signature":"v=1; a=rsa-sha256; c=relaxed/relaxed;        d=1e100.net; s=20230601; t=1729238643; x=1729843443;        h=to:subject:message-id:date:from:reply-to:in-reply-to:references         :mime-version:x-gm-message-state:from:to:cc:subject:date:message-id         :reply-to;        bh=kMphU6oi06M0ZCkCip6kdLRxXNQkZDYyIX+n96oYBcs=;        b=ARq8DmLFVf7GwQZ26lMzd7T5MkpLkJp7rfTEhUWXLIUw+8YpCap8j5XTFOHwE2bK1Y         82BxgRDhuXV1nqSJeLIy9L1eylSbES/qH7qTpCI7z+8/PlKpXBtCub1Rtajn9hOjWc6d         XAAbbpWD/cCSXIJdNAKU8awre5C5MZ65yscEhXbuO+LJiKmN03wTAEtp9uUqdZI4oCnH         EDhlZ7PUMnWnSEXm097U2vnEAsJndvG5GRsJtskXgc8vFa6wAqDkCYV7qT6GbpNaM1VE         A1I6UzFXHhPCNuSf7A2CTwVpW/iwZ3fl02kHrNk7zpQxVHXA/gG8erFF4t25CZogMGwO         zJoA==","x-gm-message-state":"AOJu0YyyK1WbsQJIb3JXMmsCZdUwPjVC0IcbFCxxA41LJ8aXu771VU6n 1Rdre2wzK1ldSemc3n1MFi4uIuAzO3FHFO2izzYiBfRf9IHHzDFfL5jCDzzsARs6nGmNWyXhwUJ 9H4dbOkn5BwxTIoO96heyBsLyKl2i57WmvSRVXJRi0CxW4aBjLGmK","mime-version":"1.0","references":"<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>","in-reply-to":"<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>","reply-to":"xxx@domain.com","from":"\"Idris Elba (xWF)\" <xxx@domain.com>","date":"Fri, 18 Oct 2024 10:03:49 +0200","message-id":"<CAFkrbWr_giG77GNkNPjFDBKBq0z8jVuh3-kQ_zEUKgMftG3j9Q@mail.gmail.com>","subject":"Re: Test Thread Reply","to":"yyy@domain.com","content-type":"multipart/mixed; boundary=\"000000000000f8f0090624bbbefc\"","x-fe-etp-metadata":"eyAidGlkIjogIjN5V2d1cnktNjIwMjYtMDhnNTFDRTI0Njg1NDc2MTIxNzYyMzYwMmQyIiwgImFj Y2VwdGVkX3RpbWVzdGFtcCI6ICIyMDI0MTAxODA4MDQwNCIsICJhY2NlcHRlZF90aW1lc3RhbXBf ZXBvY2giOiAiMTcyOTIzODY0NCIsICJkb21haW5fbmFtZSI6ICJzbXBseWxhYi5jb20iLCAiYXR0 X2NvdW50IjogLTIsICJzcmNfaXAiOiAiMjA5Ljg1LjIxOS4xNzIiIH0="},"mimetype":"multipart/mixed","text_bodies":["Here we go again\r\n\r\nOn Fri, Oct 18, 2024 at 10:03AM <yyy@domain.com> wrote:\r\n\r\n> 2024-10-18 09:02:09 UTC+01Test Thread Reply\r\n"],"html_bodies":["<div dir=\"ltr\">Here we go again</div><br><div class=\"gmail_quote\"><div dir=\"ltr\" class=\"gmail_attr\">On Fri, Oct 18, 2024 at 10:03AM &lt;<a href=\"mailto:yyy@domain.com\">yyy@domain.com</a>&gt; wrote:<br></div><blockquote class=\"gmail_quote\" style=\"margin:0px 0px 0px 0.8ex;border-left:1px solid rgb(204,204,204);padding-left:1ex\">2024-10-18 09:02:09 UTC+01Test Thread Reply</blockquote></div>\r\n"],"file_attachments":["Screenshot 2024-10-17 7.27.01 PM.png"],"date":"Fri, 18 Oct 2024 10:03:49 +0200","from":"xxx@domain.com","to":"yyy@domain.com","cc":[],"bcc":[],"in-reply-to":"<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>","reply-to":["xxx@domain.com"]}},{"Entity":"zzz@domain.com","EntityResult":{"id":"1929eac4c2ed4fac","thread_id":"1929ea6e77884359","label_ids":["UNREAD","IMPORTANT","CATEGORY_PERSONAL","INBOX"],"snippet":"TEst a reply From: yyy@domain.com &lt;yyy@domain.com&gt; Sent: Friday, October 18, 2024 10:03 AM To: xxx@domain.com &lt;xxx@domain.com&gt; Cc: Idris Elba &lt;","history_id":"220465","internal_date":1729238926000,"message_id":"<PUZPR04MB6295B60864A0A5EA942C217F95402@PUZPR04MB6295.apcprd04.prod.outlook.com>","subject":"Re: Test Thread Reply","headers":{"delivered-to":"yyy@domain.com","received":["by 2002:a17:906:5ace:b0:a9a:343:8359 with SMTP id x14csp683094ejs;        Fri, 18 Oct 2024 01:09:05 -0700 (PDT)","from mta-231cee.us.email.fireeyecloud.com (mta-231cee.us.email.fireeyecloud.com. [34.223.36.100])        by mx.google.com with ESMTPS id 41be03b00d2f7-7eacc2b99b6si1280037a12.869.2024.10.18.01.09.04        for <yyy@domain.com>        (version=TLS1_3 cipher=TLS_AES_256_GCM_SHA384 bits=256/256);        Fri, 18 Oct 2024 01:09:05 -0700 (PDT)","from [127.0.0.1] ([127.0.0.1:14734] helo=smtp-injection-worker) by prd08-usw2-17 (envelope-from <zzz@domain.com>) (ecelerity 4.7.0.20111 r(msys-ecelerity:tags/4.7.0-ga^0)) with ESMTP id 9E/E9-30849-0A712176; Fri, 18 Oct 2024 08:09:04 +0000","from SEYPR02CU001.outbound.protection.outlook.com (mail-koreacentralazon11013009.outbound.protection.outlook.com [40.107.44.9]) by prd08-usw2-19 (envelope-from <zzz@domain.com>) FireEye ETP with ESMTPS (cipher=ECDHE-RSA-AES256-GCM-SHA384) id 3yWgurC-62026-08gBDFE2453199712176344849e; batch_id BD/FE-24531-99712176; Fri, 18 Oct 2024 08:08:58 +0000 (UTC)","from SGBP274CA0016.SGPP274.PROD.OUTLOOK.COM (2603:1096:4:b0::28) by SEYPR04MB5906.apcprd04.prod.outlook.com (2603:1096:101:6a::6) with Microsoft SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.8069.18; Fri, 18 Oct 2024 08:08:53 +0000","from SG2PEPF000B66CE.apcprd03.prod.outlook.com (2603:1096:4:b0:cafe::fb) by SGBP274CA0016.outlook.office365.com (2603:1096:4:b0::28) with Microsoft SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.8069.21 via Frontend Transport; Fri, 18 Oct 2024 08:08:52 +0000","from mail.ds.dlp.protect.symantec.com (144.49.247.101) by SG2PEPF000B66CE.mail.protection.outlook.com (10.167.240.21) with Microsoft SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.8069.17 via Frontend Transport; Fri, 18 Oct 2024 08:08:51 +0000","from PUZPR04MB6295.apcprd04.prod.outlook.com (2603:1096:301:100::14) by JH0PR04MB7023.apcprd04.prod.outlook.com (2603:1096:990:2d::6) with Microsoft SMTP Server (version=TLS1_2, cipher=TLS_ECDHE_RSA_WITH_AES_256_GCM_SHA384) id 15.20.8069.19; Fri, 18 Oct 2024 08:08:46 +0000","from PUZPR04MB6295.apcprd04.prod.outlook.com ([fe80::1991:b2fa:b4f6:5893]) by PUZPR04MB6295.apcprd04.prod.outlook.com ([fe80::1991:b2fa:b4f6:5893%6]) with mapi id 15.20.8048.020; Fri, 18 Oct 2024 08:08:46 +0000"],"x-google-smtp-source":"AGHT+IG4/nmZictJ8sskTbajsGMWPMo2mMkK0prktzhU2KtXAf+wlff3x8F5l1HqvMH6yEvv65Zu","x-received":"by 2002:a05:6a21:458a:b0:1d8:d6aa:995d with SMTP id adf61e73a8af0-1d92c4a535bmr2595092637.1.1729238945414;        Fri, 18 Oct 2024 01:09:05 -0700 (PDT)","arc-seal":["i=3; a=rsa-sha256; t=1729238945; cv=pass;        d=google.com; s=arc-20240605;        b=hJDacogrp3zBxbTgfjq0d5cZa5nGYLlNQ5VLQJoch1ZnlKf/mZUJ0KrhsgumOVncE7         ynUbcLU6jFPn+/rBk+RJPVNwP6WkxSX5+AhMB15IaV5eIf1qdOc29TbxVe5ktSDx80v9         lLXAGn+YneTQ6jXCeSdogC5/A92iMkaUUERiaUka1HzFbNhfnTPBOamgb88/SkXBJJA2         9QIhvac3mBAA2YO4rWvuTKMKYt1jrosyCASzvsXg+x/m4kJFFOPWqhv5suuDAB9oomM9         4oYF+MA0FBEHWdNB3ZSz4GVVc5q9NGuAIqR4zW4PLYJYspiHjKdGEkO97WAEUVlwMPF8         JDiQ==","i=2; a=rsa-sha256; s=arcselector10001; d=microsoft.com; cv=pass; b=e5F4Bv++8A+pxlAZcPn8KtxNN2R+Lwfm0x4PjzViyDVbLkfsJ4bLMZJCNELuCa4tJwX71DsRt0THqSlspi6Q6e5IF7RwuhRQYUtMP7mMY0vAvPeeCQx8aFha9xIiADZRYreNQfFJcQDutUPXR2JIcpEQhaNnOCcunleNgZ5D31GM4N3LezkejYRjVX3O6AXDU2gbhTgcYf6N0EyyOZi21cCM1E00F03vY6GlgDqcnsKXRQkz9byvqGCWsmjQWlKT6vUgIryAUh9LDn3sbg802dGZze0FElgjVUaObYn717miK6eA+qhGhMLr/6Jinfx+uFOMAvcv5x/NZYzq+24NGQ==","i=1; a=rsa-sha256; s=arcselector10001; d=microsoft.com; cv=none; b=Mr3UbcyIQfWdnXzcCAOJ7pNChVwsGLztX32Y+c9LdZ2D6ReXiVBTD3GpgIKt0FG0Jg30B+oXhlT5nqsnl2p6tXCMT7TB2JDowCfQ44eq1oLZdCJ3bqh2YB9H5+gclaZDBI4LvDXxJFBwmh8qI46me5oPplP68mhLxi2R6xr2P4TnC5dJaGAkMWHW1N/PDYg6ojposxAiSwFAFk+sJWdhN2tU2W3kPbmF3AJFWbiXqjKgZt5FxNM6/MjfwprNdTcsDsIn+k+Yc7ockSwvwrYiLZojIM3uEwkENq6wwtNphBgzl5ABxGlMjSav0294E70KoXIak7mSzAitC51/1q07Xw=="],"arc-message-signature":["i=3; a=rsa-sha256; c=relaxed/relaxed; d=google.com; s=arc-20240605;        h=mime-version:authentication-results-original:msip_labels         :content-language:accept-language:in-reply-to:references:message-id         :date:thread-index:thread-topic:subject:to:from:dkim-signature         :dkim-signature;        bh=40rUeZcs77HCdR9M+aOAWER3XvQSq4tPYJ/2xf9pPOQ=;        fh=60ekULTQj6lvUOTJt/npkxYbNU1zbqd1eJ56jdEkHVc=;        b=UosRfan4r7WrYa44aIsM+iEFC2cMy7f/cSELm+QCBNO14dsgVfzvKl5VbiFWFKH1EJ         UWrI9lD73C/aD3OOsMU8nDPd0ZJqxaUQ0lGfLudoDct75iCtQMunxIVXrdJjGkbu9vg9         5f7+5z2K9Sfq8RHPKFKOKWLTvwko622P/OGlEnTyHu95M5wZgGcmDll3d1Tvom+m5ptu         KAkJ+rE1By+mZnB/nnsJ6Ddi9K1y5+arxVjSRMeakxKH/1fyEt6oWJwqv72PRTr5KtGE         dqYXX0OBKfqbIvcx7saA+BcTnfp2qcS9dodA6Q57PvwECfIY+nlKLcGRK6mk8TuUt+SQ         9hxw==;        dara=google.com","i=2; a=rsa-sha256; c=relaxed/relaxed; d=microsoft.com; s=arcselector10001; h=From:Date:Subject:Message-ID:Content-Type:MIME-Version:X-MS-Exchange-AntiSpam-MessageData-ChunkCount:X-MS-Exchange-AntiSpam-MessageData-0:X-MS-Exchange-AntiSpam-MessageData-1; bh=40rUeZcs77HCdR9M+aOAWER3XvQSq4tPYJ/2xf9pPOQ=; b=SXi+7dGEHKeHepU6YIdTz3mWCfErW9FekU6hG6BxK2Fwrme7ii7f0uzEWTA98/Hb7AmmQMcj7nYLTqp5nBGKyYw7YAutnR+7u/fk7DIMJtzzy9TvOqsaRaekq2aopnDgZL/wPePLYQJbtKjyE76MxvKp2knQ4st4At0LP0AHTZxeAZLcE85GRH85R1K8J9RTcadP6lDiTwJx8NhybeVyPfYGnpiJIV+fZ8f7wIl9ajI6x0Fv7OCq7XByueufLVHMuEQenGB7K5OjRQKfxBv0PF5x3TJFfiW35HAsGB5vgr1pokNXHLylP6JeAeyJiTpgV71GD0DUWZJ8H40JeWhWlQ==","i=1; a=rsa-sha256; c=relaxed/relaxed; d=microsoft.com; s=arcselector10001; h=From:Date:Subject:Message-ID:Content-Type:MIME-Version:X-MS-Exchange-AntiSpam-MessageData-ChunkCount:X-MS-Exchange-AntiSpam-MessageData-0:X-MS-Exchange-AntiSpam-MessageData-1; bh=40rUeZcs77HCdR9M+aOAWER3XvQSq4tPYJ/2xf9pPOQ=; b=hDwKTu3OAl4xuLXDuFl4ZV7jLPWZOy+rOg95G4Qd6E0mU0t2dsKahsWKRT+oocu4LmD+tAzZRabU/spVp9ChwkXpApuITC0M4kZGmvG/cdssPkDM/jDE7Ktgja8VlfEq1Wi6j9+ohW0JvP6QJjMXL5avBV26/rndAj7w9j/Lk5NmzvOtubUO4nEuvXL/8ySoerGzCUrRT+ewk5m7amP+edzsRmY1FFbxCVJvsyxfFVRjiVfidlCi2tEYYRJ5MNY6MdpUvbySxl1F5ANJIOfA2HJ0vhRdKwnxuZg54i1fciOUbbZEqlnjY7qAe10CNZA3aIAAj9Q8dwu6lwFQEkqKcA=="],"arc-authentication-results":["i=3; mx.google.com;       dkim=pass header.i=@hcltech.com header.s=selector1 header.b=T70h5Pyh;       dkim=pass header.i=@hcltech.com header.s=selector1 header.b=T70h5Pyh;       arc=pass (i=2 dkim=pass dkdomain=hcltech.com dmarc=pass fromdomain=hcltech.com);       spf=pass (google.com: domain of zzz@domain.com designates 40.107.44.9 as permitted sender) smtp.mailfrom=zzz@domain.com","i=2; mx.microsoft.com 1; spf=fail (sender ip is 144.49.247.101) smtp.rcpttodomain=smplylab.com smtp.mailfrom=hcltech.com; dmarc=pass (p=reject sp=reject pct=100) action=none header.from=hcltech.com; dkim=pass (signature was verified) header.d=hcltech.com; arc=pass (0 oda=1 ltdi=1 spf=[1,1,smtp.mailfrom=hcltech.com] dkim=[1,1,header.d=hcltech.com] dmarc=[1,1,header.from=hcltech.com])","i=1; mx.microsoft.com 1; spf=pass smtp.mailfrom=hcltech.com; dmarc=pass action=none header.from=hcltech.com; dkim=pass header.d=hcltech.com; arc=none"],"return-path":["<zzz@domain.com>","<zzz@domain.com>"],"received-spf":["pass (google.com: domain of zzz@domain.com designates 40.107.44.9 as permitted sender) client-ip=40.107.44.9;","Fail (protection.outlook.com: domain of hcltech.com does not designate 144.49.247.101 as permitted sender) receiver=protection.outlook.com; client-ip=144.49.247.101; helo=mail.ds.dlp.protect.symantec.com;"],"authentication-results":["mx.google.com;       dkim=pass header.i=@hcltech.com header.s=selector1 header.b=T70h5Pyh;       dkim=pass header.i=@hcltech.com header.s=selector1 header.b=T70h5Pyh;       arc=pass (i=2 dkim=pass dkdomain=hcltech.com dmarc=pass fromdomain=hcltech.com);       spf=pass (google.com: domain of zzz@domain.com designates 40.107.44.9 as permitted sender) smtp.mailfrom=zzz@domain.com","mta-8a969f.us.email.fireeyecloud.com; dmarc=pass (p=reject; dis=none) header.from=hcltech.com"],"x-fe-etp-sender-ip":"40.107.44.9","x-fe-etp-connecting-ip":"40.107.44.9","dkim-signature":["v=1; a=rsa-sha256; c=relaxed/relaxed; d=hcltech.com; s=selector1; h=From:Date:Subject:Message-ID:Content-Type:MIME-Version:X-MS-Exchange-SenderADCheck; bh=40rUeZcs77HCdR9M+aOAWER3XvQSq4tPYJ/2xf9pPOQ=; b=T70h5PyhgrzzAChLuIFiyrOZuMsIllkUUkXN3o4cPQVb9zkAihS72K4s1luFgFpvUON2YXNIn4r34TrmFh1grjQUJy22hoTR3qy2kQPksiJDS9X85EyILuScDm+b54tQ15p8P+YSgrz9laXJt8rEBmBZtQGJF8SRuoeSe5oKjwU97r6DMbb74fFx9jcxzYM40toLulhgcK/0BK9fgG5cnhSkh3mKUXnVPAGbD2ggXVC5LfYvlRGIgI7lGCcYtwCO98RXCB4AT0lNo/zjDdDZIKvxCkeOXp9XtbX7dQBjI9rFsvhqB20MwII8PMdoquYuuZIfKnODLJFNudEg+SRebA==","v=1; a=rsa-sha256; c=relaxed/relaxed; d=hcltech.com; s=selector1; h=From:Date:Subject:Message-ID:Content-Type:MIME-Version:X-MS-Exchange-SenderADCheck; bh=40rUeZcs77HCdR9M+aOAWER3XvQSq4tPYJ/2xf9pPOQ=; b=T70h5PyhgrzzAChLuIFiyrOZuMsIllkUUkXN3o4cPQVb9zkAihS72K4s1luFgFpvUON2YXNIn4r34TrmFh1grjQUJy22hoTR3qy2kQPksiJDS9X85EyILuScDm+b54tQ15p8P+YSgrz9laXJt8rEBmBZtQGJF8SRuoeSe5oKjwU97r6DMbb74fFx9jcxzYM40toLulhgcK/0BK9fgG5cnhSkh3mKUXnVPAGbD2ggXVC5LfYvlRGIgI7lGCcYtwCO98RXCB4AT0lNo/zjDdDZIKvxCkeOXp9XtbX7dQBjI9rFsvhqB20MwII8PMdoquYuuZIfKnODLJFNudEg+SRebA=="],"x-ms-exchange-authentication-results":"spf=fail (sender IP is 144.49.247.101) smtp.mailfrom=hcltech.com; dkim=pass (signature was verified) header.d=hcltech.com;dmarc=pass action=none header.from=hcltech.com;","x-cfilter-loop":"Reflected","from":"Idris Elba <zzz@domain.com>","to":"\"yyy@domain.com\" <yyy@domain.com>","subject":"Re: Test Thread Reply","thread-topic":"Test Thread Reply","thread-index":"AQHbITQxy/BfjOoZwUiZFeH2MS6KebKMJ2yD","date":"Fri, 18 Oct 2024 08:08:46 +0000","message-id":"<PUZPR04MB6295B60864A0A5EA942C217F95402@PUZPR04MB6295.apcprd04.prod.outlook.com>","references":"<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>","in-reply-to":"<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>","accept-language":"en-US","content-language":"en-US","x-ms-has-attach":"","x-ms-tnef-correlator":"","msip_labels":"","authentication-results-original":"dkim=none (message not signed) header.d=none;dmarc=none action=none header.from=hcltech.com;","x-ms-traffictypediagnostic":"PUZPR04MB6295:EE_|JH0PR04MB7023:EE_|SG2PEPF000B66CE:EE_|SEYPR04MB5906:EE_","x-ms-office365-filtering-correlation-id":"632c0232-dc67-465d-86df-08dcef4c1aad","x-detectorid-processed":"7a3ff160-c3d4-11eb-a2f1-967d7d39dbda","x-ms-exchange-senderadcheck":"1","x-ms-exchange-antispam-relay":"0","x-microsoft-antispam-untrusted":"BCL:0;ARA:13230040|366016|1800799024|376014|8096899003|38070700018;","x-microsoft-antispam-message-info-original":"JDRWJ6dmbV8WMnySoIoLFxg0+yZxUHbSSIn55ftGqxFVFWaut2MS0NzMz9H5yWha26uCxBw7/8pC4k8FMjjv1tfO9bm8g+SmgbT1HYMY5I8im5KVEGBoMr8VK8KP5NzXXjXGhOvsU9zU6JvCtC5KN7VP2uUlGHJOw5QSTEFBg7XH/sK390HRANJ01vz2ghdQ8Qh6GV6w4W/6g+Vs3aK6Oo/v0z9OddWDcXETvrrIToT6aB48ihFlNBlM7FXIyojmX7SpAHmioro9exvzCHHuO8dURETfK9iDyeBklk1JcauGOofGfm6I9BiDlh+0ZIWPttXSvze6wGVgcldizEH11dni1w4vtkgatFOHVAm70QcyPmRdS4LS7oO6ihwvU2osNJfieAVEAO84xYhnjkcsTsXsgqystvS1elmEa36Wp6Jig+/vv7rWMLm5HpkX1tejujDdrWmwcuJSHpMIl5nnOL5+p9Uy908y/NgCwvBbxYG+9PtHeTlSdXHzDszsfy/aag9IvO/eRrZoXfF9rGjP1B899AcIm+u4AL/eJGha8KCWbI6pxLuT1gGo/P2ReunyMD/pXJJNjEfkVKFXjIGrsYSbgU97MsiSFO/4oFcXJuyE9EcI791IPkhxi3ojJeeZItqodaXf62VkxeiIM02GokAzon5B3fRJDH14sGEPKWPKpeLoHwgwg/ZrnX99hKMjautLiBYKWzs8885BQB8dkl0cBPOKcsMnHiOWOzj3gdgmcmd3pGzDQrXjUew44wTQDmAm7K+a93C/9ZbR84Dszw+7wgty+y6qELkH6nZEjpWiIt+kKebY1sC2OyHwWESTBfOAFhq0+7ZTGYqK84a4e8EIJR4XMwDSlEZz7Prox0oAp1SiUuZYtijva1jCbOOJWMia+8eE6tULWTId4/ZNNCwtHBS0NbRWuvzx6iKPVoDBxOLCGNSnyWRyEYtTligaNqQ4rTQePZjtWf0dOlCQkWr2d6uiLvkfwBYx2vB+qRrm2b394VGpxCW2FJuCLkz11s1z3RItjQ+Igp4qkGYR5ZpzVXFTPEOGwdcb87gWW3Pz+jIQP7azR3q6XIWY/4rMAhN2tN0JcA+HbcDW+s48mnmNZIsU0zg0ZIQBsDIo0NUMt37ByHvNVbsKcaQvmBh5PdRQ+uIv/7HsHSf+7EOrZz8hxiNer87b/tCdAgDcYp7PqvRVRHUe2yHPD7fEpSNvZmt/pooorunkF8yxRLcT4nwZQQ+ZIGv8haboWFiIQe5FGdz5H9zp7qGoAtoUx6qBKZeytBjCtNo7AvkeRGeiXkevDRvS/Yz6Bmme416rLUPZ31ekoq5w2pgF2zfHhiNxIxOrrxMray4z00y8lEUl2R0FsW92yEiW7OhHKTAOxMI=","x-forefront-antispam-report-untrusted":"CIP:255.255.255.255;CTRY:;LANG:en;SCL:1;SRV:;IPV:NLI;SFV:NSPM;H:PUZPR04MB6295.apcprd04.prod.outlook.com;PTR:;CAT:NONE;SFS:(13230040)(366016)(1800799024)(376014)(8096899003)(38070700018);DIR:OUT;SFP:1101;","content-type":"multipart/alternative; boundary=\"_000_PUZPR04MB6295B60864A0A5EA942C217F95402PUZPR04MB6295apcp_\"","mime-version":"1.0","x-ms-exchange-transport-crosstenantheadersstamped":["JH0PR04MB7023","SEYPR04MB5906"],"x-eopattributedmessage":"0","x-ms-exchange-transport-crosstenantheadersstripped":"SG2PEPF000B66CE.apcprd03.prod.outlook.com","x-ms-publictraffictype":"Email","x-ms-office365-filtering-correlation-id-prvs":"db44ca06-8422-455c-78d2-08dcef4c1709","x-microsoft-antispam":"BCL:0;ARA:13230040|35042699022|82310400026|1800799024|36860700013|376014|8096899003;","x-microsoft-antispam-message-info":"XGsMLufGCKWS3wP86XUkII0UxKjUqxycoL6kfRsTRTGliTr51SVcb/P+vPm0jFj+aikJXR6IrnhaW7m75AL6gmmWQNSnNDn3lxgNrJfUYpNmEZNYcpxyjogP0qlU+HJUQ1ZDJ5WHulncsAm/xs3L8XAPRz8ZArQNVYrl17GXrtkhxxx8T40VjRL2c68872vEaEc1MFG+qOkiVed5ahz0VrI3l2VG2qVYjcgWiiEYmQrH/zlnisfwMBAbfE4AplxzD95j/+IsJQxjOyxGhKiVc0GX9CYqrZFkT4b2cwp/5hEd04a1kCL3E3cpzzveci+I3+NoJ78elXEYsxO2VbtXASgVM39g0lGT4mbRWX7LA8j9d/513U3p4J/2jAFRO7AkHT1a/TeyjYqqctyf4Y3dgEUoKIChHzUNEPGkpduWfLg4rqtDolIAX8NxV5WOnSKpCBAHQilMnNRShk+VtKEoQ4fURcTXEmJ0PcXTbOEXbh5ud1yWhMX4/qJ7vhi1hEEU2aTw2SJGlQrYuJlsU9AvcoeHQtqyIZFK4fIbcxyvD9GAqjuP5tc6CAOdQD2RE5oTI1A5cEin7Jgmm3WVLkKYLFECD1U5l0iLBBAoLG1uksNmMNgfWAZEA4apAUtx7Q5g7iRZuwfP1cp0OLje9Unkht5GcPNKIoq1vRkUn9OgabARxrFHgTEzfi62+l/mGVgXKe9fGBitH9hwKOckKrlDBWm60xqUomzt/niUVXz73PPM8sBG7xaubmFAoQg0aCtUXs2qL84s9I2yRwqLJvCwtXzDKcznX0LQAYw2qgAQLadTkKIvuQB9eeRU0dKo1WwXOo3MWvggMjHgssMDSPm6bkj63Y8r3l7KelpeY1Y+shCWX3F0nBvSOPFPCDim5Z7KC1EyUsClek/FksaSWsq4y9dL+rKSRxMsVJI1mE8DOTUZ5CV3XFVhW8CA83uu7LuPV/2YbwLz1+RlXoVA5ZUofRwQWzIWZSqlLtRe65zTlOS+ifVIkOa0+4d5AjtYrTOFxLJ1SrfS/5+sa0iRx3c7khcm2q+uAE0rNrSl75r+eFxn45Nq/NMO8mp0ydNyjlXApuICnjZ/DwN2TeThUaO9Wvho6D5Zo9PdDHGIyIcYYvCWfcVjKeSNTqXuMGIIdpAEdb4AUe4GyCreJSV5nJSET61gA2EPo+Gf23h8qJ2JUr2pr1JEUizO+x2sOdbA5PhTs0xwEWNGgY8xQXV1j7Ix2qvGKn43z1gh20md8FMQpwg24y0VnfFu46rVuTwa2l40qZe4uooQPSCjotWmhnbZnQUk0SbHbftpj1H6pAhauuChwuVbv1eV/w71mfDHvEQPmwjFn/ryAgzPX9ChNT/Shf/5SXUE2w7yaaLFKqsJ69yxjA9iV6CWILC976RQwncm7P8kYno/reK2pEOjjizjVw==","x-forefront-antispam-report":"CIP:144.49.247.101;CTRY:US;LANG:en;SCL:1;SRV:;IPV:NLI;SFV:NSPM;H:mail.ds.dlp.protect.symantec.com;PTR:InfoDomainNonexistent;CAT:NONE;SFS:(13230040)(35042699022)(82310400026)(1800799024)(36860700013)(376014)(8096899003);DIR:OUT;SFP:1101;","x-originatororg":"hcltech.com","x-ms-exchange-crosstenant-originalarrivaltime":"18 Oct 2024 08:08:51.4212 (UTC)","x-ms-exchange-crosstenant-network-message-id":"632c0232-dc67-465d-86df-08dcef4c1aad","x-ms-exchange-crosstenant-id":"189de737-c93a-4f5a-8b68-6f4ca9941912","x-ms-exchange-crosstenant-originalattributedtenantconnectingip":"TenantId=189de737-c93a-4f5a-8b68-6f4ca9941912;Ip=[144.49.247.101];Helo=[mail.ds.dlp.protect.symantec.com]","x-ms-exchange-crosstenant-authsource":"SG2PEPF000B66CE.apcprd03.prod.outlook.com","x-ms-exchange-crosstenant-authas":"Anonymous","x-ms-exchange-crosstenant-fromentityheader":"HybridOnPrem","x-fe-etp-metadata":"eyAidGlkIjogIjN5V2d1ckMtNjIwMjYtMDhnQkRGRTI0NTMxOTk3MTIxNzYzNDQ4NDllIiwgImFj Y2VwdGVkX3RpbWVzdGFtcCI6ICIyMDI0MTAxODA4MDg1NyIsICJhY2NlcHRlZF90aW1lc3RhbXBf ZXBvY2giOiAiMTcyOTIzODkzNyIsICJkb21haW5fbmFtZSI6ICJzbXBseWxhYi5jb20iLCAiYXR0 X2NvdW50IjogLTIsICJzcmNfaXAiOiAiNDAuMTA3LjQ0LjkiIH0="},"mimetype":"multipart/alternative","text_bodies":["TEst a reply\r\n________________________________\r\nFrom: yyy@domain.com <yyy@domain.com>\r\nSent: Friday, October 18, 2024 10:03 AM\r\nTo: xxx@domain.com <xxx@domain.com>\r\nCc: Idris Elba <zzz@domain.com>\r\nSubject: Test Thread Reply"],"html_bodies":["<html>\r\n<head>\r\n<meta http-equiv=\"Content-Type\" content=\"text/html; charset=us-ascii\">\r\n<style type=\"text/css\" style=\"display:none;\"> P {margin-top:0;margin-bottom:0;} </style>\r\n</head>\r\n<body dir=\"ltr\">\r\n<div class=\"elementToProof\" style=\"font-family: Aptos, Aptos_EmbeddedFont, Aptos_MSFontService, Calibri, Helvetica, sans-serif; font-size: 12pt; color: rgb(0, 0, 0);\">\r\nTEst a reply</div>\r\n<div id=\"appendonsend\"></div>\r\n<hr style=\"display:inline-block;width:98%\" tabindex=\"-1\">\r\n<div id=\"divRplyFwdMsg\" dir=\"ltr\"><font face=\"Calibri, sans-serif\" style=\"font-size:11pt\" color=\"#000000\"><b>From:</b> yyy@domain.com &lt;yyy@domain.com&gt;<br>\r\n<b>Sent:</b> Friday, October 18, 2024 10:03 AM<br>\r\n<b>To:</b> xxx@domain.com &lt;xxx@domain.com&gt;<br>\r\n<b>Cc:</b> Idris Elba &lt;zzz@domain.com&gt;<br>\r\n<b>Subject:</b> Test Thread Reply</font>\r\n<div>&nbsp;</div>\r\n</div>\r\n<div class=\"BodyFragment\"><font size=\"2\"><hr>\r\n</font>\r\n</body>\r\n</html>\r\n"],"file_attachments":[],"date":"Fri, 18 Oct 2024 08:08:46 +0000","from":"zzz@domain.com","to":"yyy@domain.com","cc":[],"bcc":[],"in-reply-to":"<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>","reply-to":[]}}]
```



#### Ping
Use the Ping action to test connectivity to Gmail.
Timeout - 600 Seconds



#### Forward Email
Use the Forward Email action to forward emails, including emails with previous threads. This action doesn’t run on Google SecOps entities
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Internet Message ID|An internet message ID of the email to search for.|True|String||
|Send To|A comma-separated list of email addresses for the email recipients, such as user1@example.com, user2@example.com.|True|String||
|CC|A comma-separated string of email addresses for the carbon copy (CC) email recipients, such as user1@example.com, user2@example.com.|False|String||
|BCC|A comma-separated string of email addresses for the blind carbon copy (BCC) email recipients, such as user1@example.com, user2@example.com.|False|String||
|Subject|A new subject for the email to forward.|True|String||
|Attachments Paths|A comma-separated string of paths for file attachments stored on the Google SecOps server.|False|String||
|Mail Content|The body of an email.|True|Email Content||



##### JSON Results
```json
{"id": "1929ea6e77884359", "thread_id": "1929ea6e77884359", "label_ids": ["SENT"], "snippet": "2024-10-18 09:02:09 UTC+01Test Thread Reply", "history_id": "220253", "internal_date": 1729238591000, "message_id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>", "subject": "Test Thread Reply", "headers": {"received": "from 1005158396512 named unknown by gmailapi.google.com with HTTPREST; Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "subject": "Test Thread Reply", "cc": "zzz@domain.com", "content-type": "multipart/alternative; boundary=\"===============2133815296867179078==\"", "date": "Fri, 18 Oct 2024 10:03:11 +0200", "message-id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>"}, "mimetype": "multipart/alternative", "text_bodies": [], "html_bodies": ["Test Thread Reply"], "file_attachments": [], "date": "Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "cc": ["zzz@domain.com"], "bcc": [], "in-reply-to": "", "reply-to": []}
```



#### Send Thread Reply
Use the Send Thread Reply action to send a message as a reply to the email thread. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Internet Message ID|An internet message ID of the email to search for.|True|String||
|Reply To|A comma-separated list of emails to send the reply to. If you don’t provide any value and the Reply All checkbox is clear, the action only sends a reply to the original email sender. If you select the Reply All parameter, the action ignores this parameter.|False|String||
|Reply All|If selected, the action sends a reply to all recipients related to the original email. Not selected by default. This parameter has a priority over the Reply To parameter.|False|Boolean|false|
|Attachments Paths|A comma-separated string of paths for file attachments stored on the Google SecOps server.|False|String||
|Mail Content|The body of an email.|True|Email Content||



##### JSON Results
```json
{"id": "1929ea6e77884359", "thread_id": "1929ea6e77884359", "label_ids": ["SENT"], "snippet": "2024-10-18 09:02:09 UTC+01Test Thread Reply", "history_id": "220253", "internal_date": 1729238591000, "message_id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>", "subject": "Test Thread Reply", "headers": {"received": "from 1005158396512 named unknown by gmailapi.google.com with HTTPREST; Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "subject": "Test Thread Reply", "cc": "zzz@domain.com", "content-type": "multipart/alternative; boundary=\"===============2133815296867179078==\"", "date": "Fri, 18 Oct 2024 10:03:11 +0200", "message-id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>"}, "mimetype": "multipart/alternative", "text_bodies": [], "html_bodies": ["Test Thread Reply"], "file_attachments": [], "date": "Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "cc": ["zzz@domain.com"], "bcc": [], "in-reply-to": "", "reply-to": []}
```



#### Search For Emails
Use the Search for Emails action to execute email search in a specified mailbox using the provided search criteria. With appropriate permissions, this action can run a search in other mailboxes. This action is asynchronous. Adjust the action timeout in the Google SecOps IDE accordingly. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Sender Filter|A filter condition that specifies the email sender to search for.|False|String||
|Recipient Filter|A filter condition that specifies the email recipient to search for.|False|String||
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration. This parameter accepts multiple values as a comma-separated string.|True|String|Default Mailbox|
|Labels Filter|A filter condition that specifies the email labels to search for. This parameter accepts multiple values as a comma-separated string. You can search for emails with specific labels, such as label1, label2. To search for emails that don’t possess the specific label, use the following format: -label1. You can configure this parameter to search for emails with and without specific labels in one string, such as label1, -label2, label3.|False|String|Inbox|
|Internet Message ID|An internet message ID of the email to search for. This parameter accepts multiple values as a comma-separated string. If you provide the internet message ID, the action ignores the Subject Filter, Sender Filter, Labels Filter, Recipient Filter, Time Frame (minutes), and Email Status parameters.|False|String||
|Subject Filter|A filter condition that specifies the email subject to search for.|False|String||
|Time Frame (minutes)|A filter condition that specifies the timeframe in minutes to search for emails.|False|String|60|
|Email Status|A status of the email to search for.|False|List|Both Read & Unread Messages|
|Headers To Return|A comma-separated list of headers to return in the action output. The action always returns the following headers: date, from, to, cc, bcc, in-reply-to, reply-to, message-id and subject headers. If you don’t provide any value, the action returns all headers.This parameter is case sensitive.|False|String|date, from, to, cc, bcc, in-reply-to, reply-to, message-id, subject|
|Return Email Body|If selected, the action returns the full body content of an email in the action output. If not selected, the information about the attachment names in the email is unavailable|False|Boolean|false|
|Max Emails To Return|The maximum number of emails for the action to return.|False|String|50|



##### JSON Results
```json
[{"Entity":"xxx@domain.com","EntityResult":[{"id": "1929ea6e77884359", "thread_id": "1929ea6e77884359", "label_ids": ["SENT"], "snippet": "2024-10-18 09:02:09 UTC+01Test Thread Reply", "history_id": "220253", "internal_date": 1729238591000, "message_id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>", "subject": "Test Thread Reply", "headers": {"received": "from 1005158396512 named unknown by gmailapi.google.com with HTTPREST; Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "subject": "Test Thread Reply", "cc": "zzz@domain.com", "content-type": "multipart/alternative; boundary=\"===============2133815296867179078==\"", "date": "Fri, 18 Oct 2024 10:03:11 +0200", "message-id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>"}, "mimetype": "multipart/alternative", "text_bodies": [], "html_bodies": ["Test Thread Reply"], "file_attachments": [], "date": "Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "cc": ["zzz@domain.com"], "bcc": [], "in-reply-to": "", "reply-to": []}]}]
```



#### Send Email
Use the Send Email action to send an email based on the provided parameters. This action is not running on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to send an email from, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Subject|The subject for an email to send.|True|String||
|Send To|A comma-separated string of email addresses for the email recipients, such as user1@example.com, user2@example.com.|True|String||
|CC|A comma-separated string of email addresses for the carbon copy (CC) email recipients, such as user1@example.com, user2@example.com.|False|String||
|BCC|A comma-separated string of email addresses for the blind carbon copy (BCC) email recipients, such as user1@example.com, user2@example.com.|False|String||
|Attachments Paths|A comma-separated string of paths for file attachments stored on the Google SecOps server.|False|String||
|Mail Content|The body of an email.|True|Email Content||
|Reply-To Recipients|A comma-separated list of recipients to use in the “Reply-To” header. Use the “Reply-To” header to redirect reply emails to the specific email address instead of the sender address that is stated in the “From” field.|False|String||



##### JSON Results
```json
{"id": "1929ea6e77884359", "thread_id": "1929ea6e77884359", "label_ids": ["SENT"], "snippet": "2024-10-18 09:02:09 UTC+01Test Thread Reply", "history_id": "220253", "internal_date": 1729238591000, "message_id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>", "subject": "Test Thread Reply", "headers": {"received": "from 1005158396512 named unknown by gmailapi.google.com with HTTPREST; Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "subject": "Test Thread Reply", "cc": "zzz@domain.com", "content-type": "multipart/alternative; boundary=\"===============2133815296867179078==\"", "date": "Fri, 18 Oct 2024 10:03:11 +0200", "message-id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>"}, "mimetype": "multipart/alternative", "text_bodies": [], "html_bodies": ["Test Thread Reply"], "file_attachments": [], "date": "Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "cc": ["zzz@domain.com"], "bcc": [], "in-reply-to": "", "reply-to": []}
```



#### Save Email To The Case
Use the Save Email To The Case action to save email or email attachments to the action Case Wall in Google SecOps. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Internet Message ID|An internet message ID of the email to search for.|True|String||
|Save Only Email Attachments|If selected, the action saves only attachments from the specified email. Not selected by default.|False|Boolean|false|
|Attachment To Save|If you selected the “Save Only Email Attachments” parameter, the action only saves attachments that this parameter specifies. This parameter accepts multiple values as a comma-separated string.|False|String||
|Base64 Encode|If selected, the action encodes the email file into a base64 format.|False|Boolean|false|



##### JSON Results
```json
{"id": "1929ea6e77884359", "thread_id": "1929ea6e77884359", "label_ids": ["SENT"], "snippet": "2024-10-18 09:02:09 UTC+01Test Thread Reply", "history_id": "220253", "internal_date": 1729238591000, "message_id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>", "subject": "Test Thread Reply", "headers": {"received": "from 1005158396512 named unknown by gmailapi.google.com with HTTPREST; Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "subject": "Test Thread Reply", "cc": "zzz@domain.com", "content-type": "multipart/alternative; boundary=\"===============2133815296867179078==\"", "date": "Fri, 18 Oct 2024 10:03:11 +0200", "message-id": "<CAAfJ0RiK+H9BEkNh5fFB=VKnggS9Txttkm86=8gCnTbFoDFs8A@mail.gmail.com>"}, "mimetype": "multipart/alternative", "text_bodies": [], "html_bodies": ["Test Thread Reply"], "file_attachments": [], "date": "Fri, 18 Oct 2024 10:03:11 +0200", "from": "yyy@domain.com", "to": "xxx@domain.com", "cc": ["zzz@domain.com"], "bcc": [], "in-reply-to": "", "reply-to": []}
```



#### Add Email Label
Use the Add Email Label action to add a label to the specified email. Adjust the action timeout in the Google SecOps IDE accordingly. This action doesn't run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration.|True|String|Default Mailbox|
|Labels Filter|A filter condition that specifies the email labels to search for. This parameter accepts multiple values as a comma-separated string. You can search for emails with specific labels, such as label1, label2. To search for emails that don’t possess the specific label, use the following format: -label1. You can configure this parameter to search for emails with and without specific labels in one string, such as label1, -label2, label3.|False|String|Inbox|
|Internet Message ID|An internet message ID of the email to search for. This parameter accepts multiple values as a comma-separated string. If you provide the internet message ID, the action ignores the Labels Filter, Subject Filter, Sender Filter, and Time Frame (minutes) parameters.|False|String||
|Subject Filter|A filter condition that specifies the email subject to search for. This filter uses the “contains” logic and requires you to specify search items in full words. This filter doesn’t support partial matches.|False|String||
|Sender Filter|A filter condition that specifies the email sender to search for. This filter uses the “equals” logic.|False|String||
|Time Frame (minutes)|A filter condition that specifies the timeframe in minutes to search for emails.|False|String|60|
|Email Status|A status of the email to search for.|False|List|Both Read & Unread Messages|
|Label|A label to update the email with. This parameter accepts multiple values as a comma-separated list. Action will create labels, if they don’t exist in the mailbox.|True|String||



##### JSON Results
```json

```



#### Delete Email
Use the Delete Email action to delete one or multiple emails from the mailbox based on the provided search criteria. By default, this action moves emails to Trash. You can configure the action to delete emails forever instead of moving them to Trash. The Delete Email action is asynchronous. Adjust the action timeout in the Google SecOps IDE accordingly. This action doesn’t run on Google SecOps entities.
Timeout - 600 Seconds


|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|Mailbox|A mailbox to search the email in, such as user@example.com. By default, the action uses the default mailbox that you configured for the integration. This parameter accepts multiple values as a comma-separated string.|True|String|Default Mailbox|
|Labels Filter|A filter condition that specifies the email labels to search for. This parameter accepts multiple values as a comma-separated string. You can search for emails with specific labels, such as label1, label2. To search for emails that don’t possess the specific label, use the following format: -label1. You can configure this parameter to search for emails with and without specific labels in one string, such as label1, -label2, label3.|False|String|Inbox|
|Internet Message ID|An internet message ID of the email to search for. This parameter accepts multiple values as a comma-separated string. If you provide the internet message ID, the action ignores the Subject Filter, Sender Filter, Labels Filter, and Time Frame (minutes) parameters.|False|String||
|Subject Filter|A filter condition that specifies the email subject to search for. This filter uses the “contains” logic and requires you to specify search items in full words. This filter doesn’t support partial matches.|False|String||
|Sender Filter|A filter condition that specifies the email sender to search for. This filter uses the “equals” logic.|False|String||
|Time Frame (minutes)|A filter condition that specifies the timeframe in minutes to search for emails.|False|String|60|
|Email Status|A status of the email to search for.|False|List|Both Read & Unread Messages|
|Move to Trash|If selected, the action moves emails to Trash and doesn’t search through emails with the Trash label unless you configure the Labels Filter parameter to include the following label: Trash. If not selected, the action executes search across the whole mailbox and deletes emails forever. Selected by default.|False|Boolean|true|



##### JSON Results
```json
[{"Entity": "xxxx@domain.com", "EntityResult": ["191dbeebcf1e35ae", "191dbec698a5085b", "191c1de46d7b5bc3", "191089a18af39dc6", "190fdd4b8fa5f06d", "190ef4913bf87405", "190ee92933c075fa", "190ee8f88c8a5f34"]}]
```









## Connectors
#### Gmail Connector
The Gmail Connector retrieves Gmail emails from the specified mailbox. To filter specific values from the email body and subject, use the dynamic list regular expressions in the following format: “key: regex”. For example, after finding a match for the following regex: “subject: (?<=Subject: ).*”, the connector creates a Google SecOps alert event and adds a new key with the “subject” name to it. The new key value matches the regular expression.

|Name|Description|IsMandatory|Type|DefaultValue|
|----|-----------|-----------|----|------------|
|DeviceProductField|Enter the source field name in order to retrieve the Product Field name.|True|String|device_product|
|EventClassId|Enter the source field name in order to retrieve the Event Field name.|True|String|event_name|
|Environment Field Name|Describes the name of the field where the environment name is stored.If the environment field isn't found, the environment is the default environment.|False|String||
|Environment Regex Pattern|A regex pattern to run on the value found in the "Environment Field Name" field.Default is .* to catch all and return the value unchanged.Used to allow the user to manipulate the environment field via regex logic.If the regex pattern is null or empty, or the environment value is null, the final environment result is the default environment.|False|String||
|Email Exclude Pattern|A regular expression to exclude specific emails from ingestion, such as spam or news. This parameter works with both the subject and the body of an email. For example, to exclude the autoreply emails from ingestion, you can configure the following regular expression: (?i)(auto|no)(\s|-)?re(ply|sponse|sponder)|False|String||
|PythonProcessTimeout|Timeout limit for the python process running the current script.|True|Integer|300|
|Service Account JSON File Content|The content of the service account key JSON file. You can configure either this parameter or the Workload Identity Email parameter. To configure this parameter, provide the full content of the service account key JSON file that you have downloaded when creating a service account.|False|Password|*****|
|Workload Identity Email|The client email address of your service account.You can configure either this parameter or the Service Account JSON File Content parameter. To impersonate service accounts with workloads, grant the Service Account Token Creator role to your Google SecOps service account.|False|String||
|Disable Overflow|If selected, the connector ignores the Google SecOps overflow mechanism during alert creation.Not selected by default.|False|Boolean|false|
|Default Mailbox|An email address to use as a default mailbox for the integration, such as user@example.com.|True|String||
|Labels Filter|The labels of emails to ingest into Google SecOps. The connector supports nested labels. Provide the labels in a format that is acceptable for Gmail, such as Inbox-label1-label2.|False|String|Inbox|
|Email Status|A status of the email to search for. Possible values are as follows: Both, Read, Unread. The default value is Both.|False|String|Both|
|Mark Emails as Read|If selected, the connector marks ingested emails as read.|False|Boolean|true|
|Extract Headers|Header values to filter from the “internetMessageHeaders” list and add to a Google SecOps event. By default, the connector adds all headers to the event. To add only specific headers, enter them as a comma-separated list, such as “DKIM-Siganture”, “Received”, “From”. To prevent the connector from adding any header, enter the following value: None. This parameter is case-insensitive.|False|String||
|Attached Mail File Prefix|A prefix to add to the extracted event keys (for example, to, from, or subject) from the attached email file received in the monitored mailbox.|False|String|attach|
|Original Mail File Prefix|A prefix to add to the extracted event keys (for example, to, from, or subject) from the original email received in the monitored mailbox.|False|String|orig|
|Attach Original EML|If selected, the connector attaches the original email to the case information as an EML file.Not selected by default.|False|Boolean|false|
|Create Alert Per Attachment File|If selected, the connector creates multiple alerts, with one alert for every attached email file.This behavior is useful when you process emails with multiple email files attached and set the Google SecOps event mapping to create entities from attached email files.Not selected by default.|False|Boolean|false|
|Max Emails Per Cycle|The maximum number of emails to retrieve for every connector iteration.The maximum number is 100 emails. The default value is 10 emails.|True|Integer|10|
|Max Hours Backwards|Number of hours before the first connector iteration to retrieve incidents from. This parameter applies to the initial connector iteration after you enable the connector for the first time or the fallback value for an expired connector timestamp.|True|Integer|24|
|Case Name Template|A custom case name. When you configure this parameter, the connector adds a new key called custom_case_name to the Google SecOps event. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. For placeholders, the connector uses the first Google SecOps event. The connector only handles keys that contain the string value. To configure this parameter, specify event fields without prefixes.|False|String||
|Alert Name Template|A custom alert name. You can provide placeholders in the following format: [name of the field]. Example: Phishing - [event_mailbox]. For placeholders, the connector uses the first Google SecOps event. The connector only handles keys containing the string value. If you don’t provide any value or use an invalid template, the connector uses the default alert name. To configure this parameter, specify event fields without prefixes.|False|String||
|Verify SSL|If enabled, verify the SSL certificate for the connection to the Google Gmail server is valid.|False|Boolean|true|
|Proxy Server Address|The address of the proxy server to use.|False|String||
|Proxy Username|The proxy username to authenticate with.|False|String||
|Proxy Password|The proxy password to authenticate with.|False|Password|*****|




