# Soal
- Kategori: Web Exploitation
- Judul : SQL Direct
- Tag : Medium, Web Exploitation, picoCTF 2022, cookie

# Resource
https://play.picoctf.org/practice?category=1&page=1&search=power

# Langkah Penyelesaian
1. Pertama tama saya start instance lalu saya menuju page dengan link yang terlampir pada description soal. Pada link tersebut kita akan mendapati tampilan antarmuka sebagai berikut.
<img width="948" height="865" alt="Screenshot 2025-09-10 085901" src="https://github.com/user-attachments/assets/8d42ea6c-6238-42ee-88e5-74d406c9c817" />

<img width="707" height="239" alt="Screenshot 2025-09-10 085914" src="https://github.com/user-attachments/assets/ca2c01b7-a536-4dcd-a113-38738944e007" />

2. Selanjutnya kita bisa coba klik button yang tersedia di tampilan antarmuka web tersebut dan akan memperoleh hasil sebagai berikut.
<img width="808" height="234" alt="Screenshot 2025-09-10 085923" src="https://github.com/user-attachments/assets/96e4bd4b-a425-47d9-b2e9-945dafff6ca0" />

3. Yang perlu kita lakukan adalah melakukan inspek pada Application dan cookies lalu mengganti nilai dari isAdmin menjadi 1 untuk mengubah hasilnya menjadi true dan kita akan dianggap sebagai admin.
<img width="1199" height="365" alt="Screenshot 2025-09-10 090141" src="https://github.com/user-attachments/assets/0119746d-5386-4213-9774-3a029f88b96d" />

4. Selanjutnya kita bisa coba refresh web dan akan muncul sebuah flag sebagai berikut. Flag yang didapat bisa langsung kita copas dan submit untuk menyelesaikan chalangenya.
<img width="1919" height="445" alt="Screenshot 2025-09-10 090208" src="https://github.com/user-attachments/assets/a81d7de2-bb67-4717-8408-aeb8beeca29a" />

<img width="953" height="868" alt="Screenshot 2025-09-10 090224" src="https://github.com/user-attachments/assets/3b61d71f-9e62-4b25-bbac-2f4c5a24ff2c" />
