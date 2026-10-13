P5 - JavaScript Dasar, DOM, Event, dan Validasi Sisi Klien
Deskripsi
Dokumentasi pengembangan halaman web pada P5, meliputi JavaScript, DOM, event listener, interaksi
navigasi, dan validasi formulir sisi klien.

Fitur dan Pengembangan

[Nama fitur/tahap]:

1. getElementById(): Fungsinya untuk mencari dan mengambil (memilih) satu elemen HTML berdasarkan atribut id, contohnya yaitu const navToggle = document.getElementById("navToggle");.<br>

2. querySelector(): Metode querySelector() digunakan untuk memilih satu elemen HTML berdasarkan selector CSS yang diberikan, contohnya yaitu const jenisPesan = document.querySelector('input[name="jenis_pesan"]:checked');.<br>

3. querySelectorAll(): Metode querySelectorAll() digunakan untuk memilih beberapa elemen HTML yang sesuai dengan selector CSS yang diberikan, contohnya yaitu const topikDipilih = document.querySelectorAll('input[name="minat"]:checked');.<br>

4. addEventListener(): Metode addEventListener() digunakan untuk mendaftarkan event listener pada suatu elemen HTML, sintaks dasar yaitu elemen.addEventListener("nama-event", fungsi);.<br>

Tambahkan entri setiap kali ada perkembangan penting pada proyek.
Pengujian

[Fitur yang diuji]:

`getElementById()`: Pengujian dilakukan dengan membuka halaman `index.html` menggunakan browser pada ukuran layar di bawah 768px. Kemudian tekan tombol hamburger (☰) untuk menampilkan menu dan tekan kembali untuk menyembunyikannya. Hasil aktualnya, elemen tombol dan menu berhasil dikenali berdasarkan ID, menu dapat dibuka dan ditutup, serta nilai atribut `aria-expanded``aria-label` berubah mengikuti kondisi menu.

`querySelector()`: Pengujian dilakukan dengan melengkapi formulir tanpa menentukan jenis pesan, lalu mencoba mengirimkannya. Setelah itu, pilih salah satu jenis pesan dan kirim kembali. Hasil aktualnya, sistem menampilkan peringatan ketika belum ada radio button yang dipilih. Setelah pilihan ditentukan, elemen yang dipilih berhasil ditemukan dan pemeriksaan formulir dapat diteruskan.

`querySelectorAll()`: Pengujian dilakukan dengan mengisi data formulir tanpa memilih topik minat. Selanjutnya, centang salah satu atau beberapa pilihan topik dan kirim kembali formulir. Hasil aktualnya, sistem mendeteksi bahwa belum ada checkbox yang aktif dan menampilkan pesan peringatan. Setelah minimal satu topik dipilih, pemeriksaan checkbox berhasil dilewati.

`addEventListener()`: Pengujian dilakukan dengan mencoba mengirim formulir menggunakan data yang belum sesuai, kemudian mengirim kembali setelah data diperbaiki. Selanjutnya, ubah isi input dan gunakan tombol Batal. Hasil aktualnya, event `submit` menjalankan validasi tanpa memuat ulang halaman, event `input` menghapus pesan umpan balik ketika data diubah, dan event `reset` membersihkan pesan ketika formulir diatur ulang. Pesan keberhasilan ditampilkan ketika seluruh data memenuhi ketentuan.

Catat perkembangan melalui commit Git yang bermakna.

[Pesan commit]: Membuat dan menghubungkan JavaScript: Membuat file script.js dan mengintegrasikannya dengan index.html.<br>
Menambahkan tombol hamburger: Membuat tombol menu untuk mengatur tampilan navigasi.<br>
Mengatur tampilan CSS: Menambahkan desain hamburger menu, responsivitas layar, dan tampilan form.<br>
Menerapkan fungsi JavaScript: Menggunakan beberapa fungsi DOM dan event untuk mengatur menu serta validasi form.<br>
mengisi readme untuk dokumentasi: Menulis dokumentasi perubahan dan pengujian<br>
