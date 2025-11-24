Sistem Peminjaman Sistem Peminjaman Alat Laboratorium Berbasis Web


Renaldi Muhammad Fauzi1,L.M.Hasrun2
Program Studi Sistem Informasi, Universitas Muhammadiyah Banten, Indonesia
renaldimfauzi3@gmail.com








Abstract (English)

The rapid advancement of technology has had a significant impact on the field of education, especially in laboratory management. Many laboratories still use manual methods in borrowing and returning equipment, which often leads to data inaccuracies and loss of equipment. Therefore, this study aims to design and develop a web-based Laboratory Equipment Borrowing System to facilitate students, lecturers, and laboratory staff in managing borrowing activities efficiently and accurately. The system was developed using the Waterfall method, consisting of several stages such as requirement analysis, system design, implementation, testing, and maintenance. The result of this research is a digital system that supports the process of borrowing, returning, verification, and reporting of laboratory equipment in a structured and integrated manner.
Keywords: Laboratory, Borrowing System, Waterfall, Information System




Abstrak (Indonesia)
Perkembangan teknologi yang pesat memberikan pengaruh besar di bidang pendidikan, khususnya pada pengelolaan laboratorium. Banyak laboratorium yang masih menggunakan metode manual dalam proses peminjaman dan pengembalian alat, sehingga sering terjadi ketidaktepatan data dan kehilangan alat. Oleh karena itu, penelitian ini bertujuan untuk merancang dan membangun sebuah Sistem Peminjaman Alat Laboratorium berbasis web yang dapat mempermudah mahasiswa, dosen, dan laboran dalam melakukan kegiatan peminjaman secara efisien dan akurat. Sistem ini dikembangkan menggunakan metode Waterfall yang terdiri dari beberapa tahapan, yaitu analisis kebutuhan, perancangan sistem, implementasi, pengujian, dan pemeliharaan. Hasil dari penelitian ini berupa sistem digital yang mampu mendukung proses peminjaman, pengembalian, verifikasi, serta pelaporan alat laboratorium secara terstruktur dan terintegrasi.
Kata Kunci: Laboratorium, Sistem Peminjaman, Waterfall, Sistem Informasi



Pendahuluan
        Laboratorium merupakan salah satu fasilitas penting dalam kegiatan praktikum di lingkungan pendidikan, terutama di perguruan tinggi. Ketersediaan alat laboratorium yang memadai dan terkelola dengan baik sangat berpengaruh terhadap kelancaran kegiatan praktikum mahasiswa. Namun, dalam praktiknya masih banyak laboratorium yang menerapkan sistem peminjaman alat secara manual, seperti pencatatan di buku atau formulir kertas. Proses tersebut sering menimbulkan berbagai kendala, antara lain kesulitan dalam melacak data alat yang sedang dipinjam, hilangnya catatan peminjaman, serta ketidakefisienan dalam proses verifikasi dan pengembalian alat.
Berdasarkan permasalahan tersebut, diperlukan sebuah sistem yang dapat membantu proses peminjaman dan pengembalian alat laboratorium secara lebih efektif dan efisien. Dengan adanya Sistem Peminjaman Alat Laboratorium Berbasis Web, proses administrasi dapat dilakukan secara terkomputerisasi, mulai dari pengajuan peminjaman, verifikasi oleh dosen atau laboran, hingga proses pengembalian alat. Sistem ini diharapkan dapat meminimalkan kesalahan pencatatan serta meningkatkan akurasi dan kecepatan pelayanan peminjaman alat.
1.Metode Penelitian 


Metode Penelitian 
Pendekatan yang digunakan dalam penelitian ini bersifat linear dengan metode Waterfall. Proses pengembangan dilakukan bertahap dan berurutan, sehingga setiap tahap baru dimulai setelah tahap sebelumnya selesai.
  
  

                                                            Gambar 1.Metode Waterfall 


Metode Waterfall menggambarkan proses pengembangan yang berlangsung secara berurutan seperti aliran air terjun, dari tahap awal hingga akhir. Model ini sesuai untuk pengembangan sistem berskala kecil dengan kompleksitas rendah, karena setiap tahapnya terdefinisi jelas dan saling berkaitan.








2.Analisis & Perancangan Sistem
        
A.Sistem Design 
  
![alt text](https://github.com/renld22/UTS-RPL/blob/main/USE%20CASE.png?raw=true)






  

                                            
                                       Gambar 3. Class diagram peminjaman alat lab






3.Implementation
 
  A.Creational Pattern
     
           Factory Method
           
![alt text](https://github.com/renld22/UTS-RPL/blob/main/factory%20method.png?raw=true)

  

             










         Builder
![alt text](https://github.com/renld22/UTS-RPL/blob/main/builder.png?raw=true)









     Singleton
  
![alt text](https://github.com/renld22/UTS-RPL/blob/main/singleton.png?raw=true)
























B.squence diagram


  



C,Activity diagram (mahasiswa)


  ![alt text](https://github.com/renld22/UTS-RPL/blob/main/Activity%20diagram%20mahasiswa.png?raw=true)

Activity diagram (laboran)

 ![alt text](https://github.com/renld22/UTS-RPL/blob/main/Acitivity%20diagram%20laboran.png
?raw=true)
  



                                                   Evaluasi dan kreasi

.State Machine Diagram


  







Evaluasi Kualitas Desain
Adapun evaluasi kualitas desain dari Sistem Peminjaman Alat Laboratorium yang telah dibuat, berdasarkan maintainability, reusability, dan scalability, adalah sebagai berikut:
• Maintainability: Baik
* Pemodelan Domain yang Jelas (Class Diagram)
Pemodelan kelas telah dipisah menjadi entitas yang kohesif seperti Mahasiswa, Petugas, Alat, dan Peminjaman.
Setiap kelas memiliki tanggung jawab jelas sehingga mempermudah pemeliharaan dan perubahan di masa mendatang.

* Penerapan Factory Method Pattern
Pola Factory digunakan untuk menangani proses pembuatan objek peminjaman secara terstandarisasi.
Pola ini memungkinkan penambahan jenis peminjaman baru tanpa harus mengubah kode inti.

* Penerapan Builder Pattern
Builder digunakan untuk membangun objek peminjaman secara bertahap (tanggal pinjam, tanggal kembali, mahasiswa, alat).
Hal ini mempermudah debugging dan memastikan objek terbentuk dengan data yang lengkap.

* State Machine Diagram
Diagram state machine memberikan representasi jelas terhadap lifecycle peminjaman seperti Menunggu, Disetujui, Dipinjam, hingga Dikembalikan.
Ini membantu menjaga konsistensi alur dalam sistem dan memudahkan maintenance.

* Activity Diagram yang Terstruktur
Activity untuk mahasiswa dan laboran dibuat terpisah sehingga mudah dibaca, dipelihara, dan diperbarui apabila prosedur operasional berubah.







• Reusability: Baik
   * Penerapan Single Responsibility Principle (SRP)
Setiap kelas memiliki satu tanggung jawab utama, misalnya:

      *  Mahasiswa: login dan permintaan peminjaman

      * Petugas: verifikasi peminjaman dan pengembalian

      * Alat: mengelola informasi ketersediaan

Peminjaman: mengatur transaksi peminjaman
Pemisahan ini memungkinkan fungsi-fungsi dalam kelas dapat digunakan kembali pada fitur lain.

         * Penggunaan Dependency Injection (DI)
Dependency Injection diterapkan pada service seperti PeminjamanService, AlatService, dan UserService.
DI memungkinkan modul diganti/diupgrade tanpa memodifikasi class utama, meningkatkan kemampuan reuse komponen.

         * Builder & Factory Bersifat Reusable
Builder untuk peminjaman serta Factory Method dapat digunakan kembali untuk berbagai jenis peminjaman atau workflow baru.

• Scalability: Baik
            * Struktur Sistem yang Modular
Setiap entitas berdiri sendiri dan saling terhubung melalui relasi yang jelas.
Hal ini memungkinkan sistem diperluas dengan mudah, misalnya dengan menambah fitur reminder, laporan bulanan, atau integrasi API.

            * Arsitektur yang Mudah Dikembangkan ke Layanan Terpisah
Dengan adanya Service Layer untuk peminjaman dan alat, sistem dapat diskalakan menjadi layanan REST API di masa depan.

            * Lifecycle Status yang Konsisten (State Machine)
Status yang terstruktur mencegah konflik data di saat banyak pengguna mengakses sistem secara bersamaan, sehingga mendukung skalabilitas jangka panjang.
Saran Improvement Fitur Baru
Membuat fitur untuk meningkatkan transparansi dan komunikasi antara Laboran dan Mahasiswa melalui Pemberitahuan Otomatis.
Sistem secara otomatis mengirimkan notifikasi (email/SMS/in-app) mengenai status pengajuan peminjaman, jadwal pengembalian alat, serta informasi ketersediaan alat laboratorium.
Adapun manfaatnya adalah sebagai berikut:
● Bagi Mahasiswa:
               * Meningkatkan Transparansi: Mahasiswa mendapat informasi status pengajuan peminjaman dan ketersediaan alat secara real-time.

               * Pengingat Pengembalian Alat: Notifikasi otomatis mengurangi risiko keterlambatan pengembalian.

               * Meningkatkan Kenyamanan: Mahasiswa tidak perlu menanyakan status peminjaman secara manual ke laboran.

● Bagi Laboran:
                  * Mengurangi Beban Pekerjaan: Mengotomatisasi pengingat dan status peminjaman mengurangi tugas manual laboran.

                  * Meningkatkan Efisiensi: Mempercepat proses verifikasi peminjaman dan pengembalian.

                  * Membangun Sistem yang Profesional: Alur peminjaman menjadi lebih tertib, terstruktur, dan responsif.
