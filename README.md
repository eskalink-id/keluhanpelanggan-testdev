## **Petunjuk Pengunaan**
Proyek ini menggunakan framework [Laravel 9](https://laravel.com/docs/9.x/deployment#server-requirements) yang siap digunakan untuk keperluan tes keahlian web developer

### **Software pendukung yang perlu disiapkan sebelum memulai**

- PHP minimal versi 8.0.2 atau versi terbaru
- Composer
- NodeJS minimal versi 16 atau versi terbaru
- Git minimal versi 2 atau versi terbaru (Optional)

#
## **Github Repository**

### **Clone Repository atau Download ZIP**

- Clone via Git Bash (Windows) atau Terminal (Linux)
  ```
  git clone https://github.com/eskalink-id/keluhanpelanggan-testdev.git
  ```
  Setelah selesai clone, pada Command line arahkan ke folder **keluhanpelanggan-testdev**, seperti perintah berikut:
  ```
  cd keluhanpelanggan-testdev
  ```
- atau **Download ZIP** jika anda tidak memiliki git di lokal komputer anda, untuk mendownload klik tombol Download ZIP seperti pada gambar berikut:

  ![image](https://user-images.githubusercontent.com/116535942/199644260-9be931e5-7f71-482c-8b52-7a5f918bd8b0.png)

  setelah download selesai, extract zip ke folder yang anda inginkan

- Kemudian lakukan instalasi laravel dan npm, seperti **Panduan Instalasi** dibawah ini


----


### **Panduan Instalasi**

- Buka Command Line arahkan ke folder ***keluhanpelanggan-testdev***
- kemudian jalankan perintah:
  ```
  composer install
  ```
- selanjutnya, jalankan perintah:
  ```
  php -r "copy('.env.example', '.env');";
  ```
- selanjutnya, jalankan perintah:
  ```
  php artisan key:generate
  ```
- selanjutnya, buat database dengan nama ***keluhan_pelanggan***
- selanjutnya, sesuaikan parameter pada file **.env**, seperti berikut:
  ```
  APP_URL=http://localhost:8000

  DB_CONNECTION=mysql
  DB_HOST=127.0.0.1
  DB_PORT=3306
  DB_DATABASE=keluhan_pelanggan
  DB_USERNAME=root
  DB_PASSWORD=
  ```
- selanjutnya, jalankan perintah:
  ```
  php artisan migrate
  ```
- selanjutnya, jalankan perintah berikut untuk compiled assets (development):
  ```
  - npm install
  - npm run dev
  ```
- selanjutnya, buka command line yang baru, jalankan perintah:
  ```
  php artisan serve
  ```

- selanjutnya, buka browser dengan url [http://localhost:8000](http://localhost:8000)
- selanjutnya, klik link **Register** dan lengkapi isian pada form register
- Selamat melanjutkan Tes, dengan membaca ketentuan pada **Soal Tes Keahlian**

----

## **Soal Tes Keahlian**

1. Pada halaman Keluhan Pelanggan buat fungsi create, read, update dan delete (CRUD)menggunakan axios atau ajax

2. Buat Model dengan nama **KeluhanPelanggan** serta migrationnya, dengan struktur table seperti berikut:
   ```
   Nama Tabel: keluhan_pelanggan
   Struktur Tabel:
   --------------------------------------------------------------
   | Column Name    | Type Data | Length | Note                 |
   --------------------------------------------------------------
   | id             | string    | 20     | not null primary key |
   | nama           | string    | 50     | not null             |
   | email          | string    | 20     | not null             |
   | nomor_hp       | integer   |        | null                 |
   | flag_aktif     | boolean   |        | default true         |
   | status_keluhan | varchar   | 1      | not null default 'O' |
   | keluhan        | text      |        | not null             |
   --------------------------------------------------------------
   ```

3. Buat Controller  dengan nama KeluhanPelangganController untuk proses CRUD
4. Ketika melakukan create dan update data berikan validasi sesuai dengan atribute table
   
5. Buatlah function untuk menampilkan nilai dari:
   - bilangan factorial dari inputan variable $nilai = 7.
   - bilangan ganjil dari inputan variable $nilai = 20.

**Selamat mengerjakan, semoga sukses**
