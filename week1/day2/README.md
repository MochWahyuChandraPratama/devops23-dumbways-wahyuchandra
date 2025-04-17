# DAY2
### LINUX Command
#### 1. ls
Perintah untuk melihat file dan folder yang ada di penyimpanan. la juga dapat digunakan untuk melihat seluruh isi directori termasuk hidden. kombinasi dari perintah ls -la untuk melihat seluruh akses, isi directory, dan letaknya.
```
 ls /direktori/folder/path
```
```
 ls -la
```
```
 ls -R (mencantumkan semua file di subdirektori)
```
#### 2. sudo
Perintah untuk mendapatkan hak akses administrator bagi user non-root. Jika ingin masuk ke root menggunakan perintah sudo su. Perintah su memungkinkan Anda menjalankan program di shell Linux sebagai user lain.
```
 sudo (perintah)
```
```
 sudo su 
```
#### 3. pwd
Perintah untuk melihat direktori yang aktif.
```
 pwd (opsi)
```
#### 4. cd
Perintah untuk menjadikan folder home sebagai direktori.
```
 cd (nama direktori dan file yang ingin ditelusuri)
```
```
 cd .. (berpindah satu direktori ke atas)
```
#### 5. mkdir
Perintah mkdir untuk membuat satu atau beberapa direktori dan mengatur izinnya.
```
 mkdir (file) direktori/
```
```
 mkdir -v (menampilkan pesan untuk setiap direktori yang dibuat)
```
#### 6. rm
Perintah untuk menghapus file atau direktori secara permanen dalam sebuah direktori.
```
 rmdir (file) nama_direktori
```
```
 rm -i (meminta konfirmasi sebelum dihapus untuk menghindari salah hapus)
```
```
 rm file file 1
```
```
 rm -rf (remove force mengizinkan penghapusan file/direktori tanpa konfirmasi secara rekursif)
```
#### 7. cp
Perintah untuk menyalin satu atau lebih file ke lokasi lain termasuk isinya.
```
 cp file.txt /direktori/tujuan
```
```
 cp file file1 (untuk menyalin isi dari file ke file1)
```
#### 8. mv
Perintah untuk memindahkan file dan direktori atau mengubah namanya.
 ```
 mv file /direktori/tujuan
```
```
 mv namaoldfile namanewfile
```
#### 9. touch
Perintah untuk membuat file kosong di path direktori.
```
 touch /direktori/tujuan/namafile
```
```
 touch namafile tujuan/
```
#### 10. file
Perintah untuk melihat tipe file.
```
file namafilenya
```
#### 11. zip, unzip
 Perintah zip untuk mengarsipkan file/direktori ke .zip dan perintah unzip untuk mengekstrak file/direktori yang berekstensi .zip.
```
zip archive.zip file.txt
```
```
unzip namafile.zip
```
#### 12. tar
Perintah untuk membuat dan mengekstrak arsip .tar, format file yang mirip dengan ZIP dengan kompresi opsional.
```
tar -cvzf archive.tar /direktori/user/tujuan
```
#### 13. nano, vi, vim, jed
Perintah untuk mengedit suatu file menggunakan editor teks. Perintah jed harus instal terlebih dulu untuk menjalankannya. Perintah vi dan jed disarankan untuk scripting dan pemrograman.
```
nano namafile.txt
```
```
vi namafile.html
```
```
jed namafile.pyd
```
#### 14. cat
Perintah untuk mencantumkan, menggabungkan, dan menuliskan isi file.
```
cat namafile
```
```
cat file1.txt file2.txt > file3.txt – menggabungkan file1.txt dan file2.txt dan menyimpan isinya di filename3.txt.
```
#### 15. grep
Perintah untuk mencari isi didalam file sesuai baris yang cocok dengan pola tertentu, berguna untuk memfilter file log besar.
```
grep carikata filetujuan.txt
```
#### 16. sed
Perintah untuk menemukan, mengganti, dan menghapus pola dalam file tanpa menggunakan editor teks. Gunakan subperintah s untuk mengganti pola yang cocok atau d untuk menghapusnya. Terakhir, tentukan file berisi pola yang akan diubah.
```
sed 's/makan/minum' obat.txt teratur.txt
```
#### 17. head
Perintah menampilkan sepuluh baris pertama dalam file teks atau data yang di-pipe di command-line interface.
```
head file.txt
```
#### 18. tail
Perintah untuk menampilkan sepuluh baris terakhir dalam sebuah file, yang berguna untuk memeriksa data baru dan error.
```
tail -n colors.txt (-n mengubah jumlah baris yang ditampilkan)
```
#### 19. wget
Perintah untuk mengunduh file dari internet menggunakan protokol HTTP, HTTPS, atau FTP.
```
wget urltujuan.zip
```
#### 20. history
Perintah untuk melihat history command yang sudah diketik.
```
history
```
#### 21. ping
Perintah untuk memberitahu user informasi koneksi jaringan internet.
```
ping 8.8.8.8 (contoh memeriksa koneksi menggunkan ip dari vm atau google.com)
```
#### 22. find
Perintah untuk mencari file atau direktori pada direktori tertentu.
```
find -type f -name file.txt
find -type d -name direktori
```
#### 23. echo
Perintah untuk menyisipkan teks ke suatu file.
```
echo "hello world" > namafile.txt (> mengganti/menimpa isi yang sudah ada)
```
```
echo "belajar" >> namafile.txt (>> menyisipkan teks baru)
```
#### 24. chown
Perintah untuk mengubah kepemilikan file,direktori atau link simbolis ke username yang ditentukan.
```
chown wahyu namafile.txt
```
```
ll (cek permission suatu file/folder)
```
#### 25. chmod
Perintah untuk mengubah ijin akses suatu file dan direktori.
```
chmod -rwxrwxrwx file.txt
```
```
chmod 744 direktori/
```
Menentukan letak user yang dimaksud :
- Pemilik (Owner) kiri -rwx
- Kelompok (Group) tengah rwx
- Lainnya (Others) kanan rwx

Setiap user dapat melakukan 3 bentuk operasi yaitu :
Pada File/Direktori
- r (Read) Ijin untuk membaca (4)
- Ijin untuk membaca daftar file dalam direktori
- w (Write) Ijin untuk mengubah / membuat (2)
- Ijin untuk mengubah/membuat file di direktori
- x (Execute) Ijin untuk menjalankan program (1)
- Ijin untuk masuk ke direktori (cd)
Jika angka notasi dijumlahkan akan memberikan akses penuh suatu user dan saran keamanan jangan memberikan sembarang akses ke group dan others.

#### IP Private
- Ruang lingkup lokal
- Didapatkan secara gratis
- Tidak bisa terhubung ke internet secara keseluruhan
- Setiap nomor IP tidak unik dan bisa digunakan berulang dengan jaringan lokal lain
- Lebih aman karena hanya tersedia pada jaringan lokal.
#### IP Public
- Ruang lingkup global
- Tidak gratis; Bisa terhubung ke internet secara keseluruhan
- Setiap nomor IP unik dan tak bisa digunakan oleh pihak lain
- Kurang aman karena dapat dilihat secara online
- Tidak membutuhkan network translation apapun untuk terhubung ke internet.

#### IP Dynamic
Alamat ip yang berubah-ubah, apabila berhenti dan dijalankan kembali pasti akan berubah atau berganti terus menerus. Kegunaan biasanya digunakan untuk ip rumahan atau kantoran.
#### IP Static
Alamat ip yang tetap atau konstan tidak akan berubah-ubah. Kegunaan paling cocok untuk server karena konfigurasi diarahkan ke 1 server yang sudah ada tidak perlu melakukan setting ulang jika akan membuka db. Apabila ip server menggunakan model dynamic pada saat membuka database tidak akan bisa.
