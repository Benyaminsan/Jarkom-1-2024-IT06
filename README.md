# Jarkom-1-2024-IT06
## Anggota kelompok
   ### Benjamin Khawarizmi Habibi 5027231078
   ### Callista Meyra Azizah 5027231060



# Write Up
## Advance Sanity Check (nc 10.15.42.60 44000)

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
Terdapat string "penword" didalamnya, maka saya masukkan lagi ke dalam terminal.

- Flag: JarkomIT{8uK4n_S4n1ty_b1a5A_Skz1qBYkSg6XUK9sUQAuwmVghSu551rKRBiPzcAzDvkVFcVam8lteIKK}


- Dokumentasi:
![1](https://github.com/user-attachments/assets/d2bf179a-ed55-4ac7-8b7b-30ac78f38e70)

## Pegawai Negeri Sebelah (nc 10.15.42.60 53000)

```
=====  Pegawai Negeri Sebelah =====
Note: You can exit anytime by typing 'exit'

Siapa yang memiliki password nNnM%coQuF?
Format: String
> Vero Tampubolon
Apa jabatan dari Taufan Kuswandari?
Format: String
> Analis Kebijakan
Siapa yang paling awal di list?
Format: String
> Cici Mustofa
Apa password paling akhir dari list?
Format: String
> RyxaJPv^yF
Benar! Ini flag-mu: JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_d4EjysuhNbOdCX7LoT4Z9gnSaL337FHGQYe5n3ieKFehKMpDry7cM4h}
```

- DOKUMENTASI:
![image](https://github.com/user-attachments/assets/6680c49f-0906-48b1-964b-629274f7c143)

![image](https://github.com/user-attachments/assets/afe69c1a-71a1-4002-99ab-19295815338e)

![image](https://github.com/user-attachments/assets/fb75ccaa-634c-4964-a332-9edfa821b405)

![image](https://github.com/user-attachments/assets/daa8108c-6bb8-49f6-b9a0-8d6d7305cd6c)
- Flag: JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_d4EjysuhNbOdCX7LoT4Z9gnSaL337FHGQYe5n3ieKFehKMpDry7cM4h}

## EZ (nc 10.15.42.60 54000)

```
===== EZ =====
Note: You can exit anytime by typing 'exit'

Temukan jawaban dari log tersebut
Format: string ex. kata kata
> jawabannya jawaban
Port berapa yang digunakan service tersebut
Format: xxxx: ex. 443
> 1234
Benar! Ini flag-mu: JarkomIT{BiAr_aman_Pake_sSh_6kgAozQUg7KBsvScORpWgISPs3zepqu7yIJd9bjAg6alxXZeTwbeEZ}
```                
```
halo mas wkwkw
pesan: submitini ke nc
eh yg atas salah
ini yang bener
pesan: "jawabannya jawaban"
itu ya yg disubmit yang ada e.petiknya
```
- DOKUMENTASI:
![WhatsApp Image 2024-09-18 at 20 42 02_c1e2efa4](https://github.com/user-attachments/assets/422a7539-8357-419b-bb4a-f70417a01751)

![WhatsApp Image 2024-09-18 at 20 40 04_1be7cca8](https://github.com/user-attachments/assets/8507152b-8e12-4da8-9807-06dc43392a55)

- Flag: JarkomIT{BiAr_aman_Pake_sSh_6kgAozQUg7KBsvScORpWgISPs3zepqu7yIJd9bjAg6alxXZeTwbeEZ}

## Illegal Breakthrough (nc 10.15.42.60 46000)

Di challanges ini diberikan file pcap/pcapng bernama break, setelah kita membuka filenya dengan wireshark, maka muncul banyak package yang ada.


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

## Corporate Breach (nc 10.15.42.60 51000)

```
Siapa nama attacker?
Format: string
> Nakhimov
Apa email yang digunakan untuk login?
Format: email@gmail.com
> jarkomsupport@gmail.com
Apa password yang digunakan untuk login?
Format: string
> j4rk0mg4c0rbg
```
- DOKUMENTASI:
![image](https://github.com/user-attachments/assets/94f5c2a0-48d7-4120-bc2a-298d57fe1249)

- Flag: JarkomIT{supp0rt_k0k_l3m4h_bg_caT1X51I2UoFwpZcw5fVTAUm8G6zDwNEsM4UwCMMTMrx4EXaNPEpG6}

## Surprise (nc 10.15.42.60 48500)

```
===== Surprise =====
Note: You can exit anytime by typing 'exit'

Apa service yang digunakan pada FTP server?
Format: service ver 
ex. proFTPd 1.1.0
> FTPd 3.0.3
Jawaban salah

Apa service yang digunakan pada FTP server?
Format: service ver 
ex. proFTPd 1.1.0
> vsFTPd 3.0.3

Apa nama file yang dikirim oleh attacker?
Format: filename.extension
> Jawaban salah

Apa nama file yang dikirim oleh attacker?
Format: filename.extension
> g0tcha.cpp
Apa pesan rahasia yang ditinggalkan oleh attacker?
Format: string ex. h4lo wor1d
> g0tchu n0w l1ttl3 m0us3
Benar! Ini flag-mu: JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_lUhvSdRHEPjx2SGkhL3AT4DiNG0xdtHFNq9LVBDvec7aLxCwkA9qTCHU}
```

- DOKUMENTASI:
![image](https://github.com/user-attachments/assets/0b8c7787-9b83-4404-ab24-60aa08f13eb7)

![WhatsApp Image 2024-09-18 at 21 19 39_f3aa4818](https://github.com/user-attachments/assets/8a8073cc-42e8-422c-9c5c-7391e31e5c7a)

```
220 (vsFTPd 3.0.3)

OPTS UTF8 ON

200 Always in UTF8 mode.

USER orange

331 Please specify the password.

PASS heather

530 Login incorrect.

USER nicole

331 Please specify the password.

PASS ginger

530 Login incorrect.

USER sn34ky

331 Please specify the password.

PASS sup3rsn1ff3r

230 Login successful.

PORT 172,21,80,1,253,130

200 PORT command successful. Consider using PASV.

STOR g0tcha.cpp

150 Ok to send data.
226 Transfer complete.

QUIT

221 Goodbye.
```
- DOKUMENTASI:
![WhatsApp Image 2024-09-18 at 20 38 22_facd4268](https://github.com/user-attachments/assets/d93c2b03-8913-495e-8254-1fc42d8041b4)

![WhatsApp Image 2024-09-18 at 21 18 51_201ac555](https://github.com/user-attachments/assets/f0eb0faa-e830-46cc-b374-04901745cebc)

- Flag: JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_lUhvSdRHEPjx2SGkhL3AT4DiNG0xdtHFNq9LVBDvec7aLxCwkA9qTCHU}

# FTP Login (nc 10.15.42.60 49000)

```
===== FTP Login =====
Note: You can exit anytime by typing 'exit'

Apa username yang berhasil digunakan untuk FTP login?
Format: username
> sn34ky
Apa password yang berhasil digunakan untuk FTP login?
Format: string
> sup3rsn1ff3r
Benar! Ini flag-mu: JarkomIT{n0t_s0_s3cur3_ftp_3ZvMs3ZibbtrySJYxKgvG72wyL0ig3hhssiawM0R2OlrquvDwBDLG1N}
```

```
USER sn34ky

331 Please specify the password.

PASS sup3rsn1ff3r

230 Login successful.

PORT 172,21,80,1,253,130

200 PORT command successful. Consider using PASV.
```
- DOKUMENTASI:
![image](https://github.com/user-attachments/assets/89e0afff-5d9e-41f4-a604-211374434269)

- Flag: JarkomIT{n0t_s0_s3cur3_ftp_3ZvMs3ZibbtrySJYxKgvG72wyL0ig3hhssiawM0R2OlrquvDwBDLG1N}
