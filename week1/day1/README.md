# DAY1
## DEVOPS
### Apa itu Devops?
Secara general devops terdiri dari kata dev dan ops. Dev adalah tim yang mengembangkan suatu aplikasi atau web. Ops adalah tim yang berkerja memanage hardware dari server. Devops adalah seseorang yang memiliki akses secara keseluruhan untuk memanage suatu server agar berjalan lancar dan terus memantau lewat infrastruktur sistem memastikan tidak ada terjadinya error, bug, kesalahan sistem, semua yang terkait dengan keberlangsungan suatu server.
#### Continuous
1. Continuous Integration (CI) - Penggabungan kode yang berkelanjutan ke dalam repositori kode. Tujuannya untuk mendeteksi bug atau error lebih awal dan memastikan aplikasi berjalan sesuai algoritma kode yang telah dibuat tim developer.
2. Continuous Delivery (CD) - Proses menyiapkan perubahan kode ke deploy staging atau tahap pra produksi setelah proses pembuatan secara manual. Kode yang masuk pada CD harus lulus pengujian unit otomatis, pengujian integrasi, dan pengujian sistem.
3. Continuous Deployment - Langkah terakhir setiap melakukan perubahan yang lolos uji otomatis akan langsung terdeploy ke produksi tanpa intervensi manual.
4. Continuous Testing - Melakukan pengujian otomatis secara berkelanjutan untuk memastikan kualitas aplikasi sejak tahap awal.
5. Continuous Monitoring - Mengawasi secara terus-menerus aplikasi yang telah dibuat untuk menjaga infrastruktur jika terjadi masalah dan memelihara sistem.

### Virtual Machine
Ada berbagai virtual machine seperti : Multipass, VMware, VirtualBox, dan masih banyak lagi.
### Command Install
```
sudo snap install multipass / sudo apt install multipass
```
#### Jika sudah terinstal dapat menggunakan command
![muplanch](https://github.com/user-attachments/assets/b52a5202-4eba-487d-a021-1320ed7f88b7)
```
multipass launch --name pratama
```
#### Untuk menjalankan multipass
![mupshel](https://github.com/user-attachments/assets/902d2b9b-9d3b-4afc-a544-db0177f52d30)
```
multipass shell pratama
```
#### Install nginx
![Screenshot from 2025-04-21 09-17-12](https://github.com/user-attachments/assets/39671610-b7d4-4c95-9be6-f64c2835f8b1)

```
sudo apt install nginx
```
