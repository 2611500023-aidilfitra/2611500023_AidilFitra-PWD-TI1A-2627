# pertemuan-06 PHP Dasar dan Pemrograman Sisi Peladen

## Deskripsi

 Pada pertemuan P6 ini dilakukan pengembangan wbsite dengan PHP dasar dan pemrograman sisi peladen yaitu mengubah index.html ke index.php penggunaan sinbtaks dasar PHP, mengelola data menggunakan variabel, konstanta, operator, percabangan dan perulangan. dan mejalankan dengan web lokal server localhost.

## Fitur dan pengembangan 

- Perubahan file HTML menjadi PHP: Mengganti `index.html` menjadi `index.php` dan menambahkan tag pembuka <?php serta penutup ?> untuk menuliskan kode PHP di dalam halaman.
- Variabel: Menggunakan tanda $ untuk membuat variabel, contohnya $nama = "Aidil"; untuk menyimpan data nama.
- Konstanta: Menggunakan const untuk menyimpan nilai yang tidak berubah, contohnya const NAMA_MATA_KULIAH = "Pemrograman Web Dasar";
- Operator: Digunakan untuk melakukan operasi perhitungan serta menentukan hubungan antar nilai. Contohnya, $sisaSemester = $batasSemester - $semester; untuk menghitung sisa semester, sedangkan $semesterValid = $semester >= 1 && $semester <= $batasSemester; untuk memeriksa apakah nilai semester berada dalam rentang yang ditentukan
- Percabangan: Menggunakan if, elseif, dan else untuk menentukan hasil berdasarkan kondisi tertentu.
- switch-case-default: Memilih satu hasil dari beberapa pilihan nilai, contohnya yaitu switch ($programStudi) { case "SI": ... case "TI": ... default: ... } untuk menentukan fokus program studi.
- Perulangan for dan while: for ($i = 1; $i <= 5; $i++) dipakai untuk membuat daftar target belajar, dan while ($nomorSemester <= 3) dipakai untuk membuat daftar semester.
- Menampilkan data: echo dan print untuk mencetak nilai, serta <?= ... ?> sebagai singkatan echo, contohnya yaitu <?= date("Y") ?> untuk tahun di footer.

## Cara Menjalankan Websitenya

Menjalankan PHP melalui Laragon: File PHP tidak dapat dijalankan secara langsung dengan klik dua kali, sehingga membutuhkan server lokal untuk memprosesnya. Langkah-langkahnya sebagai berikut:
1. Membuka aplikasi Laragon, kemudian menekan tombol Start All untuk mengaktifkan server.
2. Membuka browser dan memasukkan alamat http://localhost/PWD/2627o/ti1a/2611500009-PWD-TI1A-2627O/pertemuan-06/.
3. Mengakses halaman website melalui localhost untuk melihat hasil eksekusi kode PHP.

## Pengujian 

1. **Variabel dan konstanta:** Pengujian dilakukan dengan membuka `index.php` melalui localhost dan memeriksa bagian Beranda. Hasilnya, nama, mata kuliah, dan tahun akademik berhasil ditampilkan sesuai data yang telah ditentukan, yaitu "Aidil Fitra", "Pemrograman Web Dasar", dan "2026/2027".

2. **Operator:** Pengujian dilakukan pada bagian Tentang Saya untuk melihat hasil perhitungan dan validasi semester. Hasilnya, sisa semester menunjukkan angka 7 dan status pemeriksaan rentang semester menampilkan "Sesuai rentang".

3. **if-elseif-else:** Pengujian dilakukan dengan memperhatikan informasi pada bagian Semester. Hasilnya, nilai semester 1 menghasilkan keterangan "Semester awal". Ketika nilai diubah menjadi 4 atau 7, keterangan menyesuaikan menjadi "Semester menengah" atau "Semester akhir".

4. **Switch-case-default:** Pengujian dilakukan dengan melihat informasi Program Studi dan Fokus Program Studi. Hasilnya, program studi menampilkan "Teknik Informatika (TI)" dengan fokus "Komputasi dan pengembangan perangkat lunak". Apabila nilai program studi tidak sesuai pilihan, sistem menampilkan "Belum ditentukan".

5. **Perulangan for:** Pengujian dilakukan dengan memeriksa bagian Target Belajar. Hasilnya, program berhasil menampilkan lima daftar target belajar, dengan target kelima berisi "Belum dipetakan" karena menggunakan kondisi default.

6. **Perulangan while:** Pengujian dilakukan pada bagian daftar Semester. Hasilnya, perulangan berhasil menghasilkan tiga data semester, yaitu Semester 1, Semester 2, dan Semester 3.

7. **Format nilai dan null:** Pengujian dilakukan dengan melihat informasi IPK dan Catatan Tambahan. Hasilnya, IPK ditampilkan dalam format 3,75, sedangkan data catatan yang bernilai `null` diganti menjadi "Belum ada".

8. **Fitur lama (navigasi dan form):** Pengujian dilakukan dengan menekan tombol hamburger (☰) dan mencoba mengirim formulir menggunakan data kosong maupun data yang telah diisi. Hasilnya, menu navigasi dan proses validasi formulir tetap berjalan dengan baik seperti pada versi sebelumnya (`index.html`).

## Riwayat Pengembangan 

Riwayat pengembangan proyek dicatat berdasarkan tahapan pengerjaan melalui commit Git yang memiliki keterangan sesuai perubahan yang dilakukan.

1. **Menyalin file P5 ke P6:** Memindahkan file dan hasil pengerjaan dari pertemuan sebelumnya sebagai dasar pengembangan proyek P6.
2. **Mengubah index.html menjadi index.php:** Mengganti nama file utama agar dapat digunakan untuk menjalankan kode PHP.
3. **Menguji komentar, echo, dan tag PHP:** Mencoba penggunaan tag pembuka dan penutup PHP, komentar, serta perintah `echo` untuk memastikan kode berhasil dijalankan.
4. **Mempelajari komentar, echo, dan print:** Mencoba perintah `echo` dan `print` serta memahami bahwa komentar tidak ditampilkan pada halaman browser.
5. **Menguji penggunaan HTML dan PHP:** Membandingkan penulisan HTML biasa dengan HTML yang dibuat melalui PHP, kemudian memeriksa hasilnya menggunakan View Page Source.
6. **Membuat variabel PHP:** Menambahkan sejumlah variabel untuk menyimpan informasi mahasiswa, seperti `$nim`, `$namaMahasiswa`, `$semester`, dan `$ipk`.
7. **Mendefinisikan konstanta PHP:** Membuat konstanta `NAMA_MATA_KULIAH` dan `PROFIL_GITHUB` menggunakan perintah `const`.
8. **Menampilkan informasi mahasiswa:** Menggunakan variabel dan konstanta untuk menampilkan identitas mahasiswa, mata kuliah, tahun akademik, serta tautan GitHub pada halaman Beranda.
9. **Menerapkan operator aritmetika:** Menambahkan perhitungan sisa semester menggunakan `$batasSemester - $semester` pada bagian Profil Singkat.
10. **Membuat validasi rentang semester:** Menggunakan operator perbandingan, logika, dan ternary untuk menentukan status kesesuaian nilai semester.
11. **Menerapkan percabangan if-elseif-else:** Membuat kondisi untuk mengelompokkan semester menjadi kategori awal, menengah, dan akhir.
12. **Menggunakan operator ternary:** Menambahkan kondisi singkat untuk menentukan nama program studi serta status keaktifan mahasiswa.
13. **Menerapkan switch-case:** Membuat pemilihan fokus program studi berdasarkan kode yang tersimpan pada variabel.
14. **Membuat perulangan for:** Menampilkan lima target belajar secara otomatis dengan bantuan perulangan dan kondisi switch.
15. **Membuat perulangan while:** Menghasilkan daftar semester dari angka 1 hingga 3 menggunakan kondisi perulangan.
16. **Mengatur format tampilan IPK:** Memanfaatkan `number_format()` untuk menampilkan nilai IPK dengan dua angka desimal dan tanda koma.
17. **Menangani nilai null:** Menambahkan kondisi agar catatan tambahan menampilkan tulisan "Belum ada" apabila tidak memiliki nilai.
18. **Menampilkan tahun secara otomatis:** Menggunakan `date("Y")` pada bagian footer agar tahun dapat menyesuaikan secara dinamis.
19. **Menggunakan sintaks singkat PHP:** Menerapkan `<?= ... ?>` untuk mempersingkat penulisan keluaran PHP pada tautan GitHub dan footer.
20. **Menyesuaikan action formulir:** Mengarahkan atribut `action` pada form ke file `index.php` agar proses pengiriman formulir sesuai dengan halaman PHP.
21. **Menyusun dokumentasi README:** Melengkapi dokumentasi proyek yang mencakup deskripsi, fitur dan pengembangan, cara menjalankan program, pengujian, serta riwayat pengembangan.