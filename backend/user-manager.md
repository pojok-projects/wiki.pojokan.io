---
description: 'Main Developer: Vibi Primantono (https://github.com/hapehatelo)'
---

# User Manager

## API END POINT

* [https://api.tutorialinaja.tech/upa/v1/](https://api.tutorialinaja.tech/upa/v1/)

{% hint style="success" %}
Status: `LIVE`

Publish Date: `Sep 8, 2019 2:21 AM (AEST)`
{% endhint %}

## API Docs

* Api Docs: [https://tsupa.docs.apiary.io/\#](https://tsupa.docs.apiary.io/#)

## Codes

* Code Repository: [https://github.com/pojok-projects/tutorialsystem-user-manager](https://github.com/pojok-projects/tutorialsystem-user-manager)
* Language: PHP
* Framework: Laravel 

## Infrastructure

* CodePipeline: [tutorial-system-userm-master-cicd-pl](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines/tutorial-system-userm-master-cicd-pl/view?region=ap-southeast-1)
* CI/CD CloudFormation: [tutorial-system-userm-master-cicd-pipeline-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=us&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorial-system-userm-master-cicd-pipeline-cf%2F5f935060-d18b-11e9-9cf2-0200beb62082)
* Solution CloudFormation: [tutorial-system-userm-master-provisioning-cf](https://ap-southeast-1.console.aws.amazon.com/cloudformation/home?region=ap-southeast-1#/stacks/stackinfo?filteringText=us&filteringStatus=active&viewNested=true&hideStacks=false&stackId=arn%3Aaws%3Acloudformation%3Aap-southeast-1%3A706415835325%3Astack%2Ftutorial-system-userm-master-provisioning-cf%2F6b6baa10-d18e-11e9-9d5a-0a996106fc92)

## Description

User Manager manages the input and output processes with simple validation from the frontend to the database interface layer section.

See Red highlight below for the scope of this service:

![](../.gitbook/assets/image%20%2814%29.png)

## API Paths

### User

Represents User Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user` | GET | Get All Data |
| `user/store` | POST | Save Data |
| `user/{id}` | GET | Get Data by ID |
| `user/search` | GET | Search Data Query |
| `user/update/{id}` | PUT | Update Data by ID |
| `user/delete/{id}` | DELETE | Delete Data by ID |

#### Requests Tables Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `name` | string | required | name of user |
| `email` | string | required | email of user |
| `first_name` | string | required | first name of user |
| `last_name` | string | required | last name of user |
| `birth_date` | string | required | birth date of user |
| `gender` | string | required | gender of user \(male/female\) |
| `photo_profile` | string | optional | path of photo profile from user |
| `about` | string | optional | about of user |
| `website_link` | string | optional | website link of user |
| `facebook_link` | string | optional | facebook link of user |
| `twitter_link` | string | optional | twitter link of user |

### User Following

Represents User Following Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/following/store/{id_user}` | POST | Save Data |
| `user/following/{id_user}` | GET | Get Data by ID User |
| `user/following/delete/{id_user}/{id_following}` | DELETE | Delete Data by ID and ID Following |

#### Following Table Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `following_user_id` | string | required | User ID of Following User |

### User Follower

Represents User Follower Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/follower/store/{id_user}` | POST | Save Data |
| `user/follower/{id_user}` | GET | Get Data by ID User |
| `user/follower/delete/{id_user}/{id_follower}` | DELETE | Delete Data by ID User and ID Follower |

#### Follower Table Parameters:

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `follower_user_id` | string | required | User ID of Follower User |

### User Like Video

Represents User Like Video Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/likevideo/store/{id_user}` | POST | Save Data |
| `user/likevideo/{id_user}` | GET | Get Data by ID User |
| `user/likevideo/delete/{id_user}/{id_like_video}` | DELETE | Delete Data by ID User and ID Like Video |

#### Like Video Table Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `user_id` | string | required | User ID |
| `video_id` | string | required | ID of Metadata |

### User Dislike Video

Represents User Dislike Video Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/dislikevideo/store/{id_user}` | POST | Save Data |
| `user/dislikevideo/{id_user}` | GET | Get Data by ID User |
| `user/dislikevideo/delete/{id_user}/{id_dislike_video}` | DELETE | Delete Data by ID User and ID Disike Video |

#### Dislike Video Table Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `user_id` | string | required | User ID |
| `video_id` | string | required | ID of Metadata |

### User Saved Video

Represents User Saved Video Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/savedvideo/store/{id_user}` | POST | Save Data |
| `user/savedvideo/{id_user}` | GET | Get Data by ID User |
| `user/savedvideo/delete/{id_user}/{id_saved_video}` | DELETE | Delete Data by ID User and ID Saved Video |

#### Saved Video Table Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `video_id` | string | required | ID of Metadata |

### User History Video

Represents User History Video Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/historyvideo/store/{id_user}` | POST | Save Data |
| `user/historyvideo/{id_user}` | GET | Get Data by ID User |
| `user/historyvideo/update/{id_user}/{id_history_video}` | PUT | Update Data by ID User and ID History Video |
| `user/historyvideo/delete/{id_user}/{id_history_video}` | DELETE | Delete Data by ID User and ID History Video |

#### User History Video Table Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `video_id` | string | required | ID of Metadata |
| `last_watch` | string | required | Time of Last Watch Video |

### User Playlists

Represents User Playlists Details.

#### Table Structure End Points

| URL | Method | INFO |
| :--- | :--- | :--- |
| `user/playlists/store/{id_user}` | POST | Save Data |
| `user/playlists/{id_user}` | GET | Get Data by ID User |
| `user/playlists/update/{id_user}/{id_playlists}` | PUT | Update Data by ID User and ID Playlists |
| `user/playlists/delete/{id_user}/{id_playlists}` | DELETE | Delete Data by ID User and ID Playlists |

#### User Playlists Table Parameters

| Parameter | type | Status | Description |
| :--- | :--- | :--- | :--- |
| `playlistcategory_id` | string | required | ID From content playlists category |
| `metadata_id` | string | required | ID From content metadata |
| `order_list` | int | Optional | Order Playlist |
| `last_watch` | int | Optional | Remember Last Watch in second |

