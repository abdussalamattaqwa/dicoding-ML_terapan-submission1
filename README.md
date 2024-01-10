Nama : Abd Salam At Taqwa

Sumber dataset : https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition

#Laporan Proyek Machine Learning - Abd Salam At Taqwa

##Domain Proyek

###Latar Belakang

Pola makan dalam kehidupan seseorang harus lebih diperhatikan karena pola makan yang tidak sehat dapat menyebabkan berbagai macam penyakit, salah satunya adalah obesitas. Obesitas merupakan suatu kondisi dimana lemak menumpuk atau berlebihan sehingga dapat berdampak buruk bagi kesehatan. Kegagalan untuk segera mengatasi obesitas dapat meningkatkan risiko penyakit jantung, tekanan darah tinggi, dan diabetes.

Suatu cara untuk mengatasi obesitas adalah menjaga dan memonitor pola makan dan aktifitas kondisi fisik dalam kehidupan sehari-hari. Ada beberapa faktor yang mempengaruhi pola makan seseorang, diantaranya adalah Frekuensi konsumsi makanan berkalori tinggi (FAVC), Frekuensi konsumsi sayuran (FCVC), Jumlah makanan utama (NCP), Konsumsi makanan di antara waktu makan (CAEC), Konsumsi air setiap hari (CH20), dan Konsumsi alkohol (CALC).

Selain dari pola makan faktor-faktor yang terkait pada kondisi fisik adalah: Pemantauan konsumsi kalori (SCC), Frekuensi aktivitas fisik (FAF), Waktu penggunaan menggunakan perangkat teknologi (TUE), Transportasi yang digunakan (MTRANS), variabel lain yang diperoleh adalah: Jenis Kelamin, Usia, Tinggi dan Berat Badan.

Faktor-faktor pola makan dan kondisi fisik tersebut perlu di perhatikan lebih baik untuk mencegah obesitas. Apabila faktor tersebut tidak diperhatikan dapat dengan mudah mengalami obesitas tanpa disadari. Oleh karena itu perlunya sebuah model yang dapat memprediksi obesitas seseorang berdasarkan faktor-faktor atau atribut tersebut. Hal ini dapat memudahkan manusia untuk memonitoring dan mencegah atau memperbaiki lebih awal ketika pola makan dan kondisi fisik tidak baik.


##Business Understanding
Proyek ini dibangun untuk mengatur pola makan dan kondisi fisik seseorang untuk mencegah obesitas. Data dari pola makan dan kondisi fisik dapat digunakan untuk memprediksi tingkatan dari obesitas seseorang. Hasil dari prediksi obesitas dapat dijadikan sebagai acuan untuk mengatur atau memperbaiki pola makan dan kondisi fisik sebelum penyakit obesitas bertambah parah.


##Problem Statements
Menjelaskan pernyataan masalah latar belakang:

* Faktor atau fitur apa yang paling mempengaruhi obesitas seseorang?
* Bagaimana karakteristik obesitas seseorang dengan pola makan dan kondisi fisik tertentu?

##Goals
* Mengetahui faktor yang paling berpengaruh terhadap obesitas seseorang
* Membangun sebuah model yang dapat memprediksi tingkat obesitas seseorang berdasarkan riwayat pola makan dan kondisi fisik seseorang

## Solution statements
* Melakukan Exploratory Data Analysis terhadap semua faktor atau variabel untuk menemumak varibel yang paling berpengaruh terhadap penentuan tingkat obesitas seseorang
* Membangun 3 model machine learning sederhana dan memilih yang terbaik untuk memprediksi obesitas berdasarkan riwayat pola makan dan kondisi fisik

##Data Understanding & Removing Outlier
Dataset yang digunakan dalam proyek ini merupakan data pola makanan dan kondisi fisik yang memiliki kriteria tingkat obesitasnya masing-masing. Dataset ini sudah tersedia dan dapat diunduh pada [UCI Machine learning](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition).

Berikut informasi pada dataset :

* Dataset memiliki format CSV (Comma-Seperated Values).
* Dataset memiliki 2111 sample dengan 16 fitur.
* Dataset memiliki 4 fitur bertipe categorical 6 fitur bertipe data continuous, 4 bertipe data binary, dan 2 tipe data integer.
* Tidak ada missing value dalam dataset.

##Variable - variable pada dataset
* Gender : Jenis kelamin
* Age : Umur  
* Height : Tinggi badan
* Weight : Berat badan
* family_history_with_overweight : riwayat keluarga dengan kelebihan berat badan
* FAVC : Sering konsumsi makanan berkalori tinggi
* FCVC : Frekuensi konsumsi sayuran
* NCP  : Jumlah makanan utama
* CAEC : Konsumsi makanan di antara waktu makan
* SMOKE : Perokok atau tidak merokok
* CH2O : Konsumsi air setiap hari
* SCC  : Pemantauan konsumsi kalori
* FAF : Frekuensi aktivitas fisik
* TUE  : Waktu menggunakan perangkat teknologi
* CALC : Konsumsi alkohol
* MTRANS : Transportasi yang digunakan
* NObeyesdad  : Label tingkat obesitas

## Exploratory Data Analysis
### Assessing Data
Melihat informasi dataset
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/35cb6e80-a58b-453d-99b5-89d443a5cb4b)
Dapat dilihat fitur-fitur yang terdapat pada dataset dan tipe data yang terbaca

Melihat jumlah nilai null pada masing-masing kolom
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/b8c7611c-bbbf-4790-95c6-9dcbca08719a)
Berdasarkan hasil diatas dapat dilihat bahwa tidak terdapat nilai null pada dataset

![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/c104ff62-e1d7-4fe1-ab7f-ce051adcb83c)
Melihat deskripsi data untuk menganalisis penyebaran data masing-masing fitur dengan tipe data integeruntuk melihat apakah ada anomali data
Berdasarkan hasil didapatkan bahwa tidak terdapat data anomali atau data tidak jelas pada dataset

Visualisasi jenis kelamin yang dominan pada data untuk melihat ukuran data berdasarkan gender
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/401e295b-f486-404b-9087-61fc09fb31cb)
Berdasarkan hasil visualisasi diatas dapat dilihat bahwa data termasuk seimbang karena data laki-laki dan perempuan memiliki ukuran yang hampir sama. Jadi data cukup baik untuk digunakan untuk model machine learning

## Data Preparation
### Label Encoder
Untuk mengonversi label kata menjadi angka, kita perlu menggunakan pembuat label encoding. label encoding mengacu pada proses transformasi label kata menjadi bentuk numerik. Mengkonfersi data-data objek yang bersifat kategorikal menjadi numeric bertujuan agar dengan mudah dipahami model
### Train Test Split
Train test split adalah teknik umum yang digunakan dalam pembelajaran mesin untuk membagi data menjadi set pelatihan dan tes. Proses ini penting dalam proses pemodelan data, karena memungkinkan kita untuk menilai kinerja model pada data yang tidak terlihat. Ini juga membantu mencegah overfitting, yang terjadi ketika model berkinerja baik pada data pelatihan tetapi gagal menggeneralisasi ke data baru.

## Modelling
Pada proyek ini menggunakan 3 model machine learning sebagai perbandingan untuk menentukan model terbaik yang akan digunakan
* Algoritma K-Nearest Neighbor (KNN) adalah algoritma machine learning yang bersifat non-parametric dan lazy learning. Metode yang bersifat non-parametric memiliki makna bahwa metode tersebut tidak membuat asumsi apa pun tentang distribusi data yang mendasarinya. Dengan kata lain, tidak ada jumlah parameter atau estimasi parameter yang tetap dalam model, terlepas data tersebut berukuran kecil ataupun besar. Parameter yang digunakan pada algoritma ini adalah
+ `n_neighbors` = Jumlah k tetangga tedekat.
* Algoritma Random Forest merupakan salah satu metode machine learning yang menggunakan pohon keputusan dengan pengambilan data sampel secara acak. Parameter yang digunakan pada algoritma ini adalah
+ `n_estimators` = Jumlah maksimum estimator keputusan di mana boosting dihentikan.
+ `max_depth` = Kedalaman maksimum setiap pohon.
+ `random_state` = Mengontrol seed acak yang diberikan pada setiap iterasi boosting.
* Algoritma AdaBoost, singkatan dari Adaptive Boosting, adalah sebuah teknik Boosting yang digunakan sebagai metode ensemble dalam machine learning. Algoritma ini disebut Adaptive Boosting karena bobot diberikan ulang pada setiap instance, dengan bobot yang lebih tinggi diberikan pada instance yang salah diklasifikasikan. Parameter yang digunakan pada algoritma ini adalah
+ `n_estimators` = Jumlah maksimum estimator di mana boosting dihentikan.
+ `learning_rate` = Inisial learning rate yang digunakan untuk setiap perubahan bobot pada setiap iterasi pembelajaran.
+ `random_state` = Mengontrol seed acak yang diberikan pada setiap iterasi boosting.

* GRID Search
Grid search adalah suatu cara untuk menemukan parameter terbaik yang digunakan untuk modeling dalam machin learning. Menggunakan grid search dapat mambantu dalam mencari hyperparameter terbaik yang digunakan untuk modeling di suatu algoritma machine learning. Adapun hasil dari algoritdma grid search pada proyek ini sebagai berikut
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/a59c1bc8-2598-4328-a100-d05c1572e2d1)


## Evaluation
Mean Squared Error (MSE) digunakan sebagai metrik evaluasi pada proyek ini. MSE adalah metrik evaluasi yang umum digunakan dalam statistik dan machine learning untuk mengukur seberapa akurat sebuah model regresi dalam memprediksi nilai numerik. MSE menghitung selisih antara nilai prediksi model dan nilai sebenarnya dari data, kemudian mengkuadratkan selisih tersebut agar tidak ada selisih yang bernilai negatif. Kemudian, selisih kuadrat dijumlahkan dan diambil rata-rata dari semua sampel data.
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/53af2296-44b8-40f3-91a0-b1b3ce5bfd93)
Berikut hasil evaluasi pada proyek ini
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/a4f3561b-b1bb-42a1-bf98-ae61443bc688)
Adapun grafik perbandingan error untuk setiap model dapat dilihat sebagai berikut
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/4e19ef12-ba70-41fb-956d-ef6a9b610f40)
berdasarkan hasil diatas dapat disimpulkan bahwa model terbaik yang dapat digunakan untuk prediksi tingkat obesitas seseorang adalah menggunakan model Random Forest yang memiliki error terkecil dibandingkan model yang lainnya


