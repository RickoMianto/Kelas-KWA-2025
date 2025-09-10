# Soal
- Kategori: Web Exploitation
- Judul : SQL Direct
- Tag : Medium, Web Exploitation, picoCTF 2022, sql

# Resource
https://play.picoctf.org/practice/challenge/443?category=1&page=1&search=sql

# Langkah Penyelesaian
1. Pertama tama yang saya lakukan adalah start instance lalu membuka webshell dan mengcopas command postgresql beserta password yang ada di description soal.
<img width="950" height="866" alt="Screenshot 2025-09-10 090602" src="https://github.com/user-attachments/assets/7a5f548f-fb37-45dd-b921-6a9afc7551b4" />

2. Setelah berhasil masuk ke database saya memassukkan payload PostgreSQL untuk mendapatkan flag yang ada. Payload yang saya gunakan antara lain `/l` yang berfungsi untuk list all database, lalu `/c pico` untuk connect ke database pico, `/dt` untuk list all table, dan yang terakhir `SELECT * FROM Flags;` untuk mendapatkan seluruh isi dari colom flags
<img width="1807" height="520" alt="Screenshot 2025-09-10 091017" src="https://github.com/user-attachments/assets/668d89cc-0b32-4dd6-850d-b4ba34db7bd8" />

<img width="770" height="743" alt="Screenshot 2025-09-10 091246" src="https://github.com/user-attachments/assets/75c3e2e6-6d75-4f81-93ac-89363494a46e" />

3. Setelah mendapat flagnya, kita bisa langsung copas dan submit untuk menyelesaikan chalangenya.
<img width="948" height="810" alt="Screenshot 2025-09-10 091302" src="https://github.com/user-attachments/assets/4efa2b5d-2a59-4c51-a3ef-9b2f68d2f0c8" />
