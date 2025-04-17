# DAY 4
## Shortcut dari Text Editor Nano
Keyboard shortcut karakter dan keynya. Ctrl dilambangkan (^) dan Alt dilambangkan (M).
- Untuk keluar dari text editor nano dengan perintah Ctrl+X (^X).
- Untuk melihat bantuan dan alternatif selain tombol kombinasi Ctrl+G (^G).
![Screenshot from 2024-12-22 20-53-12](https://github.com/user-attachments/assets/293fa9b4-c2a8-432a-9668-3e50be178eb7)
##### Tombol Navigasi
- Ctrl+F (^F). Move forward one character.
- Ctrl+B (^B). Move back one character.
- Ctrl+Space (^Space). Go one word forward.
- Alt+Space (M-Space). Go one word backward.
- Ctrl+P (^P). Navigate to the previous line.
- Ctrl+N (^N). Navigate to the next line.
- Ctrl+V (^V). Go to the next page.
- Ctrl+Y (^Y). Move to the previous page.
- Ctrl+A (^A). Go to the beginning of the line.
- Ctrl+E (^E). Move to the end of the line.
- Undo an action is Alt+U (displayed as M-U).
- Perintah untuk mencari kata pada suatu file text didalam editor Ctrl+W shortcut (^W).
- Continue to the next result with Alt+W (M-W).
- Press Ctrl+R (^R) to open a new bar and type in the replacement term.
Select (Memilih teks)
- To select a part of a file, navigate to the beginning of the part, press the Alt+A shortcut (M-A), and use the arrow keys to move over the text you wish to select.
- Next, copy the selected text with the Alt+6 combination (M-6) or cut with Ctrl+K (^K). If you use these shortcuts without selecting any text first, they copy or cut the entire line of text.
- To paste the text, use Ctrl+U (^U).
- Menyisipkan file kedalam file tujuan dengan Ctrl+R (^R).
- To save a file, use the Ctrl+O (^O).
- Nano is also able to create a file backup. To do this, use the Alt+B command (M-B). Pressing the keys once enables backup, and doing it again disables it.
## Manipulation Text
#### cat
Perintah untuk mencantumkan, menggabungkan, dan menuliskan isi file.
```
cat > ingredients.txt
```
![Screenshot from 2024-12-23 01-44-30](https://github.com/user-attachments/assets/8a762e64-101b-4aa0-a23a-1f836c74a6f8)
```
cat ingredients.txt seasoning.txt > cook.txt
```
![Screenshot from 2024-12-23 01-57-17](https://github.com/user-attachments/assets/a3c83f20-28b3-4b48-9566-ae7067088981)
![Screenshot from 2024-12-23 01-59-06](https://github.com/user-attachments/assets/73e0afc8-635f-47a1-8aaf-c04d59085888)
#### grep
Perintah untuk mencari isi didalam file sesuai baris yang cocok dengan pola tertentu, berguna untuk memfilter file log besar.
```
grep carikata cook.txt
```
![Screenshot from 2024-12-23 02-08-01](https://github.com/user-attachments/assets/611a9047-6ce6-44e6-b953-eda3c169b573)
#### sed
Perintah untuk menemukan, mengganti, dan menghapus pola dalam file tanpa menggunakan editor teks. Gunakan subperintah s untuk mengganti pola yang cocok atau d untuk menghapusnya. Terakhir, tentukan file berisi pola yang akan diubah.
```
sed 's/telur/egg/g' ingredients.txt
```
![Screenshot from 2024-12-23 02-20-20](https://github.com/user-attachments/assets/0083c063-0ebc-4b08-9775-c2d818a2ee8f)
```
sed '/Bango/d' ingredients.txt
```
![Screenshot from 2024-12-23 02-26-38](https://github.com/user-attachments/assets/63dbf5e4-fef2-4f91-9ad2-7dbebc85f62d)
#### head
Perintah menampilkan sepuluh baris pertama dalam file teks atau data yang di-pipe di command-line interface.
```
head -5 cook.txt
```
![Screenshot from 2024-12-23 02-32-01](https://github.com/user-attachments/assets/6dd1b103-6acb-4bfb-ae9e-1d6eb53cf3b8)
#### tail
Perintah untuk menampilkan sepuluh baris terakhir dalam sebuah file, yang berguna untuk memeriksa data baru dan error.
```
tail -n colors.txt (-n mengubah jumlah baris yang ditampilkan)
```
![Screenshot from 2024-12-23 02-35-26](https://github.com/user-attachments/assets/7c94da71-fd28-43dd-b835-4fc6954bb1f9)
#### sort
![Screenshot from 2024-12-23 02-43-02](https://github.com/user-attachments/assets/bc4dab83-8ce7-49a8-a802-34f4674b2993)
![Screenshot from 2024-12-23 02-47-27](https://github.com/user-attachments/assets/968731fc-4e8c-4c8d-b6d2-f1123b532922)
#### diff
Perintah diff membandingkan isi dari dua file dan mencantumkan perbedaannya. Command ini digunakan untuk mengubah program tanpa memodifikasi kodenya.
![Screenshot from 2024-12-23 02-51-26](https://github.com/user-attachments/assets/65b2e1f2-369b-4070-9be4-22d79028ec16)
## Soal Case
Anda bekerja di sebuah tim data analis untuk sebuah situs web yang menampilkan data pembalap Formula 1. Data pembalap disimpan dalam sebuah file teks md yang bernama formula-one-drivers.md, dengan format sebagai berikut:```
  ID,Nama,Tim,Posisi,Gaji
  001,Lewis Hamilton,Mercedes,1,70000000
  002,Max Verstappen,Red Bull Racing,2,50000000
  003,Sergio Perez,Red Bull Racing,3,25000000
  004,Charles Leclerc,Ferrari,4,15000000
  005,Lando Norris,Mclaren,5,10000000
  006,Daniel Ricciardo,AlphaTauri,6,8000000``` 
  Tugas kalian adalah melakukan beberapa manipulasi text menggunakan perintah `sed` di Linux. Berikut adalah beberapa hal yang harus kalian lakukan.
  - Mengganti kata "Red Bull Racing" dengan "Red Bull Racing Honda" pada kolom Tim.
  - Menghapus seluruh baris yang berisi pembalap dengan posisi lebih dari 3
#### Perintah
1. "Red Bull Racing Honda"
   ![Screenshot from 2024-12-23 03-03-56](https://github.com/user-attachments/assets/ebdc6692-ab8d-44bb-982e-4ca8a54b3458)
2. Menghapus
   ![Screenshot from 2024-12-23 03-08-54](https://github.com/user-attachments/assets/38164d8d-7254-40c7-89a1-f155fdfaee70)
## Create
Bash Script untuk melakukan installasi webserver, dengan kebutuhan case: jika user menginputkan nomor 1 maka dia akan melakukan installasi WebServer Nginx dan jika user menginputkan nomor 2 maka akan melakukan installasi WebServer Apache2
- Membuat File instal-nginxorapache.sh
![Screenshot from 2024-12-23 04-22-50](https://github.com/user-attachments/assets/492378ca-1751-48cc-b54e-916e0cfeec07)
- Masuk ke superuser untuk ijin akses
![Screenshot from 2024-12-23 03-48-52](https://github.com/user-attachments/assets/2a5e3c7d-d798-4a1b-86c6-063276e1ff9f)
- Menjalankan scripts
![Screenshot from 2024-12-23 04-22-11](https://github.com/user-attachments/assets/3ee9bad8-e4bd-4efd-9d49-c775384c60be)
## Implementasi Firewall pada linux server 
- Buatlah 2 buah Virtual Machine. 
- Study case nya adalah agar hanya server A yang hanya dapat mengakses WebServer yang ada pada server B.
- Carilah cara agar UFW dapat memblokir ataupun mengizinkan specific protocol jaringan seperti TCP dan UDP.
- Jelaskan perbedaan protocol Jaringan TCP serta UDP.
#### Study case
##### Aktifkan ufw
![Screenshot from 2024-12-23 04-54-56](https://github.com/user-attachments/assets/1ac0eb70-3b26-408a-b0b6-537d2ff98cf9)
![Screenshot from 2024-12-23 04-55-02](https://github.com/user-attachments/assets/e5915f07-4d4b-4aac-914b-f314db73f970)
##### Pada server B, buat firewall hanya server A yang dapat akses webserver
![Screenshot from 2024-12-23 05-12-18](https://github.com/user-attachments/assets/75038103-3794-4ee2-a29c-30772b6d0b05)
##### Block TCP dan UDP
![Screenshot from 2024-12-23 05-16-35](https://github.com/user-attachments/assets/81142f97-6fc2-48c6-977d-ec8fbddbc348)
#### Perbedaan TCP serta UDP
1. TCP menciptakan jalur komunikasi yang aman untuk memastikan transmisi semua data yang andal. Setelah pesan dikirim, tanda terima diverifikasi untuk memastikan semua data telah ditransfer.

2. UDP tidak membuat koneksi saat mengirim data. UDP mengirim data tanpa mengonfirmasi penerimaan atau memeriksa kesalahan. Itu berarti sebagian atau semua data mungkin hilang selama transmisi.
3. TCP paling baik untuk :

- Email atau SMS

- Transfer berkas

- Penjelajahan web

4. UDP paling baik untuk :

- Streaming langsung

- Permainan daring

- Obrolan video
