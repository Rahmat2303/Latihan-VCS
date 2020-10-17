# Latihan-VCS

Nama  :Rahmat
NIM   :312010229
Kelas :TI.20.A2

Tata cara atau tutorial menggunakan GIT

Apa itu Git?
• Git adalah salah satu sistem pengontrol versi (Version Control System) pada proyek perangkat lunak yang diciptakan oleh Linus Torvalds.
• Pengontrol versi bertugas mencatat setiap perubahan pada file proyek yang dikerjakan oleh banyak orang maupun sendiri. 
• Git dikenal juga dengan distributed revision control (VCS terdistribusi), artinya penyimpanan database Git tidak hanya berada dalam satu tempat saja.

Instalasi Git
• Download Git, buka website resminya Git (git-scm.com).
• Kemudian unduh Git sesuai dengan arsitektur komputer kita. Kalau menggunakan 64bit, unduh yang 64bit. Begitu juga kalau menggunakan 32bit.
• Selamat, Git sudah terinstal di Windows. Untuk mencobanya, silahkan buka CMD atau PowerShell, kemudian ketik perintah git --version.
![12](https://user-images.githubusercontent.com/72907744/96324594-c692cb00-104c-11eb-816b-600633af2c03.PNG)

Menambahkan Global Config
• Pada saat pertama kali menggunakan git, perlu dilakukan konfigurasi user.name dan user.email
• konfigurasi ini bisa dilakukan untuk global repostiry atau individual repository.
• apabila belum dilakukan konfigurasi, akan mengakibatkan terjadi kegagalan saat menjalankan perintah git commit
• Config Global Repository
$ git config --global user.name “nama_user”
$ git config --global user.email “nama_user”

Perintah Dasar Git
• git init, perintah untuk membuat repository local 
• git add, perintah untuk menambahkan file baru, atau perubahan pada file pada staging sebelum proses commit.
• git commit, perintah untuk menyimpan perubahan kedalam database git.
• git push -u origin master, perintah untuk mengirim perubahan pada repository local menuju server repository. 
• git clone [url], perintah untuk membuat working directory yang diambil dari repositry sever. 
• git remote add origin [url], perintah untuk menambahkan remote server/reopsitory server pada local repositry (working directory) 
• git pull, perintah untuk mengambil/mendownload perubahan terbaru dari server repository ke local repository 

Membuat Reposiory Local
• Buka direktory aktif, misal: d:\labs_pemrograman1 (buka menggunakan Windows Explorer)
• klik kanan pada direktory aktif tersebut, dan pilih menu Git Bash, sehingga muncul git bash commad
• Buat direktory project praktikum pertama dengan nama latihan1
$ mkdir latihan1
$ cd latihan1
• Sehingga terbentuk satu direktori baru dibawahnya, selanjutnya masuk kedalam direktori tersebut dengan perintah cd (change directory)
• direktory aktif menjadi: d:\labs_pemrograman1\latihan1

Membuat Reposiory Local
• Jalankan perintah git init, untuk membuat repository local.
$ git init
• Repository baru berhasil di inisialisasi, dengan terbentuknya satu direktori hidden dengan nama .git 
• Pada direktori tersebut, semua perubahan pada working directory akan disimpan. 

Menambahkan File baru pada repository
• Untuk membuat file dapat menggunakan text editor, lalu menyimpan filenya pada direktori aktif (repository)
• disini kita akan coba buat satu file bernama README.md (text file)
$ echo “# Latihan 1” >> README.md
• File README.md berhasil dibuat. 
![ss](https://user-images.githubusercontent.com/72907744/96324435-1624c700-104c-11eb-9586-8b2b93c52d8c.PNG)

Menambahkan File baru pada repository
• Untuk menambahkan file yang baru saja dibuat tersebut gunakan perintah git add.
$ git add README.md
• File README.md berhasil ditambahkan.
![Capture](https://user-images.githubusercontent.com/72907744/96324447-1f159880-104c-11eb-863e-11aafa164633.PNG)

Commit (Menyimpan perubahan ke database)
• Untuk menyimpan perubahan yang ada kedalam database repository local, gunakan perintah git commit -m “komentar commit”
$ git commit -m “File pertama saya”
• Perubahan berhasil disimpan. 
![commit](https://user-images.githubusercontent.com/72907744/96324762-939d0700-104d-11eb-9bae-c021ca11fb54.PNG)

Membuat repository server
• Server reopsitory yang akan kita gunakan adalah http://github.com 
• Anda harus membuat akun terlebih dahulu. 
• Pada laman github, klik tombol start a project, atau 
• Dari menu (icon +) klik New Repository
![ser](https://user-images.githubusercontent.com/72907744/96324773-a6174080-104d-11eb-897d-7d99ac7721bb.PNG)
![ver](https://user-images.githubusercontent.com/72907744/96324785-b2030280-104d-11eb-9d84-c04e03ffc7f4.PNG)

• Isi nama repositorynya, misal: labpy1. 
• lalu klik tombol Create repository
![server](https://user-images.githubusercontent.com/72907744/96324788-b62f2000-104d-11eb-84fe-c33c5b805462.PNG)

Menambahkan Remote Repository
• Remote Repository merupakan repository server yang akan digunakan untuk menyimpan setiap perubahan pada local repository, sehingga dapat diakses oleh banyak user.
• Untuk menambahkan remote repository server, gunakan perintah git remote add origin [url]
$ git remote add origin https://github.com/abuazzam/labpy1.git

Push (Mengirim perubahan ke server)
• Untuk mengirim perubahan pada local repository ke server gunakan perintah git push.
 $ git push -u origin master
• Perintah ini akan meminta memasukkan username dan password pada akun github.com
![iiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiii](https://user-images.githubusercontent.com/72907744/96324861-09a16e00-104e-11eb-8676-37a0ddbb6c2d.PNG)

Melihat hasilnya pada server repository
• Buka laman github.com, arahkan pada repositorinya.
• Maka perubahan akan terlihat pada laman tersebut.
![iiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiii](https://user-images.githubusercontent.com/72907744/96324792-be875b00-104d-11eb-919d-231d81fcca74.PNG)

Clone Repository
• Clone repository, pada dasarnya adalah meng-copy repository server dan secara otomatis membuat satu direktory sesuai dengan nama repositorynya (working directory).
• Untuk melakukan cloning, gunakan perintah git clone [url]
![iiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiiii](https://user-images.githubusercontent.com/72907744/96324805-ca731d00-104d-11eb-997b-22152eab3c50.PNG)




