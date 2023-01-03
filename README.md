# JOBSHEET-1.1

JARINGAN SENSOR NIRKABEL MENGGUNAKAN ESP-NOW
TUJUAN

1) Mahasiswa dapat memahami konsep topologi jaringan sensor nirkabel berbasis ESPNOW.
2) Mahasiswa dapat melakukan konfigurasi berbagai topologi ESP-NOW.
3) Mahasiswa dapat menganalisis dan menentukan topologi ESP-NOW,sesuai dengan studi kasus proyek.

ALAT DAN BAHAN

1) ESP32
2) Breadboard
3) Kabel jumper
4) Resistor 10K Ohm

TEORI SINGKAT

ESP-NOW adalah protokol yang dikembangkan oleh Espressif, yang memungkinkan banyak perangkat untuk berkomunikasi satu sama lain tanpa menggunakan Wi-Fi. Protokol ini mirip dengan konektivitas nirkabel 2.4GHz berdaya rendah. Pendifinisian alamat (MAC Address) pada masing-masing ESP32 diperlukan pada awal konfigurasi. Setelah konfigurasi alamat selesai dilakukan, jaringan peer-to-peer akan terbentuk dan perangkat tidak perlu melakukan handshaking kembali ketika akan berkomunikasi. Hal ini memunjukkan bahwa setelah perangkat ESP32 saling terpasang satu sama lain, koneksi akan tetap ada. Dengan kata lain, jika tiba-tiba salah satu ESP32 kehilangan daya atau diatur ulang, ketika restart, secara otomatis akan terhubung ke pasangan ESP32 yang telah terdefinisi alamatnya untuk melanjutkan komunikasi.ESP-NOW mempunyai 2 tipe jaringan, yaitu One-Way Communication dan Two-Way Communication. One-Way Communication terbagi menjadi Point-to-Point, One-to-Many Communication dan Many-to-One Communication. Sementara Two-Way Communication terbagi menjadi Point-to-Point dan Mesh Communication.

A. Memperoleh MAC Address ESP32 Receiver

1.Ketikkan script program berikut di Arduino IDE Upload program tersebut ke ESP32.

2.Setelah program berhasil diupload, buka serial monitor Catat Mac Address ESP32.

B. ESP-NOW One-Way Point-to-Point Communication

1.Kemudian ketikkan script program berikut untuk mengkonfigurasi ESP32 sebagai sender.Isi array broadcastAddress [] dengan MAC Address ESP32 Receiver yang didapatkan pada praktikum poin A.Upload program pada ESP32 Sender.

2.Setelah ESP32 sender dikonfigurasi, kemudian konfigurasikan ESP32 yang lain sebagai Receiver. Ketikkan script program berikut untuk mengkonfigurasi ESP32 sebagai receiver.

3.Buatlah data dummy dengan ukuran yang terbaca oleh receiver ± 250 byte.Aturlah jarak awal komunikasi antara sender dan receiver yaitu 1 meter. Kemudian ubah 
jarak komunikasi dengan penambahan 1 meter. Data yang dikirim pada tiap iterasi pengujian adalah 10 data.Aturlah tinggi antena atau peletakan ESP32 pada ground level (menempel tanah), 30 cm di atas tanah, dan 1 meter di atas tanah.Masukkan hasil pengukuran pada kolom berikut dan buatlah analisisnya dengan pendekatan teori freshnel zone.

C. One-Way, One-to-Many Communication 

  a. Mengirim Pesan yang Sama Ke Beberapa Board ESP32
  
1.Ketik program berikut ini dan tambahkan semua Mac Address ESP32 Receiver pada bagian broadcastAddress[]. Upload program tersebut pada board ESP32 Sender

2.Siapkan board Receiver, kemudian ketik script berikut ini pada Arduino IDE. Upload program tersebut pada Receiver.

3.Matikan salah satu board Receiver, dokumentasikasikan hasilnya

4.Buatlah koneksi menggunakan semua board ESP32 yang ada dikelas, dengan menambahkan Receiver ke dalam jaringan secara bertahap,Dokumentasikan hasilnya.

  b. Mengirim Pesan yang Berbeda Ke Beberapa Board ESP32
  
 1.Buatlah program pada Sender agar dapat mengirim pesan yang berbeda pada 3 Receiver.
 
 D. One-Way, Many-to-One Communication 
 
 1.Unggah program untuk menemukan MAC Address pada board Receiver, kemudian catat MAC Address-nya.Ketikkan program berikut pada Arduino IDE untuk mengkonfigurasi board Sender.
 
 2.Siapkan board Receiver, ketikkan script berikut di Arduino IDE, kemudian upload program tersebut.Buka serial monitor dan dokumentasikan output program.

 E. Two-Way Communication
 
 1.Upload program berikut ini untuk melakukan pengecekan sensor DHT11. Dokumentasikan output program yang ditampilkan pada serial monitor Arduino IDE.
 
 2.Ketikkan script berikut, kemudian masukkan MAC Address receiver pada masing-masing board Buka serial monitor pada Arduino IDE, kemudian dokumentasikan outputnya.

