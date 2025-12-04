# Lab10Web
# NAMA: Muhamad Abdu
# KELAS: TI.24.A4
# NIM: 312410143




# 1. Persiapan Lingkungan Kerja
 - Langkah: Membuka editor kode Visual Studio Code (VSCode)
 - Tujuan: Memastikan lingkungan pengembangan siap untuk penulisa kode PHP.
 - Stuktur Direktori: Membuat folder proyek lab10_php_oop di dalam direktori server lokal (XAMPP/WAMP) untuk memfasilitasi eksekusi dile melalui web server.
# 2. Implementasi Class Mobil (mobil.php)
File ini berfungsi sebegai contoh implementasi Class dasar yang mencakup konsep Encapsulation dan Constructor.
 - Definisi Class: Membuat Class Mobil.
 - Property (Atribut): Memdefinisikan tiga privat properties: warna, merk,dan harga. Pengguna private memastikan bahwa akses dan modifikasi data harus melalui method publik (Encapsulation).
 - Metode Khusus (Constructor): Mengiplementasikan metode konstruktor ( _ _construct ) untuk inisialisasi objek secara otomatis saat dibuat. Metode ini menerima parameter untuk menetapkan nilai awal(merk, warna, harga).
 - Metode Publik (Behavior):
  - gantiWarna($warnaBaru): Metode Setter yang bertanggung jawab untuk memodifikasi nilai            properti $warna.
  - tampilWarna(): Metode Getter yang mengembalikan nilai properti $warna.
  - tampilDetail(): Metode untuk menampilkan semua atribut objek.
- Implementasi: Membuat dua instance objek ($a dan $b) dari Class Mobil dan mendemonstrasikan pemanggilan metode publik.
# 3. Modularisasi dan Class Library Form (form.php)
File ini mendefinisikan Class yang berfungsi sebagai library untuk menghasilkan markup HTML formulir secara dinamis, mengedepankan prinsip Modularisasi.
 - Definisi Class: Membuat Class Form.
 - Tujuan: Menyediakan struktur reusable untuk pembangunan formulir HTML.
 - Property: Menyimpan properti seperti action dan array $fields untuk menampung elemen input.
-Metode:
 - __construct($action, $method): Menginisialisasi atribut formulir.
 - addField($name, $label, $type): Menyimpan detail sebuah field input ke dalam array $fields.
 - displayForm(): Bertanggung jawab untuk melakukan iterasi pada array $fields dan merangkainya     menjadi string HTML lengkap (<form>, <label>, <input>).
# 4. Implementasi Pustaka Form (form_input.php)
File ini adalah modul eksekusi yang menunjukkan cara menggunakan Class Form yang telah didefinisikan dalam library.
 - Penggunaan Modularisasi: Menggunakan statement include "form.php" untuk memuat definisi Class    Form ke dalam skrip saat ini.
 - Instansiasi: Membuat objek baru ($form = new Form(...)).
 - Konfigurasi: Memanggil metode addField() sebanyak tiga kali untuk menambahkan input Nim,         Nama,   dan Alamat.
 - Output: Memanggil $form->displayForm() untuk merender dan menampilkan formulir HTML yang         dihasilkan ke peramban.
# 5. Implementasi Class Database (database.php)
File ini menyajikan konsep Class Library untuk abstraksi koneksi dan operasi basis data, menyederhanakan interaksi SQL.
- Definisi Class: Membuat Class Database.
- Abstraksi: Class ini menyembunyikan detail koneksi (host, user, pass, db) dari script utama.
-Fitur:
 - __construct(): Mensimulasikan upaya koneksi otomatis ke basis data.
 - query($sql): Metode generik untuk menjalankan perintah SQL bebas (Simulasi: mengembalika         status eksekusi).
 - get($table): Metode untuk mengambil data dari tabel tertentu (Simulasi: mengembalikan array      data).
 - insert(), update(), delete(): Metode spesifik untuk operasi CRUD (Create, Read, Update,          Delete), masing-masing menangani logika penambahan, pembaruan, dan penghapusan data.
# 6. Kesimpulan dan Modularisasi Proyek
- Prinsip yang di terapkan: Proyek ini sukses menerapkan Modularisasikan dan OOP melalui pemisahan tanggung jawab kode:
 - mobil.php: Studi kasus Encapsulation.
 - form.php & form_input.php: Implementasik Class Library dan Modularisasi Pengguna.
 - database.php: Contoh Abstraksi untuk koneksi sumber daya eksternal.
- Manfaat: Pemisahan ini mepermudah Debugging (mencari letak kesalahan), Maintenance (pemeliharaan), dan Reusabililty (penggunaan kembali) setiap komponen di proyek lain.
