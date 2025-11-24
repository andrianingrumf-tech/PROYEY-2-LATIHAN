# PROYEY-2-LATIHAN
LANGKAH 1
# Membuat Direktori untuk 3 Departemen MARKETING,ENGINEERING,HR
https://drive.google.com/file/d/1stgsVo-rGP9so1g6mrc4FsbGdb_cA-pH/view?usp=drivesdk
```
mkdir Marketing Enginering HR
```

# MEMBUAT SUBFOLDER DI DIREKTORI MASING-MASING
https://drive.google.com/file/d/1IOa06IuvnZAxSQxwp0d_xQV-Hp9uRZG6/view?usp=drivesdk
```
andrianingrum@andrianingrum-virtualbox:~/project_1$ cd Marketing
andrianingrum@andrianingrum-virtualbox:~/project_1/Marketing$ mkdir Documents Archives
andrianingrum@andrianingrum-virtualbox:~/project_1/Marketing$ cd Documents
andrianingrum@andrianingrum-virtualbox:~/project_1/Marketing/Documents$ touch Marketing_laporan.docx
andrianingrum@andrianingrum-virtualbox:~/project_1/Marketing/Documents$ cd ..
andrianingrum@andrianingrum-virtualbox:~/project_1/Marketing$ cd Archives

```
* Penjelasan.

mkdir→ membuat folder baru.
touch→ membuat file baru.
cd→ masuk ke folder.
cd ..→ keluar ke folder sebelumnya.

# LANGKAH 2 MEMINDAHKAN FILE YANG SALAH TEMPAT KE FIREKTORI YANG BENAR
https://drive.google.com/file/d/1yH9XuRv4Avm9gTbUWvsVAfMYh_506z5o/view?usp=drivesdk
```
mv images/file11.jpg Marketing/Documents
mv images/file12.jpg Engineering/Documents
mv images/file13.jpg HR/Documents
```

# MEMBUAT CADANGAN DI FOLDER ARSIP
https://drive.google.com/file/d/1fN6nu_DZHkOGze6RNcUnvroAn--_Albu/view?usp=drivesdk
cp -r Marketing/Dokuments/Marketing_laporan.docx Marketing/Archives
cp -r Engineering/Documents/Engineering_Documents.docx Engineering/Archives
cp -r HR/Documents/laporan_HR.docx HR/Archives

# MENAMPILAN ISI FOLDER Marketing, Engineering, HR
https://drive.google.com/file/d/18XopLmiPEZZHJ0wo-NCjFHbjKb5IOX0Q/view?usp=drivesdk
```
Tree -P "Marketing Engineering HR
```
* Penjelasan.
mv→ memindahkan file/folder.
cp -r→ meng-backup/meng-copy semua folder beserta isinya.
Tree -P→ menampilkan struktur folder pohon beserta misinya

# LANGKAH 3 SET IZIN/MEMBATASI HAK AKSES DI SETIAP FOLDER
https://drive.google.com/file/d/1YkKBWpudye42cGxNnQdpRkTMBElaARgt/view?usp=drivesdk

sudo groupadd Marketing
sudo groupadd Enginering
sudo groupadd HR 

# MENGUBAH KEPEMILIKAN FOLDER DAN SEMUA ISI DI DALAMNYA
https://drive.google.com/file/d/1Fx-nowNcLe8wrBFsDksTR3SyPlNCDs7O/view?usp=drivesdk

sudo chgrp -R Marketing Marketing
sudo chgrp -R Engineering Engineering
sudo chgrp -R HR HR

# MENGATUR IZIN FOLDER IZIN
https://drive.google.com/file/d/1JfYgyPJ_6H8xyl_N_JfUNW4ERKxWD44E/view?usp=drivesdk
sudo chmod 770 Marketing
sudo chmod 770 Engineering
sudo chmod 770 HR

* Penjelasan.

sudo groupadd→ menambahkan grup.
sudo chgrp→ mengubah kepemilikan grup.
sudo chmod 770→ mengatur izin akses
7→ buat owner.
7→ buat group.
0→ buat outher.
# LATIHAN 4 MENAMPILKAN FILE PDF -7 HATI YANG LALU
https://drive.google.com/file/d/1FoioNag8nvfpWJKiS-bWZt2sgbNEg31N/view?usp=drivesdk

find . -type f -iname "*.pdf" -mtime -7
* Penjelasan.

find→ mencari file/folder sesuai nama,tipe,ukuran,dll
