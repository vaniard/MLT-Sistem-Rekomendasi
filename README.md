# Laporan Proyek Machine Learning - Vania Rachmawati Dewi

## 1. Project Overview

### 1.1 Latar Belakang

Perpustakaan merupakan tempat koleksi besar dari buku dan bahan bacaan lainnya yang pada umumnya dikelola oleh instansi untuk dimanfaatkan oleh masyarakat luas sebagai sarana informasi dan pengetahuan [[1]](https://d1wqtxts1xzle7.cloudfront.net/78554060/587-libre.pdf?1642017276=&response-content-disposition=inline%3B+filename%3DSistem_Rekomendasi_Buku_Menggunakan_Weig.pdf&Expires=1749060878&Signature=Pm8~dXNHGF90jpgVV1pNvHshKa9qOAQn9pZdu2qRBqwHuPyTQ6azONAP2-Pj6gmkVP91SI19IiQuHzs8-lmL~6zG1fUhfYUTMkCV0bQFhjaMeH-3H9f1NB93VSoG59BrtF3ml32wTNE6QqmkgYNwzN4V3E7BNIIUHS3JZq8HSFFmJu9UqX40UyZ6qI8GF~RSXKxFPvKjZ-q7XAZdhNRK8Rls~aMPOqL1S7POARS6G7Tc42FxABchzCnFzTnIbWFMv5FGq6DIn1shuFpTxrZPtPywK-9dGxg-IYvcxPLQbvP0LkQ-ng6e2mUc3Tp8843jXMPIAtv-JxtfToz2NuvXbg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA). Pada perkembangan teknologi informasi, perpustakaan pun ikut berkembang dengan penyediaan koleksi buku bahan bacaan dalam bentuk digital yang umumnya diistilahkan sebagai sistem informasi perpustakaan. Salah satu layanan sistem informasi penelusuran buku, yaitu pencarian dan temu buku untuk kebutuhan pengunjung dalam mencari buku dan informasi buku yang diinginkan. 
Pengunjung sering mengalami kesulitan dalam mencari buku yang memiliki kesamaan atau berkaitan dengan buku yang dipilih sebelumnya. Sehingga pengunjung memerlukan waktu yang cukup lama untuk mencari dan menemukan buku lain yang mirip dengan yang diinginkan ketika buku tersebut telah dipinjam. Maka dari itu, perlu adanya peningkatan kualitas pelayanan dengan menyediakan sistem rekomendasi buku. Dan dengan adanya sistem rekomendasi tersebut atau saran buku-buku lain yang berhubungan diharapkan dapat membantu pengunjung yang datang.
Sistem rekomendasi memungkinkan pengunjung untuk dengan mudah menemukan referensi baru mengenai buku yang sesuai dengan kategori buku yang disukai oleh pembaca sebelumnya [[2]](https://ejurnal.umri.ac.id/index.php/coscitech/article/view/5131/2462). Saat ini, sistem rekomendasi telah banyak digunakan di berbagai aspek kehidupan. Dan sistem rekomendasi terdiri dari beberapa model termasuk *Content-Based Filtering*, *Collaborative Filtering* dan *Hybrid Recommender System* [[3]](https://citec.amikom.ac.id/main/index.php/citec/article/view/231). Dalam penelitian ini, akan dibuat sistem rekomendasi menggunakan metode *Content-Based Filtering* dan *Collaborative Filtering*, sistem rekomendasi ini bertujuan untuk memudahkan pengunjung mencari data buku dan diharapkan pengunjung dapat menemukan data yang relevan dan sesuai dengan kebutuhan mereka dengan lebih cepat dan mudah.

## 2. Business Understanding

### 2.1 Problem Statement 

1. Bagaimana cara membuat sistem rekomendasi menggunakan teknik *Content-Based Filtering*?
2. Bagaimana perpustakaan dapat merekomendasikan alternatif buku yang mungkin disukai atau sering dibaca dan belum pernah dibaca oleh pengunjung?

### 2.2 Goals 

1. Membuat sistem rekomendasi buku pada perpustakaan menggunakan teknik *Content-Based Filtering*.
2. Membuat sistem rekomendasi mengenai alternatif buku yang mungkin akan disukai atau sering dibaca dan belum pernah dibaca menggunakan teknik *Collaborative Filtering*.

### 2.3 Solution Statement

Untuk mengatasi masalah tersebut, peneliti mengusulkan sistem rekomendasi buku menggunakan dua model *Content-Based Filtering* dan *Collaborative Filtering*. 

1. **Content-Based Filtering** merupakan metode yang mempertimbangkan perilaku dari pengguna masa lalu yang kemudian diidentifikasi pola perilakunya untuk merekomendasikan barang yang sesuai dengan pola perilaku tersebut [[4]](https://link.springer.com/chapter/10.1007/978-981-13-1927-3_42). Model akan dicocokkan dengan serangkaian karakteristik atribut dari barang yang akan direkomendasikan. Barang dengan tingkat kecocokan tertinggi akan menjadi rekomendasi untuk pengguna.
Kelebihan dari *Content-Based Filtering* yaitu [[5]](https://d1wqtxts1xzle7.cloudfront.net/84205803/02-EKO-WIJAYA-libre.pdf?1650030063=&response-content-disposition=inline%3B+filename%3DSistem_Rekomendasi_Laptop_Menggunakan_Co.pdf&Expires=1749066372&Signature=QwbSdVsHpoDNf2r-kHUyoELmKFUew32ZrKQ1QIHfeLPBbsQzfT694rqozpuZrIXVVIIA4ybsJZNHlzPZTXGlDU~XdhVNUYJPhl6lfdhavNQqrQabBVk6FNUCMDDnwg8XZocZuCoSQ72EKLR8XlHgUak62nuOMBUx7gjXjmc80NgavK0HoxOVG3nbS1NAywrQh2DTvtm40TSXNE7ESwxgO27GASK8hNi2jleqVRr--ErJJe4gy9hdKabAo2LG3IU7aPIZBCvkF-Rv5jrcqudIO~l5cwHS-y16qUuJ~EwyoM8WRRHTyTj~3UbrsQzENI09MBHOPikm2UyE14HE9rbKVg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA) : Dapat menjelaskan bagaimana hasil rekomendasi didapatkan dan dapat merekomendasikan item-item yang bahkan belum pernah di-rate oleh siapapun.
Namun, sistem rekomendasi *Content-Based Filtering* juga memiliki kekurangan yaitu [[6]](https://d1wqtxts1xzle7.cloudfront.net/84205803/02-EKO-WIJAYA-libre.pdf?1650030063=&response-content-disposition=inline%3B+filename%3DSistem_Rekomendasi_Laptop_Menggunakan_Co.pdf&Expires=1749066372&Signature=QwbSdVsHpoDNf2r-kHUyoELmKFUew32ZrKQ1QIHfeLPBbsQzfT694rqozpuZrIXVVIIA4ybsJZNHlzPZTXGlDU~XdhVNUYJPhl6lfdhavNQqrQabBVk6FNUCMDDnwg8XZocZuCoSQ72EKLR8XlHgUak62nuOMBUx7gjXjmc80NgavK0HoxOVG3nbS1NAywrQh2DTvtm40TSXNE7ESwxgO27GASK8hNi2jleqVRr--ErJJe4gy9hdKabAo2LG3IU7aPIZBCvkF-Rv5jrcqudIO~l5cwHS-y16qUuJ~EwyoM8WRRHTyTj~3UbrsQzENI09MBHOPikm2UyE14HE9rbKVg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA) Sistem rekomendasi berbasis kontent ini memerlukan sebuah profil user yang berisikan ketertarikan dan minat pengguna, bagi pengguna baru yang belum pernah melakukan aktivitas apapun dan tidak memiliki profil user yang cukup, sistem rekomendasi tidak dapat memberikan rekomendasi yang handal kepadanya.

2. **Collaborative Filtering** memilih data yang bersumber pada kesamaan karakter pengguna untuk memberikan informasi berdasarkan pola kelompok konsumen yang serupa, memungkinkan informasi baru diberikan kepada pengguna [[7]](https://ejournal.akakom.ac.id/index.php/jiko/article/view/727/pdf). *Collaborative Filtering* memiliki beberapa kelebihan yaitu rekomendasi tetap akan bekerja dalam keadaan dimana konten sulit dianlisi sekalipun. Namun metode ini juga memiliki kekurangan yaitu membutuhkan parameter rating, sehingga jika ada item baru sistem tidak akan merekomendasikan item tersebut [[8]](https://d1wqtxts1xzle7.cloudfront.net/84205803/02-EKO-WIJAYA-libre.pdf?1650030063=&response-content-disposition=inline%3B+filename%3DSistem_Rekomendasi_Laptop_Menggunakan_Co.pdf&Expires=1749066372&Signature=QwbSdVsHpoDNf2r-kHUyoELmKFUew32ZrKQ1QIHfeLPBbsQzfT694rqozpuZrIXVVIIA4ybsJZNHlzPZTXGlDU~XdhVNUYJPhl6lfdhavNQqrQabBVk6FNUCMDDnwg8XZocZuCoSQ72EKLR8XlHgUak62nuOMBUx7gjXjmc80NgavK0HoxOVG3nbS1NAywrQh2DTvtm40TSXNE7ESwxgO27GASK8hNi2jleqVRr--ErJJe4gy9hdKabAo2LG3IU7aPIZBCvkF-Rv5jrcqudIO~l5cwHS-y16qUuJ~EwyoM8WRRHTyTj~3UbrsQzENI09MBHOPikm2UyE14HE9rbKVg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA).

## 3. Data Understanding 

### 3.1 Deskripsi Dataset 

| Jenis     | Keterangan |
|-----------|------------|
| **Title** | *Book Recommendation Dataset* |
| **Source** | [Kaggle](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset) |
| **License** | CC0: Public Domain |
| **Visibility** | Public |
| **Tags** | *Online Communities*, *Literature*, *Art*, *Recommender Systems*, *Culture and Humanities* | 
| **Usability** | 10.00 |

Tabel 1 Informasi Dataset 

Dataset berasal dari kaggle tentang Rekomendasi Buku. Pada data Books terdapat 271.360 baris dengan 8 kolom yang terdiri dari ISBN, book title, book author, year of publication, publisher, image url s, image url m dan image url l. Kemudian pada data Users terdapat 278.858 baris dan 3 kolom yang tediri dari User-Id, location dan age. Pada data Ratings terdapat 11.497.80 baris dan 3 kolom yang tediri dari User-Id, ISBN, Book rating. Pada dataset ini, input dan output difokuskan pada pemberian rekomendasi buku, dengan rating yang mencerminkan kualitas atau tingkat apresiasi pengguna terhadap buku tersebut. Rating 0 dapat berarti rating implisit, sedangkan rating dari 1 hingga 10 menunjukkan tingkat kualitas buku berdasarkan penilaian pengguna.

### 3.2 Deskripsi Variabel 

| Nama Variabel Books                                              | Deskripsi                                                                                            |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| ISBN                                                             | Identifikasi unik untuk buku.                                                                        |
| Book Title                                                       | Berisikan judul buku.                                                                                |
| Book Author                                                      | Berisikan penulis buku.                                                                              |
| Year of Publication                                              | Tahun buku diterbitkan.                                                                              |
| Publisher                                                        | Penerbit buku.                                                                                       |
| Image-URL-S                                                      | URL untuk gambar sampul buku berukuran kecil.                                                        |
| Image-URL-M                                                      | URL untuk gambar sampul buku berukuran sedang.                                                       |
| Image-URL-L                                                      | URL untuk gambar sampul buku berukuran besar.                                                        |

Tabel 2 Deskripsi Variabel Books

![image](https://github.com/user-attachments/assets/5f9dd415-389d-41a5-bde3-a45f9d7d2c52)

Gambar 1 Informasi Dataset Books

![image](https://github.com/user-attachments/assets/6b6b2ce4-ea18-4af1-9963-c01ad1730ed9)

Gambar 2 Sampel Dataset

| Nama Variabel Users                                              | Deskripsi                                                                                            |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| User-ID                                                          | Mengidentifikasi pengguna secara unik.                                                               |
| Location                                                         | Menyimpan informasi lokasi pengguna.                                                                 |
| Age                                                              | Menyimpan informasi usia pengguna.                                                                   |

Tabel 3 Deskripsi Variabel Users

![image](https://github.com/user-attachments/assets/7df394d4-8f1c-4ecf-b3dc-31c9e77c9e6f)

Gambar 3 Informasi Dataset Users




| Nama Variabel Ratings                                            | Deskripsi                                                                                            |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| User-ID                                                          | Mengidentifikasi pengguna secara unik.                                                               |
| ISBN                                                             | Identifikasi unik untuk buku.                                                                        |
| Book Rating                                                      | Menunjukkan rating yang diberikan oleh pengguna untuk buku-buku tertentu dan berskala 0 sampai 10.   |

Tabel 4 Deskripsi Variabel Ratings





