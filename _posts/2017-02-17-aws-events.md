---
layout: post
title:  "AWS Events"
date:   2017-02-09 10:10:02
categories: aws
tags: events
excerpt:
---

1. [AWS Sample Events](http://docs.aws.amazon.com/lambda/latest/dg/eventsources.html)

2. SNS Push of S3 event example:
  
          {
          "Records": [
            {
              "EventVersion": "1.0",
              "EventSubscriptionArn": "arn:aws:sns:eu-west-1:903892408011:myltop:1ff2eeda-5d9e-4e86-8b34-43c8331dfc8f",
              "EventSource": "aws:sns",
              "Sns": {
                "SignatureVersion": "1",
                "Timestamp": "2017-02-10T14:44:02.359Z",
                "Signature": "cJ12Z57pVKxsEBOzFYyWd7RoCElHiXUU3gBoJOkYuI+7rnSajYBuFyyVLsrxfU5zPD/LreUwOem4U0i898pDot7cgp7MS3JWh098m4kjTt5vCruX9cYZv6/yygnfEkQtIZYbjWPKN7Y/kmBzKBq2IyJVPZmyIDzQ+RdBr6aslFV0E0/N4CNy6z/UpvVSZAr9u2nlDUYYihQwu7RqZ5M+Y7ibMDo0mOtRc27LpCauyBukl6Zl0cMfiAy/DE8LbcOvQmb2tVPmS1fgNOZc82JEbuRFJ19+4N1niVLFutCoDZ0gZQ1VbDlj0yIJUriucofF2vpO3yEnI/8Uw8AZWBX9uQ==",
                "SigningCertUrl": "https://sns.eu-west-1.amazonaws.com/SimpleNotificationService-b95095beb82e8f6a046b3aafc7f4149a.pem",
                "MessageId": "1c9bba4b-e96f-5d30-aa70-eb5c3a9d9a0b",
                "Message": "{\"Records\":[{\"eventVersion\":\"2.0\",\"eventSource\":\"aws:s3\",\"awsRegion\":\"eu-west-1\",\"eventTime\":\"2017-02-10T14:44:02.267Z\",\"eventName\":\"ObjectCreated:Put\",\"userIdentity\":{\"principalId\":\"A1XOGEKUPGMQQ9\"},\"requestParameters\":{\"sourceIPAddress\":\"78.158.110.114\"},\"responseElements\":{\"x-amz-request-id\":\"639D278FC156D85A\",\"x-amz-id-2\":\"jviLA4RFAuSpToaNmPhd1WVCDFNOo0tTNhuwsqarwkwCFPyzotK3TsYwrAli9tcQ\"},\"s3\":{\"s3SchemaVersion\":\"1.0\",\"configurationId\":\"fg\",\"bucket\":{\"name\":\"testbuckprop\",\"ownerIdentity\":{\"principalId\":\"A1XOGEKUPGMQQ9\"},\"arn\":\"arn:aws:s3:::testbuckprop\"},\"object\":{\"key\":\"ncd_csv.zip\",\"size\":368508,\"eTag\":\"897f10db190a9d9cd7bdd1b0b14dad81\",\"sequencer\":\"00589DD1B23460D277\"}}}]}",
                "MessageAttributes": {},
                "Type": "Notification",
                "UnsubscribeUrl": "https://sns.eu-west-1.amazonaws.com/?Action=Unsubscribe&SubscriptionArn=arn:aws:sns:eu-west-1:903892408011:myltop:1ff2eeda-5d9e-4e86-8b34-43c8331dfc8f",
                "TopicArn": "arn:aws:sns:eu-west-1:903892408011:myltop",
                "Subject": "Amazon S3 Notification"
              }
            }
          ]
          }
          

3. Schedular event example: 

        {
          "account": "$12digitAccountCode", 
          "region": "$AccountRegion e.g. eu-west-1", 
          "detail": {}, 
          "detail-type": "Scheduled Event", 
          "source": "aws.events", 
          "time": "2017-02-17T00:00:00Z", 
          "id": "event id, put any sample string for testing", 
          "resources": [
            "arn:aws:events:$AccountRegion:$account:rule/lcd_data_downloader"
          ]
        }
    
    
4. S3 event example:

        
        {
        "Records": [
        {
        "eventVersion": "2.0", 
        "eventTime": "2017-02-17T15:56:37.313Z", 
        "requestParameters": {
        "sourceIPAddress": "34.250.56.143"
        }, 
        "s3": {
        "configurationId": "219d6a6f-eaec-4410-a007-a0d625e947de", 
        "object": {
        "eTag": "c18d561de3c1d8fd81fe445e7bb4bbe0-2", 
        "sequencer": "0058A71D339D122B8B", 
        "key": "data/timestamps/2017-02-17T15%3A56%3A09Z/all_article.zip", 
        "size": 16500150
        }, 
        "bucket": {
        "arn": "arn:aws:s3:::lcddata", 
        "name": "lcddata", 
        "ownerIdentity": {
        "principalId": "KDJFJKDFJI"
        }
        }, 
        "s3SchemaVersion": "1.0"
        }, 
        "responseElements": {
        "x-amz-id-2": "iTHrvdAkRfT9f/qV49wVfCJrFcp3B+5QSWUhAcSPvu/3ek60bPw9gzfCd84VU7g/DhVHkQXjzbQ=", 
        "x-amz-request-id": "dfasdfadsf"
        }, 
        "awsRegion": "eu-west-1", 
        "eventName": "ObjectCreated:CompleteMultipartUpload", 
        "userIdentity": {
        "principalId": "AWS:df:l_lcd_data_downloader"
        }, 
        "eventSource": "aws:s3"
        }
        ]
        }