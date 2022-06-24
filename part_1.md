# Pelatihan Version Control System (GitHub Environment) Lab RPL ITS 2022

## Part 1 : Pengenalan Git Version Control System

### Version Control Systems
Pernahkah kalian mengerjakan tugas, atau apa pun itu dan pada akhirnya menjadi begini?

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/vcs_intro_1.jpg" width="600">
</p>

Menyimpan banyak file dengan nama yang berbeda-beda pasti sangat memusingkan dan memerlukan banyak ruang. Mungkin hal tersebut bisa saja diakali dengan menyimpan file kalian pada layanan berikut :

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/vcs_intro_2.jpg" width="600">
</p>

Tetap, melakukan kedua hal tersebut sangat tidak efisien, apalagi kalau kalian seorang programmer yang berurusan dengan ratusan bahkan ribuan file dan folder. Solusi dari permasalahan tersebut adalah Version Control System (VCS). Version Control System (VCS) adalah jenis perangkat lunak yang membantu developer dalam melacak dan megelola perubahan pada file. Terdapat beberapa version control system yang terkenal seperti Git, Subversion, CVS, dan Mercurial. Namun, yang akan kita bahas adalah Git.

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/vcs_intro_3.jpg" width="600">
</p>

### Apa itu Git?
Git adalah perangkat lunak pengendali versi atau proyek manajemen kode perangkat lunak yang diciptakan oleh Linus Torvalds, yang pada awalnya ditujukan untuk pengembangan kernel Linux. Git adalah perangkat lunak yang bersifat open source dan gratis.

#### Kenapa Pakai Git?
- Melacak perubahan terhadap pekerjaan (Who, What, When, Why)
- Membantu pemulihan apabila terjadi kendala
- Berkolaborasi dengan tim
- Banyak digunakan oleh developer di seluruh dunia

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/why_git.jpg" width="600">
</p>

Git dapat dianggap sebagai kamera yang meng-capture tiap versi dari suatu direktori dan memungkinkan untuk mengembalikan atau berpindah versi direktori.

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_capture.jpg" width="600">
</p>

### Istilah-Istilah yang Perlu Diketahui
- Repository  : Tempat git melacak perubahan, dalam konteks Git dapat juga dianggap sebagai folder tempat bekerja
- Branch  : Cabang pada Git
- Commit  : Perubahan file yang telah disimpan/snapshot dari repository
- Merge   : Proses menggabungkan beberapa branch
- Hash    : Penanda unik pada commit
- Remote  : Sumber yang memiliki repository
- Clone   : Mengambil repository dari remote
- Push    : Mengirimkan commit ke repository
- Pull    : Mengambil commit dari repository

### Penggunaan Git

#### Cara Instalasi Git
Aplikasi Git dapat diunduh melalui laman resmi Git pada https://git-scm.com/downloads. Silakan mengikuti instruksi instalasi Git sesuai dengan sistem operasi masing-masing.

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_download.png" width="600">
</p>


Instalasi Git pada Linux dapat dilakukan dengan command :

```bash
sudo apt install git
```

#### Dokumentasi Git
Git juga resmi menyediakan tata cara penggunaan dan referensi belajar lainnya. Semua hal tersebut dapat diakses pada dokumentasi Git pada laman https://git-scm.com/doc.

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_docs.png" width="600">
</p>

Tata cara Git pada Linux/CLI dapat diakses dengan command :

```bash
git --help
```

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_help_terminal.png" width="600">
</p>



#### Konfigurasi User
Sebelum menggunakan Git, konfigurasi terlebih dahulu username dan password secara lokal yaitu dengan command :

```bash
git config --global user.name “username”
git config --global user.email “email@email.id”
```

#### Inisialisasi Repo
Repository atau repo adalah folder .git pada folder yang telah di-git init, folder tersebut menyimpan data mengenai operasi-operasi git yang dilakukan pada direktori tersebut. Data tersebut dapat dilihat pada folder /.git/objects. Git juga menyimpan file-file yang kemudian dikompres dan dinamai dengan bantuan enkripsi hash SHA1 agar aman dan mempermudah operasi-operasi pada Git.

Inisialisasi repository dapat dilakukan dengan command :
```bash
git init
```

#### Alur Kerja Git (Basic Workflow)
Terdapat beberapa perintah yang perlu diketahui : 
```bash
git add <nama_file> #menambahkan file ke staging area
git commit -m <pesan> #menambahkan file ke history area
git log #menunjukkan riwayat commit git
git status #menunjukkan status branch saat ini
```

Alur kerja Git
Terdapat 3 area pada sebuah repository git
- Working Tree
  > Tempat kita bekerja pada local machine
- Staging Area (Index)
  > Tempat yang digunakan agar Git dapat melacak perubahan terhadap file kita
- History
  > Tempat yang digunakan Git untuk menyimpan progress

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_areas.jpg" width="600">
</p>

Telah disebutkan bahwa git menyimpan data mengenai apa yang telah dikerjakan, tetapi bagaimana git menyimpannya? Git menyimpan setiap folder/direktori sebagai sebuah tree dan file di dalamnya sebagai blob (binary large object). Blob tersebut nantinya akan dikompres dan namanya diubah menjadi enkripsi hash SHA1.

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_data_modelling.jpg" width="600">
</p>

Git menyimpan tiap capture atau commit dalam bentuk graf, yang berbentuk seperti berikut :


<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_data_modelling_2.jpg" width="600">
</p>

Graf tersebut dapat dilihat melalui command berikut pada terminal :

```bash
git log --all --graph --decorate
```

#### Alur Kerja Git (Branching and Merging)

Terdapat beberapa perintah yang perlu diketahui : 
```bash
git branch #digunakan untuk melihat branch yang ada
git branch <nama_branch> #digunakan untuk membuat branch baru
git checkout <nama_branch> #digunakan untuk berpindah branch
git merge <nama_branch> #menyatukan branch lain dengan branch saat ini
git rebase <nama_branch> #menyatukan branch lain dengan branch saat ini dengan satu alur
git stash #menyimpan perubahan sementara sehingga memungkinkan untuk berpindah branch walaupun ada unsaved work
```
Branch adalah cabang dari sebuah perubahan pada repository git. Contoh kasus penggunaan branch adalah saat mengembangkan aplikasi bersama-sama dan pembagian tugas adalah per fitur untuk tiap orang. Branch tersebut nantinya dapat di git merge ke branch utama agar menjadi satu. 

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_branches.jpg" width="600">
</p>

Merging adalah proses penggabungan dua branch yang akan menyimpan semua riwayat commit kedua branch, terdapat dua jenis merging yaitu
- Fast Forward Merge
   > Saat ada jalur langsung dari suatu commit ke commit yang akan dimerge ke commit tersebut
   > > <p align="center"><img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_fast_forward_merge.jpg" width="600"></p>
- 3-way Merge
  > Saat tidak ada jalur langsung dari suatu commit ke comit yang akan dimerge ke commit tersebut
  > > <p align="center"><img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_3-way_merge.jpg" width="600"></p>

Rebase adalah proses penggabungan dua branch juga, tetapi hanya memasukkan riwayat commit perubahan branch yang akan disatukan.

<p align="center">
  <img src="https://github.com/LabSE-ITS/Pelatihan_VCS_2022/blob/main/images/git_rebase.jpg" width="600">
</p>

