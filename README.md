# Jarkom_Modul1_Lapres_C04

### Kelompok C04
### Anggota :
#### Khofifah Nurlaela 	05111840000029
#### Yulia Niza		05111840000053
    
  - [Display Filter](#display-filter)
    - [Soal 1](#soal-1)
    - [Soal 2](#soal-2)
    - [Soal 3](#soal-3)
    - [Soal 4](#soal-4)
    - [Soal 5](#soal-5)
    - [Soal 6](#soal-6)
    - [Soal 7](#soal-7)
    - [Soal 8](#soal-8)
    - [Soal 9](#soal-9)
    - [Soal 10](#soal-10)
  - [Capture Filter](#capture-filter)
    - [Soal 11](#soal-11)
    - [Soal 12](#soal-12)
    - [Soal 13](#soal-13)
    - [Soal 14](#soal-14)
    - [Soal 15](#soal-15)



## Display Filter
### Soal 1 
**Sebutkan webserver yang digunakan pada "testing.mekanis.me"!**
- Masukkan display filter  ` http.host == testing.mekanis.me `  
- Lalu ` klik kanan-> follow-> http stream `
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture1.png?raw=true) 
- Disitu dapat dilihat bahwa servernya adalah `ngix/1.14.0 (Ubuntu)`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture2.png?raw=true) 


<br>


### Soal 2 
**Simpan gambar "Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg"!**
- Klik `file -> export object -> http` 
- Lalu pada kolom search masukkan `Tim_Kunjungan_Kerja_BAKN_DPR_RI_ke_Sukabumi141436.jpg`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture3.png?raw=true)
- Lalu klik `save` hasilnya seperti berikut
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture4.png?raw=true) 
<br>

### Soal 3 
**Cari username dan password ketika login di "ppid.dpr.go.id"!**
- Masukkan display filter `http.host contains "ppid.dpr.go.id" && http.request.method == POST`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture5.png?raw=true)
- Didapatkan hasil username : `10pemuda` dan password : `guncangdunia`
<br>

### Soal 4 
**Temukan paket dari web-web yang menggunakan basic authentication method!**
- Masukkan display filter `http.authbasic`
- Dapat dilihat daftar paket yang menggunakan basic authentication
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture6.png?raw=true)
<br>

### Soal 5 
**Ikuti perintah di aku.pengen.pw! Username dan password bisa didapatkan dari file .pcapng!**
- Masukkan display filter `http.host contains "aku.pengen.pw"`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture7.png?raw=true)
- Klik pada paket ketiga, lalu pada bagian `Hypertext Transfer Protocol-> Authorization` 
- Dapat dilihat username : `kakakgamtenk` dan password : `hartatahtabermuda`
- Setelah itu kita dapat membuka link "aku.pengen.pw" dan memasukkan jawaban berikut
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture8.png?raw=true)
<br>

### Soal 6 
**Seseorang menyimpan file zip melalui FTP dengan nama "Answer.zip". Simpan dan Buka file "Open This.pdf" di Answer.zip. Untuk mendapatkan password zipnya, temukan dalam file zipkey.txt (passwordnya adalah isi dari file txt tersebut).**
- Mencari file "Answer.zip" dengan masukkan display filter `ftp-data contains "Answer.zip"`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_6_1.PNG?raw=true)
- Simpan file dengan `klik kanan -> Follow -> TCP Stream`. Jangan lupa untuk mengubah `Show and save data as Raw`.
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_6_2.png?raw=true)
- Untuk mendapatkan password untuk membuka file "Answer.zip", cari file "zipkey.txt" dengan masukkan display filter `ftp-data contains "zipkey.txt"`

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_6_3.PNG?raw=true)
- Buka file dengan `klik kanan -> Follow -> TCP Stream`

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_6_4.PNG?raw=true)
- Buka file "Answer.zip".

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_6_5.png?raw=true)
- Buka file "Open This.pdf" dan masukan password yang telah didapat.

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_6_6.png?raw=true)
<br>


### Soal 7 
**Ada 500 file zip yang disimpan ke FTP Server dengan nama 1.zip, 2.zip, ..., 500.zip. Salah satunya berisi pdf yang berisi puisi. Simpan dan Buka file pdf tersebut. Your Super Mega Ultra Rare Hint = nama pdf-nya "Yes.pdf"**
- Mencari file "Yes.pdf" dengan masukkan display filter `tcp contains "Yes.pdf"`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_7_1.png?raw=true)
- Didapat paket folder zip yang di dalamnya terdapat file "Yes.pdf" yaitu "473.zip"
- Simpan file dengan `klik kanan -> Follow -> TCP Stream`. Jangan lupa untuk mengubah `Show and save data as Raw`.

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_7_2.png?raw=true)
- Buka file zip, kemudian buka file "Yes.pdf"

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_7_3.png?raw=true)
<br>


### Soal 8 
**Cari objek apa saja yang didownload (RETR) dari koneksi FTP dengan Microsoft FTP Service!**
- Masukkan display filter `ftp.request.command == RETR && ip.dst == 198.246.117.106`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_8.PNG?raw=true)
<br>

### Soal 9 
**Cari username dan password ketika login FTP pada localhost!**
- Untuk mendapatkan username, masukkan display filter `ftp.request.command == USER`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_9_2.PNG?raw=true)
- Didapat username `dhana`.
- Untuk mendapatkan password, masukkan display filter `ftp.request.command == PASS`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_9_1.PNG?raw=true)
- Didapat password untuk usernama `dhana` adalah `dhana123`.
<br>

### Soal 10 
**Cari file .pdf di wireshark lalu download dan buka file tersebut! clue: "25 50 44 46"** 
- Masukkan display filter `frame contains "application/pdf"` 
- Atau dapat juga dengan `frame contains 25:50:44:46` 
- Lalu `klik kanan-> follow -> TCP Stream`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture9.png?raw=true)
- Setelah itu ubah pada 'show and save data as' menjadi `Raw`
- Lalu klik `Save as`
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture10.png?raw=true)
- Diperolah hasil berupa file pdf berikut ini :
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture11.png?raw=true)

## Capture Filter
### Soal 11 
**Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!**
- Pilih `Adapter for loopback traffic capture`
- Lalu masukkan `port 21` pada capture filter
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture12.png?raw=true)
- Berikut ini adalah daftar paket yang maengandung port 21
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture13.png?raw=true)
  <br>

### Soal 12
**Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80!**
- Pilih `Wifi`
- Lalu masukkan `src port 80` pada capture filter
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture14.png?raw=true)
- Berikut adalah daftar paket yang berasal dari port 80 :
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Picture15.png?raw=true)
### Soal 13
**Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!**
- Pilih interface `Wifi` pada halaman utama Wireshark.
- Lalu masukkan `dst port 443` pada capture filter.
- Berikut adalah daftar paket yang menuju dari port 443 :
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_13.png?raw=true)
<br>

### Soal 14
**Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!**
- Untuk mendapatkan ip address sendiri, buka cmd kemudian ketik `ipconfig`
- Didapat ip address sendiri.

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_14_1.png?raw=true)
- Pilih interface `Wifi` pada halaman utama Wireshark.
- Lalu masukkan `src host  192.168.43.254` pada capture filter.
- Berikut adalah daftar paket yang berasal dari ip kita :
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_14_2.png?raw=true)
<br>

### Soal 15
**Filter sehingga wireshark hanya mengambil paket yang tujuannya ke monta.if.its.ac.id!**
- Dapat dicari dengan menggunakan ip dari monta.if.its.ac.id, buka cmd kemudian ketik `ping monta.if.its.ac.id`
- Didapat ip address dari monta.if.its.ac.id

  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_15_1.png?raw=true)
- Pilih interface `Wifi` pada halaman utama Wireshark.
- Lalu masukkan `dst host == 103.94.190.11` pada capture filter.
- Berikut adalah daftar paket yang menuju ke monta.if.its.ac.id :
  
  ![alt text](https://github.com/nizayulia/Jarkom_Modul1_Lapres_C04/blob/main/Assets/Capture_15_2.png?raw=true)
<br>


















