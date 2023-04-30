LAPORAN RESMI

KONSEP JARINGAN


![](Aspose.Words.1685ee39-35a4-45e0-a942-10bbeb6fba2f.001.png)



|<p></p><p>Dr. Ferry Astika Saputra ST, M.Sc.</p>|
| :- |




Nama	: Dimas Fahrul Putra Arismanto

Kelas	: D4 Teknik Informatika - A

NRP	: 3121600005

1. **Identifikasi Kernel**

"uname -a" memberikan informasi lengkap tentang kernel dan sistem operasi Debian yang sedang berjalan pada suatu perangkat. Informasi yang ditampilkan meliputi:

- "Linux": Menunjukkan bahwa sistem operasi yang sedang berjalan adalah kernel Linux.
- Nama host: Nama dari sistem operasi Debian yang sedang berjalan.
- Versi kernel: Nomor versi dari kernel Linux yang digunakan oleh sistem operasi Debian.
- Tipe prosesor: Jenis prosesor yang digunakan oleh sistem operasi Debian, seperti "x86\_64" untuk prosesor Intel 64-bit.
- Sistem operasi: Nama sistem operasi yang digunakan, yaitu "GNU/Linux" dalam kasus Debian.
- Versi sistem operasi: Nomor versi dari sistem operasi Debian yang digunakan.

![](Aspose.Words.1685ee39-35a4-45e0-a942-10bbeb6fba2f.002.png)


1. **Identifikasi Directory Structure**

1. /bin:

Direktori /bin pada Debian berisi program bawaan (built-in) yang diperlukan untuk menjalankan sistem, seperti perintah bash, ls, cp, mv, dan sebagainya. Direktori ini berisi file executable (berisi kode yang dapat dijalankan) yang diperlukan untuk menjalankan fungsi-fungsi sistem dasar.

1. /sbin:

Direktori /sbin pada Debian berisi program sistem (system binaries) yang hanya bisa dijalankan oleh root atau administrator. Direktori ini berisi perintah-perintah untuk administrasi sistem, seperti ifconfig, iptables, dan sebagainya.

1. /home:

Direktori /home pada Debian adalah direktori home untuk pengguna (user) pada sistem. Setiap pengguna akan memiliki direktori /home/{nama\_pengguna} yang berisi file dan folder pribadi masing-masing pengguna.

1. /root:

Direktori /root pada Debian adalah direktori home untuk pengguna root atau administrator. Direktori ini digunakan untuk menyimpan file dan konfigurasi root atau administrator.

1. /usr: 

Direktori /usr pada Debian berisi program, library, dan file konfigurasi yang digunakan oleh pengguna dan sistem. Direktori ini dibagi menjadi beberapa sub-direktori, seperti /usr/bin, /usr/sbin, /usr/lib, dan sebagainya.

1. /var:

Direktori /var pada Debian berisi file dan direktori yang berubah secara dinamis saat sistem berjalan, seperti file log, file cache, dan file yang digunakan oleh aplikasi yang sedang berjalan.

1. /tmp: 

Direktori /tmp pada Debian adalah direktori yang digunakan untuk menyimpan file sementara. Direktori ini bersifat volatile, artinya isinya akan hilang setelah sistem di-restart.

1. /apt: 

Direktori /apt pada Debian adalah direktori yang digunakan untuk menyimpan file paket yang di-download oleh APT (Advanced Package Tool), yaitu sistem manajemen paket pada Debian.

1. /etc:

Direktori /etc pada Debian berisi file konfigurasi sistem dan aplikasi, seperti file konfigurasi jaringan, konfigurasi layanan sistem, dan konfigurasi program tertentu.

![](Aspose.Words.1685ee39-35a4-45e0-a942-10bbeb6fba2f.003.png)


1. **Identifikasi Perbedaan sudo dan su**

"su" (substitute user) adalah perintah untuk mengubah identitas pengguna saat ini menjadi pengguna superuser (root). Dalam hal ini, pengguna harus mengetahui kata sandi superuser untuk dapat memasukkannya ke dalam perintah. Sedangkan "sudo" (superuser do) adalah perintah yang memungkinkan pengguna untuk menjalankan perintah sebagai pengguna superuser tanpa harus masuk terlebih dahulu ke dalam akun superuser.

![](Aspose.Words.1685ee39-35a4-45e0-a942-10bbeb6fba2f.004.png)

1. **Identifikasi Jenis Repository**

![](Aspose.Words.1685ee39-35a4-45e0-a942-10bbeb6fba2f.005.png)

- **# deb cdrom: [Debian GNU/Linux 11.6.0 \_Bullseye\_ - Official amd64 NETINST 20221217-10:42]/ bullseye main**
- **#deb cdrom: [Debian GNU/Linux 11.6.0 \_Bullseye\_ - Official amd64 NETINST 20221217-10:42]/ bullseye main**

Baris pertama dan kedua dimulai dengan tanda pagar # dan tidak diaktifkan, yang menunjukkan bahwa sumber paket berasal dari CD-ROM Debian yang diinstal pada sistem. Kedua baris ini dapat diaktifkan jika pengguna ingin mengunduh paket dari CD-ROM.

- **deb http: //kebo.pens.ac.id/debian/ bullseye main**

Baris ketiga merupakan sumber paket utama untuk distribusi Debian Bullseye dari server kebo.pens.ac.id. Sumber paket utama ini berisi banyak paket utama yang diperlukan oleh sistem Debian.

- **deb-src http://kebo.pens.ac.id/debian/ bullseye main**
- **deb http://security.debian.org/debian-security bullseye-security main**

Baris keempat dan kelima merupakan sumber paket kode sumber (source code) dari paket yang terdapat pada sumber paket utama pada baris ketiga. Kedua sumber paket ini diperlukan jika pengguna ingin membangun (build) paket dari kode sumber.

- **deb http://security.debian.org/debian-security bullseye-security main**
- **deb-src http://security.debian.org/debian-security bullseye-security main**

Baris keenam dan kedelapan adalah sumber paket keamanan (security updates) untuk Debian Bullseye dari server security.debian.org. Sumber paket ini berisi pembaruan keamanan untuk menjaga sistem tetap aman dan stabil.

- deb http://kebo.pens.ac.id/debian/ bullseye-updates main
- deb-src http://kebo.pens.ac.id/debian/ bullseye-updates main

Baris kesembilan dan kesepuluh adalah sumber paket pembaruan (update) untuk Debian Bullseye dari server kebo.pens.ac.id. Sumber paket ini berisi pembaruan paket-paket yang telah dirilis sejak perilisan awal Debian Bullseye.





1. **Identifikasi Perintah apt**

Perintah apt (Advanced Package Tool) adalah salah satu perintah yang sangat berguna dalam mengelola paket pada sistem operasi Debian. Berikut adalah beberapa perintah apt yang umum digunakan:

- **apt update** : Perintah ini digunakan untuk mengupdate daftar paket yang tersedia pada sumber paket yang terdaftar dalam file konfigurasi /etc/apt/sources.list.
- **apt upgrade** : Perintah ini digunakan untuk melakukan pembaruan paket-paket yang telah terinstal pada sistem. Perintah ini akan men-download dan menginstall paket-paket yang telah diperbarui.
- **apt install** : Perintah ini digunakan untuk menginstal paket baru pada sistem. Contoh: apt install apache2 akan menginstal web server Apache.
- **apt remove** : Perintah ini digunakan untuk menghapus paket yang telah terinstal pada sistem. Contoh: apt remove apache2 akan menghapus paket Apache yang telah terinstal.
- **apt search** : Perintah ini digunakan untuk mencari paket yang sesuai dengan kata kunci yang diinputkan. Contoh: apt search web server akan menampilkan daftar paket-paket yang terkait dengan kata kunci "web server".
- **apt show** : Perintah ini digunakan untuk menampilkan informasi lengkap tentang sebuah paket. Contoh: apt show apache2 akan menampilkan informasi lengkap tentang paket Apache.
- **apt autoclean** : Perintah ini digunakan untuk membersihkan file-file cache paket yang tidak terpakai pada sistem.
- **apt autoremove** : Perintah ini digunakan untuk menghapus paket-paket yang tidak terpakai pada sistem, misalnya karena paket dependensi telah dihapus sebelumnya.
- **apt list** : Perintah ini digunakan untuk menampilkan daftar paket yang terinstal pada sistem.
