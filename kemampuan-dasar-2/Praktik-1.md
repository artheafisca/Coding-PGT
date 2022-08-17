**<h1>Step 1: Inisialisasi Proyek Baru<h1>**
<h3>Buka Github dan klik tombol '+' di pojok kanan rop dan pilih 'New Repository'.<h3>


![1](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/1.png)


<h3>Kemudian isi kolom Repository name dan Description. Tetap publik, dan jangan "Initialize this repository with a README". Jangan mengubah apa pun. Klik "Create repository".<h3>

![2](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/2.png)

<h3>Selanjutnya Anda akan melihat halaman pengaturan. Ini adalah instruksi untuk menghubungkan Repo yang baru saja Anda buat di Github (Remote) ke direktori yang Anda buat di terminal Anda (Lokal).<h3>

![3](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/3.png)

<h3>Rekatkan baris di kotak merah baris demi baris yang dimulai dengan "echo ..." ke terminal saat Anda masuk ke direktori yang baru saja Anda buat secara lokal. Terminal Anda akan terlihat seperti ini setelah Anda selesai.<h3>

![4](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/4.png)

<h3>Dan jika Anda pergi ke halaman Repo Github Anda, Anda akan melihat ReadMe yang Anda inisialisasi dan referensi ke komit pertama yang Anda buat.<h3>

![5](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/5.png)

<h3>Sekarang mari kita perbarui Repo ini. Kembali ke terminal Anda dan git add, git commit, dan git Push.<h3>

```
$ git add .
$ git commit -m "Second commit"
$ git push
```

![6](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/6.png)

![7](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/7.png)

<h3>Anda telah diinisialisasi dan siap untuk mulai bekerja!<h3>


<h1>Step 2: Siapkan Tim Anda<h1>
<h3>Klik pada tab "Setting" perwakilan Anda, lalu "Collaborators" lalu cari pengguna Github dan tambahkan mereka dengan mengklik "Add Collaborator".<h3>

![8](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/8.png)

![9](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/9.png)

<h3>Mereka akan menerima email yang memberi tahu mereka bahwa Anda menambahkan mereka dan akan terdaftar sebagai kolaborator.<h3>

![10](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/10.png)

<h3>Jika Anda seorang kolaborator, buka halaman Github Repo, Git Clone the project, dan cd ke direktori. Jangan memotongnya! Forking akan menyalinnya di Repo baru ke halaman Github Anda, tetapi Anda tidak menginginkannya — Anda ingin berkolaborasi di Repo Github yang sama dengan rekan tim Anda.<h3>

![11](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/11.png)

```
$ git clone git@github.com:MinesJA/github_guide.git
$ cd github_guide/
```

<h3>Dan sekarang Anda siap untuk berkolaborasi!<h3>

<h1>Step 3: Berkolaborasi<h1>
<h3>Saat Anda menggunakan git untuk mengerjakan proyek yang sama dengan banyak orang, ada satu aturan utama yang harus Anda ikuti.<h3>

<h3>CABANG UTAMA HARUS SELALU DIPLOYABLE<h3>

<h3>Cara agar Master dapat digunakan adalah dengan membuat cabang baru untuk fitur-fitur baru dan menggabungkannya ke dalam Master setelah selesai. Inilah cara kerjanya.<h3>

<h1>Step 3a: Branches<h1>
<h3>Jadi katakanlah Anda ingin membuat model Pengguna. Di terminal Anda, buat cabang baru.<h3>
```
$ git co -b create_user
```
<h3>“co” adalah singkatan dari “checkout” yang digunakan untuk berpindah antar cabang. Menambahkan "-b" dan nama di akhir membuat cabang baru dan kemudian pindah ke cabang baru itu untuk kita.
Anda harus dapat memverifikasi ini dengan perintah.<h3>

```
$ git branch
```

![12](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/12.png)

<h3>Anda sekarang berada di cabang baru dan dapat mulai membuat kode.<h3>
<h3>Catatan: Sebagai aturan umum, Anda harus sering git add dan git commit ketika Anda menyelesaikan sesuatu yang memungkinkan kode Anda berfungsi (berakhir menjadi beberapa kali dalam satu jam). Misalnya, ketika Anda menyelesaikan suatu metode dan basis kode berfungsi, git commit seperti ini.<h3>

```
$ git commit -m "Added function to allow Users to say 'Hello World'"
```

<h1>Step 3b: Submitting Pull Requests<h1>
<h3>Pertama, tentukan siapa yang akan bertanggung jawab menangani penggabungan. Semakin sedikit orang yang bertindak secara independen dalam penggabungan, semakin baik sehingga untuk tim yang terdiri dari 4 orang, Anda mungkin perlu memiliki satu "Reviewer" atau "Merge Master" resmi.
Selanjutnya, minta semua orang git Push cabang mereka.<h3>

```
$ git push
```
<h3>Sekarang pergi ke halaman Repo Github. Anda akan melihat cabang yang Anda dorong di bilah kuning di bagian atas halaman dengan tombol "Compare & pull request”".
Catatan: Atau, Anda dapat memilih cabang di menu tarik-turun “Branch:” dan pilih cabang yang baru saja Anda tekan. Anda kemudian akan memiliki tombol "Pull Request" dan "Compare" di sisi kanan.<h3>

![13](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/13.png)

<h3>Klik "Compare & pull request Ini akan membawa Anda ke halaman "Open a pull request". Dari sini, Anda harus menulis deskripsi singkat tentang apa yang sebenarnya Anda ubah. Dan Anda harus mengklik tab “Reviewers” dan memilih siapa pun yang diputuskan oleh tim Anda sebagai “Merge Master”. Setelah selesai, klik "Create ull request".<h3>

![14](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/14.png)

<h1>Step 3c: Merging Pull Requests<h1>
<h3>Perhatikan bahwa jika Anda seorang kolaborator, Anda dapat menggabungkan permintaan tarik Anda sendiri. Namun, sekali lagi, jika Anda bekerja dalam tim, lebih masuk akal jika satu orang melakukan semua penggabungan dan semua orang lainnya mengirimkan "Pull requests" dan menetapkan "Master Merger" sebagai peninjau hanya untuk memastikan Anda berurusan dengan konflik gabungan apa pun satu cabang pada satu waktu.
Jadi, dengan asumsi Anda adalah orang yang bertanggung jawab untuk mengurus semua penggabungan dan seseorang telah menugaskan Anda sebagai "Reviewer" pada permintaan tarik, ketika Anda masuk ke Github Anda, Anda akan melihat Anda memiliki pemberitahuan yang memberi tahu Anda bahwa seseorang telah menugaskan Anda sebagai pengulas. Anda juga akan melihat bilah kuning yang menunjukkan salah satu rekan tim Anda sebagai "requested on this pull request."
Silakan dan klik tombol “Add your reviewer”.<h3>

![15](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/15.png)

<h3>Ini akan membawa Anda ke halaman Permintaan Tarik. Bagaimana Anda bergerak maju dari sini terserah Anda dan tim Anda. Jika Anda bekerja bersama, saya akan menggunakan setiap pagi untuk duduk sebagai sebuah tim dan melakukan pull request bersama. Jika Anda melakukannya, Anda tidak perlu meninggalkan Ringkasan Ulasan yang bertele-tele dan terperinci.
Namun, jika Anda bekerja dari jarak jauh, ini akan menjadi alat utama Anda untuk memberi tahu pemohon jika mereka perlu membuat perubahan atau jika Anda akan menggabungkan permintaan mereka.<h3>

![16](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/16.png)

<h3>Ketika Anda mengklik "Submit review" pada tarik-turun "Review changes", ulasan Anda sekarang akan ada sebagai komentar di utas permintaan tarik.<h3>

![17](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/17.png)

<h3>Saat Anda puas dengan permintaan tarik, buka bagian bawah permintaan tarik dan klik "Merge pull request".
Anda kemudian akan melihat pesan "Pull request successfully merged and closed" dan tombol untuk "Delete branch" yang harus Anda klik.<h3>

![18](https://raw.githubusercontent.com/artheafisca/github/main/gambar-1/18.png)