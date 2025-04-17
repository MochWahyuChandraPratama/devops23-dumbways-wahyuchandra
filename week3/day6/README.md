# DAY 6
## Task
1. Jelaskan apa itu Web server dan gambarkan bagaimana cara webserver bekerja.
2. Buatlah Reverse Proxy untuk aplilkasi yang sudah kalian deploy kemarin. ( dumbflix-frontend) dan implementasikan penggunaan pm2 di aplikasi tersebut, untuk domain nya sesuaikan nama masing" ex: alvin.xyz .
3. Jelaskan apa itu load balance.
4. implementasikan load balancing kepada aplikasi  dumbflix-frontend yang telah kalian gunakan.
##### Web Server
Web server adalah perangkat lunak penghubung antara client dan aplikasi yang memberi layanan berupa data atau bentuk halaman web.
- Secara garis besar, cara kerja web server adalah dengan menerima permintaan data klien, untuk kemudian mengirimnya kembali dalam bentuk berkas atau konten website.
- Ketika klien melakukan permintaan data ke web server, maka data akan tersimpan pada Transmission Control Protocol (TCP).
- Kemudian, data akan dikirim menuju ke alamat website tujuan.
- Setelah permintaan berhasil diproses, maka browser akan menampilkan data server dalam bentuk halaman, konten website atau berkas yang tampil di layar monitor Anda.
- Namun, jika request data tidak dapat ditemukan, maka otomatis web server akan menolak permintaan tersebut dan menampilkan notifikasi “Page Not Found” atau “Error 404”.
#### Reverse Proxy
![Screenshot from 2024-12-24 07-34-36](https://github.com/user-attachments/assets/ef5cbc3d-873a-4877-9ada-8f90a4b5cf23)
![Screenshot from 2024-12-24 07-33-59](https://github.com/user-attachments/assets/2d7e835a-17dd-4093-9f95-1219d8cf6eee)
![Screenshot from 2024-12-24 07-38-12](https://github.com/user-attachments/assets/08f066f7-929b-42bb-aafa-c0437ea98e76)
![Screenshot from 2024-12-24 07-44-31](https://github.com/user-attachments/assets/aec22607-9218-40b6-ace0-02de17745191)
![Screenshot from 2024-12-24 07-58-12](https://github.com/user-attachments/assets/ddaecc39-381b-4f2b-b8a3-1fc1a948a0ac)
![Screenshot from 2024-12-24 08-00-29](https://github.com/user-attachments/assets/7e668b31-c24c-4df0-b247-923bf7b01187)
### Menggunakan reload lebih aman dibandingkan dengan restart karena reload walaupun terdapat error server tetap dapat berjalan. Jika ingin menjalankan restart pastikan tidak terdapat error, apabila masih terdapat error server akan berhenti dan halaman web tidak akan dapat diakses.
![Screenshot from 2024-12-24 08-06-08](https://github.com/user-attachments/assets/b0dd6201-aea3-43df-83fd-4001b67ba55c)
![Screenshot from 2024-12-24 08-23-14](https://github.com/user-attachments/assets/d319197d-472f-47b0-9324-f089de754565)
![Screenshot from 2024-12-24 08-22-46](https://github.com/user-attachments/assets/cff62b16-d2cb-4957-ad6b-eba6357ba34c)
![Screenshot from 2024-12-24 08-52-15](https://github.com/user-attachments/assets/24114996-cfa5-4faa-a7ac-f4d85668a3fe)
![Screenshot from 2024-12-24 08-53-37](https://github.com/user-attachments/assets/a7a84404-ca60-4a24-b8ff-cc9365914706)

#### Load Balance
Load balance adalah suatu konfigurasi sebagai respon antisipasi jika sewaktu-waktu terjadi kendala pada salah satu server, akan ada backup server. Biasanya menggunkan algoritma Round Robin, metode ini bekerja dengan cara menyalurkan lalu lintas jaringan secara berurutan dari satu server ke server lainnya sehingga menciptakan rotasi pembagian yang stabil.
#### Implementasi Load Balancing
![Screenshot from 2024-12-24 08-57-07](https://github.com/user-attachments/assets/bc70ce08-6aa7-4d0a-b300-5d3c82b308bc)
![Screenshot from 2024-12-24 09-11-22](https://github.com/user-attachments/assets/1abc77d6-c495-4edb-81b9-2b6a7e1b799a)
![Screenshot from 2024-12-24 09-12-51](https://github.com/user-attachments/assets/6c6a4a57-1548-4ebc-bd9d-7fab87be74f0)
![Screenshot from 2024-12-24 09-13-39](https://github.com/user-attachments/assets/e2f9df08-3fb6-48e3-af36-11cfa2ec0ba1)
![Screenshot from 2024-12-24 09-17-53](https://github.com/user-attachments/assets/eddf4fe2-54a6-4ff8-8f0b-af6403eab95e)
![Screenshot from 2024-12-24 09-22-15](https://github.com/user-attachments/assets/da65e912-7857-41db-8245-387d6ce14673)
![Screenshot from 2024-12-24 09-34-07](https://github.com/user-attachments/assets/0e489ff5-a2d1-4cf7-ac8d-083b5bb59257)
![Screenshot from 2024-12-24 09-32-53](https://github.com/user-attachments/assets/6f8d0c3d-5e7e-477a-8a41-9d1ef2acdb6f)
![Screenshot from 2024-12-24 09-39-54](https://github.com/user-attachments/assets/31ecc1b1-f127-4f1a-a7df-38f5ab7738d0)
