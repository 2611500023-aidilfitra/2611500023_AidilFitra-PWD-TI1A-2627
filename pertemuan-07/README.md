# pertemuan-07 Pemrosesan Formulir dengan PHP, Validasi Sisi Peladen, dan RPG

## Deskripsi

Dokumentasi pengembangan halaman web pada P7, meliputi pengiriman data formulir dengan GET dan Post, validasi sisi peladen, pengaman keluaran HTML, penggunaan session, dan pola Post-Redirect-Get (PRG). pengembangan dilanjutkan dari artefak P6.

## fitur dan Pengembangan

- **Persiapan proyek dari P6:** Menyalin seluruh file dari pertemuan sebelumnya, seperti `index.php`, `style.css`, `script.js`, dan folder `img` ke direktori `pertemuan-07` sebagai dasar pengerjaan P7.

- **Penerapan metode GET (`$_GET`):** Menggunakan metode GET untuk menerima data melalui parameter URL. Data tersebut kemudian diambil menggunakan `$_GET`, contohnya `if (isset($_GET['nama'])) { $nama = $_GET['nama']; }`. Penerapannya dibuat pada file `indexGet.php`.

- **Penerapan metode POST (`$_POST`):** Mengubah metode pengiriman formulir menjadi `method="post"` agar informasi dikirim melalui request body dan tidak terlihat pada alamat URL. Data diterima menggunakan `$_POST`, contohnya `$nama = trim((string) ($_POST['nama'] ?? ''));`.

- **Penggunaan checkbox minat (`minat[]`):** Mengatur nama input checkbox menjadi `minat[]` supaya pengguna dapat memilih lebih dari satu pilihan. Penyesuaian juga dilakukan pada JavaScript agar proses pemeriksaan checkbox tetap berjalan.

- **Validasi data menggunakan PHP:** Menambahkan pemeriksaan di sisi server untuk memastikan data yang diterima sesuai ketentuan. Validasi meliputi pengisian data, pemeriksaan email menggunakan `filter_var()`, pengecekan semester menggunakan `FILTER_VALIDATE_INT`, serta pembatasan pilihan dengan `in_array()`.

- **Pembersihan input (normalisasi data):** Memanfaatkan fungsi `trim((string) ...)` untuk menghilangkan spasi berlebih pada data yang dimasukkan sebelum dilakukan pemeriksaan.

- **Keamanan tampilan data:** Menggunakan `htmlspecialchars($nilai, ENT_QUOTES, 'UTF-8')` ketika menampilkan kembali input pengguna agar karakter tertentu tidak diproses sebagai kode HTML.

- **Penggunaan session dan metode PRG:** Menyimpan hasil pengolahan formulir ke dalam `$_SESSION`, kemudian menerapkan pengalihan halaman menggunakan `header('Location: index.php'); exit;`. Pesan kesalahan dihapus setelah ditampilkan, sedangkan data formulir tetap disimpan agar tidak perlu dimasukkan kembali.

## Pengujian

1. **Pengujian parameter GET:** Dilakukan dengan membuka `indexGet.php?nama=Aidil`, kemudian mengganti parameter menjadi `?nama=Aidil%20Fitra` dan mencoba mengakses halaman tanpa parameter. Hasilnya, halaman menampilkan nama sesuai nilai yang dikirim melalui URL. Apabila parameter tidak tersedia, halaman tidak menampilkan teks maupun peringatan kesalahan.

2. **Pengujian formulir GET:** Dilakukan dengan mengisi seluruh bagian formulir menggunakan data yang valid pada `indexGet.php`, kemudian menekan tombol Kirim. Hasilnya, data berhasil dikirim melalui URL dengan parameter yang dipisahkan menggunakan tanda `&`, dan nama yang dimasukkan muncul pada halaman.

3. **Pengujian formulir POST:** Dilakukan dengan mengisi formulir pada `index.php` menggunakan data yang diperlukan, lalu mengirimkannya. Hasilnya, informasi berhasil diterima dan ditampilkan pada halaman tanpa memperlihatkan nilai input pada alamat URL.

4. **Pengujian checkbox minat (`minat[]`):** Dilakukan dengan mencoba mengirim dua pilihan topik, satu pilihan, dan tanpa memilih topik pada kedua formulir. Hasilnya, sistem dapat membaca beberapa pilihan sekaligus. Jika tidak ada pilihan yang dicentang, muncul pemberitahuan "Pilih minimal satu topik yang diminati."

5. **Pengujian validasi sisi peladen:** Dilakukan dengan menonaktifkan sementara `script.js`, kemudian mengirim formulir dalam keadaan kosong dan mencoba memasukkan alamat email yang tidak sesuai format. Hasilnya, PHP tetap melakukan pemeriksaan dan menampilkan pesan kesalahan berwarna merah, seperti "Nama lengkap wajib diisi", "Email wajib diisi", serta "Format email tidak valid." Setelah pengujian selesai, JavaScript diaktifkan kembali.

6. **Pengujian keamanan keluaran:** Dilakukan dengan memasukkan teks `<b>Mahasiswa</b>` pada kolom pesan, kemudian mengirim formulir. Hasilnya, teks ditampilkan dalam bentuk tulisan biasa dan tidak berubah menjadi format huruf tebal karena telah melalui proses pengamanan keluaran.

7. **Pengujian session dan PRG:** Dilakukan dengan mengirim formulir menggunakan data yang valid, kemudian memuat ulang halaman menggunakan `CTRL + SHIFT + R`. Hasilnya, halaman diarahkan kembali ke `index.php`, informasi pada bagian "Data yang Diterima Peladen" tetap tersedia, dan browser tidak meminta pengiriman formulir ulang.

## Riwayat Pengembangan

Proses pengembangan proyek dicatat melalui beberapa commit Git untuk mendokumentasikan perubahan yang dilakukan selama pengerjaan P7.

1. **Menyiapkan proyek P7 dari hasil P6:** Menggunakan kembali file hasil pertemuan sebelumnya dengan menempatkannya ke dalam direktori `pertemuan-07` sebagai dasar pengerjaan.
2. **Menerapkan pembacaan data GET:** Mempelajari cara mengambil informasi dari alamat URL menggunakan `$_GET` serta menampilkan data dengan bantuan `htmlspecialchars()`.
3. **Menguji pengiriman formulir melalui GET:** Menambahkan perintah `contactForm.submit();` pada `script.js` agar formulir dapat dikirim setelah proses validasi berhasil.
4. **Membuat file khusus demonstrasi GET:** Menggandakan `index.php` menjadi `indexGet.php` untuk memperlihatkan contoh penggunaan metode GET secara terpisah.
5. **Mengganti metode pengiriman formulir:** Mengatur formulir utama agar menggunakan metode `POST` melalui perubahan atribut `method`.
6. **Mengolah data menggunakan POST:** Menyesuaikan proses penerimaan data dengan mengganti penggunaan `$_GET` menjadi `$_POST`.
7. **Memperbarui sistem pembacaan dan validasi input:** Menyesuaikan pengambilan seluruh data formulir, menerapkan nama checkbox `minat[]`, serta memperbaiki selector pada JavaScript.
8. **Menambahkan pemeriksaan data oleh PHP:** Membuat validasi di sisi peladen dan menampilkan informasi kesalahan apabila data yang dikirim tidak memenuhi ketentuan.
9. **Menerapkan perlindungan pada keluaran formulir:** Menggunakan `htmlspecialchars()` untuk mengamankan data pengguna sebelum ditampilkan kembali ke halaman.
10. **Mengelola data dengan session dan PRG:** Menyimpan hasil pengiriman formulir menggunakan session serta menerapkan pengalihan halaman setelah proses selesai.
11. **Menyelesaikan dokumentasi proyek:** Melengkapi README dengan penjelasan fitur, tahapan pengembangan, hasil pengujian, dan catatan riwayat perubahan.
