Nama : Abd Salam At Taqwa

# Laporan Proyek *Machine Learning* - Abd Salam At Taqwa

## Domain Proyek

### Latar Belakang

Kebiasaan makan dalam kehidupan seseorang harus lebih diperhatikan karena pola makan yang tidak sehat dapat menyebabkan berbagai macam penyakit, salah satunya adalah obesitas. Obesitas merupakan suatu kondisi dimana lemak menumpuk atau berlebihan sehingga dapat berdampak buruk bagi kesehatan. Kegagalan untuk segera mengatasi obesitas dapat meningkatkan risiko penyakit jantung, tekanan darah tinggi, dan diabetes. Obesitas menyebabkan berbagai masalah di berbagai bidang (kesehatan, demografi, tenaga kerja, keluarga, dan ekonomi) [[1](https://www.mdpi.com/2075-4418/13/18/2949). Menurut [WHO [2]](https://www.who.int/news-room/fact-sheets/detail/obesity-and-overweight) tingkat obesitas global meningkat hampir tiga kali lipat sejak tahun 1975. Pada tahun 2016, lebih dari 1,9 miliar orang dewasa berusia 18 tahun ke atas mengalami kelebihan berat badan. Lebih dari 650 juta orang di antaranya mengalami obesitas. Pada tahun 2016, 39% orang dewasa berusia di atas 18 tahun  mengalami kelebihan berat badan  dan 13% mengalami obesitas. Sebagian besar penduduk dunia tinggal di negara-negara dimana lebih banyak orang meninggal karena kelebihan berat badan atau obesitas  dibandingkan karena kekurangan berat badan. Pada tahun 2020, 39 juta anak di bawah usia lima tahun mengalami kelebihan berat badan atau obesitas. Pada tahun 2016, lebih dari 340 juta anak-anak dan remaja berusia antara 5 dan 19 tahun mengalami kelebihan berat badan atau obesitas. Menurut [Kementrian Kesehatan Republik Indonesia [3]](https://ayosehat.kemkes.go.id/pub/files/0b43c48e8765bf62a02f42a1359349d5.pdf) pada tahun 2030 diperkirakan 1 dari 5 wanita dan 1 dari 7 pria akan hidup dengan obesitas (setara dengan lebih dari 1 miliar orang di seluruh dunia. Prevalensi obesitas global lebih tinggi pada perempuan dibanding laki-laki dan jumlah terbesar orang dengan obesitas berada di negara berkembang, di mana beban ganda malnutrisi terus berlanjut dan sistem sangat kurang siap dan tidak dilengkapi dengan baik untuk mengatasi obesitas dan konsekuensinya secara efektif.

Untuk mengatasi masalah penyakit obesitas ini, lembaga dan perusahaan swasta, serta organisasi internasional mendorong untuk pencegahan dan pengobatan yang berfokus pada aktivitas fisik dan kebiasaan gizi [[4]](https://www.mdpi.com/1660-4601/18/19/10187), karena keduanya merupakan dua faktor risiko utama dalam mencegah penyakit obesitas. Pada penelitian [ [5] ](https://www.sciencedirect.com/science/article/pii/S2352340919306985?via%3Dihub) telah mengumpulkan dataset berdasarkan kebiasan makan dan kondisi fisik untuk setiap tingkat obesitas berdasarkan standar WHO. Masing-masing data yang didapatkan dihitung tingkat BMInya, kemudian kriteria WHO diterapkan untuk mengklasifikasikan tingkat obesitas sebagai berikut: berat badan kurang = BMI kurang dari 18,5; normal = BMI antara 18,5 dan 24,9; kelebihan berat badan = BMI antara 25,0 dan 29,9; obesitas I = BMI antara 30,0 dan 34,9; obesitas II = BMI antara 35,0 dan 39,9; dan obesitas III = BMI lebih tinggi dari 40. Kriteria WHO didasarkan pada hubungan antara BMI dan risiko penyakit kronis dan kematian.

Fitur yang digunakan untuk kebiasaan makan pada dataset tersebut adalah Frekuensi konsumsi makanan berkalori tinggi (FAVC), Frekuensi konsumsi sayuran (FCVC), Jumlah makanan utama (NCP), Konsumsi makanan di antara waktu makan (CAEC), Konsumsi air setiap hari (CH20), dan Konsumsi alkohol (CALC). Selain dari pola makan fitur terkait pada kondisi fisik uang juga digunakan pada dataset adalah: Pemantauan konsumsi kalori (SCC), Frekuensi aktivitas fisik (FAF), Waktu penggunaan menggunakan perangkat teknologi (TUE), Transportasi yang digunakan (MTRANS), variabel lain yang diperoleh adalah: Jenis Kelamin, Usia, Tinggi dan Berat Badan.

Pada proyek ini dibangun sebuah model pembelajaran untuk memprediksi tingkat obesitas seseorang berdasarkan kebiasan makan dan kondisi fisik seseorang. Hal ini dapat memudahkan manusia untuk memonitoring tingkat obesitas seseorang sehingga mendapatkan tingkat obesitas yang ideal dan membantu untuk mencegah tingkat obesitas meningkat.


## *Business Understanding*
Proyek ini dibangun untuk mengatur kebiasaan makan dan kondisi fisik seseorang agar mendapatkan tingkat obesitas yang ideal. Data dari kebiasaan makan dan kondisi fisik dapat digunakan untuk memprediksi tingkatan dari obesitas seseorang. Hasil dari prediksi tingkatan obesitas dapat dijadikan sebagai acuan untuk mengatur atau memperbaiki kebiasaa makan dan kondisi fisik sebelum penyakit obesitas bertambah parah. Ketika model memprediksi hasil tingkat obesitas yang tinggi pada seseorang hasil tersebut bisa dijadikan peringatan untuk memperbaiki kebiasaan makan dan aktifitas fisik. Seseorang dapat memperbaiki kebiasan tersebut hingga model memprediksi bahwa tingkat obesitas orang tersebut ideal. Model prediksi tingkat obesitas ini diharapkan mampu meningkatkan kesadaran masyarakat terhadap kebiasaan makan dan aktifitas fisik untuk mencegah tingginya tingkat obesitas seseorang.


## *Problem Statements*
Adapun masalah yang bisa diangkat berdasarkan latar belakang adalah:
* Bagaimana memperbaiki kebiasaan makan dan kondisi fisik seseorang untuk mencegah tingginya tingkat obesitas?
* Bagaimana memilih model terbaik untuk memprediksi tingkat obesitas seseorang?

## *Goals*
* Membangun sebuah model yang dapat memprediksi tingkat obesitas seseorang untuk memberikan rekomendasi bagaimana kebiasaan makan dan kondisi fisik yang baik sebagai pencegahan tingginya tingkat obesitas seseorang.
* Memilih model prediksi yang terbaik berdasarkan tingkat kesalahan dari MSE yang terkecil

## *Solution statements*
* Membangun 3 model machine learning sederhana untuk memprediksi tingkat obesitas seseorang
* Memilih model machine learning yang terbaik berdasarkan tingkat kesalahan terkecil dari MSE

## *Data Understanding & Removing Outlier*
Dataset yang digunakan dalam proyek ini merupakan data kebiasaan makan dan kondisi fisik yang memiliki kriteria tingkat obesitasnya masing-masing. Dataset ini sudah tersedia dan dapat diunduh pada [UCI *Machine learning*](https://archive.ics.uci.edu/dataset/544/estimation+of+obesity+levels+based+on+eating+habits+and+physical+condition).

Berikut informasi pada dataset :
* Dataset memiliki format CSV (*Comma-Seperated Values*).
* Dataset memiliki 2111 sample dengan 16 fitur.
* Dataset memiliki 4 fitur bertipe categorical 6 fitur bertipe data *continuous*, 4 bertipe data *binary*, dan 2 tipe data *integer*.
* Tidak ada *missing value* dalam dataset.

## Variabel- variabel pada dataset
* *Gender* : Jenis kelamin
* *Age* : Umur  
* *Height* : Tinggi badan
* *Weight* : Berat badan
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

## *Exploratory Data Analysis*
### *Assessing Data*
Sebelum melakukan *exploratory* pertama-tama dilakukan penilaian terhadap informasi dataset yang dapat dilihat pada Tabel 1.
<br> Tabel 1. Informasi dataset
| No |  Column                         | Non-Null Count | Dtype | 
| --- | ------                        | -------------- | -----  |
| 1 |  Gender                         | 2111 non-null  | object |
| 2 |  Age                            | 2111 non-null  | float64 |
| 3 |  Height                         | 2111 non-null  | float64 |
| 4 |  Weight                         | 2111 non-null  | float64 |
| 5 |  family_history_with_overweight | 2111 non-null  | object | 
| 6 |  FAVC                           | 2111 non-null  | object |
| 7 |  FCVC                           | 2111 non-null  | float64 |
| 8 |  NCP                            | 2111 non-null  | float64 |
| 9 |  CAEC                           | 2111 non-null  | object |
| 10 |  SMOKE                          | 2111 non-null  | object |
| 11 |  CH2O                          | 2111 non-null  | float64 |
| 12 |  SCC                           | 2111 non-null  | object |
| 13 |  FAF                           | 2111 non-null  | float64 |
| 14 | TUE                            | 2111 non-null  | float64 |
| 15 | CALC                           | 2111 non-null  | object |
| 16 | MTRANS                         | 2111 non-null  | object|

Tabel 1 diatas menunjukkan kolom atau fitur-fitur pada dataset yang akan digunakan beserta informasi jumlah data yaitu 2111 dan tipe data masing-masing fitur yang akan digunakan pada model. Langkah selanjutnya adalah melihat jumlah nilai *null* pada masing-masing kolom. Tujuan untuk pengecekan ini adalah untuk melakukan penanganan jika terdapat nilai *null* atau data yang hilang pada dataset. Penyebab data yang hilang dapat berupa kerusakan data atau kegagalan pencatatan data. Penanganan data yang hilang sangat penting selama prapemrosesan kumpulan data karena banyak algoritma *machine learning* tidak mendukung nilai yang hilang. Hasil dari perhitungan nilai *null* pada setiap kolom dapat dilihat pada Tabel 2 berikut.
<br> Tabel 2. Jumlah nilai *null* masing-masing kolom
|Column                           | Total |
| ----                             |---|
|Gender                           | 0 |
|Age                              | 0 |
|Height                           | 0 |
|Weight                           | 0 |
|family_history_with_overweight   | 0 |
|FAVC                             | 0 |
|FCVC                             | 0 |
|NCP                              | 0 |
|CAEC                             | 0 |
|SMOKE                            | 0 |
|CH2O                             | 0 |
|SCC                              | 0 |
|FAF                              | 0 |
|TUE                              | 0 |
|CALC                             | 0 |
|MTRANS                           | 0 |

Berdasarkan hasil diatas dapat dilihat bahwa tidak terdapat nilai *null* pada dataset. Sehingga tidak perlu dilakukan penanganan untuk nilai *null* atau data yang hilang. Langkah selanjutnya adalah melihat deskripsi data untuk kolom-kolom dengan tipe data numerik yang dapat dilihat pada Tabel 3 berikut .
<br> Tabel 3. Deskripsi Data
|index|Gender|Age|Height|Weight|family\_history\_with\_overweight|FAVC|FCVC|NCP|CAEC|SMOKE|CH2O|SCC|FAF|TUE|CALC|MTRANS|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|count|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|2111\.0|
|mean|0\.5059213642823307|24\.312599908574136|1\.7016773533870204|86\.58605812648035|0\.817621980104216|0\.8839412600663192|2\.4190430615821885|2\.6856280497394596|1\.8593083846518237|0\.020843202273803884|2\.0080114040738986|0\.045476077688299386|1\.0102976958787304|0\.657865923732828|2\.2685930838465183|2\.3652297489341545|
|std|0\.5000833972849265|6\.345968273732234|0\.09330481986792007|26\.1911717452047|0\.3862472640373802|0\.3203712366137241|0\.5339265785033002|0\.7780386488418612|0\.4685434677350143|0\.14289309147889065|0\.6129534517968722|0\.208395241212829|0\.850592430836698|0\.6089272596763782|0\.5154980665488972|1\.2614232283157334|
|min|0\.0|14\.0|1\.45|39\.0|0\.0|0\.0|1\.0|1\.0|0\.0|0\.0|1\.0|0\.0|0\.0|0\.0|0\.0|0\.0|
|25%|0\.0|19\.947192|1\.63|65\.473343|1\.0|1\.0|2\.0|2\.658738|2\.0|0\.0|1\.5848125|0\.0|0\.124505|0\.0|2\.0|3\.0|
|50%|1\.0|22\.77789|1\.700499|83\.0|1\.0|1\.0|2\.385502|3\.0|2\.0|0\.0|2\.0|0\.0|1\.0|0\.62535|2\.0|3\.0|
|75%|1\.0|26\.0|1\.768464|107\.430682|1\.0|1\.0|3\.0|3\.0|2\.0|0\.0|2\.47742|0\.0|1\.6666775|1\.0|3\.0|3\.0|
|max|1\.0|61\.0|1\.98|173\.0|1\.0|1\.0|3\.0|4\.0|3\.0|1\.0|3\.0|1\.0|3\.0|2\.0|3\.0|4\.0|

Tabel 3 diatas adalah untuk menganalisis penyebaran data masing-masing fitur dengan tipe data *integer* untuk melihat apakah ada data anomali. Count mrtupakan jumlah data untuk masing-masing fitur. Min dan max selanjutnya adalah nilai terkecil dan nilai terbesar dari suatu fitur. *Mean* (rata-rata) merupakan suatu ukuran pemusatan data. Mean suatu data juga merupakan statistik karena mampu menggambarkan bahwa data tersebut berada pada kisaran mean data tersebut. *Median* menentukan letak tengah data setelah data disusun menurut urutan  nilainya. Bisa juga nilai tengah dari data-data yang terurut. Simbol untuk median adalah Me.  Dengan *median* Me, maka 50% dari banyak data nilainya paling tinggi sama dengan Me, dan 50% dari banyak data nilainya paling rendah sama dengan Me. Dalam  mencari median, dibedakan  untuk banyak data ganjil  dan banyak data genap. Standar deviasi adalah ukuran statistik yang digunakan untuk mengukur sejauh mana data dalam sebuah himpunan cenderung bervariasi dari nilai rata-ratanya. Standar Deviasi dan Varians Salah satu teknik statistik yg digunakan untuk menjelaskan homogenitas kelompok. Varians merupakan jumlah kuadrat semua deviasi nilai-nilai individual thd rata-rata kelompok. Sedangkan akar dari varians disebut dengan standar deviasi atau simpangan baku. Standar Deviasi dan Varians Simpangan baku merupakan variasi sebaran data. Semakin kecil nilai sebarannya berarti variasi nilai data makin sama Jika sebarannya bernilai 0, maka nilai semua datanya adalah sama. Semakin besar nilai sebarannya berarti data semakin bervariasi. Berdasarkan hasil analisis deskriptif diatas didapatkan bahwa tidak terdapat data anomali atau data tidak jelas pada dataset, sehingga tidak perlu dilakukan penanganan data anomali atau menghapus outlier pada dataset.<br> 

### *Univariate Analysis*
Persentasi dan visualisasi distribusi *gender* yang dominan pada data untuk melihat ukuran data berdasarkan *gender* .
<br>Tabel 4. Persentasi distribusi *gender*
|index|jumlah sampel|persentase|
|---|---|---|
|Male|1068|50\.6|
|Female|1043|49\.4|

![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/1e0cedde-d7d1-44bd-8c81-dc6b18f9bc78) 
<br>Gambar 1. Visualisasi distribusi *gender*
<br>Berdasarkan hasil persenrtasi dan visualisasi diatas dapat dilihat bahwa data termasuk seimbang karena data dengan *gender* *male* dan *female* memiliki ukuran yang hampir sama atau seimbang. Hal ini menandakan ukuran dataset yang digunakan baik digunakan untuk proses pelatihan model. Data yang tidak seimbang dapat membuat Sebagian besar algoritma *machine learning* tidak bekerja dengan baik <br> 

<br> Persentasi dan visualisasi distribusi data berdasarkan fitur tingkatan obesitas
<br> Tabel 5. Persentasi distribusi tingkat obesitas
|index|jumlah sampel|persentase|
|---|---|---|
|Obesity\_Type\_I|351|16\.6|
|Obesity\_Type\_III|324|15\.3|
|Obesity\_Type\_II|297|14\.1|
|Overweight\_Level\_I|290|13\.7|
|Overweight\_Level\_II|290|13\.7|
|Normal\_Weight|287|13\.6|
|Insufficient\_Weight|272|12\.9|

![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/d187058a-ac41-439b-ba04-9dfde7e1f7b8)
<br>Gambar 2. Visualisasi distribusi tingkat obesitas
<br> Dapat dilihat distribusi maing-masing tingkat obesitas dimulai dari tingkat *insufficient weight* atau berat badan kurang yang memiliki BMI kurang dari 18,5. Orang dengan tingkat obesitas ini seharusnya memperbaiki kebiasan makan dan kondisi fisik agar mendapatkan tingkat obesitas ideal atau normal. Normal weight yang memiliki BMI antara 18,5 dan 24,9 adalah tingkat obesitas yang ideal yang seharusnya dimiliki oleh orang yang sehat yang memiliki kebiasaan makan dan kondisi fisik yang baik. *Overweight* atau kelebihan berat badan yang memiliki BMI antara 25,0 dan 29,9. Terdapat dua level pada tingkat obesitas *overweight*, level 1 menandakan jika seseorang sudah memiliki berat badan yang berlebih dari idealnya, sedangkan level 2 orang tersebut sudah hampir pada tahap memiliki penyakit obeitas. Tingkatan obesitas terakhir adalah penyakit obesitas dimana terdapat beberapa tipe yang menandakan semakin tinggi tipenya maka semakin parah penyakit obesitas yang diderita. Obesitas tipe I memiliki BMI antara 30,0 dan 34,9; obesitas tipe II memiliki BMI antara 35,0 dan 39,9; dan obesitas tipe III = BMI lebih tinggi dari 40. Berdasarkan hasil persentasi dan visualisasi jumlah data terkait jenis-jenis tingkat obesitas diatas dapat dilihat bahwa data dengan jenis tingkatan obesitas yang berbeda-beda memiliki jumlah yang hampir sama dan tidaka ada jenis tingkatan obesitas yang memiliki terlalu banyak data atau memiliki terlalu sedikit data, sehingga dataset cukup bagus digunakan model untuk proses pembelajaran.

<br> Visualisasi distribusi data berdasarkan fitur *height*, dan *age* dapat dilihat pada Gambar 3.
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/18d84ce2-0658-499e-9459-92d2b34b78c5)
<br>Gambar 3. Visualisasi distribusi data berdasarkan fitur *height*, dan *age*
<br> Visualisasi distribusi ukuran data diatas bertujuan untuk melihat distribusi data yang akan digunakan. Dalam *machine learning*, data yang memenuhi distribusi normal bermanfaat untuk pembuatan model. Hal ini membuat matematika lebih mudah ketika melakukan proses pembelajaran. Berdasarkan hasil diatas dapat diketahui bahwa fitur *height* memiliki distribusi normal sedangkan fitur *age* cenderung condong kekanan. Sebagian besar fitur *age* yang diambil adalah antara 19 hingga 25 tahun.

### *Multivariate Analysis*
Visualisasi persebaran data dari fitur *weight, height, dan gender*. <br> 
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/bbc3f731-e517-4b04-827a-6d1587d93e10)
<br> Gambar 4. Visualisasi persebaran data dari fitur *weight, height, dan gender* 
<br> Berdasarkan visualisasi pada Gambar 4 diatas dapat dilihat bahwa pada dataset yang digunakan kebanyakan pria memiliki fitur *height* yang lebih tinggi dibandingkan wanita. Sedangkan wanita mendominasi untuk *weight* diatas 130 dibandingkan pria.

## *Data Preparation*
### *Label Encoding*
Untuk mengonversi label kata menjadi angka, perlu menggunakan pembuat label *encoding*. label *encoding* mengacu pada proses transformasi label kata menjadi bentuk numerik. Mengkonfersi data-data objek yang bersifat kategorikal menjadi numerik bertujuan agar dengan mudah dipahami model. Berikut keseluruhan fitur dapat dilihat pada Tabel 6 yang telah dilakukan label *encoding*, dapat dilihat bahwa semua nilai pada fitur sudah dalam bentuk angka dan bisa dimasukkan kedalam model *machine learning*.
<br> Tabel 6. Hasil label *encoding* pada semua fitur dataset
|index|Gender|Age|Height|Weight|family\_history\_with\_overweight|FAVC|FCVC|NCP|CAEC|SMOKE|CH2O|SCC|FAF|TUE|CALC|MTRANS|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|0|21\.0|1\.62|64\.0|1|0|2\.0|3\.0|2|0|2\.0|0|0\.0|1\.0|3|3|
|1|0|21\.0|1\.52|56\.0|1|0|3\.0|3\.0|2|1|3\.0|1|3\.0|0\.0|2|3|
|2|1|23\.0|1\.8|77\.0|1|0|2\.0|3\.0|2|0|2\.0|0|2\.0|1\.0|1|3|
|3|1|27\.0|1\.8|87\.0|0|0|3\.0|3\.0|2|0|2\.0|0|2\.0|0\.0|1|4|
|4|1|22\.0|1\.78|89\.8|0|0|2\.0|1\.0|2|0|2\.0|0|0\.0|0\.0|2|3|

<br> Selain fitur yang dilakukan encoder kedalam bentuk angka, data target juga perlu dilakukan label *encoding* untuk dimasukkan kedalam model. Berikut hasil label *encoding* pada data target:
<br> Tabel 7. Hasil label *encoding* pada label datau data taerget
|index|NObeyesdad|
|---|---|
|0|1|
|1|1|
|2|1|
|3|5|
|4|6|

### *Train Test Split*
*Train test split* adalah teknik umum yang digunakan dalam *machine learning* untuk membagi data menjadi set pelatihan dan tes. Proses ini penting dalam proses pemodelan data, karena memungkinkan untuk menilai kinerja model pada data yang tidak terlihat. Pada proyek ini memisahkan data latih dan data uji dengan pembagian 80 % data latih dan 20 % data uji. Proses pemisahan ini dilakukan untuk menghindari terjadinya overfitting, yaitu suatu kondisi pelatihan yang hasil uji terhadap data yang dilatih sangat bagus tetapi diuji oleh data lain yang tidak digunakan dalam pelatihan sangat buruk. Overfitting terjadi karena kegagalan model dalam proses generalisasi data.

## *Modelling*
Pada proyek ini karena 
label yang akan diprediksi berupa numerik, maka algoritma yang digunakan adalah algoritma regresi. Regresi adalah metode pada *supervised learning* yang mengembalikan target numerik untuk setiap sampel. Adapun algoritma sederhana sebagai tahapan awal yang digunakan adalah algoritma *K-Nearest Neighbor (KNN)*, *Random Forest* dan *Boosting*. Algoritma KNN digunakan karena dibandingkan algoritma lainnya, KNN relatif mudah diimplementasikan. Algoritma KNN menggunakan kesamaan fitur untuk memprediksi nilai  setiap data  baru.  Dengan kata lain, setiap bagian data baru diberi nilai berdasarkan seberapa mirip poin-poin dalam set pelatihan. Pada kasus ini setiap fitur-fitur kebiasaan makan dan kondisi fisik seseorang akan dicari tingkat obesitasnya berdasarkan kesamaan fitur yang paling dekat dengan tingkat obesitas pada dataset. Algoritma selanjutnya yang digunakan adalah algoritma *Random Forest*. Ini adalah algoritma *machine learning* yang fleksibel dan mudah digunakan yang tidak memerlukan banyak parameter untuk mencapai hasil yang relatif baik.  Algoritma ini juga merupakan salah satu algoritma yang paling umum digunakan karena kesederhanaan dan fleksibilitasnya (dapat digunakan untuk tugas klasifikasi dan regresi). *Boosting* merupakan algoritma terakhir yang digunakan pada proyek ini karena algoritma *boosting* mengurangi kesalahan dalam analisis data prediktif. Peningkatan meningkatkan akurasi dan kinerja prediktif model mesin dengan mengubah beberapa pembelajar yang lemah menjadi model pembelajaran yang kuat.

* Algoritma *K-Nearest Neighbor (KNN)* adalah algoritma *machine learning* yang bersifat *non-parametric* dan *lazy learning*. Metode yang bersifat *non-parametric* memiliki makna bahwa metode tersebut tidak membuat asumsi apa pun tentang distribusi data yang mendasarinya. Dengan kata lain, tidak ada jumlah parameter atau estimasi parameter yang tetap dalam model, terlepas data tersebut berukuran kecil ataupun besar. Parameter yang digunakan pada algoritma ini adalah
<br> `n_neighbors` = Jumlah k tetangga tedekat, nilai yang ditunning pada proyek ini adalah `1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15`
* Algoritma *Random Forest* merupakan salah satu metode *machine learning* yang menggunakan pohon keputusan dengan pengambilan data sampel secara acak. Parameter yang digunakan pada algoritma ini adalah
<br>  `n_estimators` = Jumlah maksimum estimator keputusan di mana *boosting* dihentikan, nilai yang ditunning pada proyek ini adalah `25, 50, 100`.
<br>  `max_depth` = Kedalaman maksimum setiap pohon, nilai yang ditunning pada proyek ini adalah `8, 16, 32`.
<br>  `random_state` = Mengontrol *seed* acak yang diberikan pada setiap iterasi *boosting*, nilai yang ditunning pada proyek ini adalah `11, 33, 55`.
* Algoritma AdaBoost, singkatan dari *Adaptive Boosting*, adalah sebuah teknik *Boosting* yang digunakan sebagai metode ensemble dalam *machine learning*. Algoritma ini disebut *Adaptive Boosting* karena bobot diberikan ulang pada setiap *instance*, dengan bobot yang lebih tinggi diberikan pada *instance* yang salah diklasifikasikan. Parameter yang digunakan pada algoritma ini adalah
<br> `n_estimators` = Jumlah maksimum *estimator* di mana *boosting* dihentikan, nilai yang ditunning pada proyek ini adalah `25, 50, 100`.
<br> `learning_rate` = Inisialisasi *learning rate* yang digunakan untuk setiap perubahan bobot pada setiap iterasi pembelajaran, nilai yang ditunning pada proyek ini adalah `0.1, 0.01, 0.001`.
<br> `random_state` = Mengontrol *seed acak* yang diberikan pada setiap iterasi *boosting*, nilai yang ditunning pada proyek ini adalah `11, 33, 55`.

* *GRID Search*
Menggunakan algoritma *GRID search* untuk *hyperparameter tunning*. *Hyperparameter* dapat secara langsung mengontrol struktur, fungsionalitas, dan performa model yang dibangun. Menggunakan *hyperparameter* yang tepat dapat mengoptimalkan performa model dan mencapai hasil yang optimal. Proses ini merupakan bagian penting dari *machine learning*, dan memilih nilai *hyperparameter* yang sesuai sangat penting untuk keberhasilan. Misalkan ketika ingin melakukan proses pembelajaran. Jika nilainya terlalu besar, model mungkin akan konvergen terlalu cepat dan memberikan hasil yang kurang optimal. Di sisi lain, jika levelnya terlalu rendah, pelatihan mungkin memakan waktu terlalu lama dan  tidak efektif. Pemilihan *hyperparameter* yang  seimbang akan menghasilkan model yang akurat dan performa model yang  baik. *GRID search* adalah suatu cara untuk menemukan parameter terbaik yang digunakan untuk modeling dalam *machine learning*. Adapun hasil dari hyperparameter tunning setiap model menggunakan *GRID search* adalah pada Tabel 8 sebagai berikut:
<br> Tabel 8. Hasil hyperparameter tunning menggunakan *GRID search*
|index|model|best\_score|best\_params|
|---|---|---|---|
|0|knn|0\.8226496475499843|\{'n\_neighbors': 5\}|
|1|boosting|0\.6166451022207549|\{'learning\_rate': 0\.1, 'n\_estimators': 100, 'random\_state': 55\}|
|2|random\_forest|0\.9647466948911856|\{'max\_depth': 32, 'n\_estimators': 25, 'random\_state': 55\}|


## Evaluation
*Metode Mean Squared Error (MSE)* digunakan pada proyek ini untuk menentukan algoritma model *machine learning* yang terbaik. Secara umum MSE digunakan untuk mengecek estimasi berapa nilai kesalahan pada hasil prediksi. Nilai MSE yang rendah atau nilai MSE mendekati nol menunjukkan bahwa hasil prediksi sesuai dengan data aktual dan bisa dijadikan untuk perhitungan prediksi di periode mendatang. Metode MSE biasanya digunakan untuk membandingkan kinerja model yang berbeda dalam pemodelan statistik. Saat membandingkan estimator yang berbeda menggunakan MSE, MSE yang lebih kecil lebih baik. Hal ini karena MSE yang lebih kecil menunjukkan bahwa nilai perkiraan lebih dekat dengan nilai sebenarnya, sehingga menunjukkan bahwa model tersebut lebih akurat dan dapat diandalkan. Sebaliknya, MSE yang lebih besar akan menunjukkan perbedaan yang lebih besar antara nilai estimasi dan nilai aktual, sehingga hal ini kurang diinginkan dalam estimasi statistik.<br> 
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/53af2296-44b8-40f3-91a0-b1b3ce5bfd93)
<br> Gambar 5. Rumus metode *mean squared error*
<br> Berikut hasil evaluasi pada proyek ini dapat dilihat pada tabel 9.
<br> Tabel 9. Hasil evaluasi MSE pada setiap model
|index|train|test|
|---|---|---|
|KNN|0\.0006203080568720379|0\.001080094562647754|
|RF|5\.736303317535546e-05|0\.00039486335697399525|
|Boosting|0\.0015170262746941174|0\.0016553523001821653|

Berdasarkan hasil diatas didapatkan bahwa *random forest* memiliki tingkat kesalahan terkecil dibandingkan yang lainnya. Selisih antara nilai prediksi dan nilai aktual sebesar 0,00000573 untuk data training dan 0.000394 untuk data testing terbilang rendah dan dapat dikatakan model dapat memprediksi data sangat baik karena jarak perbedaan label tingkat obesitas masing-masing adalah 1. Model terbaik kedua untuk memprediksi tingkat obesitas adalah KNN, dan model *boosting* merupakan model yang memprediksi tingkat obesitas dengan tingkat kesalahan MSE yang paling besar dibandingkan dengan model yang lainnya. Visualisasi dengan box plot untuk mempermudah membandingkan masing-masing kesalahan pada model. <br>
![image](https://github.com/abdussalamattaqwa/dicoding-ML_terapan-submission1/assets/67810655/4e19ef12-ba70-41fb-956d-ef6a9b610f40)
<br> Gambar 6. Grafik MSE setiap model.

Berdasarkan hasil visualisasi didapatkan bahwa masing masing model memiliki jarak tingkat kesalahan yang sangat berbeda-beda. Hasil visualisasi memperlihatkan dengan jelas seberapa besar perbedaan kesalahan pada model yang memiliki tingkat kesalahan yang paling kecil dan yang paling besar, yaitu *random forest* dan *boosting*. Setiap tingkat kesalahan menggunakan data training dan data testing pada masing-masing model, hasil yang diberikan tetap sama untuk model yang memiliki tingkat kesalahan yang paling kecil ke terbesar, yaitu *random forest*, KNN, dan *boosting*. 

Membuat prediksi menggunakan beberapa data test pada masing-masing model. Terlihat bahwa prediksi dengan *Random Forest (RF)* memberikan hasil yang paling mendekati dibandingkan dengan model-model lainnya dapat dilihat pada Tabel 10 berikut.
<br> Tabel 10. Hasil prediksi dari model menggunakan data tes.
|index|y\_true|prediksi\_KNN|prediksi\_RF|prediksi\_Boosting|
|---|---|---|---|---|
|0|0|0\.0|0\.0|0\.3|
|1|3|3\.0|3\.0|3\.3|
|2|5|4\.2|4\.9|3\.9|
|3|2|2\.6|2\.0|4\.0|
|4|0|0\.0|0\.0|0\.3|

Berdasarkan hasil diatas dapat disimpulkan bahwa tingkatan obesitas berdasarkan kebiasaan makan dan kondisi fisik dapat diprediksi dengan baik menggunakan model *machine learning*. Model ini dapat digunakan sebagai pembantu untuk menjaga tingkat obesitas yang normal bagi seseorang dengan memperbaiki kebiasaan makan dan kondisi fisik apabila model memprediksi bahwa orang tersebut memiliki tingkat obesitas yang tidak ideal. Model terbaik yang dapat digunakan untuk prediksi tingkat obesitas seseorang adalah menggunakan model *random forest* yang memiliki *error MSE* terkecil dibandingkan model yang lainnya. 

# Referensi

[1] Gozukara Bag, H. G., Yagin, F. H., Gormez, Y., González, P. P., Colak, C., Gülü, M., ... & Ardigò, L. P. (2023). Estimation of obesity levels through the proposed predictive approach based on physical activity and nutritional habits. Diagnostics, 13(18), 2949.

[2] WHO. (2021). Obesity and overweight. Diakses dari https://www.who.int/news-room/fact-sheets/detail/obesity-and-overweight

[3] Kementrian Kesehatan Republik Indoenesia. (2023). Panduan hari Obesitas Sedunia Tahun 2023.Diakses dari https://ayosehat.kemkes.go.id/pub/files/0b43c48e8765bf62a02f42a1359349d5.pdf

[4] Navidad, L., Padial-Ruz, R., & González, M. C. (2021). Nutrition, Physical activity, and new technology programs on obesity prevention in primary education: a systematic review. International Journal of Environmental Research and Public Health, 18(19), 10187.

[5] Palechor, F. M., & de la Hoz Manotas, A. (2019). Dataset for estimation of obesity levels based on eating habits and physical condition in individuals from Colombia, Peru and Mexico. Data in brief, 25, 104344.


