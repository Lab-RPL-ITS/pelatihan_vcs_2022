# Pelatihan Version Control System (GitHub Environment) Lab RPL ITS 2022

## Part 1 : Pengenalan Git Version Control System

### Apa itu Git?
Git adalah salah satu Version Control System (VCS) yang open source dan gratis. Version Control System (VCS) adalah jenis perangkat lunak yang membantu developer dalam melacak dan megelola perubahan pada file. Git dibuat oleh Linus Torvalds saat sedang mengembangkan kernel Linux.

#### Kenapa Pakai Git?
- Melacak perubahan terhadap pekerjaan (Who, What, When, Why)
- Mengurangi risiko error pada pengembangan proyek
- Membantu pemulihan apabila terjadi kendala
- Berkolaborasi dengan tim
- Banyak digunakan oleh developer di seluruh dunia

Git dapat dianggap sebagai kamera yang meng-capture tiap versi dari suatu direktori dan memungkinkan untuk mengembalikan atau berpindah versi direktori.

### Penggunaan Git

#### Cara Instalasi Git
Aplikasi Git dapat diunduh melalui laman resmi Git pada https://git-scm.com/downloads. Silakan mengikuti instruksi instalasi Git sesuai dengan sistem operasi masing-masing.

Instalasi Git pada Linux dapat dilakukan dengan command :

```bash
sudo apt install git
```

#### Dokumentasi Git
Git juga resmi menyediakan tata cara penggunaan dan referensi belajar lainnya. Semua hal tersebut dapat diakses pada dokumentasi Git pada laman https://git-scm.com/doc.

Tata cara Git pada Linux/CLI dapat diakses dengan command :

```bash
git --help
```

#### Konfigurasi User
Sebelum menggunakan Git, konfigurasi terlebih dahulu username dan password secara lokal yaitu dengan command :

```bash
git config --global user.name “username”
git config --global user.email “email@email.id”
```

#### Inisialisasi Repo
Repository atau repo adalah file .git pada folder yang telah di-git init, file tersebut menyimpan data mengenai operasi-operasi git yang dilakukan pada direktori tersebut. Data tersebut dapat dilihat pada folder /.git/objects. Git juga menyimpan file-file yang kemudian dikompres dan dinamai dengan bantuan enkripsi hash SHA1 agar aman dan mempermudah operasi-operasi pada Git.

Inisialisasi repository dapat dilakukan dengan command :
```bash
git init
```

#### Alur Kerja Git
Alur kerja Git
Terdapat 3 area pada sebuah repository git
- Working Tree
  > Tempat kita bekerja pada local machine
- Staging Area (Index)
  > Tempat yang digunakan agar Git dapat melacak perubahan terhadap file kita
- History
  > Tempat yang digunakan Git untuk menyimpan progress

Terdapat pula yang namanya Branch. Branch adalah cabang dari sebuah perubahan pada repository git. Contoh kasus penggunaan git branch adalah saat mengembangkan aplikasi bersama-sama dan pembagian tugas adalah per fitur untuk tiap orang. Branch tersebut nantinya dapat di git merge ke branch utama agar menjadi satu kesatuan. 


#### Working With Git
Terdapat beberapa command dasar Git yang harus diketahui

```bash
git status #digunakan untuk melihat status working tree
git add #menambahkan file ke staging area
git commit #menambahkan file ke history area
git log #menunjukkan riwayat commit git
git diff #menunjukkan perbedaan file
git branch #menunjukkan, membuat, atau menghapus branch
git checkout #berpindah branch
```




