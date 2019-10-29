---
description: 'Main Developer: Juni Yadi (https://github.com/JuniYadi)'
---

# Database Interface Layer

## API END POINT

* [https://api.tutorialinaja.tech/dbil/v1/](https://api.tutorialinaja.tech/dbil/v1/)

{% hint style="success" %}
Status: `LIVE`

Publish Date: `Aug 24, 2019 12:32 PM (AEST)`
{% endhint %}

## API Docs

* Api Docs: [https://tsdbil.docs.apiary.io/\#](https://tsdbil.docs.apiary.io/#)

## Entity Relationship Diagram

* [x] [Sprint 1](https://dbdiagram.io/d/5d28c8f8ced98361d6dc9bab)
* [x] [Sprint 2](https://dbdiagram.io/d/5d2edb4fced98361d6dcbc9f)
* [ ] [Sprint 2 \(Refactoring\)](https://dbdiagram.io/d/5d60b65bced98361d6dddf7b) \[We Are Here Now\]

## Codes

* Code Repository: [https://github.com/pojok-projects/tutorialsystem-database-interface-layer](https://github.com/pojok-projects/tutorialsystem-database-interface-layer)
* Language: JavaScript
* Framework: node.js Express 

## Infrastructure

* CodePipeline: [tutorialsystem-dbil-master-cicd-pl](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines/tutorialsystem-dbil-master-cicd-pl/view?region=ap-southeast-1)
* CI/CD CloudFormation: [tutorialsystem-dbil-master-cicd-pipeline-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=dbil&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorialsystem-dbil-master-cicd-pipeline-cf%2F95f91370-fa7f-11e9-81fc-06abab1199f8)
* Solution CloudFormation: [tutorialsystem-dbil-master-provisioning-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=dbil&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorialsystem-dbil-master-provisioning-cf%2F3de26fe0-fa6d-11e9-a21b-062b7ab1ef08)

## Description

Database Interface Layer is governing input and output process of database communication from any other micro services. In this abstraction layer, this repository will provide the API for communication with the following tables:

* content-category \(master table\)
* content-metadata \(transactional table with one of the foreign key comes from content-category table\)

As the result of this service, the Input and Output query into content-category and content-metadata tables will be provided as rest APIs.

See Red highlight below for the scope of this service.

![](../.gitbook/assets/image%20%289%29.png)

## Table Structure API End Points

### Content Metadata Table Routes

| URL | Method | INFO |
| :--- | :--- | :--- |
| `content/metadata` | GET | Get All Data |
| `content/metadata/store` | POST | Save Data |
| `content/metadata/{id}` | GET | Get Data by ID |
| `content/metadata/search` | POST | Search Data Query |
| `content/metadata/update/{id}` | POST | Update Data by ID |
| `content/metadata/delete/{id}` | POST | Delete Data by ID |

### Content Table Routes

| URL | Method | INFO |
| :--- | :--- | :--- |
| `content/subtitle` | GET | Get All Data |
| `content/subtitle/store` | POST | Save Data |
| `content/subtitle/{id}` | GET | Get Data by ID |
| `content/subtitle/search` | POST | Search Data Query |
| `content/subtitle/update/{id}` | POST | Update Data by ID |
| `content/subtitle/delete/{id}` | POST | Delete Data by ID |
| `content/category` | GET | Get All Data |
| `content/category/store` | POST | Save Data |
| `content/category/{id}` | GET | Get Data by ID |
| `content/category/search` | POST | Search Data Query |
| `content/category/update/{id}` | POST | Update Data by ID |
| `content/category/delete/{id}` | POST | Delete Data by ID |
| `content/playlists/category` | GET | Get All Data |
| `content/playlists/category/store` | POST | Save Data |
| `content/playlists/category/{id}` | GET | Get Data by ID |
| `content/playlists/category/search` | POST | Search Data Query |
| `content/playlists/category/update/{id}` | POST | Update Data by ID |
| `content/playlists/category/delete/{id}` | POST | Delete Data by ID |

### User Table Routes

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user` | GET | Get All Data |
| `user/store` | POST | Save Data |
| `user/{id}` | GET | Get Data by ID |
| `user/search` | POST | Search Data Query |
| `user/update/{id}` | POST | Update Data by ID |
| `user/delete/{id}` | POST | Delete Data by ID |

## Example screen shots of API invocations

![content/category/store](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01283.png)

![content/category/store](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01284.png)

![content/category/&amp;lt;id&amp;gt;](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01285.png)

![content/category/](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01286.png)

![content/category/update/&amp;lt;id&amp;gt;](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01287.png)

![content/category/search](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01290.png)

![content/category/search](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-database-interface-layer/master/images/Selection_01291.png)

