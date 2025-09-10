# Soal
- Kategori: Web Exploitation
- Judul : No SQL Injection
- Tag : Medium, Web Exploitation, picoCTF 2024, browser_webshell_solvable

# Resource
https://play.picoctf.org/practice/challenge/443?category=1&page=1&search=sql

# Langkah Pengerjaan
1. Pertama tama kita bisa start instance dan buka webshel yang disediakan picoCTF, hal yang harus dilakukan di webshell adalah mendownload file yang dapat kita copy link nya di deskripsi soal setelah kita start instance.
<img width="964" height="422" alt="Screenshot 2025-09-09 200328" src="https://github.com/user-attachments/assets/d6a8e4bb-6947-470d-8fd0-157aa7c83421" />

<img width="1898" height="437" alt="Screenshot 2025-09-09 200711" src="https://github.com/user-attachments/assets/bd6ee016-6501-4624-81f7-99264b3142e4" />

2. Setelah selesai melakukan download kita bisa langsung ekstrak filenya dan kita eksplorasi isi directory dari file tersebut untuk mendapatkan email atau user yang akan kita gunakan untuk login nantinya. Disini saya menemukan emailnya di server.js
<img width="720" height="802" alt="Screenshot 2025-09-10 231859" src="https://github.com/user-attachments/assets/ecd6659d-1432-4a25-8b4b-8c854ff9b00f" />

3. Setelah mendapatkan emailnya kita bisa langsung saja login menggunakan email tersebut dan memasukkan sebuah payload di field password. Payload yang saya gunakan disini adalah `{"$ne":""}`, fungsi dari payload ini adalah untuk membuat query login atau filter selalu true, sehingga penyerang bisa bypass autentikasi.
<img width="1919" height="1018" alt="Screenshot 2025-09-09 201647" src="https://github.com/user-attachments/assets/77f3df1f-231b-4239-a8b7-4feff7e56e07" />

<img width="1919" height="1021" alt="Screenshot 2025-09-09 202047" src="https://github.com/user-attachments/assets/f79b3b05-e237-4d4c-9413-f79fb1d5004e" />

4. Seperti yang terlihat dari gambar sebelumnya saya mencoba melakukan inspeksi dari request login yang saya lakukan namun tidak bisa melihat response yang didapat, jadi saya menggunakan burpsuite untuk menangkap request dan mengirimkannya melalui repeater untuk mendapatkan responsenya.
<img width="1901" height="1010" alt="Screenshot 2025-09-09 203536" src="https://github.com/user-attachments/assets/23fa1035-fe13-43d7-a823-77250022082b" />


5. Disini saya mendapat sebuah token yang bisa di decode menggunakan base 64 decoder untuk mendapatkan flagnya, setelah di decode kita bisa langsung saja submit flagnya untuk menyelesaikan chalange
<img width="1206" height="719" alt="Screenshot 2025-09-09 203831" src="https://github.com/user-attachments/assets/de592fd4-a90a-46f4-b2ae-135ed3f337be" />

<img width="958" height="792" alt="Screenshot 2025-09-09 203857" src="https://github.com/user-attachments/assets/5ccd6f39-401c-4c4b-806c-fffbe6dd67da" />

