# zpush
Generate APNs Safari WebPush Package
Kindly repost any issue or Chat for instant support [ https://zupago.slack.com/messages/C9M45284T/apps/A0F7XDW93/ ](https://zupago.slack.com/messages/C9M45284T/apps/A0F7XDW93/) .

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

`Python`, `Java`, `Json`, `Net`, `Swift`, `Ruby`, `NodeJs` all work

A post request to https://zpush.zupago.pe/pusher/safari/generator

with the following perimeters


| Key                | Value                | Description                 |
| :------------------| :------------------- | :---------------------------|
| `websitePushID`    | `web.pe.zupago.test` | TThe Website Push ID, as specified in your developer account. Required |
| `certfile`         | `Certificates.p12`   | Your Certificates.p12 Certificate Required |
| `certPassw`        | `password`           | `file` Your Certificates.p12 Certificate Password if Any |
| `saflogo`          |  `logo.png`          | `file` Website Logo Required |
| `website`          | `https://zpush.zupago.pe` | An array of websites that are allowed to request permission from the user. Required |
| `websiteName`      | `ZuPago WebPush Generator`| The website name. This is the heading used in Notification Center. Required |
| `authenticationToken` | `B82CF5AED-7F81-4BB3-A128-3DCE18977DC6` | A string that helps you identify the user. It is included in later requests to your web service. This string must 16 characters or greater. Required |
| `webServiceURL` | `https://zpush.zupago.pe/pusher/safari` | The location used to make requests to your web service. The trailing slash should be omitted. Required |
| `urlFormatString` | `https://zpush.zupago.pe/url/?url=%@` | The URL to go to when the notification is clicked. Use %@ as a placeholder for arguments you fill in when delivering your notification. This URL must use the http or https scheme; otherwise, it is invalid. Required |


Kindly repost any issue or Chat for instant support [ https://zupago.slack.com/messages/C9M45284T/apps/A0F7XDW93/ ](https://zupago.slack.com/messages/C9M45284T/apps/A0F7XDW93/) .
