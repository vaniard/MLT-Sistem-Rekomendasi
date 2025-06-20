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
Namun, sistem rekomendasi *Content-Based Filtering* juga memiliki kekurangan yaitu [[6]](https://d1wqtxts1xzle7.cloudfront.net/84205803/02-EKO-WIJAYA-libre.pdf?1650030063=&response-content-disposition=inline%3B+filename%3DSistem_Rekomendasi_Laptop_Menggunakan_Co.pdf&Expires=1749066372&Signature=QwbSdVsHpoDNf2r-kHUyoELmKFUew32ZrKQ1QIHfeLPBbsQzfT694rqozpuZrIXVVIIA4ybsJZNHlzPZTXGlDU~XdhVNUYJPhl6lfdhavNQqrQabBVk6FNUCMDDnwg8XZocZuCoSQ72EKLR8XlHgUak62nuOMBUx7gjXjmc80NgavK0HoxOVG3nbS1NAywrQh2DTvtm40TSXNE7ESwxgO27GASK8hNi2jleqVRr--ErJJe4gy9hdKabAo2LG3IU7aPIZBCvkF-Rv5jrcqudIO~l5cwHS-y16qUuJ~EwyoM8WRRHTyTj~3UbrsQzENI09MBHOPikm2UyE14HE9rbKVg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA) Sistem rekomendasi berbasis konten ini memerlukan sebuah profil user yang berisikan ketertarikan dan minat pengguna, bagi pengguna baru yang belum pernah melakukan aktivitas apapun dan tidak memiliki profil user yang cukup, sistem rekomendasi tidak dapat memberikan rekomendasi yang handal kepadanya.

2. **Collaborative Filtering** memilih data yang bersumber pada kesamaan karakter pengguna untuk memberikan informasi berdasarkan pola kelompok konsumen yang serupa, memungkinkan informasi baru diberikan kepada pengguna [[7]](https://ejournal.akakom.ac.id/index.php/jiko/article/view/727/pdf). *Collaborative Filtering* memiliki beberapa kelebihan yaitu rekomendasi tetap akan bekerja dalam keadaan dimana konten sulit dianalisis sekalipun. Namun metode ini juga memiliki kekurangan yaitu membutuhkan parameter rating, sehingga jika ada item baru sistem tidak akan merekomendasikan item tersebut [[8]](https://d1wqtxts1xzle7.cloudfront.net/84205803/02-EKO-WIJAYA-libre.pdf?1650030063=&response-content-disposition=inline%3B+filename%3DSistem_Rekomendasi_Laptop_Menggunakan_Co.pdf&Expires=1749066372&Signature=QwbSdVsHpoDNf2r-kHUyoELmKFUew32ZrKQ1QIHfeLPBbsQzfT694rqozpuZrIXVVIIA4ybsJZNHlzPZTXGlDU~XdhVNUYJPhl6lfdhavNQqrQabBVk6FNUCMDDnwg8XZocZuCoSQ72EKLR8XlHgUak62nuOMBUx7gjXjmc80NgavK0HoxOVG3nbS1NAywrQh2DTvtm40TSXNE7ESwxgO27GASK8hNi2jleqVRr--ErJJe4gy9hdKabAo2LG3IU7aPIZBCvkF-Rv5jrcqudIO~l5cwHS-y16qUuJ~EwyoM8WRRHTyTj~3UbrsQzENI09MBHOPikm2UyE14HE9rbKVg__&Key-Pair-Id=APKAJLOHF5GGSLRBV4ZA).

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

![image](https://github.com/user-attachments/assets/74755378-6a0d-41b1-9d88-66b361d12f7d)

Gambar 4 Sampel Dataset


| Nama Variabel Ratings                                            | Deskripsi                                                                                            |
| ---------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------- |
| User-ID                                                          | Mengidentifikasi pengguna secara unik.                                                               |
| ISBN                                                             | Identifikasi unik untuk buku.                                                                        |
| Book Rating                                                      | Menunjukkan rating yang diberikan oleh pengguna untuk buku-buku tertentu dan berskala 0 sampai 10.   |

Tabel 4 Deskripsi Variabel Ratings

![image](https://github.com/user-attachments/assets/6f5a4e41-0a4c-4dd2-a39a-d2b7fd51600b)

Gambar 5 Informasi Dataset

![image](https://github.com/user-attachments/assets/ab1edfa4-8766-456f-9685-7c87029eb7d4)

Gambar 6 Sampel Dataset

### 3.3 Univariate Exploratory Data Analysis

![image](https://github.com/user-attachments/assets/02e55cdf-d596-47db-95bd-71c00a9d823b)

Gambar 7 Histogram Distribusi Tahun Publikasi Buku

Distribusi menunjukkan adanya ekplorasi dan ekspansi besar-besaran di dunia penerbitan buku sejak 1980-an, yang kemudian memuncak pada awal 2000-an. Setelah itu, terjadi penurunan, yang bisa jadi bukan karena minat baca yang menurun akan tetapi karena perubahan format media atau keterbatasan data baru.

![image](https://github.com/user-attachments/assets/645b7895-0664-43a6-9604-0fc8d3c145c1)

Gambar 8 Histogram Distribusi Usia Pengguna

Distribusi menunjukkan bahwa pengguna didominasi oleh kelompok usia produktif, terutama antara 20 hingga 35 tahun. Hal ini bisa menjadi dasar untuk menyesuaikan strategi pemasaran, desain antarmuka, maupun fitur produk agar lebih sesuai dengan karakteristik usia dominan. 

![image](https://github.com/user-attachments/assets/b51ef162-07bd-4606-ae71-ace8c4233ecc)

Gambar 9 Diagram Rating Buku

Berdasarkan diagram diatas sebagian besar buku kemungkinan belum diberi rating. Dari buku yang diberi rating, kebanyakan mendapatkan nilai cukup tinggi yaitu 7 sampai 10, hal ini menunjukkan kepuasan pengguna terhadap buku-buku tersebut. Distribusi ini dapat digunakan untuk mengidentifikasi buku yang populer serta untuk cleaning data sebelum digunakan dalam model rekomendasi. 

## 4. Data Preparation

Data preparation *Content-Based Filtering* : 

1. Mengurangi Entitas Variabel :
   - `books` :
     
     a. Dataset `books` asli memiliki 271.360 entri.
     
     b. Baris kode yang digunakan adalah : `books = books[1:7001]`
     
     c. Kode ini memilih slice dari dataframe `books. [1:7001]` berarti mengambil baris dari indeks 1 hingga indeks 7000.
     
     d. Setelah baris ini dieksekusi, variabel books sekarang hanya berisi 7000 baris data buku.
     
     e. Kode `books.info()` dijalankan setelahnya untuk memverifikasi bahwa jumlah entri pada dataframe books telah berkurang menjadi 7000.
     
   - `users` :
     
     a. Dataset `users` asli memiliki 278.858 entri.
     
     b. Baris kode yang digunakan adalah : `users = users[1:7001]`
     
     c. Kode ini mengambil slice dari dataframe `users` dari indeks 1 hingga 7000.
     
     d. Setelah baris ini dieksekusi, variabel `users` sekarang hanya berisi 7000 baris data pengguna.
     
     e. Kode `users.info()` dijalankan setelahnya untuk memverifikasi bahwa jumlah entri pada dataframe users telah berkurang menjadi 7000.
     
   - `ratings` :
     
     a. Dataset `ratings` asli memiliki lebih dari 11 juta entri.
     
     b. Baris kode yang digunakan adalah: `ratings = ratings[1:7001]`
     
     c. Kode ini mengambil slice dari dataframe `ratings` dari indeks 1 hingga 7000.
     
     d. Setelah baris ini dieksekusi, variabel `ratings` sekarang hanya berisi 7000 baris data rating.
     
     e. Kode `ratings.info()` dan `ratings.describe()` dijalankan setelahnya untuk memverifikasi jumlah entri dan melihat statistik deskriptif dari data rating yang sudah diperkecil.
     
2. Menghapus fitur gambar (Image-URL-S, Image-URL-M, Image-URL-L) :
   - `books.drop()` : Ini adalah fungsi pandas yang digunakan untuk menghapus baris atau kolom dari DataFrame.
   - `columns = ['Image-URL-S', 'Image-URL-M', 'Image-URL-L']` : Ini menentukan kolom mana yang ingin dihapus.
   - `axis=1` : Ini menunjukkan bahwa kita ingin menghapus kolom (jika `axis=0`, itu akan menghapus baris).
   
3. Representasi Teks dengan TF-IDF :
   - Judul buku merupakan data teks, dan machine learning model membutuhkan data numerik. TF-IDF merupakan teknik yang digunakan untuk mengubah teks menjadi representasi numerik.
   - Menggunakan `TfidfVectorizer()` dari scikit-learn.
   - `tf.fit(new_book['book_title'])` mempelajari kosakata dari judul buku.
   - `tf.get_feature_names_out()` menampilkan kata-kata yang dipertimbangkan.
   - `tfidf_matrix = tf.fit_transform(new_book['book_title'])` mengubah judul buku menjadi matriks TF-IDF. Ukuran matriks menunjukkan jumlah buku dan jumlah kata unik yang digunakan          sebagai fitur.
   - `tfidf_matrix.todense()` mengubah matriks TF-IDF yang tadinya dalam format sparse menjadi format dense (matriks biasa).
   - Membuat DataFrame dari matriks TF-IDF untuk melihat representasi numerik dari beberapa judul buku.
     
4. Mengatasi Missing Value :
   - Setelah menggabungkan dataset `ratings` dengan informasi buku dari dataset `books`, muncul nilai yang hilang (missing value) pada kolom `Book-Title` dan `Book-Author`.
   - Untuk menangani missing value ini, kode menggunakan metode `dropna()` pada DataFrame `books_all`. Metode ini akan menghapus baris-baris yang mengandung nilai yang hilang.
   - Pengecekan ulang missing value dilakukan setelah menggunakan `dropna()` untuk memastikan tidak ada lagi missing value.
     
5. Mengurutkan Data :
   - Data pada DataFrame yang sudah dibersihkan dari missing value `books_all_clean` diurutkan berdasarkan kolom `ISBN` secara menaik `ascending=True`. Hasil pengurutan ini disimpan dalam DataFrame baru bernama `preparation`.

6. Mengatasi Data Duplikat :
   - Setelah diurutkan, terdapat kemungkinan adanya data duplikat berdasarkan `ISBN`. Kode menggunakan metode `drop_duplicates('ISBN')` pada DataFrame `preparation` untuk menghapus baris-baris yang memiliki nilai ISBN yang sama, sehingga setiap buku hanya muncul sekali.

7. Konversi Data Series Menjadi List :
   - Kolom `ISBN`, `Book-Title`, dan `Book-Author` dari DataFrame `preparation` yang sudah bersih dan unik dikonversi menjadi list Python. Ini dilakukan untuk memudahkan akses dan penggunaan data dalam pembuatan model rekomendasi.
   - Panjang dari setiap list (jumlah `Book ID`, `Book Title`, dan `Book Author`) dicetak untuk memastikan jumlah data konsisten.
  
8. Membuat Dictionary Baru :
   - List `book_id`, `book_title`, dan `book_author` kemudian digunakan untuk membuat DataFrame baru bernama `new_book`.
   - DataFrame ini memiliki tiga kolom: `id` (untuk ISBN), `book_title`, dan `book_author`.
   - DataFrame `new_book` ini berisi informasi unik untuk setiap buku yang akan digunakan dalam pembangunan model *Content-Based Filtering*.
  
Data preparation Collaborative Filtering : 

1. Menggunakan Dataset Ratings :
   - Data awal yang digunakan untuk collaborative filtering merupakan dataset `ratings`.
   - Variabel `data` didefinisikan ulang untuk merujuk pada dataset `ratings`.
     
2. Mengubah User-ID menjadi List dan Encoding :
   -  Semua nilai unik dalam kolom `User-ID` dari dataset `data` diekstrak dan disimpan dalam list bernama `users_id`.
   - Kemudian, dilakukan "encoding" untuk `User-ID`. Ini berarti setiap `User-ID` unik diberikan representasi numerik berupa integer. `users_encoded` merupakan dictionary yang memetakan `User-ID` asli ke integer yang di-encode, sementara `users_encoded_to_user` adalah kebalikannya (memetakan integer ke `User-ID` asli). Ini diperlukan karena model machine learning bekerja lebih baik dengan input numerik.

3. Mengubah ISBN menjadi List dan Encoding :
   - Langkah yang serupa dilakukan untuk kolom `ISBN`. Nilai unik `ISBN` disimpan dalam list `books_id`.
   - Dilakukan encoding untuk `ISBN` menggunakan `books_to_book_encoded` (`ISBN` asli ke integer) dan `books_encoded_to_book` (integer ke `ISBN` asli).

4. Membuat Kolom Encoding Baru :
   - Dua kolom baru ditambahkan ke DataFrame `data: user dan book`.
Kolom user diisi dengan nilai integer yang di-encode dari kolom `User-ID` menggunakan dictionary `users_encoded`.
   - Kolom `book` diisi dengan nilai integer yang di-encode dari kolom `ISBN` menggunakan dictionary `books_to_book_encoded`. Ini menciptakan representasi numerik dari interaksi pengguna dan buku.
  
5. Mendapatkan Informasi Data :
   - Jumlah pengguna unik `(num_users)` dan jumlah buku unik `(num_book)` dihitung dari hasil encoding.
   - Nilai minimum `(min_rating)` dan maksimum `(max_rating)` dari kolom `Book-Rating` diidentifikasi.
   - Tipe data kolom `Book-Rating` diubah menjadi float32, yang umum digunakan dalam model deep learning.
   - Informasi mengenai jumlah pengguna, buku, serta rentang rating dicetak.

6. Normalisasi Rating :
   - Nilai rating dalam kolom `Book-Rating` dinormalisasi ke dalam rentang antara 0 dan 1. Rumus normalisasi yang digunakan adalah: `(x - min_rating)` / `(max_rating - min_rating)`. Normalisasi ini membantu model untuk belajar lebih efektif, terutama dengan fungsi aktivasi sigmoid pada output layer model.
  
7. Pembagian Data Training dan Validasi :
   - DataFrame `data` diacak secara acak `(sample(frac=1, random_state=42))` untuk memastikan distribusi data yang merata.
   - Data fitur `(X)` dibuat dari kolom `user dan book`, dan data target `(y)` dibuat dari kolom `Book-Rating` yang sudah dinormalisasi.
   - Data kemudian dibagi menjadi set pelatihan (80%) dan set validasi (20%) berdasarkan indeks. `X_train`, `y_train` untuk pelatihan, dan `X_val`, `y_val` untuk validasi.

## 5. Modeling 

Algoritma yang digunakan untuk menyelesaikan permasalahan serta menyajikan top-N recommendation sebagai solusi yaitu menggunakan algoritma *Content-Based Filtering* dan *Collaborative Filtering*. 

**Tujuan Content Based Filtering**

Content Based Filtering merupakan salah satu pendekatan dalam sistem rekomendasi yang merekomendasikan item kepada pengguna menggunakan fitur-fitur dari item itu sendiri. Ide dasarnya ialah jika seorang pengguna menyukai sebuah item dengan karakteristik tertentu, kemungkinan besar mereka juga akan menyukai item lain dengan karakteristik serupa. 

**Langkah-langkah dalam Model Development**

1. Pemilihan Fitur :
   - Fitur yang digunakan untuk *Content-Based Filtering* adalah `Book-Title`. Ini berarti model akan mencari kemiripan antara buku berdasarkan judulnya.
2. Mengukur Kemiripan dengan Cosine Similarity :
   - Setelah judul buku direpresentasikan sebagai vektor numerik, kemudian perlu mengukur seberapa mirip satu buku dengan buku lainnya.
   - Menggunakan `cosine_similarity(tfidf_matrix)` dari scikit-learn untuk menghitung matriks kemiripan antar semua pasangan buku berdasarkan matriks TF-IDF.
   - Matriks `cosine_similar` memiliki ukuran (jumlah buku) x (jumlah buku), di mana setiap elemen (i, j) adalah skor kemiripan antara buku i dan buku j.
   - Membuat DataFrame `df_cosine_similar` dari matriks kemiripan, dengan baris dan kolom diindeks oleh penulis buku untuk memudahkan interpretasi meskipun kemiripan dihitung berdasarkan judul buku.
3. Menghasilkan Rekomendasi :
   - Fungsi `book_recommendations` dibuat untuk menghasilkan rekomendasi.
   - Fungsi ini mengambil nama penulis (`author_name`), matriks kemiripan (`data_similarity`), DataFrame item (`items` yang berisi penulis dan judul buku), dan jumlah rekomendasi yang diinginkan (n) sebagai input.
   - `data_similarity.loc[:, author_name].to_numpy().argpartition(range(-1, -n, -1))` menemukan indeks dari `n` buku yang paling mirip dengan buku yang ditulis oleh `author_name`. `argpartition` efisien untuk menemukan indeks nilai terbesar tanpa mengurutkan seluruh array.
   - `closest = data_similarity.columns[index[-1:-(n+2):-1]]` mendapatkan nama penulis dari buku-buku yang paling mirip.
   - `closest = closest.drop(author_name, errors='ignore')` menghapus buku yang ditulis oleh penulis yang sama dari daftar rekomendasi, agar tidak merekomendasikan buku yang sudah dikenal pengguna (atau penulis yang sama).
   - Terakhir, `pd.DataFrame(closest).merge(items).head(n)` menggabungkan daftar penulis buku yang direkomendasikan dengan DataFrame `new_book` untuk mendapatkan judul buku yang sesuai dan menampilkan n rekomendasi teratas.
   - Kemudian menguji fungsi dengan mencari buku-buku oleh 'Peter Carey' dan kemudian mendapatkan rekomendasi berdasarkan penulis tersebut.

Parameter yang Digunakan : 
1. Cosine Similarity :

   a. `book_recommendations` function :
   - `author_name` : Nama penulis sebagai input untuk mencari rekomendasi.
   - `data_similarity` : DataFrame kemiripan konsinus.
   - `items` : DataFrame yang berisi `book_author` dan `book_title`.
   - `n=10` : Jumlah rekomendasi teratas yang akan ditampilkan.
     
     
![image](https://github.com/user-attachments/assets/164e8c26-79d3-4b05-a681-31dbf3939ef6)

Gambar 10 Mencari buku-buku oleh 'Peter Carey' 

![image](https://github.com/user-attachments/assets/7d156228-943f-408a-bf42-c6ab35accbb6)

Gambar 11 Rekomendasi buku berdasarkan penulis 'Peter Carey' 

Output dari fungsi gambar diatas menunjukkan bahwa daftar buku yang direkomendasikan kepada pengguna yang menyukai buku dari penulis 'Peter Carey'. Rekomendasi dihasilkan oleh model *Content-Based Filtering* yang bekerja dengan mencari buku-buku lain yang memiliki judul yang paling mirip dengan buku-buku yang ditulis oleh 'Peter Carey'. Dan model berhasil menemukan dan merekomendasikan buku-buku dari penulis lain seperti 'Willian Goldman' yang judulnya memiliki kemiripan tektual dengan buku yang ditulis oleh Peter Carey. Daftar rekomendasi ini juga memberikan alternatif bacaan bagi penggemar karya Peter Carey berdasarkan kesamaan dalam judul buku. 

Keuntungan *Content-Based Filtering* yaitu :
- Dapat merekomendasikan item niche yang mungkin tidak diminati oleh banyak pengguna lain.
- Dapat merekomendasikan item baru dengan cepat setelah tersedia, karena fitur-fiturnya sudah ada. 

**Tujuan Collaborative Filtering**

Collaborative Filtering merupakan pendekatan dalam sistem rekomendasi yang merekomendasikan item kepada pengguna berdasarkan preferensi atau perilaku pengguna lain yang serupa. Ide dasarnya ialah jika pengguna A memiliki preferensi yang mirip dengan pengguna B, maka item yang disukai oleh pengguna B yang belum pernah dilihat oleh pengguna A, kemungkinan besar juga akan disukai oleh pengguna A. 

**Langkah-langkah dalam Model Development** 

1. Pemilihan Data :
   - Menggunakan dataset `ratings`, yang berisi interaksi pengguna dengan buku dalam bentuk rating (`User-ID`, `ISBN`, `Book-Rating`). Ini adalah data kunci untuk Collaborative Filtering karena menunjukkan preferensi pengguna.

2. Data Preparation :
   - Encoding ID: Melakukan encoding untuk `User-ID` dan `ISBN` menjadi indeks numerik berurutan (mulai dari 0).
        - `users_encoded` : Mapping dari `User-ID` asli ke indeks numerik.
        - `users_encoded_to_user` : Mapping dari indeks numerik kembali ke `User-ID` asli.
        - `books_to_book_encoded` : Mapping dari `ISBN` asli ke indeks numerik.
        - `books_encoded_to_book` : Mapping dari indeks numerik kembali ke `ISBN` asli.
        - Menambahkan kolom baru `'user'` dan `'book'` ke DataFrame data yang berisi ID yang sudah di-encode.
   - Jumlah Pengguna dan Buku : Menghitung jumlah pengguna dan buku unik setelah encoding. Untuk mendefinisikan ukuran layer embedding dalam model.
   - Normalisasi Rating : Rating (`Book-Rating`) dinormalisasi ke dalam rentang [0, 1] menggunakan skala minimum dan maksimum rating yang ditemukan dalam data. Normalisasi ini membantu model untuk belajar lebih efektif, terutama saat menggunakan fungsi aktivasi sigmoid pada output.
   - Pemecahan Data : Membagi data yang sudah disiapkan menjadi set training (`X_train, y_train`) dan set validasi (`X_val, y_val`). Data diacak (`data.sample(frac=1, random_state=42`)) sebelum dibagi untuk memastikan distribusi yang baik. Input X terdiri dari pasangan (`user` yang di-encode, `book` yang di-encode), dan target `y` merupakan rating yang dinormalisasi.

3. Pembangunan Model (RecommenderNet) :
   - Mendefinisikan model kustom menggunakan TensorFlow/Keras, bernama RecommenderNet.
   - Model terdiri dari beberapa layer embedding:
     1. `user_embedding` : Layer embedding untuk pengguna. Setiap pengguna diwakili oleh sebuah vektor (embedding) berdimensi `embedding_size`. Ukuran input layer ini adalah jumlah pengguna (`num_users`).
     2. `user_bias` : Layer embedding untuk bias pengguna. Setiap pengguna memiliki sebuah nilai bias skalar. Ukuran input layer ini adalah jumlah pengguna (`num_users`).
     3. `book_embedding` : Layer embedding untuk buku. Setiap buku diwakili oleh sebuah vektor (embedding) berdimensi `embedding_size`. Ukuran input layer ini adalah jumlah buku (`num_book`).
     4. `book_bias` : Layer embedding untuk bias buku. Setiap buku memiliki sebuah nilai bias skalar. Ukuran input layer ini adalah jumlah buku (`num_book`).
     5. `call` : Metode `call` mendefinisikan bagaimana input diproses oleh model.
     6. `tf.tensordot(user_vector, book_vector, 2)` menghitung perkalian dot antara vektor embedding pengguna dan buku. Perkalian dot ini mengukur kompatibilitas antara pengguna dan buku dalam ruang embedding.
     7. `X = dot_user_book + user_bias + book_bias` menggabungkan hasil perkalian dot dengan bias pengguna dan bias buku. Ini menghasilkan prediksi rating sebelum aktivasi.
     8. `tf.nn.sigmoid(X)` menerapkan fungsi aktivasi sigmoid pada hasil. Karena rating dinormalisasi ke [0, 1], sigmoid (yang menghasilkan output dalam rentang [0, 1]) adalah pilihan yang tepat untuk memprediksi rating yang dinormalisasi.

4. Kompilasi Model :
   - `loss = tf.keras.losses.BinaryCrossentropy()` : Binary Crossentropy digunakan karena output model adalah nilai antara 0 dan 1 (setelah sigmoid) yang dapat diinterpretasikan sebagai probabilitas atau skor kecocokan. Ini merupakan pendekatan umum dalam sistem rekomendasi berbasis embedding.
   - `optimizer = keras.optimizers.Adam(learning_rate=0.001)` : Optimizer Adam digunakan untuk memperbarui bobot model selama pelatihan.
   - `metrics=[tf.keras.metrics.RootMeanSquaredError()]` : RMSE digunakan sebagai metrik evaluasi selama pelatihan untuk mengukur seberapa besar perbedaan antara rating prediksi dan rating sebenarnya.

5. Pelatihan Model :
   - `history = model.fit(...)` melatih model menggunakan data training (`X_train, y_train`) dan memvalidasinya pada data validasi (`X_val, y_val`) selama 100 epoch dengan ukuran batch 8.

6. Mendapatkan Rekomendasi :
   - Mengidentifikasi buku-buku yang belum pernah dilihat oleh pengguna (`book_not_visited`).
   - Untuk setiap buku yang belum dilihat, membuat pasangan input (`user_encoder`, `book_encoder`) dan menggabungkannya menjadi array (`user_book_array`).
   - `rating = model.predict(user_book_array).flatten()` menggunakan model yang sudah dilatih untuk memprediksi rating yang dinormalisasi yang mungkin diberikan pengguna untuk setiap buku yang belum dilihat. `flatten()` mengubah output menjadi array 1D.
   - `top_rating_indices = rating.argsort()[-10:][::-1]` mendapatkan indeks dari 10 rating prediksi tertinggi.
   - `recommended_book_ids = [...]` mengonversi kembali indeks buku yang di-encode menjadi `ISBN` asli.
   - Kemudian menampilkan buku-buku yang paling sering diberi rating tinggi oleh pengguna tersebut (berdasarkan data history) dan membandingkannya dengan 10 buku yang direkomendasikan oleh model *Collaborative Filtering*.
  
Parameter yang Digunakan : 

2. `RecommenderNet` class :
- `num_users` : Jumlah total pengguna unik dalam dataset.
- `num_book` : Jumlah total buku unik dalam dataset.
- `embedding_size` : Dimensi (ukuran) vektor embedding untuk pengguna dan buku. Dalam kode, ini diatur ke `50`.
- Loss Function: `tf.keras.losses.BinaryCrossentropy()`. Digunakan untuk membuat kemiripan dengan memprediksi probabilitas rating tinggi.
- Optimizer : `keras.optimizers.Adam(learning_rate=0.001)`. Adam adalah optimizer populer yang adaptif, secara otomatis menyesuaikan tingkat pembelajaran selama pelatihan.
- Metrik Evaluasi: `tf.keras.metrics.RootMeanSquaredError()`. RMSE digunakan selama pelatihan untuk mengukur seberapa baik model memprediksi rating sebenarnya.
- Batch Size (`batch_size=8`) : Jumlah pasangan pengguna-buku yang diproses dalam satu iterasi pelatihan.
- `epochs=100` : Jumlah iterasi penuh melalui seluruh dataset pelatihan.
- Validation Data (`validation_data = (X_val, y_val`)): Data yang digunakan untuk mengevaluasi kinerja model setelah setiap epoch dan memantau overfitting.

![image](https://github.com/user-attachments/assets/2bb21a39-4c2d-46ed-bf8b-434b6c423b0e)

Gambar 12 10 Rekomendasi Teratas berdasarkan Book Author

Buku-buku dalam daftar rekomendasi model memiliki genre, penulis atau tema yang mirip dengan buku-buku yang disukai pengguna di masa lalu, hal ini menunjukkan bahwa model telah berhasil mempelajari pola preferensi pengguna dan merekomendasikan buku-buku yang relevan. Dan output tersebut menunjukkan rekomendasi berdasarkan Book Author dan Book Title. 

Keuntungan *Collaborative Filtering* yaitu : 
- Dapat merekomendasikan item yang mungkin tidak memiliki fitur yang jelas mirip dengan item yang disukai pengguna sebelumnya.
- Tidak memerlukan informasi fitur dari item, hanya data interaksi pengguna.
- Mempertimbangkan perilaku pengguna secara keseluruhan untuk menemukan pola dan kemiripan.

## 6. Evaluasi 

6.1 Metrik evaluasi Content-Based Filtering : 

1. Precision@k : mengukur berapa banyak item yang direkomendasikan di antara k item teratas yang sebenarnya relevan bagi pengguna, yaitu buku yang disukai pengguna di set pengujian. Rumusnya adalah :

   $Precision@k = {Jumlah item yang direkomendasikan yang relevan} / {Jumlah item yang direkomendasikan} (k) . 100%

   - Hasil : 0.0074

2. Recall@k: mengukur berapa banyak item relevan di set pengujian yang berhasil ditangkap oleh rekomendasi k teratas. Rumusnya adalah:

   $Recall@k = {Jumlah item yang direkomendasikan yang relevan} / {Jumlah item relevan di set pengujian}

   - Hasil : 0.0556

Hasil evaluasi menunjukkan bahwa rata-rata sekitar **0.74%** dari 10 rekomendasi teratas yang diberikan oleh model *Content-Based Filtering* relevan bagi pengguna, dan model berhasil merekomendasikan sekitar **5.56%** dari total buku yang disukai pengguna dalam 10 rekomendasi teratas. Nilai ini dihitung pada pengguna yang memiliki buku disukai di set pengujian dan juga memiliki setidaknya satu buku disukai di set pelatihan untuk mendasari rekomendasi.

Metrik ini umum digunakan dalam sistem rekomendasi untuk mengukur seberapa baik model dalam memberikan item yang disukai pengguna. Precision@k fokus pada akurasi dari rekomendasi teratas, sementara Recall@k fokus pada kemampuan model untuk menemukan semua item relevan yang mungkin diminati pengguna. 

6.2 Metrik Evaluasi Collaborative Filtering : 

1. Metrik RMSE (Root Mean Square Error) untuk mengevaluasi kinerja model yang dihasilkan. RMSE merupakan akar kuadrat dari MSE, memberikan skala yang sama dengan variabel target. RMSE memberikan gambaran tentang seberapa dekat prediksi dengan nilai sebenarnya dalam unit yang sama seperti variabel target [[9]](https://www.google.co.id/books/edition/EKSPLORASI_MACHINE_LEARNING_DENGAN_SCIKI/8GsWEQAAQBAJ?hl=id&gbpv=1&dq=definisi+RMSE&pg=PA75&printsec=frontcover). Seperti MSE, semakin rendah nilai RMSE, semakin baik performa modelnya. 

![image](https://github.com/user-attachments/assets/60b3e006-e5ac-4c02-be14-2c22d90397ad)

Gambar 13 Rumus RMSE 

Berikut merupakan plot metrik RMSE setelah proses pelatihan model.

![image](https://github.com/user-attachments/assets/c0a4e6e8-0cf4-4870-a584-9aab2e7af24b)

Gambar 14 Plot RMSE 

Plot di atas menunjukkan bahwa nilai error akhir yang di dapatkan sekitar 0.30 dan error pada data validasi kurang dari 0.10. Dan nilai ini bisa dibilang cukup bagus untuk sistem rekomendasi. 

2. MSE (Mean Squared Error) merupakan rata-rata dari kuadrat perbedaan antara prediksi dan nilai sebenarnya [[10]](https://www.google.co.id/books/edition/Memahami_Konsep_dan_Implementasi_Machine/_831EAAAQBAJ?hl=id&gbpv=1&dq=definisi+MSE&pg=PA29&printsec=frontcover).

![image](https://github.com/user-attachments/assets/ea7a9e32-c804-4a33-b55e-7e2116968da7)

Gambar 15 Hasil MSE

Berdasarkan gambar di atas MSE dari data train yaitu 0.0292 dan MSE dari data validation yaitu 0.0880.


## Referensi 

1. ALKAFF, Muhammad; KHATIMI, Husnul; ERIADI, Andi. Sistem Rekomendasi Buku pada Perpustakaan Daerah Provinsi Kalimantan Selatan Menggunakan Metode Content-Based Filtering. MATRIK: Jurnal Manajemen, Teknik Informatika dan Rekayasa Komputer, 2020, 20.1: 193-202.
2. ARDIANSYAH, Ryky; BIANTO, Mufti Ari; SAPUTRA, Bagus Dwi. Sistem Rekomendasi Buku Perpustakaan Sekolah menggunakan Metode Content-Based Filtering. Jurnal CoSciTech (Computer Science and Information Technology), 2023, 4.2: 510-518.
3. BIANTO, Mufti Ari; KUSRINI, Kusrini; SUDARMAWAN, Sudarmawan. Perancangan Sistem Klasifikasi Penyakit Jantung Mengunakan Naïve Bayes. Creative Information Technology Journal, 2020, 6.1: 75-83.
4. REDDY, S. R. S., et al. Content-based movie recommendation system using genre correlation. In: Smart Intelligent Computing and Applications: Proceedings of the Second International Conference on SCI 2018, Volume 2. Springer Singapore, 2019. p. 391-397.
5. WIJAYA, Anderias Eko; ALFIAN, Deni. Sistem Rekomendasi Laptop Menggunakan Collaborative Filtering Dan Content-Based Filtering. Jurnal Computech & Bisnis, 2018, 12.1: 11-27.
6. CHOLIL, Saifur Rohman; RIZKI, Novita Aria; HANIFAH, Trinanda Fajri. Sistem Rekomendasi Tempat Wisata Di Kota Semarang Menggunakan Metode Collaborative Filtering. JIKO (Jurnal Informatika dan Komputer), 2023, 7.1: 118-125.
7. EKSPLORASI MACHINE LEARNING DENGAN SCIKIT-LEARN Strategi Belajar Machine Learning. (2024). (n.p.): Uwais Inspirasi Indonesia.
8. Memahami Konsep dan Implementasi Machine Learning. (2024). (n.p.): PT. Sonpedia Publishing Indonesia.
























