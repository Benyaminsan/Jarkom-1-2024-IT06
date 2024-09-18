# Jarkom-1-2024-IT06
## Anggota kelompok
   ### Benjamin Khawarizmi Habibi 50272310__
   ### Callista Meyra Azizah 5027231060



# Write Up
## Advance Sanity Check (nc 10.15.42.60 44000)

```
===== Advanced Sanity Check =====
Note: You can exit anytime by typing 'exit'
Apa username pengirim?
Format: username
> JaneD03
Apa nama file yang dikirim?
Format: filename.extension
> Clue3.txt
Ikuti petunjuk untuk mendapatkan pesan rahasia
Format: string
> penword
Benar! Ini flag-mu: JarkomIT{8uK4n_S4n1ty_b1a5A_PZsva59iSBLGsLwPMcz5nvnQbSu576bmxnNYiYxCiUqBudYOAOmDDIKK}
```

```coba periksa peraturan soal shift, ada suprise - Jane Doe```

![WhatsApp Image 2024-09-18 at 18 43 56_fd9aded0](https://github.com/user-attachments/assets/c6fb06e7-4348-4119-a3ca-ce21bbbf374e)

```didapatkan cGVud29yZA== ```

![WhatsApp Image 2024-09-18 at 18 50 46_8090be62](https://github.com/user-attachments/assets/df2b2e48-f250-4be5-b4d6-c41ffa2a275b)

```dari decode didapatkan penword```
- Flag: JarkomIT{8uK4n_S4n1ty_b1a5A_PZsva59iSBLGsLwPMcz5nvnQbSu576bmxnNYiYxCiUqBudYOAOmDDIKK}

## Pegawai Negeri Sebelah (nc 10.15.42.60 53000)
- Flag: JarkomIT{Tum8eN_p45SnYa_Ku4t_B1aS4Nya_d4EjysuhNbOdCX7LoT4Z9gnSaL337FHGQYe5n3ieKFehKMpDry7cM4h}

## EZ (nc 10.15.42.60 54000)

![WhatsApp Image 2024-09-18 at 20 40 04_1be7cca8](https://github.com/user-attachments/assets/8507152b-8e12-4da8-9807-06dc43392a55)

```
halo mas wkwkw
pesan: submitini ke nc
eh yg atas salah
ini yang bener
pesan: "jawabannya jawaban"
itu ya yg disubmit yang ada e.petiknya
```

- Flag: JarkomIT{BiAr_aman_Pake_sSh_6kgAozQUg7KBsvScORpWgISPs3zepqu7yIJd9bjAg6alxXZeTwbeEZ}

## Illegal Breakthrough (nc 10.15.42.60 46000)

![WhatsApp Image 2024-09-18 at 20 59 46_35a90d67](https://github.com/user-attachments/assets/17bb26ae-d60b-4e97-868d-249bfb524650)

![WhatsApp Image 2024-09-18 at 20 54 23_cd6f8643](https://github.com/user-attachments/assets/5ae06938-554d-4f39-b7bc-86329f5216d7)

- Flag: JarkomIT{d34th_fr0m_th3_sky_UYeAVgZYgYoKcPKU8JVO2FIbrH1W3pgPc7F6BKOCCE32Q3wBc3JPWW1}

## Corporate Breach (nc 10.15.42.60 51000)

![image](https://github.com/user-attachments/assets/94f5c2a0-48d7-4120-bc2a-298d57fe1249)

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
- Flag: JarkomIT{supp0rt_k0k_l3m4h_bg_caT1X51I2UoFwpZcw5fVTAUm8G6zDwNEsM4UwCMMTMrx4EXaNPEpG6}

## Surprise (nc 10.15.42.60 48500)

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
![WhatsApp Image 2024-09-18 at 21 18 51_201ac555](https://github.com/user-attachments/assets/f0eb0faa-e830-46cc-b374-04901745cebc)

- Flag: JarkomIT{l1ttl3_m0us3_1n_th3_h0us3_lUhvSdRHEPjx2SGkhL3AT4DiNG0xdtHFNq9LVBDvec7aLxCwkA9qTCHU}

# FTP Login (nc 10.15.42.60 49000)

```
USER sn34ky

331 Please specify the password.

PASS sup3rsn1ff3r

230 Login successful.

PORT 172,21,80,1,253,130

200 PORT command successful. Consider using PASV.
```
- Flag: JarkomIT{n0t_s0_s3cur3_ftp_3ZvMs3ZibbtrySJYxKgvG72wyL0ig3hhssiawM0R2OlrquvDwBDLG1N}
