---
description: 'Iman Suherman (https://github.com/iman-suherman)'
---

# Setup AWS CodePipeline for Strapi

## Description

AWS CodePipeline adalah rangkaian dari Infrastructure as a Code yang merupakan bagian dari Continuously Integration \(CI\) dan Continuously Deployment \(CD\) pipeline untuk process deployment dari code commit pada GitHub repository \(pada master branch\) secara otomatis ke AWS infrastructure tanpa human intervention.

Adapun AWS CodePipeline setup untuk Strapi deployment berada pada lokasi berikut:

[https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines/gdi-cms-master-cicd-pl/view?region=ap-southeast-1](https://ap-southeast-1.console.aws.amazon.com/codesuite/codepipeline/pipelines/gdi-cms-master-cicd-pl/view?region=ap-southeast-1)

![](../../.gitbook/assets/image%20%2836%29.png)

Code Pipeline untuk GDI CMS ini terdiri dari beberapa components:

### Source

Source adalah process trigger secara otomatis melalui GitHub Repository GDI CMS melalui repository berikut:

{% embed url="https://github.com/Pojokan-Guru-Ahli/gdi-cms" %}

yang secara otomatis akan men-trigger CI/CD pipeline deployment apabila dilakukan pull request approval atau code commit pada master branch.

Berikut ini contoh code commit yang dibuat dalam GitHub repository:

![](../../.gitbook/assets/image%20%2821%29.png)

Maka script update tersebut akan melakukan process trigger terhadap source step pada AWS CodePipeline:

![](../../.gitbook/assets/image%20%2824%29.png)

### Build

Pada process build, dilakukan compilation terhadap code melalui predefined CodePipeline CloudFormation stack yang sudah dibuat dari code berikut:

[https://github.com/Pojokan-Guru-Ahli/gdi-cms/blob/master/pipeline.yaml](https://github.com/Pojokan-Guru-Ahli/gdi-cms/blob/master/pipeline.yaml)

Adapun commands yang di-eksekusi pada tahap ini adalah:

![](../../.gitbook/assets/image%20%2842%29.png)

Dengan waktu timeout selama 10 menit. 

Berikut ini screen shot pada AWS CodePipeline untuk tahap ini:

![](../../.gitbook/assets/image%20%2834%29.png)

### Deploy

Process deploy adalah tahap dimana hasil code build diatas disimpan sebagai artifact pada S3 bucket untuk dilakukan deployment pada server CMS Strapi.

Berikut ini screen shot pada AWS CodePipeline untuk tahap ini:  

![](../../.gitbook/assets/image%20%2861%29.png)

Berikut ini adalah artifact hasil deployment ini yang berhasil di simpan di S3 bucket:

![](../../.gitbook/assets/image%20%2816%29.png)

### Restart

Setelah artifact dibuat, process terakhir adalah melakukan copy dari hasil build diatas ke dalam server menggantikan script yang ada sebelumnya di server.

