# Jarkom-1-IT06-2024
## Anggota kelompok
   ### Benjamin Khawarizmi Habibi 5027231078
   ### Callista Meyra Azizah 5027231060

```
Note: nc dijalankan di terminal, dan file pcap dijalankan di wireshark sesuai dengan soalnya.
```


# Write Up
## Advance Sanity Check (nc 10.15.42.60 44000 // sanity.pcap)

Pada soal ini, ada beberapa pertanyaan apabila kita memasukkan command nc kepada terminal.

Pertanyaan pertama adalah:
```
Apa username pengirim?
Format: username
```
Darisana, secara manual menggunakan follow tcp, sehingga memasuki stream berikut.
![janeD03](https://github.com/user-attachments/assets/8fcbe473-0722-4aad-8ddc-5feba2797a16)
Maka saya coba memasukkan username JaneD03 tersebut kedalam terminal. 
Darisana muncullah pertanyaan kedua, yaitu:
```
Apa nama file yang dikirim?
Format: filename.extension
```
Sama seperti sebelumnya, saya follow tcp stream sehingga mendapat yang kira-kira benar, yaitu sebagai berikut:
![filename clu3 txt + cek ada surprise](https://github.com/user-attachments/assets/54a3a9a5-5a6b-474d-9a14-58734d507853)
Dan saya masukkan Clu3.txt sebagai jawabannya. Yang berlanjut dengan: 
```
Ikuti petunjuk untuk mendapatkan pesan rahasia
Format: string
```
Setelah kita analisis dari foto sebelumnya, ada kalimat menarik:
```
coba periksa peraturan soal shift, ada suprise - Jane Doe
```

Dengan itu saya mencoba untuk membuka linktree jarkom dan masuk kedalam peraturan praktikum, kemudian ke bagian peraturan soal shift. Lo and behold, ada string binary64 yang merupakan :
```cGVud29yZA==```
![WhatsApp Image 2024-09-18 at 18 43 56_fd9aded0](https://github.com/user-attachments/assets/c6fb06e7-4348-4119-a3ca-ce21bbbf374e)

Lalu di convert menjadi string biasa:
![WhatsApp Image 2024-09-18 at 18 50 46_8090be62](https://github.com/user-attachments/assets/df2b2e48-f250-4be5-b4d6-c41ffa2a275b)
Terdapat string "penword" didalamnya, maka saya masukkan ke dalam terminal.

Lalu muncul flagnya:
```
Benar! Ini flag-mu: JarkomIT{8uK4n_S4n1ty_b1a5A_Skz1qBYkSg6XUK9sUQAuwmVghSu551rKRBiPzcAzDvkVFcVam8lteIKK}
```

- Dokumentasi Terminal:
  
![1](https://github.com/user-attachments/assets/d2bf179a-ed55-4ac7-8b7b-30ac78f38e70)

- Flag: JarkomIT{8uK4n_S4n1ty_b1a5A_Skz1qBYkSg6XUK9sUQAuwmVghSu551rKRBiPzcAzDvkVFcVam8lteIKK}

## Pegawai Negeri Sebelah (nc 10.15.42.60 53000 // rahasia.pcap)

Sama seperti sebelumnya, kita memasukkan command nc diatas kedalam terminal, yang akan mengeluarkan soal sebagai berikut:
```
Siapa yang memiliki password nNnM%coQuF?
Format: String
```
Sama seperti sebelumnya, saya mencoba follow tcp stream hingga pada stream di bawah ini, lalu memasukkan nNnM%coQuF? pada tool "find" di dalamnya:
![pegawai pass](https://github.com/user-attachments/assets/feeb362a-10a3-40b3-b2d4-1266e99e6aee)
Dari sini terlihat yang memiliki passwordnya adalah Vero Tampubolon. Kita masukkan ke dalam terminal, lalu muncul pertanyaan selanjutnya:
```
Apa jabatan dari Taufan Kuswandari?
Format: String
```
Sama seperti sebelumnya, kita gunakan tool find lagi dan memasukkan nama Taufan Kuswandari untuk dicari, dan didapatlah jawabannya, Analisis Kebijakan:
![pegawai taufan](https://github.com/user-attachments/assets/4f9ebd3c-29ef-44bd-b5a5-1402ab359c6d)
Setelah itu muncullah pertanyaan lagi, pertanyaan kali ini adalah:
```
Siapa yang paling awal di list?
Format: String
```
Untuk ini kita scroll aja ke paling atas dan copy-paste namanya, Cici Mustofa.
![pegawai 1](https://github.com/user-attachments/assets/b5e762d6-456e-4a74-b6ed-0ba753d52b3c)
Pertanyaan muncul lagi, yaitu:
```
Apa password paling akhir dari list?
Format: String
```
Seperti sebelumnya, kita ke paling bawah dan copy paste passwordnya, yaitu RyxaJPv^yF
 ![pegawai terakhir](https://github.com/user-attachments/assets/ef144077-bbcf-4dd3-994e-2abe0cdafad4)
 Lalu muncul flagnya:
```
Benar! Ini flag-mu: JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_vtgqiVzSDRb5vZ0wu2wXiiK7WL3n2Dbu77NR0BrNTbC4eMuEq0vgM4h}  
```

 - Dokumentasi Terminal:
   
![pegawau](https://github.com/user-attachments/assets/c5aa0cc1-8996-45a9-ae87-dafb522d0b8f)

 - Flag: JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_vtgqiVzSDRb5vZ0wu2wXiiK7WL3n2Dbu77NR0BrNTbC4eMuEq0vgM4h}

## EZ (nc 10.15.42.60 54000 // ez.pcap)
Sama seperti sebelumnya, kita memasukkan comman nc diatas kedalam terminal yang akan me-reveal sebuah pertanyaan:
```
Temukan jawaban dari log tersebut
Format: string ex. kata kata
```
Lalu, secara manual follow tcp stream hingga mendapatkan sesuatu yang menarik, yaitu:
![string rahasia halo mas](https://github.com/user-attachments/assets/b553f12f-9283-459d-a67c-d019bd0f81b4)
Maka kita masukkan "jawabannya jawaban" sebagai jawabannya. Kemudian muncul pertanyaan selanjutnya:
```
Port berapa yang digunakan service tersebut
Format: xxxx: ex. 443
```
Darisini kita lihat port yang digunakan, yaitu 1234:
![WhatsApp Image 2024-09-18 at 20 42 02_7c253e47](https://github.com/user-attachments/assets/e5ed7ade-906a-4e79-bf4c-ead242c28acb)
Lalu muncul flagnya:
```
Benar! Ini flag-mu: JarkomIT{BiAr_aman_Pake_sSh_0JHNcd71asFzioyKGzm8Ukf3P3zUHfNr25O9KhH5qBjJAvq9VN6dEZ}
```

- Dokumentasi Terminal:

 ![ez](https://github.com/user-attachments/assets/43173132-ccde-426c-b380-4552c789c41a)

- Flag: JarkomIT{BiAr_aman_Pake_sSh_0JHNcd71asFzioyKGzm8Ukf3P3zUHfNr25O9KhH5qBjJAvq9VN6dEZ} 
## Illegal Breakthrough (nc 10.15.42.60 46000 // break.pcap)

Di challenge ini diberikan file pcap/pcapng bernama break, setelah kita membuka filenya dengan wireshark, maka muncul banyak package yang ada.


- DOKUMENTASI:
![WhatsApp Image 2024-09-18 at 20 59 46_35a90d67](https://github.com/user-attachments/assets/17bb26ae-d60b-4e97-868d-249bfb524650)

karena diberikan pertanyaaan mengenai IP address korbannya kita melihat dari packagenya langsung

![image](https://github.com/user-attachments/assets/6b2e519b-4bd7-4678-bda4-836ee704a2d0)

Setelah itu, diberikan pertanyaan terkait port dan endpoint(yg ditanyakan dengan format /endpoint/path.php

![WhatsApp Image 2024-09-19 at 00 01 57_6b14430f](https://github.com/user-attachments/assets/32f6f486-4257-4e2f-9ec6-b7d8f3258ac1)

Endpoint bisa dilihat dengan follow tcp stream pada salah satu package 
![Username Paswd](https://github.com/user-attachments/assets/9c0e9539-c804-4377-a9ac-5ef3b4ec4bb6)

Username dan passwd bisa dilihat juga
![WhatsApp Image 2024-09-19 at 00 02 41_d0269ba7](https://github.com/user-attachments/assets/2c6feec5-45e5-4f69-b029-3f4341e6f4d4)

Tools yang digunakan juga sudah terpampang dengan menginputnya dengan format singkat, yaitu ffuf-v2.1.0-deb
![Toolsnya](https://github.com/user-attachments/assets/0c1cd168-3836-4fbc-abfd-43d1fc61d306)

akhirnya, mendapatkan flagnya

![WhatsApp Image 2024-09-18 at 20 54 23_cd6f8643](https://github.com/user-attachments/assets/5ae06938-554d-4f39-b7bc-86329f5216d7)

- Flag: JarkomIT{d34th_fr0m_th3_sky_UYeAVgZYgYoKcPKU8JVO2FIbrH1W3pgPc7F6BKOCCE32Q3wBc3JPWW1}

## Corporate Breach (nc 10.15.42.60 51000 // breach.pcap)
Gunakan command nc pada terminal, yang akan me-reveal pertanyaan sebagai berikut:
```
Siapa nama attacker?
Format: string
```
Dengan follow tcp stream beberapa kali, saya temukan kalimat berikut:
![user nakhimov](https://github.com/user-attachments/assets/94235d5a-8816-4c99-9fd4-becf38673fb9)
Dengan asumsi bahwa "Nakhimov" ini attackernya, maka dimasukkan ke dalam terminal. Selanjutnya, ada pertanyaan baru:
```
Apa email yang digunakan untuk login?
Format: email@gmail.com
```
Dari sekian banyak login attempt yang Nakhimov lakukan, saya memilih email dan password yang ini karena tidak ada kata-kata "login attempt failed" dan semacamnya, yang memberikan indikasi bahwa login attempt yang dibawah ini itu  benar:
![email](https://github.com/user-attachments/assets/72f5a512-2a7d-40e0-b71e-fd349d94a7f4)
Setelah email kita diminta memasukkan password, maka ditulislah password diatas, j4rk0mg4c0rbg :
```
Apa password yang digunakan untuk login?
Format: string
```
Lalu muncullah flag:
```
Benar! Ini flag-mu: JarkomIT{supp0rt_k0k_l3m4h_bg_f68jgtOBxq5UC4uueQ6u1LDQrG6i5sYwhURcm3VbaGde8oo9ZYlsG6}
```

- Dokumentasi Terminal:

![corporate](https://github.com/user-attachments/assets/2657884c-66b6-46e1-a3e9-c88b0c1a705c)

- Flag: JarkomIT{supp0rt_k0k_l3m4h_bg_f68jgtOBxq5UC4uueQ6u1LDQrG6i5sYwhURcm3VbaGde8oo9ZYlsG6}

## Surprise (nc 10.15.42.60 48500 // ftplogin.pcap)
Saya masukkan nc kedalam terminal seperti sebelum-sebelumnya, lalu muncul pertanyaamn:
```
Apa service yang digunakan pada FTP server?
Format: service ver 
ex. proFTPd 1.1.0
```
Dari sini, saya follow tcp stream lagi sehingga muncul berikut:
![Screenshot (249)](https://github.com/user-attachments/assets/7db1565d-9929-4e26-9285-381d3654da2e)
Karena yang diminta adalah service ver yang berakhiran dengan versinya (seperti 1.1.0), saya berpikir mungkin yang dikotaki adalah jawabannya, yang ternyata benar.
Muncullah soal kedua:
```
Apa nama file yang dikirim oleh attacker?
Format: filename.extension
```
Dari sini dalam tcp stream yang sama, kita scroll kebawah dan ditemukanlah sebuah file cpp, yaitu file c++. Kita masukkan sebagai jawaban, dan ternyata benar juga. Muncullah soal selanjutnya:
```
Apa pesan rahasia yang ditinggalkan oleh attacker?
Format: string ex. h4lo wor1d
```
Dari sini, saya coba follow ke stream selanjutnya yang membawa kita ke sebuah program c++. Kita coba jalankan, dan gunakan hasilnya sebagai jawaban.
![sebelum gotchu](https://github.com/user-attachments/assets/5a34106c-1878-4175-82be-cb8cc81b0e7a)
Hasil compile:
![gotchu now](https://github.com/user-attachments/assets/27174847-ba23-4d10-9c19-dcdea6d95907)
Lalu dapatlah Flagnya:
```
Benar! Ini flag-mu: JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_xu3chlvqPnrqxqoH6crAojzgpG06uLkbVQe3IvH1sf306gANQPSNTCHU}  
```

- Dokumentasi Terminal:

![surprise](https://github.com/user-attachments/assets/9029b6d2-17eb-4b3b-9b7f-6a2fa7e3f522)
- Flag: JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_xu3chlvqPnrqxqoH6crAojzgpG06uLkbVQe3IvH1sf306gANQPSNTCHU}  
 
# FTP Login (nc 10.15.42.60 49000 // ftplogin.pcap)
Masukkan nc kedalam terminal yang akan membuat pertanyaan berikut muncul:
```
Apa username yang berhasil digunakan untuk FTP login?
Format: username
```
Kita cek tcp streamnya lagi, sehingga muncullah jawabannya. Mengapa saya memilih ini? karena di dalam attempt yang lain, semuanya incorrect kecuali sebagai berikut.
![user sneaky](https://github.com/user-attachments/assets/7311bc01-f613-4cdc-a776-f78d0c2454ff)
```
Apa password yang berhasil digunakan untuk FTP login?
Format: string
```
Untuk jawaban sudah ada pada gambar sebelumnya. Selanjutnya kita dapat flag:
```
Benar! Ini flag-mu: JarkomIT{n0t_s0_s3cur3_ftp_QknRz3qFMAI37nKe2kVbygytUL0V0cSmTlid2a6IlaVIROPNATdEG1N} 
```

- Dokumentasi Terminal:
  
 ![2](https://github.com/user-attachments/assets/28d155e1-b3ee-4720-8169-a937114e5afd)

- Flag: JarkomIT{n0t_s0_s3cur3_ftp_QknRz3qFMAI37nKe2kVbygytUL0V0cSmTlid2a6IlaVIROPNATdEG1N}


---
# Revisi
---
## Baby Hengker (nc 10.15.42.60 55000)
Challanges dari baby hengker, lebih mengarah ke analysis HID keyboard dari hasil ekstraksi paket tertentu yang sudah di filter agar lebih tepat lagi.

Pertama kita buka
```
nc 10.15.42.60 55000
```

Setelah itu, muncul pertanyaan yaitu, terkait waktu :
![pertanyaan pertama](https://github.com/user-attachments/assets/ce10c908-8b9b-40d9-be87-0a1b296bda6b)

Jawabannya cukup simpel, karena bisa dilihat dari salah satu paket yang ada, bila salah memasukkan jawaban, tinggal masukkan beberapa jawaban hingga ketemu (karena paketnya hanya sedikit).
Setelah tahu waktunya, sekarang mencari kata kata yang diketik oleh penyerang. Bagaimana cara mengetahuinya?

Pertama lihat dengan seksama seluruh informasi data yang ada di paketnya, di case ini kita menemukan HID Data
![ada HID Data di salah satu paket](https://github.com/user-attachments/assets/68a2a407-e669-45a4-9473-18e0b1ca2396)
Dalam paketnya lainnya juga ada, maka dari itu bisa diasumsikan bahwa HID data ini perlu didecode agar menjadi text yang setidaknya bisa dibaca.

HID(Human Interface Device), secara sederhana adalah alat agar manusia bisa memberikan input ke komputer semacam mouse, keyboard, game controller,dll sehingga komputer bisa menerima input dari alat-alat tadi untuk menjelankan sesuatu. Dalam case ini ada HID data berupa seperti ini [0x02, 0x00, 0x04, 0x00, 0x00, 0x00, 0x00, 0x00], yang mana ini merupakan HID data dari keyboard USB.
untuk lengkapnya bisa melihat referensi ini:

[https://usb.org/sites/default/files/documents/hut1_12v2.pdf]
[https://learn.microsoft.com/id-id/windows-hardware/drivers/hid/]

Melihat itu, kami berencana untuk memfilter beberapa paket agar proses decodenya sempurna dari

```
Sorce 1.2.1 ke host, tapi dengan keterangan info hanya URB_interrupt
```

Karena kalau semisal memilih paket host ke 1.2.1 hasil decodenya tidak ada (saya sudah mencoba) 
![Filter 1 21  ke host, lalu select](https://github.com/user-attachments/assets/6ed85ca5-da4e-4bc2-9b15-7c93221b6251)

sebelum itu, kita juga bisa membuat filter dengan cepat 1.2.1 ke host, bisa dengan :
![kalau mau cepet filter package khusus](https://github.com/user-attachments/assets/f2fbb88e-3e8c-450c-9c11-e7fb7bd18406)

biar bisa otomatis ke filter secara spesifik, lanjut untuk exportfile dengan seperti ini :
![exportfilenya](https://github.com/user-attachments/assets/c02c27ed-d38f-4080-8c4b-4411e9b6a0e2)

Setelah kita melakukan exportfile berupa pcap, kita fokus untuk decode dalam filenya dengan bantuan beberapa source github seperti :
https://gist.github.com/not-inept/3219ca6e56d62594c1be9e6f0c6067af
ataupun penjelasannya singkatnya disini :
https://github.com/TeamRocketIst/ctf-usb-keyboard-parser?tab=readme-ov-file

setelah melakukan git clone ke github tersebut, kita tinggal memproses file pcap hasil export dengan tshark command dari githubnya sendiri, dengan command :

```
tshark -r ./(namafilemu).pcap -Y 'usb.capdata && usb.data_len == 8' -T fields -e usb.capdata > (contohnamafile.txt)
```

agar hasil decode HID data bisa lebih bisa terlihat seperti ini:
![HasilexportfilePCAP](https://github.com/user-attachments/assets/59a7b65f-70d2-4583-9351-3d0d1695b744)

setelah itu jalankan python dengan syntax yang sudah ada dari githunya sendiri [disini](https://github.com/TeamRocketIst/ctf-usb-keyboard-parser/blob/master/usbkeyboard.py) untuk membuat hasil file TXT bisa terbaca:
![Decode file txtnya](https://github.com/user-attachments/assets/33cafe0d-aa14-41f4-a380-1c5ca15b1723)

Note : saya menggunakan syntax python berbeda namun tetap hasilnya bisa sama, karena dari device saya sendiri ada kesalahan syantaxnya sehingga perlu saya perbaiki ulang file pythonya agar bisa melakukan decodenya. Maka dari itu, nama filenya [decodefilebaru.py](https://github.com/Benyaminsan/Jarkom-1-IT06-2024/blob/main/filedecodebaru.py)

setelah mengethaui kata-kata yang diketik, kita tinggal masukkan ke pertanyaan tadi:
![Jawabannya salah](https://github.com/user-attachments/assets/86435487-f34c-44fa-8e13-93c068b59016)

Namun, jawabannya salah sehingga membuat saya terus mengetik jawaban yang kemungkinan mendekati maksudnya: 
![Ketemu flagnya](https://github.com/user-attachments/assets/4473bdcd-40b6-455a-bb1d-332d5d1dc5fe)

Akhirnya, ketemu flagnya


 





