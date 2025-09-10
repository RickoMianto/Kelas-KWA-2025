# Soal
- Kategori: Web – Injection
- Poin : ★★★★ (4 bintang)
- Judul : Christmas Special
- Tag : (tidak ada tag khusus)

# Resource
https://demo.owasp-juice.shop/#/score-board?categories=Injection

# Langkah Penyelesaian 
1. Pertama tama saya menambahkan sebuah item ke dalam basket, dan menangkap request http tersebut menggunakan burpsuite, setelah mendapatkannya saya lalu mengirimkan request tersebut ke repeater.
<img width="1170" height="549" alt="Screenshot 2025-09-10 212430" src="https://github.com/user-attachments/assets/2376abff-0f1b-48b3-bb82-d4835980492b" />

<img width="729" height="606" alt="Screenshot 2025-09-10 212831" src="https://github.com/user-attachments/assets/d2596500-a2c1-431b-b4e6-061742508a80" />

2. Selanjutnya di repeater kita bisa langsung mengedit ProductId menjadi Id dari item Christmast Special lalu kita send request, untuk mengetahui Idnya kita bisa mendapatkannya di database dengan menggunakan payload yang sama seperti yang digunakan pada chalange Database Schema.
<img width="644" height="253" alt="Screenshot 2025-09-10 212320" src="https://github.com/user-attachments/assets/f34be97e-7c0b-4420-9f44-abefe81a96d7" />

<img width="1501" height="788" alt="Screenshot 2025-09-10 212858" src="https://github.com/user-attachments/assets/7a14183c-7044-4a37-9874-e7f5e67f987b" />

3. Setelahnya kita bisa kembali ke web pada bagian basket dan menyelesaikan checkout, maka setelah proses checkout berhasil chalange akan terselesaikan
<img width="1177" height="704" alt="Screenshot 2025-09-10 212912" src="https://github.com/user-attachments/assets/3c6f0eb6-7cd4-4c87-9b16-0686e9d81059" />

<img width="1796" height="790" alt="Screenshot 2025-09-10 212939" src="https://github.com/user-attachments/assets/56597c6a-1e7a-4725-9edb-18c879a7bd93" />
