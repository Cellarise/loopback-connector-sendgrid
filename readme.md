# loopback-connector-sendgrid
[![view on npm](http://img.shields.io/npm/v/loopback-connector-sendgrid.svg?style=flat)](https://www.npmjs.org/package/loopback-connector-sendgrid)
[![npm module downloads per month](http://img.shields.io/npm/dm/loopback-connector-sendgrid.svg?style=flat)](https://www.npmjs.org/package/loopback-connector-sendgrid)
[![Dependency status](https://david-dm.org/Cellarise/loopback-connector-sendgrid.svg?style=flat)](https://david-dm.org/Cellarise/loopback-connector-sendgrid)
[![Coverage](https://img.shields.io/badge/coverage-64%25_skipped:0%25-yellow.svg?style=flat)](https://www.npmjs.org/package/loopback-connector-sendgrid)

> Loopback connector module which allow to send emails via SendGrid


## Installation

````sh
npm install loopback-connector-sendgrid --save
````

## Configuration

datasources.json

    {
        "sendgrid": {
            "connector": "loopback-connector-sendgrid",
            "username": '[your username here]'
            "password": '[your password here]'
        }
    }

model-config.json

    {
        "Email": {
            "dataSource": "sendgrid",
            "public": false
        }
    }

Configuration in JavaScript

    var DataSource = require('loopback-datasource-juggler').DataSource;
    var dsSendGrid = new DataSource('loopback-connector-sendgrid', {
        username: '[your username here]'
        password: '[your password here]'
    });
    loopback.Email.attachTo(dsSendGrid);

## Usage

Basic option same as built in Loopback

    loopback.Email.send({
        to: "test@to.com",
        from: "test@from.com",
        subject: "subject",
        text: "text message",
        html: "html <b>message</b>"
    },
    function(err, result) {
        if(err) {
            console.log('Upppss something crash');
            return;
        }
        console.log(result);
    });


# API

*documented by [jsdoc-to-markdown](https://github.com/75lb/jsdoc-to-markdown)*.


#Changelog

<table style="width:100%;border-spacing:0px;border-collapse:collapse;margin:0px;padding:0px;border-width:0px;">
  <tr>
    <th style="width:20px;text-align:center;"></th>
    <th style="width:80px;text-align:center;">Type</th>
    <th style="width:80px;text-align:left;">ID</th>
    <th style="text-align:left;">Summary</th>
  </tr>
    
<tr>
        <td colspan=4><strong>Version: 0.1.1 - released 2015-02-03</strong></td>
      </tr>
        
<tr>
            <td style="width:20px;text-align:center;"><img src='https://jira.cellarise.com:80/secure/viewavatar?size=xsmall&amp;avatarId=10419&amp;avatarType=issuetype'/></td>
            <td style="width:80px;text-align:center;">Non-functional</td>
            <td style="width:80px;text-align:left;">MDLPCNSG-3</td>
            <td>Package: Update package dependencies</td>
          </tr>
        
    
<tr>
        <td colspan=4><strong>Version: 0.1.0 - released 2015-02-02</strong></td>
      </tr>
        
<tr>
            <td style="width:20px;text-align:center;"><img src='https://jira.cellarise.com:80/secure/viewavatar?size=xsmall&amp;avatarId=10411&amp;avatarType=issuetype'/></td>
            <td style="width:80px;text-align:center;">Feature</td>
            <td style="width:80px;text-align:left;">MDLPCNSG-2</td>
            <td>Email connector: Add a loopback connector for sending emails from SendGrid</td>
          </tr>
        
    
</table>



# License

MIT License (MIT). All rights not explicitly granted in the license are reserved.

Copyright (c) 2015 John Barry
## Dependencies
[asn1@0.1.11](&quot;https://github.com/mcavage/node-asn1&quot;) - &quot;MIT*&quot;, [assert-plus@0.1.5](&quot;https://github.com/mcavage/node-assert-plus&quot;) - &quot;MIT*&quot;, [async@0.9.0](&quot;https://github.com/caolan/async&quot;) - [&quot;MIT&quot;], [aws-sign2@0.5.0](&quot;https://github.com/mikeal/aws-sign&quot;) - &quot;Apache*&quot;, [bl@0.9.4](&quot;https://github.com/rvagg/bl&quot;) - &quot;MIT&quot;, [boom@2.6.1](&quot;https://github.com/hapijs/boom&quot;) - [&quot;BSD&quot;], [caseless@0.9.0](&quot;https://github.com/mikeal/caseless&quot;) - &quot;BSD&quot;, [combined-stream@0.0.7](&quot;https://github.com/felixge/node-combined-stream&quot;) - &quot;MIT*&quot;, [core-util-is@1.0.1](&quot;https://github.com/isaacs/core-util-is&quot;) - &quot;MIT&quot;, [cryptiles@2.0.4](&quot;https://github.com/hapijs/cryptiles&quot;) - [&quot;BSD&quot;], [ctype@0.5.3](&quot;https://github.com/rmustacc/node-ctype&quot;) - &quot;MIT*&quot;, [delayed-stream@0.0.5](&quot;https://github.com/felixge/node-delayed-stream&quot;) - &quot;MIT*&quot;, [forever-agent@0.5.2](&quot;https://github.com/mikeal/forever-agent&quot;) - &quot;Apache*&quot;, [form-data@0.2.0](&quot;https://github.com/felixge/node-form-data&quot;) - [&quot;MIT&quot;], [hawk@2.3.1](&quot;https://github.com/hueniverse/hawk&quot;) - [&quot;BSD&quot;], [hoek@2.11.0](&quot;https://github.com/hapijs/hoek&quot;) - [&quot;BSD&quot;], [http-signature@0.10.1](&quot;https://github.com/joyent/node-http-signature&quot;) - &quot;MIT&quot;, [inherits@2.0.1](&quot;https://github.com/isaacs/inherits&quot;) - &quot;ISC&quot;, [isarray@0.0.1](&quot;https://github.com/juliangruber/isarray&quot;) - &quot;MIT&quot;, [isstream@0.1.1](&quot;https://github.com/rvagg/isstream&quot;) - &quot;MIT&quot;, [json-stringify-safe@5.0.0](&quot;https://github.com/isaacs/json-stringify-safe&quot;) - &quot;BSD&quot;, [lodash@2.4.1](&quot;https://github.com/lodash/lodash&quot;) - &quot;MIT&quot;, [lodash@3.0.1](&quot;https://github.com/lodash/lodash&quot;) - &quot;MIT&quot;, [loopback-connector-sendgrid@0.0.0](&quot;https://github.com/Cellarise/loopback-connector-sendgrid&quot;) - &quot;MIT License (MIT)&quot;, [mime-db@1.6.0](&quot;https://github.com/jshttp/mime-db&quot;) - &quot;MIT&quot;, [mime-types@2.0.8](&quot;https://github.com/jshttp/mime-types&quot;) - &quot;MIT&quot;, [mime@1.2.11](&quot;https://github.com/broofa/node-mime&quot;) - &quot;MIT*&quot;, [node-uuid@1.4.2](&quot;https://github.com/broofa/node-uuid&quot;) - [&quot;MIT&quot;], [oauth-sign@0.6.0](&quot;https://github.com/mikeal/oauth-sign&quot;) - &quot;Apache*&quot;, [punycode@1.3.2](&quot;https://github.com/bestiejs/punycode.js&quot;) - &quot;MIT&quot;, [q@1.1.2](&quot;https://github.com/kriskowal/q&quot;) - &quot;MIT&quot;, [qs@2.3.3](&quot;https://github.com/hapijs/qs&quot;) - [&quot;BSD&quot;], [readable-stream@1.0.33](&quot;https://github.com/isaacs/readable-stream&quot;) - &quot;MIT&quot;, [request@2.52.0](&quot;https://github.com/request/request&quot;) - &quot;Apache-2.0&quot;, [sendgrid@1.5.0](&quot;https://github.com/sendgrid/sendgrid-nodejs&quot;) - &quot;MIT*&quot;, [smtpapi@1.0.5](&quot;https://github.com/sendgrid/smtpapi-nodejs&quot;) - &quot;BSD&quot;, [sntp@1.0.9](&quot;https://github.com/hueniverse/sntp&quot;) - [&quot;BSD&quot;], [string_decoder@0.10.31](&quot;https://github.com/rvagg/string_decoder&quot;) - &quot;MIT&quot;, [stringstream@0.0.4](&quot;https://github.com/mhart/StringStream&quot;) - &quot;MIT&quot;, [tough-cookie@0.12.1](&quot;https://github.com/goinstant/tough-cookie&quot;) - &quot;MIT&quot;, [tunnel-agent@0.4.0](&quot;https://github.com/mikeal/tunnel-agent&quot;) - &quot;Apache*&quot;, 
*documented by [npm-licenses](http://github.com/AceMetrix/npm-license.git)*.