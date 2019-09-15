---
description: 'Main Developer: Iman Suherman (https://github.com/iman-suherman)'
---

# Video Uploader

## API END POINT

* [https://api.tutorialinaja.tech/vidu/v1/](https://api.tutorialinaja.tech/vidu/v1/)

{% hint style="success" %}
Status: `LIVE`

First Publish Date: `Sep 14, 2019 9:31 AM (AEST)`
{% endhint %}

## API Docs

* Api Docs: [https://tutorialinajavideouploader.docs.apiary.io/\#](https://tutorialinajavideouploader.docs.apiary.io/#)

## API Repository

* Api Repository: [https://github.com/pojok-projects/tutorialsystem-video-uploader](https://github.com/pojok-projects/tutorialsystem-video-uploader)

## Description

Video Uploader upload the video into S3 bucket \(media.tutorialinaja.tech\) for future reference. Upon successful upload, the API will return the video upload status includes its ETag.

Note: Due to the limitation of the API gateway \(see: [https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html](https://docs.aws.amazon.com/apigateway/latest/developerguide/limits.html)\) we can only upload up to 10 MB per file.  

See below process flow of this API and its relationship with other API:

![Video Upload Relationship with other APIs](../.gitbook/assets/image%20%281%29.png)

## Table Structure End Points

See API Docs

## Example screen shots of API invocations

See API Docs

