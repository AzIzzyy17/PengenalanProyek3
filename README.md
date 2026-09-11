# Praktikum Modul 1 - [NIM] - [Ikhwan Syahid Azizy]

## Ringkasan halaman
Halaman web profil pribadi ini dikembangkan menggunakan HTML semantik dan CS3 murni tanpa bantuan framework eksternal. Proyek ini bertujuan untuk menampilkan profil mahasiswa secara terstruktur, serta memastikan aksesibilitas dan tata letak yang responsif di berbagai ukuran perangkat.

## Tiga keputusan teknis
1. **Penggunaan Elemen Semantik**: Mengganti seluruh struktur `<div>` generik dengan elemen semantik yang bermakna seperti `<header>`, `<nav>`, `<main>`, `<section>`, dan `<footer>` guna meningkatkan keterbacaan kode oleh mesin pencari dan teknologi bantu[cite: 1].
2. **Penerapan *Box-Sizing: Border-Box***: Diterapkan secara global pada seluruh elemen untuk memastikan lebar total komponen (`width`) tetap konsisten sesuai batas kontainer meskipun diberikan *padding* dan *border*[cite: 1].
3. **Pendekatan *Mobile-First* & Flexbox**: Mengatur tata letak dasar secara vertikal untuk layar kecil, kemudian menggunakan *media query* (`min-width: 768px`) untuk mengubah susunan elemen menjadi horizontal secara fleksibel[cite: 1].

## Masalah, diagnosis, dan perbaikan
- **Masalah 1**: Gambar profil sempat mengalami *overflow* atau keluar dari batas area tampilan pada layar seluler berukuran kecil.
  - **Diagnosis**: Lebar gambar diatur menggunakan nilai piksel statis tanpa pembatas persentase responsif[cite: 1].
  - **Perbaikan**: Menambahkan properti `max-width: 100%` dan `height: auto` pada elemen gambar agar ukurannya menyesuaikan kontainer secara proporsional[cite: 1].
- **Masalah 2**: Tautan navigasi kurang ramah aksesibilitas karena indikator fokus *keyboard* tidak terlihat jelas saat tombol `Tab` ditekan.
  - **Diagnosis**: Peramban web secara default terkadang menghilangkan atau kurang memperjelas batas fokus elemen interaktif tanpa aturan CSS spesifik[cite: 1].
  - **Perbaikan**: Menambahkan status `:focus-visible` dengan *outline* kontras tinggi yang jelas tanpa merusak fungsi bawaan peramban[cite: 1].

## Hasil pengujian empat viewport
- **320 px**: Tata letak tersusun rapi secara vertikal satu kolom, teks terbungkus sempurna, dan bebas dari *horizontal scroll* yang tidak diinginkan[cite: 1].
- **375 px**: Konsisten dengan ukuran sebelumnya, memberikan ruang jarak antar komponen yang nyaman dilihat pada perangkat seluler standar[cite: 1].
- **768 px**: Komponen mulai beradaptasi secara struktural seiring bertambahnya lebar ruang layar tablet[cite: 1].
- **1024 px**: Tata letak optimal tercapai dengan kontainer yang berada di tengah (`margin-inline: auto`) serta susunan visual yang seimbang[cite: 1].

## Refleksi belajar
Melalui praktikum modul pertama ini, saya memperoleh pemahaman mendalam mengenai pentingnya memisahkan struktur konten (HTML) dan lapisan presentasi (CSS). Tantangan yang saya hadapi adalah kemampuan saya sendiri, saya merasa bahwasanya saya masih sangat jauh untuk bisa mengerjakan semua yang telah ditugaskan sendiri tanpa bantuan AI sehingga dalam proses pengerjaan tugas ini, saya masih sangat banyak melibatkan AI entah itu bertanya atau membantu dalam pembuatan codenya. Ke depannya, saya ingin terus memperkuat kompetensi dalam merancang  web.

## Log AI atau sumber bantuan
- **Sumber Utama**: Modul 1 Proyek 3 — Dasar Web (HTML & CSS) serta dokumentasi resmi MDN Web Docs[cite: 1].
- **Bantuan AI**: Saya di tahap awal pengerjaan tugas ini masih digunakan sebagai teman diskusi dan code sepenuhnya saya sendiri yang membangun, tapi mulai dari pertengahan saya merasa sangat kesulitan, mungkin karena faktor kemampuan saya yang masih sangat kurang dan juga saya merasa kekurangan waktu untuk mengerjakan ini sehingga saya akhirnya banyak menggunakan AI untuk membantu dan mempercepat pengerjaan saya agar bisa mengejar Deadline.