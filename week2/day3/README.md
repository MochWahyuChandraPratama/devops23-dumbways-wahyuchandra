# DAY 3
## VCS (Version Control System)
Sebuah alat yang gunanya untuk memanajeman perubahan suatu code. Tools yang dapat membantu developer untuk mentracking perubahan disetiap waktu. VCS pada dasarnya memiliki database terpusat yang harus terkoneksi ke jaringan bersifat online.

## GIT (Penciptanya Linus Torvalds)
Adalah salah satu tools manajemen data yang memiliki keunggulan lokasi penyimpanan tidak hanya berada dalam satu tempat. Jadi semua orang yang memiliki akses dapat terlibat dalam proyek aplikasi mulai dari pengkodean sampai menyimpan database git, sehingga dapat dimanajemen secara online maupun offline. Kenapa memilih git :
- Menyimpan seluruh versi source code.
- Memahami cara kolaborasi dalam proyek.
- Lebih aman karena tercatat siapa yang melakukan perubahan.
- Memahami cara deploy aplikasi modern.
- Ikut berkontribusi dalam proyek open source.

## Flow dari cara kerja Git
Dalam satu repository git memiliki berbagai jenis file jika akan melakukan revisi user dapat dengan mudah melakukan perubahan. File yang diubah dapat dilakukan versioning sampai final proyek. Perubahan ini akan tercatat dan terbackup secara aman, saat user ingin memanage file lama tidak akan terhapus masih bisa diakses dalam database git. Jauh lebih rapi dibandingkan penyimpanan lokal. Siapapun yang terlibat dalam proyek harus melakukan komunikasi dengan yang lain jika terjadi perubahan apapun sehingga tidak akan terjadi yang namanya error.

## Command GIT
#### Git init
Perintah git init digunakan untuk membuat project baru, lebih tepatnya fungsi git init untuk membuat repository baru. Selain itu git init juga dapat digunakan secara spesifik untuk menjadikan directory suatu project yang sedang dikerjakan menjadi repository baru digit.
```
git init
```
```
git init directory/
```
#### Git add
Perintah untuk memberi tahu git mengenai file yang akan ditambahkan untuk commit berikutnya. Ketika melakukan perintah git add, file akan masuk ke dalam fase staging dan perubahannya tidak akan dicatat sampai dengan kita menjalankan perintah git commit.
Menambahkan semua perubahan di satu project.
```
git add .
```
Menambahkan secara spesifik file dengan tipe tertentu (*.php/txt/conf)
```
git add *.exe
```
```
git add namafile/direktori
```
#### Git commit
Perintah untuk menyimpan perubahan, dimana perubahan yang sudah diakukan sebelumnya akan tersimpan dan tercatat dalam log. Log tersebut akan berguna jika suatu saat mengalami masalah pada commit-commit selanjutnya, agar dapat mengembalikan program yang sudah tersimpan sebelumnya. Alangkah baiknya sebelum melakukan git commit pastikan selalu status file/direktori sudah masuk fase apa dengan perintah
```
git status
```
Jika belum melakukan setup konfigurasi ke git
```
git config --global user.email "alamat@email.com"
```
```
git config --global user.name "username"
```
mengecek list config
```
git config --list
```
Jika sudah yakin benar bisa masuk fase commit
```
git commit -m "commit message/first commit"
```
Mendefinisikan url repository tujuan git
```
git remote add origin url
```
Setup SSH Key akun git
```
ssh-keygen
cd .ssh/
ls
cat id_darivmuser.pub
```
copypaste id.pub ke SSH Key github, lalu cek status
```
ssh -T git@github.com
```
cek remote git
```
git remote -v
```
#### Git push
Perintah untuk mengunggah (upload) file dari local repository ke remote repository git. (origin=nama remote default, master=nama branch default)
```
git push origin master
```
#### Git pull
Perintah untuk menyamakan konten dari remote repository git dan memperbarui repositori lokal agar sesuai dengan remote repository git. Perbedaan perintah git pull dan git fetch adalah git pull akan mengambil commit terbaru lalu otomatis menggabungkan (merge) dengan branch yang aktif, sedangkan git fetch akan mengambil commit saja.
Jika branch sudah tersimpan sebelumnya
```
git pull
```
#### Git clone
Perintah git clone biasa digunakan untuk membuat clone atau salinan dari existing repo di tempat lain. Ketika melakukan git clone, repo salinan tersebut akan mempunyai log tersendiri, file sendiri, dan environtment yang berbeda dari repo aslinya.
```
git clone url_repository
```
```
git clone --branch master url_repository
```
#### Git branch
Perintah yang digunakan untuk membuat suatu versi dari repository yang ada mirip seperti clone. Fungsi branch akan digunakan untuk men-develop fitur tanpa harus mengganggu cabang utama sehingga konflik bisa dihindari.
```
git branch namabranch
```
untuk cek list branch
```
git branch -a
```
untuk menghapus branch
```
git branch -d namabranch
```
#### Git fetch
Perintah untuk mengambil semua branch dari repositori. Ini juga mengunduh semua komit dan file yang diperlukan dari repositori lain.
```
git fetch remote
```
Mengambil branch secara spesifik
```
git fetch remote namabranch
```
Mengambil semua remote terdaftar dan semua branch-nya
```
git fetch --all
```
#### Git checkout
Perintah untuk melakukan switch branch yang sedang aktif.
```
git checkout namabranch
```
Membuat branch baru dan switch ke branch tersebut
```
git checkout -b namabranch
```
#### Git merge
Perintah untuk menggabungkan beberapa urutan commit menjadi satu riwayat terpadu. Pada umumnya, git merge digunakan untuk menggabungkan dua branch.
```
git checkout main-branch
git merge --no-ff branchbaruatauprojectterkait
```
#### Git ignore
Perintah untuk mengasingkan suatu file/direktori dari git
Buat dulu file
```
touch .gitignore
```
Menyisipkan nama file yang akan diasingkan
```
nano "contohfile" > .gitignore
```
## Study Case
Ada 2 Developer yang sedang melakukan development aplikasi dari perusahaan A sebut saja Reyhan dan Teguh mereka kebetulan sedang mengerjakan suatu proyek yang sama, dan mereka sedang mengerjakan file yang sama index.html. Reyhan membuat perubahan pada file index.html dan melakukan commit: git add index.html; git commit -m "fix: Typo on Description". Teguh kebetulan juga membuat perubahan pada index.html dan melakukan commit: git add index.html ; git commit -m "feat: Header Adjustment". Kemudian disini ternyata Reyhan melakukan push ke repository. Teguh, yang belum melakukan push, mencoba untuk melakukan push ke repositori. Karena ternyata ada perubahan baru di remote yang belum dimiliki Teguh, Git menolak push Teguh dan memberi tahu bahwa ada konflik. Disini Teguh harus melakukan Fix Conflict tersebut agar perubahan yang di buat oleh Teguh dapat tersimpan ke dalam repositori app tersebut. lalu bagaimana cara menangani case yang dimiliki oleh Teguh?
#### Kesimpulan
Pertama-tama lakukan perintah
```
git pull origin namabranch
```
lihat apa perubahan dalam file index.html
```
cat index.html
```
copy perintah yang ada di git pull sebelumnya
- Ada 3
- Perintah false untuk menggabungkan commit terbaru ke repo lokal kita tanpa rebase/merubah
```
git config pull.rebase false
```
- Perintah true untuk melakukan rebase/merubah repo lokal sesuai commit jadi file yang sudah dibuat dilokal bisa hilang
```
git config pull.rebase true
```
- Perintah untuk mempercepat pull dengan mengesampingkan konfigurasi bawaan dari repo utama
```
git config pull.ff only
```
Pilih false karena file yang dibuat dilokal tidak akan hilang
```
git config pull.rebase false
```
Cek status
```
git status
```
Lakukan pull
```
git pull origin namabranch
```
```
git status
```
Terakhir push file index.html dilokal teguh
```
git push origin namabranch
```
