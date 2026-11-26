## Pertemuan-11

Pada P11, kegiatan yang saya lakukan meliputi:

1. **Menjadikan P10 sebagai dasar pengembangan P11**

   Menyalin seluruh berkas dari pertemuan 10 ke direktori pertemuan 11 sebagai bahan awal pengerjaan. Kemudian membuka aplikasi melalui browser untuk memastikan tampilan dan fitur masih berjalan seperti pada hasil pertemuan sebelumnya.

2. **Mempersiapkan folder dan lingkungan kerja P11**

   Membuat serta memeriksa kelengkapan direktori pertemuan 11. Pengujian dilakukan dengan menjalankan Laragon dan memastikan layanan Apache serta MySQL berada dalam kondisi aktif.

3. **Memastikan database dan tabel kontak sudah tersedia**

   Memeriksa database `db_pwd_2611500023` beserta tabel `tbl_kontak_2611500023` melalui PhpMyAdmin. Selanjutnya mengecek sembilan kolom, yaitu id, nama, email, semester, tanggal, jenis_pesan, minat, prodi, dan pesan, serta memastikan data dapat dilihat melalui menu Browse.

4. **Membuat file koneksi.php untuk P11**

   Menambahkan file `koneksi.php` sebagai tempat pengaturan hubungan antara PHP dan MySQL. Pengujian dilakukan dengan memastikan file tersebut berada di dalam folder pertemuan-11 dan satu direktori dengan `index.php`.

5. **Mengisi konfigurasi koneksi database**

   Menuliskan empat parameter koneksi pada file `koneksi.php`, meliputi host, username, password, dan nama database. Kemudian memeriksa kembali setiap nilai agar sesuai dengan konfigurasi database yang digunakan pada P10.

6. **Mengatur konfigurasi laporan kesalahan MySQLi**

   Menambahkan pengaturan `mysqli_report(MYSQLI_REPORT_OFF);` setelah deklarasi parameter koneksi. Pengujian dilakukan dengan memeriksa ketepatan penulisan fungsi dan konstanta agar pengaturan dapat digunakan dengan benar.

7. **Membangun proses koneksi PHP dengan MySQL**

   Mengimplementasikan fungsi `mysqli_connect()` pada file `koneksi.php` berdasarkan parameter yang sudah disiapkan. Setelah itu, memeriksa susunan kode mulai dari konfigurasi koneksi, pengaturan laporan kesalahan, hingga kondisi untuk menangani koneksi yang tidak berhasil.

8. **Melakukan percobaan koneksi menggunakan file uji**

   Membuat file sementara bernama `uji_koneksi.php` untuk mengetahui apakah PHP sudah terhubung dengan MySQL. Pengujian dinyatakan berhasil apabila halaman menampilkan tulisan Koneksi ke basis data berhasil. Setelah selesai, file pengujian dihapus dari direktori proyek.

9. **Memastikan penanganan koneksi yang mengalami kegagalan**

   Melakukan pengujian dengan mengubah sementara parameter database menjadi nama yang tidak sesuai. Kemudian mengakses halaman untuk melihat apakah pesan Koneksi ke basis data gagal ditampilkan. Setelah pengujian, mengembalikan nama database ke konfigurasi yang benar dan memeriksa kembali koneksinya.

10. **Menyiapkan pemanggilan file koneksi**

    Menambahkan pemanggilan file `koneksi.php` menggunakan `require_once()`. Pengujian dilakukan dengan memastikan nama file sudah benar dan lokasinya dapat dijangkau dari `index.php`.

11. **Menghubungkan file koneksi dengan halaman utama**

    Memasukkan perintah `require_once("koneksi.php");` ke dalam file `index.php` bersama pemanggilan `fungsi.php`. Selanjutnya memeriksa kembali penulisan nama file agar kedua berkas dapat dimuat tanpa kesalahan.

12. **Memeriksa urutan penggunaan variabel koneksi**

    Meninjau hubungan antara `index.php` dan `koneksi.php` untuk memastikan variabel `$koneksi` sudah tersedia sebelum digunakan dalam proses pengambilan data. Pemeriksaan kegagalan koneksi juga dipastikan tetap berada pada file `koneksi.php`.

13. **Mencoba integrasi koneksi pada halaman P11**

    Membuka halaman utama melalui browser setelah kedua file berhasil dihubungkan. Pengujian dilakukan untuk memastikan halaman dapat dimuat dengan normal dan tidak menampilkan pesan kegagalan koneksi database.

14. **Menyiapkan perintah SELECT untuk membaca data kontak**

    Menentukan perintah SQL pada variabel `$sql` untuk mengambil seluruh isi tabel `tbl_kontak_2611500023`. Kemudian mencocokkan nama tabel dengan yang tersedia di database `db_pwd_2611500023` melalui PhpMyAdmin.

15. **Menjalankan pembacaan data menggunakan MySQLi**

    Menggunakan fungsi `mysqli_query()` untuk menjalankan perintah SELECT dengan bantuan variabel `$koneksi`. Pengujian dilakukan dengan memeriksa kesesuaian variabel koneksi, perintah SQL, dan nama variabel hasil kueri.

16. **Menambahkan pemeriksaan apabila SELECT mengalami kesalahan**

    Menguji kondisi ketika proses pembacaan data tidak berhasil dengan mengganti nama tabel sementara menjadi `tbl_kontak_tidak_tersedia`. Setelah aplikasi dibuka melalui browser, memastikan pesan Kueri SELECT gagal dijalankan muncul. Kemudian mengembalikan nama tabel ke `tbl_kontak_2611500023`.

17. **Mengolah hasil pembacaan data dari database**

    Menggunakan `mysqli_fetch_assoc()` untuk mengambil baris hasil kueri dalam bentuk array asosiatif. Setiap baris yang diperoleh kemudian dimasukkan ke dalam array `$dataKontak` agar dapat diproses dan ditampilkan pada halaman.

18. **Memeriksa isi array hasil SELECT**

    Melakukan pemeriksaan sementara menggunakan `var_dump()` terhadap variabel `$dataKontak`. Tujuannya untuk mengetahui apakah data kontak berhasil diambil dari database. Setelah hasilnya diperiksa, kode pengujian sementara dihilangkan kembali.

19. **Menampilkan seluruh informasi kontak pada website**

    Memastikan tabel database sudah memiliki data, kemudian mengakses halaman pertemuan 11 melalui browser. Memeriksa apakah seluruh informasi kontak dapat ditampilkan pada bagian Data Kontak dari Basis Data, termasuk kesesuaian setiap kolom dan format pesan yang memiliki baris baru. Selanjutnya mengosongkan isi tabel tanpa menghapus strukturnya untuk memastikan pesan Belum ada data kontak yang tersimpan dapat muncul. Setelah pengujian selesai, mengembalikan data awal ke dalam tabel melalui fasilitas SQL di PhpMyAdmin.

20. **Menyimpan hasil ekspor database praktikum**

    Melakukan ekspor database ke dalam berkas berekstensi `.sql`. Kemudian membuka berkas tersebut menggunakan VS Code untuk memeriksa apakah perintah pembuatan tabel `tbl_kontak_2611500023` serta perintah penyimpanan data kontak sudah tercantum di dalamnya.