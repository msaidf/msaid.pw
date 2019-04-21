+++
title = "Membandingkan 2 Versi Revisi File di Dropbox dan pCloud"
date = 2018-07-05T06:26:42Z
draft = false

# Tags and categories
# For example, use `tags = []` for no tags, or the form `tags = ["A Tag", "Another Tag"]` for one or more tags.
tags = ["Software"]
categories = []

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""

+++

Layanan sinkronisasi seperti [Dropbox](https://db.tt/fIoPf32j), OneDrive dan lainnya mempermudah kerja kolaborasi dalam tim. Semua anggota tim dapat senantiasa memiliki versi terbaru dari file tanpa harus saling berkirim email versi terbaru sebagaimana biasa dilakukan di jaman old. 

Namun seringkali kita juga perlu untuk melacak editing/perubahan yang dilakukan oleh rekan tim kepada file tersebut. Untuk dokumen word processor (MS-Office, LibreOffice, Google Docs), sudah ada fasilitas tracking changes. Namun untuk file-file berbasis teks seperti skrip program, readme, atau dokumen latex dan markdown, tidak ada software editor yang mendukung fasilitas track changes sebagaimana dokumen word processor. 

Sebagai alternatif untuk track changes, aplikasi diff/compare bisa digunakan untuk membandingkan dua teks atau lebih. Akan tetapi ini memerlukan file berbeda untuk tiap versi yang dibandingkan. Sementara dalam alur kerja menggunakan sinkronisasi, editing tidak menghasilkan file baru, walau versi lama masih tersimpan hingga waktu tertentu. Kita bisa secara manual mengunduh versi lama untuk dibandingkan dengan versi sekarang atau versi lama lainnya. 

Tentu akan lebih mudah jika kita bisa langsung membandingkan antar versi tanpa harus mengunduh terlebih dulu. Beruntung ada aplikasi untuk itu berupa ekstensi browser Chrome bernama CloudDiff. Aplikasi ini dapat membandingkan antar versi file di [Dropbox](https://db.tt/fIoPf32j) dan [pCloud](https://my.pcloud.com/#page=register&invite=ppa2ZaDkvby). Saya belum menemukan aplikasi semacam ini untuk Google Drive dan OneDrive.


## Cara setup CloudDiff
1. Buka link berikut di browser Google Chrome dan klik tombol Add to Chrome. https://chrome.google.com/webstore/detail/clouddiff/hlmlielnekakcdfpkbgcpnphenleogfp
2. Install https://bitbucket.org/vshih/clouddiff-helper/downloads/clouddiff-helper_windows.exe


## Cara menggunakan CloudDiff

Setelah itu jika anda melihat Revision History dari suatu file di [Dropbox](https://db.tt/fIoPf32j) atau [pCloud](https://my.pcloud.com/#page=register&invite=ppa2ZaDkvby), akan ada 2 check radio button di sebelah kiri tiap versi. Pilih 2 versi yang ingin dibandingkan dengan mencek radio button sebelah kiri untuk versi yang ingin ditampilkan di sebelah kiri, dan radio button sebelah kanan untuk versi yang ingin ditampilkan di sebelah kanan. Lalu klik tombol Inline.

![](https://d2mxuefqeaa7sj.cloudfront.net/s_EC57CC8791B30B808B9A73C9508C27079FD0F9B76E77FE8A90890E80EB795C19_1530382926028_img_20180630_165853.jpg)

maka hasil perbandingannya akan nampak seperti di bawah ini.

![](https://d2mxuefqeaa7sj.cloudfront.net/s_EC57CC8791B30B808B9A73C9508C27079FD0F9B76E77FE8A90890E80EB795C19_1530382992638_IMG_20180630_170047.jpg)

Sementara untuk tombol Diff sendiri akan membuka aplikasi diff eksternal yang terinstal di komputer. Untuk mensetup-nya, ikuti petunjuk nomor 2-4 di option ekstensi CloudDiff.

![](https://d2mxuefqeaa7sj.cloudfront.net/s_EC57CC8791B30B808B9A73C9508C27079FD0F9B76E77FE8A90890E80EB795C19_1530383336046_IMG_20180630_170142.jpg)