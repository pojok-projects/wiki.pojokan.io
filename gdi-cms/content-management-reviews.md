---
description: >-
  Contributors: Iman Suherman (https://github.com/iman-suherman), Juni Yadi
  (https://github.com/JuniYadi), Aldy Prastyo (https://github.com/dipras), Agung
  Jati (https://github.com/agungjati)
---

# Content Management Reviews

## Main Consideration

Dari sisi CMS pertimbangan utamanya adalah:

* Simple dan mudah di kembangkan secara kolaborasi
* Mendukung NoSQL database agar tidak menjadi single point of failure
* Secure dan tidak mudah di hack sebab menggunakan platform dan infrastruktur yang aman
* Ringan eksekusi tanpa menggunakan banyak memory
* Robust sehingga tidak mudah crash kalau traffic tinggi
* Scalable sehingga dapat secara otomatis di replicate server dan databasenya dalam hitungan miliseconds

Edge case:

Bayangkan seperti ini, kita punya ribuan content disimpan dalam traditional database lalu traffic membludak sampai jutaan. Resiko yang terjadi adalah database bisa down dan juga untuk scale biayanya akan sangat mahal[.](https://pojokanguruahli.slack.com/archives/CPJMCVCSD/p1572593757047300) NoSQL dengan DocumentDB sudah by default auto scale dengan cost yang lebih murah, sehingga tidak membebankan operasional dan juga performance super cepat, mengakibatkan system menjadi anti down dan anti crash.

Note:

CMS ini dapur dari suatu system, untuk itu keamanan menjadi nomor satu, jangan sampai content dapat dengan mudah di hack orang dan system dapat mudah menjadi crash.

## CMS Reviews

Berikut ini adalah list candidate CMS yang akan digunakan:

* enduro.js - minimalistic, lean & mean, node.js cms for professionals \| [https://www.endurojs.com](https://www.endurojs.com/)
* ApostropheCMS - An open-source Node.js CMS for the Enterprise \| [https://apostrophecms.com](https://apostrophecms.com/features,)
* pencilblue - Business class content management for Node.js \| [https://github.com/pencilblue/pencilblue](https://github.com/pencilblue/pencilblue)
* Strapi - Open source Node.js Headless CMS 🚀\| [https://strapi.io](https://strapi.io/)

Review Results:

### enduro.js

![Screen shot from mobile device](../.gitbook/assets/image%20%2832%29.png)

Kelebihan:

* Dari segi theme nya tampilan bagus 
* Dari sisi code nya mudah dibaca dan mudah dimengerti 
* Dari sisi eksekusi ringan dijalankan

Kelemahan: 

* Enduro tidak menggunakan database yg digunakan adalah flat files
* Theme bawaan Enduro js nya banyak error yg muncul 
* Banyak bug dalam code nya serta banyak file missing 
* Di github enduro juga banyak yg mendapat masalah error dalam menggunakan theme bawaan Enduro

### ApostropheCMS

![Screen shot from desktop device](../.gitbook/assets/image%20%2846%29.png)

Kelebihan:

* Fiturnya bisa drag drop widgetnya
* Backend nodejs \(express\)
* Frontend menggunakan nuckjs yang kurang popular
* Database menggunakan mongoDB

Kelemahan:

* Starting coding yang tidak mudah diikuti \(harus pergi ke source code utk menambah widget\)
* Harus pelajari widgetnya dahulu sehingga proses development bisa terhambat 
* Setiap tambahan feature dalam CMS harus diawali dengan edit codingan \(buat user managed feature seperti WordPress misalnya\)
* Teknologi yang digunakan tidak popular

### pencilblue

![Screen shot from desktop device](../.gitbook/assets/image%20%2821%29.png)

Kelemahan:

* Fiturnya terbatas hanya pada content management system
* Coding menggunakan vanilla.js yang sulit untuk dikembangkan dengan cepat
* Front end menggunakan angular.js versi lama dan jquery yang sudah tidak up to date
* Front sulit untuk di maintain karna menggunakan teknologi lama



### Strapi

Kelebihan:

* Flexible dalam database, dapat menggunakan sqllite \(file based storage\) maupun NoSQL database:

![](../.gitbook/assets/image%20%285%29.png)

* Memiliki build-in connector ke MongoDB:

![](../.gitbook/assets/image%20%2813%29.png)

* Struktur database strapi menggunakan NoSQL dengan object storage dan un-normalise data structure di MongoDB:

![](../.gitbook/assets/image%20%2811%29.png)

* Dapat membuat content baru secara otomatis:

![](../.gitbook/assets/image%20%2844%29.png)

* Memiliki role based permission untuk mengatur akses user dan API:

![](../.gitbook/assets/image%20%2825%29.png)

* Default api yang secure karena tidak bisa akses public, sehingga harus set dari permission =&gt; public:

![](../.gitbook/assets/image%20%2833%29.png)

* Memiliki support untuk GraphQL API dan Playground:

![](../.gitbook/assets/image%20%2824%29.png)

* API Documentation yang dibuat secara otomatis menggunakan Swagger:

![](../.gitbook/assets/image%20%2823%29.png)

* Random table reference ID yang auto generate menggunakan unique identifier untuk memastikan record yang dihasilkan akan selalu secure:

![](../.gitbook/assets/image%20%2819%29.png)

* Content thumbnail yang secara otomatis di-generate oleh system pada saat upload:

![](../.gitbook/assets/image%20%2812%29.png)

![](../.gitbook/assets/image%20%2827%29.png)

* Menggunakan table referensi yang berbeda untuk uploaded contents:

![](../.gitbook/assets/image%20%2829%29.png)

Kelemahan:

* Beberapa dependency yang digunakan memiliki resiko vulnerability issue yang harus di antisipasi dengan patch versi terbaru:

![](../.gitbook/assets/image%20%2828%29.png)

