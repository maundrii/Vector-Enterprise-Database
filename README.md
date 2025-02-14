# Membuat Vector Database

# Membuat Vector Database

## Install PostgreSQL dan PostGIS
1. Download PostgreSQL dari [situs resminya](https://www.postgresql.org/download/).
2. Jalankan Stack Builder setelah instalasi PostgreSQL selesai.  
   ![alt text](image-2.png)
3. Pilih PostgreSQL versi yang diinstal.  
   ![alt text](image-1.png)
4. Pilih **Spatial Extensions → PostGIS**.  
   ![alt text](image-3.png)
5. Klik **Next** dan ikuti proses instalasi hingga selesai.

## Pembuatan dan Pengaturan Database (Server)
### Pembuatan Database
1. Buka pgAdmin dan login ke PostgreSQL.
2. Klik kanan pada Databases → Create → Database.
![alt text](image-4.png)
3. Isi detail database:
> Database Name: nama file database (contoh: tes_jabar)
> Owner: postgres (atau user lain yang Anda buat)
![alt text](image-5.png)
4. Klik Save untuk menyimpan database.
5. Aktifkan PostGIS di database:
> Klik Kanan pada Database --> Query Tool di pgAdmin. ![alt text](image-6.png)
> Akan ditampilkan jendela Query di pgAdmin ![alt text](image-7.png)
> Isikan SQL: CREATE EXTENSION postgis; ![alt text](image-8.png)
> Kemudian klik Execute/Refresh (lingkaran merah pada gambar diatas) untuk menjalankan perintah.
> Jika berhasil maka akan muncuk messages “successfully” pada bagian bawah jendela query, dan menandakan ekstensi postGIS telah aktif.
> Untuk memastikan PostGIS telah aktif bisa juga dilihat di jendela Object Explorer, pilih pada bagian Database (tes_jabar) --> Extensions, akan tampak extensi PostGIS.
![alt text](image-9.png)
### Menghubungkan QGIS ke Enterprise Geodatabase
1.	Buka QGIS.
2.	Pilih Layer → Data Source Manager → PostgreSQL.
![alt text](image-10.png)
![alt text](image-11.png)
3.	Klik New dan isi:
> Name: Isikan bebas (misal: PostGISDB)
> Host: localhost (atau IP server PostgreSQL)
> Port: 5432
> Database: Isikan nama database yang telah dibuat sebelumnya (contoh: tes_jabar)
> Username: postgres
> Password: (password user PostgreSQL)
![alt text](image-12.png)
4.	Klik Test Connection untuk memastikan koneksi berhasil.
5.	Klik OK, lalu Connect untuk melihat tabel dalam database.
6.	Jika sudah terkoneksi, maka PostGISDB akan tampil di jendela browser
![alt text](image-13.png)



## Setting Firewall dan Port Database


## Pembuatan dan Pengaturan Database (Server)
## Setting Firewall dan Port Database
