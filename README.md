# Wiki-Git
Panduan Git untuk Pengembangan Proyek di Organisasi


## Memulai Proyek
Jika Anda sudah tergabung ke dalam proyek pengembangan perangkat lunak, Anda dapat:
1. Clone project organisasi anda. Ikuti perintah dibawah.
```
git clone https://github.com/<username>/<nama_project>
```
## Membuat cabang baru
Jika Anda telah siap untuk melakukan perubahan kode di proyek Anda, Anda dapat membuat cabang baru sesuai jobdesk anda di Tim. Jangan membuat perubahan di cabang Main, karena itu adalah cabang utama.
Ikuti perintah dibawah
```
git checkout -d "nama cabang baru"
```
## Oke, Setelah membuat cabang baru dan teman tim juga membuat cabang baru. Apa yang harus saya lakukan?
Saat mengerjakan proyek bersama, muncul branch baru tak dapat dihindari. Branch baru di gunakan untuk memisahkan perubahan kode dari cabang utama. Biasanya branch yang dibentuk difokuskan pada satu fitur. Anda dapat menamainya dengan fitur yang Anda kerjakan. Misal: 'feature: login-register'.
``
Ynag harus Anda lakukan adalah fokus pada branch yang Anda buat, jangan mencampurkan kode yang tidak berhubungan dengan branch yang Anda kerjakan.
``
## Saya ingin menggunakan code dari branch lain untuk fitur yang saya kembangkan. Bagaimana caranya?
Caranya cukup mudah. Anda dapat mengikuti langkah dibawah ini.
```
git fetch
```
tujuanya adalah untuk mengambil semua branch dari repository remote beserta sejarah commitnya.
```
git branch -a
```
tujuanya mengecek apakah branch dan sejarah commit branch dari repository remote sudah terekam di repository lokal
```
git checkout -b nama_branch_lokal
```
perintah *checkout* digunakan untuk berpindah ke branch lain darai branch sekarang, sedangkan *-b* digunakan untuk membuat branch baru yang belum ada di repository lokal.
```
git pull origin nama_branch_remote
```
tujuanya adalah mengambil perubahan terbaru dari proyek pada branch beserta sejarah perubahanya/commit. Saat menggunakan perintah ini branch Anda akan berubah mengikuti kodingan branch yang anda pull.
`Alternatif lain:`
```
git chekout -b nama_branch_lokal origin/nama_branch_remote
```
Jika dilihat perintah di atas lebih singkat dari beberpa perintah sebelumnya. Hal ini dikarenakan pada perintah di atas hanya mengambil branch beserta sejarah commitnya ke repository lokal. Berbeda dengan git fetch yang mengambil semua branch repository remote kemudian di simpan ke repository lokal. 
