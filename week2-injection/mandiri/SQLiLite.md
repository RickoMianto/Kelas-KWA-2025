# Soal
- Kategori: Web Exploitation
- Judul : SQLiLite
- Tag : Medium, Web Exploitation, picoCTF 2022, sql

# Resource
https://play.picoctf.org/practice/challenge/443?category=1&page=1&search=sql

# Langkah Pengerjaan
1. Pertama tama yang saya lakukan adalah start instance dan menuju login page yang dapat kita temukan di description, seperti pada hint bahwa kita ingin login sebagai admin maka saya memasukkan admin pada field username dan mengisi password dengan random karena saya belum mengetahuinya.
<img width="959" height="855" alt="Screenshot 2025-09-10 084010" src="https://github.com/user-attachments/assets/e78c2857-4ed4-421d-a01f-ee859c20ba56" />

<img width="1442" height="330" alt="Screenshot 2025-09-10 233617" src="https://github.com/user-attachments/assets/72cf22bb-97a2-4d98-a733-1513695cfccc" />

2. Setelah saya diklik login maka kita akan mendapat tampilan antarmuka di webnya sebagai berikut.
<img width="806" height="202" alt="Screenshot 2025-09-10 084056" src="https://github.com/user-attachments/assets/29c9bd1f-19d0-4900-94ba-7803242f2974" />

3. Dari sini saya mencoba login kembali dengan memasukkan payload `' or 1=1--` pada field password, fungsi dari payload ini adalah untuk menutup input string dan menambahkan kondisi selalu benar sehingga baypass login dapat dilakukan.
<img width="1144" height="270" alt="Screenshot 2025-09-10 084218" src="https://github.com/user-attachments/assets/86b217d0-34ee-42d8-91c7-02d704362715" />

4. Dari gambar sebelumnya kita tahu bahwa kita masih blum bisa mendapatkan flagnya, cara untuk mendapatkan flagnya cukup mudah hanya dengan inspeksi pada bagian element maka kita akan mendapatkan flagnya dan bisa langsung kita submit untuk menyelesaikan chalangenya.
<img width="1919" height="869" alt="Screenshot 2025-09-10 234127" src="https://github.com/user-attachments/assets/709ffd59-e5e3-4f51-9367-2bf961d1609a" />

<img width="953" height="825" alt="Screenshot 2025-09-10 084446" src="https://github.com/user-attachments/assets/ae423dd3-4273-4787-b765-a0208cd0ca92" />
