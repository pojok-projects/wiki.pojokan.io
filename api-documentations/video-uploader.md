---
description: 'Main Developer: Iman Suherman (https://github.com/iman-suherman)'
---

# Video Uploader

## API END POINT

* [https://api.tutorialinaja.tech/vidu/v1/](https://api.tutorialinaja.tech/vidu/v1/)

{% hint style="success" %}
Status: `LIVE`

Publish Date: `Sep 14, 2019 9:31 AM (AEST)`
{% endhint %}

## API Docs

* Api Docs: [https://tsvidu.docs.apiary.io/\#](https://tsvidu.docs.apiary.io/#)

## Codes

* Api Repository: [https://github.com/pojok-projects/tutorialsystem-video-uploader](https://github.com/pojok-projects/tutorialsystem-video-uploader)
* Language: JavaScript
* Framework: node.js Express 

## Infrastructure

* CodePipeline: [tutorial-system-vidu-master-cicd-pl](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines/tutorial-system-vidu-master-cicd-pl/view?region=ap-southeast-1)
* CI/CD CloudFormation: [tutorial-system-vidu-master-cicd-pipeline-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=vidu&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorial-system-vidu-master-cicd-pipeline-cf%2F79ab8ce0-d67e-11e9-8917-02c6c7bea9ac)
* Solution CloudFormation: [tutorial-system-vidu-master-provisioning-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=vidu&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorial-system-vidu-master-provisioning-cf%2F157cec90-d67f-11e9-9d8f-02d60855aea4)

## Description

Video Uploader upload the video into S3 bucket \(media.tutorialinaja.tech\) for future reference. Upon successful upload, the API will return the video upload status includes its ETag.

Note: Due to the limitation of the API gateway \(see: [https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html](https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html)\) we can only upload up to 10 MB per file.  

See below process flow of this API and its relationship with other API:

![Video Upload Relationship with other APIs](../.gitbook/assets/image%20%281%29.png)

## Table Structure End Points

See API Docs

## Example screen shots of API invocations

See API Docs

