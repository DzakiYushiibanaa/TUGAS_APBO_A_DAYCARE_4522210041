# TUGAS_APBO_A_DAYCARE_4522210041

# USE CASE 
![use case daycare](https://github.com/DzakiYushiibanaa/TUGAS_APBO_A_DAYCARE_4522210041/assets/145998330/e8422e8f-9c34-4c57-a880-52cd58e6f122)

Aktor dan Use Case
## 1.	Aktor
### •	Staff: Pengguna yang bekerja di daycare dan memiliki tanggung jawab dalam proses registrasi, pencatatan pembayaran, pencatatan kehadiran, dan pembuatan laporan.
### •	Pengasuh: Pengguna yang bertanggung jawab atas pengasuhan anak di daycare dan terlibat dalam pencatatan kehadiran anak serta pembuatan laporan harian.
### •	Orang Tua: Pengguna yang mendaftarkan anaknya ke daycare, melakukan pembayaran, serta menerima laporan tentang aktivitas dan kehadiran anak mereka.
## 2.	Use Case
### •	Registrasi
### •	Deskripsi: Proses ini dilakukan oleh staff untuk mendaftarkan anak-anak baru ke dalam sistem daycare.
### •	Aktor yang terlibat: Staff, Orang Tua
### •	Pembayaran
### •	Deskripsi: Proses ini mencakup pencatatan dan pemrosesan pembayaran yang dilakukan oleh orang tua untuk layanan daycare.
### •	Aktor yang terlibat: Staff, Orang Tua
### •	Kehadiran
### •	Deskripsi: Pencatatan kehadiran anak-anak di daycare. Kehadiran ini dapat dicatat oleh pengasuh dan staff.
### •	Aktor yang terlibat: Staff, Pengasuh, Orang Tua
### •	Laporan
### •	Deskripsi: Pembuatan laporan harian atau periodik tentang aktivitas dan kehadiran anak di daycare yang dibuat oleh pengasuh dan dapat diakses oleh orang tua.
### •	Aktor yang terlibat: Staff, Pengasuh, Orang Tua
## Interaksi antara Aktor dan Use Case
### •	Staff
### •	Berinteraksi dengan use case Registrasi untuk mendaftarkan anak-anak baru.
### •	Berinteraksi dengan use case Pembayaran untuk mencatat dan memproses pembayaran dari orang tua.
### •	Berinteraksi dengan use case Kehadiran untuk mencatat kehadiran anak dan pengasuh.
### •	Berinteraksi dengan use case Laporan untuk membuat dan menyimpan laporan aktivitas anak.
### •	Pengasuh
### •	Berinteraksi dengan use case Kehadiran untuk mencatat kehadiran anak yang mereka asuh.
### •	Berinteraksi dengan use case Laporan untuk membuat laporan harian tentang aktivitas anak.
### •	Orang Tua
### •	Berinteraksi dengan use case Registrasi untuk mendaftarkan anak mereka ke daycare.
### •	Berinteraksi dengan use case Pembayaran untuk melakukan pembayaran layanan daycare.
### •	Berinteraksi dengan use case Kehadiran untuk memeriksa kehadiran anak mereka.
### •	Berinteraksi dengan use case Laporan untuk menerima laporan tentang aktivitas dan kehadiran anak mereka di daycare.
## Penjelasan Alur
### •	Registrasi: Staff melakukan proses registrasi ketika orang tua datang untuk mendaftarkan anak mereka ke daycare. Data anak dan orang tua dimasukkan ke dalam sistem.
### •	Pembayaran: Orang tua melakukan pembayaran biaya daycare. Staff mencatat pembayaran tersebut dan memprosesnya.
### •	Kehadiran: Setiap hari, pengasuh mencatat waktu masuk dan keluar anak-anak yang mereka asuh. Staff juga dapat mencatat kehadiran pengasuh dan anak-anak.
### •	Laporan: Pengasuh membuat laporan harian tentang aktivitas anak-anak. Laporan ini dapat diakses oleh orang tua untuk mengetahui perkembangan dan aktivitas anak mereka di daycare.

# ERD (DAYCARE)
![image (2)](https://github.com/DzakiYushiibanaa/TUGAS_APBO_A_DAYCARE_4522210041/assets/145998330/6bfdebe8-73ed-4348-b0c9-4b1cbb155fae)

# CLASS DIAGRAM
![class diagram (daycare)](https://github.com/DzakiYushiibanaa/TUGAS_APBO_A_DAYCARE_4522210041/assets/145998330/59585c27-eaca-4ec3-8b85-9a0cc947f511)
## Penjelasan Kelas dan Hubungannya
Kelas Staff

Atribut:
id_staff : int - Identifikasi unik untuk setiap staff.
nama : string - Nama staff.
No_Telp : string - Nomor telepon staff.
Metode:
mencatatKehadiranPengasuh() - Metode untuk mencatat kehadiran pengasuh.
mencatatKehadiranStaff() - Metode untuk mencatat kehadiran staff.
memprosesPembayaran() - Metode untuk memproses pembayaran.
Kelas Orang_Tua

Atribut:
id_orangtua : int - Identifikasi unik untuk setiap orang tua.
nama : string - Nama orang tua.
No_Telp : string - Nomor telepon orang tua.
Email : string - Email orang tua.
nama_jalan : string - Nama jalan tempat tinggal orang tua.
kota : string - Kota tempat tinggal.
No_Rumah : string - Nomor rumah.
kecamatan : string - Kecamatan tempat tinggal.
provinsi : string - Provinsi tempat tinggal.
kelurahan : string - Kelurahan tempat tinggal.
Metode:
mendapatkanLaporan() - Metode untuk mendapatkan laporan.
Kelas Anak

Atribut:
id_anak : int - Identifikasi unik untuk setiap anak.
id_orangtua : int - Identifikasi orang tua dari anak tersebut.
nama : string - Nama anak.
jenis_kelamin : string - Jenis kelamin anak.
tgl_lahir : date - Tanggal lahir anak.
Tempat_Lahir : string - Tempat lahir anak.
umur : int - Umur anak.
Kelas Pengasuh

Atribut:
id_pengasuh : int - Identifikasi unik untuk setiap pengasuh.
nama : string - Nama pengasuh.
no_telp : string - Nomor telepon pengasuh.
Metode:
mencatatKehadiranPengasuh() - Metode untuk mencatat kehadiran pengasuh.
mencatatKehadiranAnak() - Metode untuk mencatat kehadiran anak.
Kelas Kehadiran_Pengasuh

Atribut:
id_kehadiran_pengasuh : int - Identifikasi unik untuk setiap catatan kehadiran pengasuh.
id_staff : int - Identifikasi staff yang mencatat.
id_pengasuh : int - Identifikasi pengasuh.
tanggal : date - Tanggal kehadiran.
waktu_masuk : time - Waktu masuk pengasuh.
waktu_keluar : time - Waktu keluar pengasuh.
deskripsi : string - Deskripsi tambahan.
Kelas Kehadiran_Staff

Atribut:
id_kehadiran_staff : int - Identifikasi unik untuk setiap catatan kehadiran staff.
id_staff : int - Identifikasi staff.
tanggal : date - Tanggal kehadiran.
waktu_masuk : time - Waktu masuk staff.
waktu_keluar : time - Waktu keluar staff.
deskripsi : string - Deskripsi tambahan.
Kelas Kehadiran_Anak

Atribut:
id_kehadiran_anak : int - Identifikasi unik untuk setiap catatan kehadiran anak.
id_anak : int - Identifikasi anak.
id_pengasuh : int - Identifikasi pengasuh yang mencatat.
tanggal : date - Tanggal kehadiran.
waktu_masuk : time - Waktu masuk anak.
waktu_keluar : time - Waktu keluar anak.
deskripsi : string - Deskripsi tambahan.
Kelas Pembayaran

Atribut:
id_pembayaran : int - Identifikasi unik untuk setiap pembayaran.
id_orangtua : int - Identifikasi orang tua yang melakukan pembayaran.
id_staff : int - Identifikasi staff yang memproses pembayaran.
tanggal : date - Tanggal pembayaran.
Metode_Pembayaran : string - Metode pembayaran yang digunakan.
Kelas Laporan

Atribut:
id_laporan : int - Identifikasi unik untuk setiap laporan.
id_pengasuh : int - Identifikasi pengasuh yang membuat laporan.
id_kehadiran_anak : int - Identifikasi catatan kehadiran anak yang dilaporkan.
id_anak : int - Identifikasi anak yang dilaporkan.
Tanggal : date - Tanggal laporan.
deskripsi : string - Deskripsi laporan.
Hubungan Antar Kelas
Staff memiliki hubungan dengan Kehadiran_Pengasuh (1 staff dapat mencatat banyak kehadiran pengasuh).
Staff memiliki hubungan dengan Kehadiran_Staff (1 staff dapat mencatat banyak kehadiran staff).
Staff memiliki hubungan dengan Pembayaran (1 staff dapat memproses banyak pembayaran).
Pembayaran memiliki hubungan dengan Orang_Tua (1 pembayaran dilakukan oleh satu orang tua).
Orang_Tua memiliki hubungan dengan Anak (1 orang tua dapat memiliki banyak anak).
Pengasuh memiliki hubungan dengan Kehadiran_Pengasuh (1 pengasuh dapat memiliki banyak catatan kehadiran pengasuh).
Pengasuh memiliki hubungan dengan Kehadiran_Anak (1 pengasuh dapat mencatat banyak kehadiran anak).
Laporan memiliki hubungan dengan Orang_Tua (1 laporan dapat didapatkan oleh banyak orang tua).

