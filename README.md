# flutter_plugin_pubdev

Praktikum Menerapkan Plugin di Project Flutter

## Langkah 1: Buat Project Baru

Buatlah sebuah project flutter baru dengan nama **flutter_plugin_pubdev**. Lalu jadikan repository di GitHub Anda dengan nama **flutter_plugin_pubdev**.

## Langkah 2: Menambahkan Plugin

Tambahkan plugin `auto_size_text` menggunakan perintah berikut di terminal
````
flutter pub add auto_size_text
````

## Langkah 3: Buat file red_text_widget.dart

Buat file baru bernama `red_text_widget.dart` di dalam folder lib lalu isi kode seperti berikut.

![screenshoot](images/1.PNG)

## Langkah 4: Tambah Widget AutoSizeText

Masih di file `red_text_widget.dart`, untuk menggunakan plugin `auto_size_text`, ubahlah kode return `Container()` menjadi seperti berikut.

![screenshoot](images/2.PNG)

Setelah Anda menambahkan kode di atas, Anda akan mendapatkan info error. Mengapa demikian? Jelaskan dalam laporan praktikum Anda!

Jawab : Terjadinya error karena tidak ada variabel text dan paramater di dalam constructor setelah menambahkan langkah 5 yang dibawah ini maka sudah tidak terjadi error

## Langkah 5: Buat Variabel text dan parameter di constructor

Tambahkan variabel `text` dan parameter di constructor seperti berikut.

![screenshoot](images/3.PNG)

## Langkah 6: Tambahkan widget di main.dart

Buka file `main.dart` lalu tambahkan di dalam `children:` pada class `_MyHomePageState`

![screenshoot](images/4.PNG)

# Tugas Praktikum

1. Selesaikan Praktikum tersebut, lalu dokumentasikan dan push ke repository Anda berupa screenshot hasil pekerjaan beserta penjelasannya di file README.md!

2. Jelaskan maksud dari langkah 2 pada praktikum tersebut!

Jawab : Maksud dari langkah 2 pada praktikum yaitu menambahkan plugin `auto_size_text`

3. Jelaskan maksud dari langkah 5 pada praktikum tersebut!

Jawab : Dari langkah 5 pada praktikum yaitu terdapat kode program tersebut agar text yang digunakan dapat diubah secara dinamis pada komponen yang lainnya, dapat dilihat pada widget `AutoSizeText()` bagian baris pertama terdapat `text` yang belum memiliki nilai berupa String, jadi nilai tersebut didapatkan dari variable `text` pada parameter di constructornya.

4. Pada langkah 6 terdapat dua widget yang ditambahkan, jelaskan fungsi dan perbedaannya!

Jawab : Fungsi dari kedua widget tersebut adalah sama-sama untuk menampilkan text. Perbedaannya terletak pada pengunaannya, untuk yang widget pertama memanggil class `RedTextWidget` yang didalamnya terdapat parameter `text` untuk digunakan pada widget `AutoSizeText()`. Sedangkan untuk widget yang kedua, langsung memanggil widget `Text()` tanpa menggunakan plugin tambahan atau pemanggilan class yang lainnya.

5. Jelaskan maksud dari tiap parameter yang ada di dalam plugin `auto_size_text` berdasarkan tautan pada dokumentasi <https://pub.dev/documentation/auto_size_text/latest/> !!

Jawab : 

| Parameter     | Description   | 
| ------------- |:--------------| 
| `key`*     | Melakukan control bagaimana widget satu me-replace widget yang lain | 
| `textKey`    | Melakukan inisialisasi key sebagai hasil pada `Text` widget |
| `style`* | Melakukan styling pada text |   
| `minFontSize` | Font minimal yang digunakan text |
| `maxFontSize` | Font maksimal yang digunakan text |
| `stepGranularity` | Menentukan pengurangan size text pada tiap baris |
| `presetFontSizes` | Menentukan besarnya fontsize pada `minFontSize`, `maxFontSize` dan `stepGranularity` |
| `group` | Digunakan untuk sinkronisasi ukuran pada saat menggunakan multiple `AutoSizeText` |
| `textAlign`* | Digunakan sebagai perataan text |
| `textDirection`* | Menentukan arah text, seperti `TextAlign.start` dan `TextAlign.end`. |
| `locale`* | Digunakan untuk memilih font ketika karakter Unicode yang sama dapat dirender secara berbeda, tergantung pada lokal. |
| `softWrap`* | Menentukan breakline dari text |
| `wrapWords` | Jika kalimat tidak memuat pada satu baris, maka akan di wrap. |
| `overflow`* | Untuk memvisualisasikan text yang overflow |
| `overflowReplacement` | Untuk memvisualisasikan text yang overflow dengan mengganti dengan text atau widget yang lain. |
| `textScaleFactor`* | Intensitas dari font pixels. |
| `maxLines` | Batas maksimal baris text |
| `semanticsLable`* | Label semantik pada text |

6. Kumpulkan laporan praktikum Anda berupa link repository GitHub ke LMS!