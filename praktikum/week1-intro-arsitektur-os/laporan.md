
# Laporan Praktikum Minggu [X]
Topik: [Tuliskan judul topik, misalnya "Arsitektur Sistem Operasi dan Kernel"]

---

## Identitas
- **Nama**  : [Nama Mahasiswa]  
- **NIM**   : [NIM Mahasiswa]  
- **Kelas** : [Kelas]

---

## Tujuan
Tuliskan tujuan praktikum minggu ini.  
Contoh:  
> Mahasiswa mampu menjelaskan fungsi utama sistem operasi dan peran kernel serta system call.

---

## Dasar Teori
Tuliskan ringkasan teori (3–5 poin) yang mendasari percobaan.

---

## Langkah Praktikum
1. Langkah-langkah yang dilakukan.  
2. Perintah yang dijalankan.  
3. File dan kode yang dibuat.  
4. Commit message yang digunakan.

---

## Kode / Perintah
Tuliskan potongan kode atau perintah utama:
```bash
uname -a
lsmod | head
dmesg | head
```

---

## Hasil Eksekusi
Sertakan screenshot hasil percobaan atau diagram:
![Screenshot hasil](screenshots/example.png)

---

## Analisis
- Jelaskan makna hasil percobaan.  
- Hubungkan hasil dengan teori (fungsi kernel, system call, arsitektur OS).  
- Apa perbedaan hasil di lingkungan OS berbeda (Linux vs Windows)?  

---

## Kesimpulan
Tuliskan 2–3 poin kesimpulan dari praktikum ini.


## Tugas
a. Monolithic Kernel
Monolithic kernel adalah arsitektur sistem operasi yang di mana seluruh komponen inti OS — seperti manajemen memori, sistem file, manajemen proses, serta device driver — dijalankan dalam satu ruang kernel (kernel space). Semua bagian sistem inti memiliki akses langsung ke perangkat keras dan dapat berinteraksi tanpa batasan yang ketat.
Kelebihan: Kinerja tinggi karena tidak ada overhead komunikasi antarproses; interaksi langsung membuat operasi sistem berjalan cepat.
Kekurangan: Kompleksitas tinggi dan rentan terhadap crash — jika satu komponen gagal, seluruh sistem bisa ikut terganggu. Selain itu, debugging sulit karena semua kode berjalan dalam satu ruang alamat.

b. Microkernel
Microkernel berusaha meminimalkan ukuran kernel dengan hanya menempatkan fungsi inti yang paling dasar, seperti manajemen komunikasi antarproses (IPC), manajemen memori dasar, dan penjadwalan. Komponen lain, seperti device driver, sistem file, dan manajemen jaringan, dijalankan di ruang pengguna (user space) sebagai proses terpisah.
Kelebihan: Stabilitas dan keamanan lebih tinggi, karena kegagalan pada satu layanan tidak memengaruhi kernel secara keseluruhan; juga lebih mudah untuk dikembangkan dan dipelihara.
Kekurangan: Kinerja lebih rendah dibandingkan monolithic kernel karena adanya overhead komunikasi antarproses (IPC) antara kernel dan layanan di user space.


c. Layered Architecture
Pada arsitektur berlapis, sistem operasi dibangun dalam beberapa lapisan hierarkis. Setiap lapisan memiliki fungsi tertentu dan hanya berinteraksi dengan lapisan di atas dan di bawahnya. Lapisan paling bawah berinteraksi langsung dengan perangkat keras, sementara lapisan paling atas berinteraksi dengan pengguna.
Kelebihan: Struktur yang jelas, modularitas tinggi, serta kemudahan debugging dan pengembangan — karena setiap lapisan dapat diuji secara independen.
Kekurangan: Overhead komunikasi antar-lapisan bisa memperlambat sistem; sulit menentukan batas fungsi yang tepat antar-lapisan.


---

## Quiz
1. [Pertanyaan 1]
   .Sebutkan tiga fungsi utama sistem operasi.
   **Jawaban:**
   Tiga fungsi utama sistem operasi adalah:
1.	Manajemen Sumber Daya 
   Sistem Operasi mengelola semua sumber daya komputer seperti CPU, memori, perangkat penyimpanan, dan perangkat input/output. Tujuannya agar setiap proses atau aplikasi mendapat jatah sumber daya secara efisien tanpa saling mengganggu.
2.	Manajemen File dan Sistem I/O
   Sistem Operasi bertanggung jawab atas penyimpanan, pengambilan, dan pengorganisasian data dalam bentuk file di media penyimpanan (seperti hard disk atau SSD). Selain itu, OS menyediakan mekanisme untuk berkomunikasi dengan perangkat input/output (keyboard, mouse, layar, dll.).
	3.	Manajemen Proses dan Pengguna (Process & User Management)
  Sistem Operasi mengatur eksekusi program (proses), mulai dari pembuatan, penjadwalan, hingga penghentian proses. Selain itu, OS juga menangani interaksi antara pengguna dan sistem melalui antarmuka seperti CLI atau GUI, serta mengelola hak akses dan keamanan pengguna.
3. [Pertanyaan 2]
   •Jelaskan perbedaan antara kernel mode dan user mode.
   Jawaban:
   Kernel mode digunakan oleh sistem operasi untuk menjalankan tugas-tugas penting dengan hak penuh, sedangkan user mode digunakan oleh aplikasi pengguna dengan hak terbatas untuk menjaga keamanan dan stabilitas sistem.
5. [Pertanyaan 3]
   •Sebutkan contoh OS dengan arsitektur monolithic dan microkernel
   Jawaban:
Contoh OS dengan monolithic kernel:
	•	Linux → Kernel Linux bersifat monolitik walaupun mendukung modul dinamis (loadable kernel modules).
	•	Unix → Sistem seperti FreeBSD, OpenBSD, dan Solaris (versi awal) menggunakan arsitektur kernel monolitik.
	•	MS-DOS → Sistem operasi lama ini sangat sederhana dan berjalan sepenuhnya dalam satu ruang eksekusi tanpa pemisahan mode.
Contoh OS dengan microkernel:
	•	MINIX → Dikembangkan oleh Andrew Tanenbaum sebagai contoh sistem dengan arsitektur microkernel murni.
	•	QNX → Digunakan di sistem industri dan otomotif, terkenal karena stabilitas dan keandalannya.
	•	GNU HURD → Proyek sistem operasi berbasis microkernel dari Free Software Foundation.
---

## Refleksi Diri
Tuliskan secara singkat:
- Apa bagian yang paling menantang minggu ini?  
- Bagaimana cara Anda mengatasinya?  

---

**Credit:**  
_Template laporan praktikum Sistem Operasi (SO-202501) – Universitas Putra Bangsa_
