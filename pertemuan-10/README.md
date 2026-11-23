# pertemuan-10 Analisis Kebutuhan Data dan Dasar MySQL Satu Tabel

# pertemuan-10

Pada P10, yang saya lakukan adalah:

### Fitur, Pengembangan, dan Pengujian Pertemuan 10

1. Menyalin seluruh artefak dari bahan pertemuan 09 untuk dijadikan dasar pengerjaan pertemuan 10. **Pengujian:** Membuka alamat `http://localhost/PWD/2627o/ti1a/2611500023-PWD-TI1A-2627O/pertemuan-10/` dan memastikan tampilan website masih sama seperti hasil pertemuan 09.

2. Mempersiapkan folder serta lingkungan kerja untuk pengembangan pertemuan 10. **Pengujian:** Menjalankan Laragon dan mengecek apakah layanan Apache dan MySQL sudah aktif serta berjalan dengan baik.

3. Mengecek kesiapan phpMyAdmin dan repositori pertemuan 10. **Pengujian:** Membuka phpMyAdmin untuk memastikan halaman pengelolaan database MySQL dapat diakses dengan normal.

4. Menganalisis kebutuhan data yang terdapat pada formulir kontak P10. **Pengujian:** Meninjau kembali formulir pada file `pertemuan-10\index.php` dan memastikan delapan data yang dibutuhkan sudah sesuai dengan atribut `name` serta jenis input yang digunakan.

5. Menetapkan data formulir yang akan dimasukkan ke dalam database. **Pengujian:** Membandingkan delapan data yang akan disimpan dengan elemen formulir pada `pertemuan-10\index.php` serta memastikan informasi profil tidak ikut dimasukkan ke dalam data kontak.

6. Menentukan bentuk penyimpanan data pada pilihan minat. **Pengujian:** Mengecek kode formulir pada `pertemuan-10\index.php` dan memastikan kedua checkbox menggunakan atribut `name="minat[]"` dengan pilihan nilai HTML berupa `HTML` dan `CSS`.

7. Menetapkan nama database dan tabel untuk P10 berdasarkan NIM. **Pengujian:** Memeriksa kesesuaian penamaan database dan tabel menggunakan NIM sendiri, yaitu `2611500023`, dengan nama database `db_pwd_2611500023` dan nama tabel `tbl_kontak_2611500023`.

8. Menyusun atribut beserta tipe data yang diperlukan untuk tabel kontak. **Pengujian:** Mengecek delapan atribut yang sudah dirancang, memastikan penamaannya sesuai dengan data formulir P9 serta ukuran tipe datanya mencukupi batas input yang digunakan.

9. Menambahkan primary key dan pengaturan auto increment pada tabel kontak. **Pengujian:** Memastikan kolom `id` sudah tersedia dengan tipe `INT`, berfungsi sebagai `PRIMARY KEY`, dan memiliki pengaturan `AUTO_INCREMENT`.

10. Melakukan pemeriksaan terhadap rancangan akhir struktur tabel kontak. **Pengujian:** Meninjau kesembilan atribut yang telah dibuat untuk memastikan seluruh data formulir P9 sudah tercakup, tipe data sesuai dengan kebutuhan masing-masing atribut, serta hanya kolom `id` yang menjadi `PRIMARY KEY` dengan `AUTO_INCREMENT`.

11. Menambahkan data pertama ke dalam tabel kontak. **Pengujian:** Memastikan proses pemasukan data berhasil tanpa menampilkan kesalahan, kemudian mengecek setiap nilai atribut dan memastikan nomor `id` dibuat secara otomatis.

12. Memahami penggunaan perintah SQL `INSERT` untuk menambahkan data. **Pengujian:** Mengamati keterkaitan antara perintah `INSERT` dengan atribut yang tersedia pada tabel melalui fitur SQL Insert, lalu memastikan data berhasil disimpan.

13. Mengecek hasil pemasukan data awal pada tabel kontak. **Pengujian:** Membuka tab Browse dan memastikan kedua data yang dimasukkan, yaitu melalui fitur Insert dan SQL Insert, sudah tampil sesuai dengan nilai yang sebelumnya diberikan. Selanjutnya, memeriksa setiap atribut agar tidak ada data yang hilang maupun mengalami perubahan.

14. Meninjau kembali serta membenahi data awal yang tersimpan pada tabel kontak. **Pengujian:** Memastikan seluruh isi tabel sudah sesuai dengan ketentuan atribut dan nilai data yang digunakan pada formulir P9.

15. Mengatur proses ekspor database yang telah dibuat. **Pengujian:** Memastikan database `db_pwd_2611500023` sudah dipilih dengan metode ekspor Quick dan format berkas SQL.

16. Melakukan ekspor database menjadi file SQL. **Pengujian:** Memastikan file `db_pwd_2611500023.sql` berhasil diunduh dan disimpan ke dalam folder `pertemuan-10`.

17. Memastikan filee hasil ekspor SQL sudah lengkap. **Pengujian:** Memeriksa isi file untuk memastikan struktur database, tabel `tbl_kontak_2611500023`, sembilan atribut, serta seluruh data awal yang telah dimasukkan sudah tercantum dengan benar.