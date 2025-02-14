# Laprak3 jarkom_M.Daffa-al-haq.s_028_TK4B
Nama : M.Daffa' al haq.s <br>
NIM  : 09030282327028 <br>
Kelas: TK4B <br>

**judul praktikum : analisis trafik jaringan (HTTP,DNS,PING) (IPv4)** <hr>

langkah-langkah percobaan : <br>
  1. pastikan laptop terhubung ke jaringan internet <br>
  
  2. cek alamat ip website yang ingin digunakan, menggunakan cmd contoh "ping yad.com" <br>
     <img src="https://github.com/user-attachments/assets/feec2a28-558e-49b4-bd43-9d5b596104ce" alt="Image" width="300"> <br>
     
  3. buka aplikasi wireshark, lalu pilih interface yang terhubung ke internet <br>
     <img src="https://github.com/user-attachments/assets/04c0cac8-1097-4da1-81d9-2b54fbfa3225" alt="Image" width="400"> <br>

  4. jalankan wireshark, lalu buka browsing dan masuk ke website yang ingin digunakan lalu mainkan dan tunggu sekitar 5 menit <br>
     <img src="https://github.com/user-attachments/assets/00318310-ebaa-4368-856e-fb59bb7c9187" alt="Image" width="400"> <br>
    
  5. setelah 5 menit an membuka website dan memainkannya buka wireshark kembali lalu stop capturing packet <br>
     <img src="https://github.com/user-attachments/assets/d7a383ec-5b01-4ff6-9c28-a0b9b59e077c" alt="Image" width="400"> <br>
  
  6. lalu cek ip website yang digunakan apakah ke detect atau tidak dengan cara ip.dst==104.18.29.238 jika ada maka website berhasil ke detect <br>
     <img src="https://github.com/user-attachments/assets/81528b2c-446a-454a-81aa-83f39ea34b8e" alt="Image" width="400"> <br>

  7. selanjutnya lihat properties dari hasil packet capture dengan menekan statistik > capture file properties, atau bisa dengan kombinasi Ctrl+Alt+Shift+C <br>
     <img src="https://github.com/user-attachments/assets/f907013c-34a9-421a-9e73-40036ba4b99b" alt="Image" width="400"> <br>

  8. dari statistic yang telah dibuka kita dapat melakukan perhitungan througput, packet loss, delay, dan jitternya <br>
     <img src="https://github.com/user-attachments/assets/9de6903c-ae4b-4157-bfef-17d384b9a3c8" alt="Image" width="400"> <br>

  9. hitung througput, packet loss, delay, dan jitter <br>
     - througput :
       jumlah byte : time span = hasil byte x 8 <br>
       46006141 : 455.996 = 100,8915451012728182 x 8 = 807 K <br>
       kategori sedang dan indeks nya 2 <br>

     - packet loss :
       ((packet data dikirim - packet data yang diterima)/packet data yang di kirim) x 100 <br>
       ((42706 - 42306)/42706)x100 = (400 : 42706) x 100 = 0,9% <br>
       kategori sangat bagus dan indeks nya 4 <br>

       untuk menghitung delay dan jitter kita memerlukan excel, sebelumnya kita save dulu filenya dengan format csv <br>
       <img src="https://github.com/user-attachments/assets/f4882b4f-d31b-488d-bbef-97a3f147315d" alt="Image" width="400"> <br>

     - untuk mencari delay : <br>
       <img src="https://github.com/user-attachments/assets/18c4f844-264a-4ea6-8514-3d731a0bc510" alt="Image" width="400"> <br>
       delay : <br>
       total delay : 455.99591426000000000000 s <br>
       rata-rata delay : 0.01067756086404720000 s x 1000 = 10.67756086404720000000 ms <br>
       kategori sangat bagus dan indeks nya 4 <br>

     - untuk mencari jitter : <br>
       <img src="https://github.com/user-attachments/assets/b043491e-f615-49af-9f2f-7ca6180dda76" alt="Image" width="400"> <br>
       jitter :
       total jitter : -0.23852247799999300000 s <br>
       rata-rata jitter : -0.00000558522170186843 s x 1000 = -0.00558522170186843000 ms <br>
       kategori sangat bagus dan indeks nya 4 <br>

