# Soal
- Kategori: Web Exploitation
- Judul : More SQLi
- Tag : Medium, Web Exploitation, picoCTF 2023, sql

# Resource
https://play.picoctf.org/practice/challenge/443?category=1&page=1&search=sql

# Langkah Penyelesaian
1. Pertama tama yang saya lakukan start instance seperti biasa lalu menuju ke login page yang linknya terdapat pada description soal.
<img width="956" height="862" alt="image" src="https://github.com/user-attachments/assets/88791b9a-5e87-4667-9c28-afacbfcbd4ea" />

2. Seperti yang terdapat pada hint soal yang menyatakan SQLiLite, disini saya login dengan cara yang sama pada soal SQLiLite.
<img width="566" height="435" alt="Screenshot 2025-09-10 084851" src="https://github.com/user-attachments/assets/5769f3b7-ec93-4615-8aa7-a80ef6a6c17e" />

3. Lalu untuk mendapatkan flagnya saya menggunakan burpsuite untuk menangkap request login dan mengirimkannya menggunakan repeater, dan setelah melakukan langkah ini maka kita akan mendapatkan flagnya yang bisa langsung kita submit untuk menyelesaikan soalnya.
<img width="1908" height="1013" alt="Screenshot 2025-09-10 085337" src="https://github.com/user-attachments/assets/71585645-2e5b-4025-9a48-28689073ef75" />

<img width="947" height="853" alt="Screenshot 2025-09-10 085414" src="https://github.com/user-attachments/assets/12208b56-aa83-418e-ab7d-64bde2cae729" />
