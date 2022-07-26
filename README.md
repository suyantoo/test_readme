###### Nama : suyantoo
###### Kelas : RPL
###### No. Absen : 23

# modul 1

Soal nomor 1
Lakukan proses instalasi framework laravel kedalam folder dengan nama masing-masing
![image](https://user-images.githubusercontent.com/109930613/180918926-2a53a79b-194b-43c3-87a7-5a62af9e5bbe.png)
'''
composer create-project laravel/laravel penjualan
'''


# modul 2
Soal nomor 2
Buatlah migration tabel kategori dengan teknik yang telah di pelajari dalam
modul ini.

### langkah pertama

Buatlah Tabel Kategori terlebih dahulu 
'''
php artisan make:migration create_produk_table;
'''

### langkah kedua

isikan kode dibawah ini kedalam file yang sudah dibuat
![image](https://user-images.githubusercontent.com/109930613/180921215-18f57443-5420-4c8a-9b31-45be97757b3d.png)
Pastisnya kodenya berjalan saat dijalankan di terminal menggunakan
'''
php artisan migrate
'''
Setelah bisa dijalankan mari kita buat model kategoori

### Langkah ketiga

ketik code ini didalam terminal untuk membuat model

'''
php artisan make:model kategori
'''

Hasil dari perintah di atas,akan ada satu file baru pada folder **penjualan/app/models** dengan nama **kategori.php**, hasil dari perintah artisan di atas dapat dilihat pada gambar dibawah.

![image](https://user-images.githubusercontent.com/109930613/180923175-55133057-b791-491a-a784-7d1f29710638.png)

jika nama file model disini adalah kategori maka nama tabel yang ada di dalam database adalah kategoris.namun hal tersebut dapat dikonfigurasi dengan cara membuka file model kategori.php yang baru saja dibuat dan tambahkan script berikut:
![image](https://user-images.githubusercontent.com/109930613/180923764-9277db49-866a-4dca-95a4-add1e3eedf33.png)
value dari variable ini akan dianggap sebagai nama tabel yang diwakilioleh model ini.

## Soal nomor 2

berikan data dengan menggunakan seeder yang telah anda pelajari pada modul ini

### Langkah pertama

untuk membuat seeder,gunakanperintah artisan pada **CMD** seperti berikut:

![image](https://user-images.githubusercontent.com/109930613/180924890-169c7258-7356-4851-8382-94b96462b301.png)

'''
php artisan make:seeder kategoriTableSeeder
'''

perintah tersebut akan menghasilkan satu file baru pada folder database/seeder dengan nama
kategoriTableSeeder.php atau yang diketikkan pada perintah. Hasil dari perintah artisan diatas dapat dilihat pada gambar dibawah:

![image](https://user-images.githubusercontent.com/109930613/180925381-8f5149eb-db59-45cc-9e68-28c2330baf8b.png)


### Langkah kedua

buka file kategoriTableSeeder yang telah dibuat dan tambahkan kode sihingga menjadi seperti berikut:

![image](https://user-images.githubusercontent.com/109930613/180925647-0ed4624a-eb13-4e78-81d8-514cec7caae0.png)

### Langkah ketiga

buka file database .php yang ada pada folder database/seeds dan panggil seeder yang baru dibuat pada method run dengan menambahkan script sebagai sebagai berikut:

![image](https://user-images.githubusercontent.com/109930613/180926046-0e2178b2-d75a-487f-a655-a2e5e0a8da74.png)


setelah itu jalankan perintah artisan pada **CMD** untuk mengeksekusi seeder yang telah dibuat dengan perintah seperti berikut:
'''
php artisan db:seed
'''

<?php
