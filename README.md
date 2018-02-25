# zpush
Generate APNs Safari WebPush Package

# Safari WebPush Package Generator API

[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE.md)
[![Build Status](https://scrutinizer-ci.com/g/zupago/zpush/badges/build.png?b=master)](https://scrutinizer-ci.com/g/zupago/zpush/build-status/master)
[![sight](https://insight.sensiolabs.com/projects/30d57a0c-06db-45e4-97fc-2e164cbca54f/big.png)](https://insight.sensiolabs.com/projects/30d57a0c-06db-45e4-97fc-2e164cbca54f)

This package makes it so easy to Generate Safari WebPush Packages Required By Apple.

## No Installation Required

You can Generate Safari WebPush Packages Via our website or directly from your project via our api:

## Website

[ https://zpush.zupago.pe/safari/generator ](https://zpush.zupago.pe/safari/generator) or [https://zpush.zupago.pe/safari/generator](https://zpush.zupago.pe/safari/generator)


## API PHP
```
<?php

$client = new http\Client;
$request = new http\Client\Request;

$body = new http\Message\Body;
$body->addForm(array(
  'websitePushID' => 'web.pe.zupago.test',
  'certPassw' => 'test123456',
  'website' => 'https://zpush.zupago.pe',
  'websiteName' => 'ZuPago WebPush Generator',
  'authenticationToken' => 'B82CFAED-7F81-4BB3-A128-3DCE18977DC6',
  'webServiceURL' => 'https://zpush.zupago.pe/pusher/safari',
  'urlFormatString' => 'https://zpush.zupago.pe/url/?url=%@'
), NULL);

$request->setRequestUrl('https://zpush.zupago.pe/pusher/safari/generator');
$request->setRequestMethod('POST');
$request->setBody($body);

$client->enqueue($request)->send();
$response = $client->getResponse();

echo $response->getBody();


```



## API Curl
``` API Curl
curl -X POST \
  https://zpush.zupago.pe/pusher/safari/generator \
  -H 'content-type: multipart/form-data; boundary=----WebKitFormBoundary7MA4YWxkTrZu0gW' \
  -F websitePushID=web.pe.zupago.test \
  -F certfile=undefined \
  -F certPassw=test123456 \
  -F saflogo=undefined \
  -F website=https://zpush.zupago.pe \
  -F 'websiteName=ZuPago WebPush Generator' \
  -F authenticationToken=B82CFAED-7F81-4BB3-A128-3DCE18977DC6 \
  -F webServiceURL=https://zpush.zupago.pe/pusher/safari \
  -F 'urlFormatString=https://zpush.zupago.pe/url/?url=%@'
```
## API Other methods
```
Python Java Json Net swith all work

A post request to https://zpush.zupago.pe/pusher/safari/generator

with the following perimeters

{"key":"websitePushID",     "value":"web.pe.zupago.test",       "description":"The Website Push ID, as specified in your developer account.
Required\n\n","type":"text","enabled":true},


{"key":"certfile",  "value":Certificates.p12file, "description":"Your Certificates.p12 Certificate Required","type":"file","enabled":true},


{"key":"certPassw",  "value":"test123456",  "description":"Your Certificates.p12 Certificate Password if Any","type":"text","enabled":true},


{"key":"saflogo",  "value":null,  "description":"Website Logo Required","type":"file","enabled":true},


{"key":"website",  "value":"https://zpush.zupago.pe",  "description":"An array of websites that are allowed to request permission from the user. Required","type":"text","enabled":true},


{"key":"websiteName",  "value":"ZuPago WebPush Generator", "description":"The website name. This is the heading used in Notification Center. Required","type":"text","enabled":true},



{"key":"authenticationToken",  "value":"B82CFAED-7F81-4BB3-A128-3DCE18977DC6",  "description":"A string that helps you identify the user. It is included in later requests to your web service. This string must 16 characters or greater. Required","type":"text","enabled":true},


{"key":"webServiceURL",  "value":"https://zpush.zupago.pe/pusher/safari",  "description":"The location used to make requests to your web service. The trailing slash should be omitted. Required","type":"text","enabled":true},


{"key":"urlFormatString",  "value":"https://zpush.zupago.pe/url/?url=%@",  "description":"The URL to go to when the notification is clicked. Use %@ as a placeholder for arguments you fill in when delivering your notification. This URL must use the http or https scheme; otherwise, it is invalid. Required","type":"text","enabled":true}]

```

Kindly repost if any issue.
