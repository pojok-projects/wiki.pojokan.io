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

Pertimbangan menggunakan NoSQL database:

* Flexibility \(we don’t have to define a schema using migrations, unless we want to set indexes or unique keys\) 
* Speed \(since we do not rely on tables and we rely on JSON-encoded files that are written on disk, we get high I/O\) 
* Scalability \(we can create replicas, just like in MySQL, but we can shard, or “split” the database content, and we can scale it across multiple regions without cutting off speed or availability\)

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
* 首页 \| Laravel-admin \| [https://laravel-admin.org](https://laravel-admin.org/)

Review Results:

### enduro.js

![Screen shot from mobile device](../.gitbook/assets/image%20%2835%29.png)

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

![Screen shot from desktop device](../.gitbook/assets/image%20%2850%29.png)

Kelebihan:

* Fiturnya bisa drag drop widgetnya
* Backend nodejs \(express\)
* Database menggunakan mongoDB

Kelemahan:

* Starting coding yang tidak mudah diikuti \(harus pergi ke source code utk menambah widget\)
* Harus pelajari widgetnya dahulu sehingga proses development bisa terhambat 
* Setiap tambahan feature dalam CMS harus diawali dengan edit codingan \(buat user managed feature seperti WordPress misalnya\)
* Frontend menggunakan nuckjs yang kurang popular

### pencilblue

![Screen shot from desktop device](../.gitbook/assets/image%20%2824%29.png)

Kelemahan:

* Fiturnya terbatas hanya pada content management system
* Coding menggunakan vanilla.js yang sulit untuk dikembangkan dengan cepat
* Front end menggunakan angular.js versi lama dan jquery yang sudah tidak up to date
* Front sulit untuk di maintain karna menggunakan teknologi lama



### Strapi

Kelebihan:

* Flexible dalam database, dapat menggunakan sqllite \(file based storage\) maupun NoSQL database:

![](../.gitbook/assets/image%20%286%29.png)

* Memiliki build-in connector ke MongoDB:

![](../.gitbook/assets/image%20%2815%29.png)

* Struktur database strapi menggunakan NoSQL dengan object storage dan un-normalise data structure di MongoDB:

![](../.gitbook/assets/image%20%2812%29.png)

* Dapat membuat content baru secara otomatis:

![](../.gitbook/assets/image%20%2848%29.png)

* Memiliki role based permission untuk mengatur akses user dan API:

![](../.gitbook/assets/image%20%2828%29.png)

* Default api yang secure karena tidak bisa akses public, sehingga harus set dari permission =&gt; public:

![](../.gitbook/assets/image%20%2836%29.png)

* Memiliki support untuk GraphQL API dan Playground:

![](../.gitbook/assets/image%20%2827%29.png)

* API Documentation yang dibuat secara otomatis menggunakan Swagger:

![](../.gitbook/assets/image%20%2826%29.png)

* Random table reference ID yang auto generate menggunakan unique identifier untuk memastikan record yang dihasilkan akan selalu secure:

![](../.gitbook/assets/image%20%2822%29.png)

* Content thumbnail yang secara otomatis di-generate oleh system pada saat upload:

![](../.gitbook/assets/image%20%2813%29.png)

![](../.gitbook/assets/image%20%2830%29.png)

* Menggunakan table referensi yang berbeda untuk uploaded contents:

![](../.gitbook/assets/image%20%2832%29.png)

Kelemahan:

* Beberapa dependency yang digunakan memiliki resiko vulnerability issue yang harus di antisipasi dengan patch versi terbaru:

![](../.gitbook/assets/image%20%2831%29.png)

### Laravel Admin

Kelebihan:

* Teknologi yang digunakan umum di pasaran sehingga dapat meningkatkan kecepatan process development:

![](../.gitbook/assets/image%20%2814%29.png)

* Laravel admin memiliki tampilan yang mirip dengan package [https://github.com/jeroennoten/Laravel-AdminLTE](https://github.com/jeroennoten/Laravel-AdminLTE), hanya perbedaannya adalah Laravel Admin memiliki feature content management system sedangkan Laravel-AdminLTE hanya merupakan admin template
* Laravel-admin memiliki support forms yang banyak dan system input dari 1 table ke table lain serta table relational yang otomatis diatur langsung dari code

Kelemahan:

* Laravel Admin masih heavily depends on RDBMS dan table relationship: 

![](../.gitbook/assets/image%20%283%29.png)

* Laravel admin belum mendukung NoSQL database \(seperti MongoDB misalnya\): [https://github.com/z-song/laravel-admin/issues/4098](https://github.com/z-song/laravel-admin/issues/4098)
* Laravel Admin menggunakan Discovery Package untuk melakukan process route ke dalam database pada admin menu sehingga perubahan database engine layer menjadi NoSQL menjadi sulit dilakukan
* Laravel Admin masih menggunakan base framework Laravel 5.5 \(release tahun 2017 dan support hanya sampai 30 Agustus 2020 saja\) yang cukup tertinggal dari Long Term Support versi laravel terbaru yaitu versi 6.0
* Walaupun support page dapat di translate ke bahasa Inggris namun main community heavily menggunakan Chinese language yang akan menjadi kendala di kemudian hari dalam hal troubleshooting:

![](../.gitbook/assets/image%20%2847%29.png)

* Umur community yang masih muda ini \(belum mature\) sehingga masih perlu tambahan waktu agar memiliki feature yang sebanding dengan CMS lainnya

## CMS Review Scoring

### enduro.js

| Factors | Scores |
| :--- | :--- |
| Simplicity | **✮✮✮✮✮** |
| NoSQL database support | **✮** |
| Security | **✮** |
| Memory and CPU footprints | **✮✮✮** |
| Robustness | **✮✮✮** |
| Scalability | **✮✮✮** |
| **Total Score** | 16 |

### ApostropheCMS

| Factors | Scores |
| :--- | :--- |
| Simplicity | **✮** |
| NoSQL database support | **✮✮✮✮✮** |
| Security | **✮✮✮** |
| Memory and CPU footprints | **✮✮✮** |
| Robustness | **✮✮✮** |
| Scalability | **✮** |
| **Total Score** | 17 |

### pencilblue

| Factors | Scores |
| :--- | :--- |
| Simplicity | **✮** |
| NoSQL database support | **✮** |
| Security | **✮** |
| Memory and CPU footprints | **✮✮✮** |
| Robustness | **✮✮✮** |
| Scalability | **✮** |
| **Total Score** | 10 |

### Strapi

| Factors | Scores |
| :--- | :--- |
| Simplicity | **✮✮✮** |
| NoSQL database support | **✮✮✮✮✮** |
| Security | **✮✮** |
| Memory and CPU footprints | **✮✮✮** |
| Robustness | **✮✮✮** |
| Scalability | **✮✮✮** |
| **Total Score** | 19 |

### Laravel-admin

| Factors | Scores |
| :--- | :--- |
| Simplicity | **✮✮✮✮✮** |
| NoSQL database support | **✮** |
| Security | **✮✮** |
| Memory and CPU footprints | **✮✮** |
| Robustness | **✮✮✮** |
| Scalability | **✮✮✮** |
| **Total Score** | 18 |

## Final Score Comparison

| CMS Name | Scores |
| :--- | :--- |
| Strapi | **19** |
| Laravel-admin | **18** |
| ApostropheCMS | **17** |
| enduro.js | **16** |
| pencilblue | **10** |

## Conclusion

Dari hasil score diatas Strapi unggul tipis dibandingkan dengan Laravel-admin satu point saja. Dari sisi code simplicity, Laravel-admin lebih unggul karena memiliki teknologi yang umum digunakan di pasaran sehingga process development jadi cepat dan mudah. Namun dari sisi database support, Laravel-admin masih belum mendukung NoSQL database. Sedangkan di sisi lain Stapi selain memiliki kelebihan support NoSQL mongoDB database, Strapi juga dibangun di atas node.js framework yang memiliki memory serta CPU footprints yang lebih kecil dibanding Laravel-admin yang menggunakan PHP.  

