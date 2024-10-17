# flutter_plugin_pubdev

A new Flutter project.

    Nama: Cinthya Achwatul Ifnu
    NIM: 2241720051
    Kelas: TI 3H
    No: 07

## Praktikum Menerapkan Plugin di Project Flutter
### Langkah 1: Buat Project Baru
Buatlah sebuah project flutter baru dengan nama flutter_plugin_pubdev. Lalu jadikan repository di GitHub Anda dengan nama flutter_plugin_pubdev.

### Langkah 2: Menambahkan Plugin
![alt](/images/02.png)

### Langkah 3: Buat file red_text_widget.dart
![alt](/images/03.png)

### Langkah 4: Tambah Widget AutoSizeText
![alt](/images/04.png)

### Langkah 5: Buat Variabel text dan parameter di constructor
![alt](/images/05.png)

### Langkah 6: Tambahkan widget di main.dart
![alt](/images/06.png)

### Hasil Output
![alt](/images/01.png)

## Tugas Praktikum

2. Perintah `flutter pub add auto_size_text` digunakan untuk menambahkan plugin `auto_size_text` ke dalam proyek Flutter secara otomatis. Saat dijalankan, perintah ini:

    - **Mengunduh Plugin:** Mengunduh paket `auto_size_text` beserta dependensi yang dibutuhkannya.

    - **Menambahkan ke pubspec.yaml:** Menambahkan entri `auto_size_text` di file `pubspec.yaml` pada bagian `dependencies`, sehingga plugin siap digunakan di proyek.

    - **Memudahkan Pengelolaan Dependensi:** Memastikan versi plugin yang sesuai diunduh tanpa perlu menambahkannya secara manual ke file `pubspec.yaml`.

    Plugin `auto_size_text` ini membantu dalam menyesuaikan ukuran teks secara otomatis agar sesuai dengan ruang yang tersedia di aplikasi.
    <br><br>

3. `RedTextWidget` adalah widget Flutter yang menampilkan teks dengan warna merah menggunakan `AutoSizeText` dari plugin `auto_size_text`. Fitur utamanya:

    - **Teks Otomatis Menyesuaikan Ukuran:** Mengatur ukuran font agar sesuai dengan area tampilan.
    - **Maksimal 2 Baris:** Teks ditampilkan maksimal dalam 2 baris.
    - **Potongan Otomatis:** Jika terlalu panjang, teks akan dipotong dengan tanda `...`. 

    Ini membuat teks mudah dibaca dalam ruang terbatas tanpa menghilangkan informasi penting.
    <br><br>

4. Kedua widget pada langkah 6 ini memiliki perbedaan dalam penggunaan widget dan warna latar belakang:

    1. **Container Pertama:**
    - **Latar Belakang:** `Colors.yellowAccent`
    - **Lebar:** `50`
    - **Widget:** Menggunakan `RedTextWidget`, yang otomatis menyesuaikan ukuran teks agar sesuai dengan ruang, memotong dengan `...` jika terlalu panjang.
    - **Teks:** "You have pushed the button this many times:"

    2. **Container Kedua:**
    - **Latar Belakang:** `Colors.greenAccent`
    - **Lebar:** `100`
    - **Widget:** Menggunakan `Text`, menampilkan teks apa adanya tanpa penyesuaian otomatis.
    - **Teks:** "You have pushed the button this many times:"

    Container pertama memiliki teks yang menyesuaikan ukuran dalam ruang kecil, sementara yang kedua menampilkan teks apa adanya di ruang yang lebih lebar.
    <br><br>

5. Jelaskan maksud dari tiap parameter yang ada di dalam plugin auto_size_text berdasarkan tautan pada dokumentasi ini !

    Berikut adalah penjelasan mengenai tiap parameter dalam plugin `auto_size_text`:

    - **key***: Mengatur bagaimana satu widget dapat menggantikan widget lain. Ini membantu Flutter dalam mengenali dan mengelola widget yang mengalami perubahan.

    - **textKey**: MDigunakan untuk menetapkan key pada widget yang dihasilkan, memberikan identitas unik sehingga mempermudah pengelolaan widget tersebut.

    - **style***: Jika diisi, menentukan gaya visual teks seperti font, warna, dan ukuran, memungkinkan penyesuaian tampilan sesuai kebutuhan.

    - **minFontSize**: Menentukan ukuran minimum yang dapat digunakan teks saat mengubah ukurannya secara otomatis. Parameter ini diabaikan jika presetFontSizes sudah diatur.

    - **maxFontSize**: Menentukan ukuran maksimum teks saat menyesuaikan ukuran secara otomatis. Parameter ini juga diabaikan jika presetFontSizes digunakan.

    - **stepGranularity**: Mengatur langkah-langkah perubahan ukuran font, memungkinkan penyesuaian yang lebih halus saat teks diubah ukurannya.

    - **presetFontSizes**: Menyediakan daftar ukuran font yang dapat digunakan, diatur dalam urutan menurun. Ini memungkinkan penggunaan ukuran font yang spesifik sebelum melakukan penyesuaian otomatis.

    - **group**: Menyinkronkan ukuran beberapa widget AutoSizeText. Dengan ini, beberapa teks dapat dibuat memiliki ukuran yang seragam.

    - **textAlign***: Mengatur perataan horizontal teks, mirip dengan properti textAlign pada widget Text. Bisa diatur menjadi TextAlign.left, TextAlign.center, TextAlign.right, dan lainnya.

    - **textDirection***: Mengontrol arah teks, yang memengaruhi bagaimana properti seperti TextAlign.start dan TextAlign.end dipahami. Ini berguna untuk bahasa dengan penulisan kanan-ke-kiri.

    - **locale***: Memilih font berdasarkan locale yang digunakan, penting untuk memastikan karakter Unicode dirender dengan benar sesuai konteks bahasa.

    - **softWrap***: Menentukan apakah teks akan dibungkus atau tidak ketika mencapai batas lebar.

    - **wrapWords**: Mengatur apakah kata-kata akan dibungkus jika tidak muat dalam satu baris. Secara default bernilai true, mirip dengan pengaturan pada widget Text.

    - **overflow***: Mengatur bagaimana teks yang melebihi batas ruang akan ditangani. Bisa digunakan untuk memotong teks atau menambahkan tanda elipsis (...).

    - **overflowReplacement**: Jika teks tidak muat dalam batas ruang yang disediakan, widget alternatif ini akan ditampilkan sebagai gantinya.

    - **textScaleFactor***: Mengontrol skala ukuran teks berdasarkan jumlah piksel font per piksel logis. Ini juga memengaruhi parameter seperti minFontSize, maxFontSize, dan presetFontSizes.

    - **maxLines**: Menentukan jumlah baris maksimum yang dapat digunakan teks. Ini berguna untuk membatasi tampilan teks dalam ruang tertentu.

    - **semanticsLabel***: Menyediakan label alternatif untuk teks, penting untuk tujuan aksesibilitas. Membantu perangkat pembaca layar memahami dan menyampaikan konteks teks.
    <br><br>
    
## Tugas Kelompok PBL
Berikut link untuk repository kelompok 5: https://github.com/Doniwyk/down-care