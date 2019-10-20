---
description: 'Main Developer: Vibi Primantono (https://github.com/hapehatelo)'
---

# Category Manager

## API END POINT

* [https://api.tutorialinaja.tech/catm/v1/](https://api.tutorialinaja.tech/catm/v1/)[ ](https://api.tutorialinaja.tech/catm/v1/)

{% hint style="success" %}
Status: `LIVE`

Publish Date: `Sep 6, 2019 3:29 AM (AEST)`
{% endhint %}

## API Docs

* Api Docs: [https://tscatm.docs.apiary.io/\#](https://tscatm.docs.apiary.io/#)

## Codes

* Api Repository: [https://github.com/pojok-projects/tutorialsystem-catm](https://github.com/pojok-projects/tutorialsystem-catm)
* Language: JavaScript
* Framework: node.js Express 

## Infrastructure

* CodePipeline: [tutorialsystem-catm-master-cicd-pl](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines/tutorialsystem-catm-master-cicd-pl/view?region=ap-southeast-1)
* CI/CD CloudFormation: [tutorialsystem-catm-master-cicd-pipeline-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=cat&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorialsystem-catm-master-cicd-pipeline-cf%2F3a174470-f2d5-11e9-851d-0ad08b3552b8)
* Solution CloudFormation: [tutorialsystem-catm-master-provisioning-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=cat&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorialsystem-catm-master-provisioning-cf%2F8caa2ef0-f2d5-11e9-b5e2-0a0613236510)

## Description

Category Manager manages the input and output processes with simple validation from the frontend to the database interface layer section.

See Red highlight below for the scope of this service:

![](../.gitbook/assets/image%20%2821%29.png)

## Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `category` | GET | Get All Data |
| `category/store` | POST | Save Data |
| `category/{id}` | GET | Get Data by ID |
| `category/search` | GET | Search Data Query |
| `category/update/{id}` | PUT | Update Data by ID |
| `category/delete/{id}` | DELETE | Delete Data by ID |

## Example screen shots of API invocations

### \[GET\] Get Category

![Get Category](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/01-get-category.png)

### \[POST\] Input Category Success

![Input Category Success](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/02-post-category-success.png)

### \[POST\] Input Category Already Availale

![Input Category Already Availale](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/03-post-category-already-available.png)

### \[GET\] Get Detail Category

![Get Detail Category](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/04-get-detail-category.png)

### \[PUT\] Update Category Success

![Update Category Success](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/06-put-update-category-success.png)

### \[PUT\] Update Category Already Availale

![Update Category Already Availale](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/07-put-update-category-already-availabe.png)

### \[DELETE\] Delete Category

![Delete Category](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/08-delete-category.png)

### \[POST\] Input Category Validation

![Input Category Validation](https://raw.githubusercontent.com/pojok-projects/tutorialsystem-category-manager/master/images/09-post-category-validation.png)

