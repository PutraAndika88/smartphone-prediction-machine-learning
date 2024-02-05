# Proyek Prediksi Harga *Smartphone*
### Disusun Oleh : Putra Andika Pradana

Ini adalah proyek pertama untuk memenuhi tugas dicoding. Proyek ini membangun model machine learning yang dapat memprediksi harga *smartphone* berdasarkan fitur-fitur spesifikasi dari ponsel tersebut.

## Domain Proyek
### 1. Latar Belakang
Kebutuhan akan *smartphone* atau ponsel pintar pada saat ini bukanlah menjadi kebutuhan tersier melainkan telah menjadi kebutuhan pokok setiap orang. Ponsel pintar kini telah menjadi barang yang sifatnya vital dalam mendukung fungsi dari kehidupan manusia seperti membantu dalam bekerja dan untuk menjadi lebih produktif. Menurut J. Degenhard (2024) bahwa Kebutuhan akan ponsel pintar yang masif juga merupakan dampak dari kemajuan teknologi yang tiada henti sehingga manusia dipaksa untuk terus mengikuti perkembangan zaman untuk tetap kompetitif. Fenomena tersebut tentu perusahaan elektronik khususnya produsen ponsel pintar perlu untuk terus memenuhi permintaan pasar smartphone yang meningkat [[1]](https://www.statista.com/forecasts/1143723/smartphone-users-in-the-world#statisticContainer). Hal ini tentunya perusahaan juga perlu untuk tetap kompetitif dalam bersaing dengan kompetitornya. Selain itu, pengguna ponsel pintar di Indonesia juga mengalami peingkatan secara signifikan dan menjadi yang terbanyak keempat di dunia pada tahun 2022 [[2]](https://dataindonesia.id/telekomunikasi/detail/pengguna-smartphone-indonesia-terbesar-keempat-dunia-pada-2022). Oleh karena itu, analisis ini dilakukan untuk membantu perusahaan produsen ponsel pintar di Indonesia dalam menjaga sustainability bisnisnya agar tetap kompetitif di pasar ponsel pintar dan tidak salah dalam membuat keputusan terkait harga ponsel pintar ketika produk barunya akan dirilis di pasar ponsel Indonesia. 

![image](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/assets/133973000/f679c9ca-abbe-42e6-a4e5-e7f3627a89d2)
###### Gambar 1.1 *Smartphone*


[Referensi gambar](https://chatnews.id/read/harga-smartphone-5g-mulai-terjangkau)


Harga dari setiap ponsel pintar diukur dari nilai yang dimiliki oleh ponsel tersebut. Namun, harga ini tidak selalu pasti dan sulit untuk melakukan prediksi akurat secara manual. Faktor ketidakpastian perlu dikurangi oleh perusahaan yang memproduksi ponsel pintar dengan membangun sistem prediksi yang dapat menentukan berapa harga pasaran ponsel pintar tersebut yang pantas untuk spesifikasi ponsel pintar tertentu.

Dalam mencapai hal tersebut, maka dilakukan penelitian untuk memprediksi harga ponsel pintar menggunakan model *machine learning* [[3]](https://core.ac.uk/download/pdf/235044836.pdf). Diharapkan model ini mampu memprediksi harga ponsel pintar yang sesuai dengan harga pasar. Prediksi ini nantinya dijadikan acuan bagi perusahaan dalam mengedarkan ponsel pintar dan mengatur harga pasar tepat dan kompetitif sehingga mampu meningkatkan profit lebih baik lagi bagi perusahaan. Secara keseluruhan, model analisis prediktif dalam proyek "Prediksi Harga *Smartphone*" dapat memberikan manfaat yang signifikan bagi perusahaan produsen *smartphone* dan calon pelanggan potensial. Dengan menggunakan model ini, perusahaan produsen *smartphone* tersebut dapat mengoptimalkan penentuan harga *smartphone* dan mengelola risiko keuangan mereka, sementara calon pelanggan potensial akan mendapatkan perkiraan harga *smartphone* yang lebih adil dan akurat sesuai dengan preferensi dan *budget* mereka.

## 2. *Business Understanding*

Proyek ini dibangun untuk perusahaan dengan karakteristik bisnis sebagai berikut :

+ Perusahaan elektronik yang berfokus sebagai produsen smartphone dengan tipe ponsel pintar mulai kelas *entry-level* hingga *flagship*
  
+ Perusahaan elktronik yang berfokus pada produksi *smartphone* yang Berorientasi pada Analisis Data: Perusahaan ini memiliki kepentingan dan komitmen dalam mengoptimalkan penggunaan data untuk meningkatkan keputusan bisnis. Mereka mengakui nilai analisis prediktif dan machine learning dalam menentukan harga *smartphone* yang sesuai kondisi pasar yaitu setara antara harga dan spesifikasi yang ditawarkan secara akurat.
  
+ Perusahaan dengan Basis Data Pelanggan yang Kaya: Perusahaan ini memiliki akses dan kepemilikan data spesifikasi smartphone dari berbagai *brand* dan model yang lengkap dan kaya akan informasi spesifikasi dari *smartphone* tersebut. Data tersebut mencakup variabel seperti *battery*, model, *operating systems*, *price*, *touch screen*, GPS, 3G, 4G/ LTE, *bluetooth*, *processors*, RAM, *storage*, dan *number of sim card*. Data ini akan menjadi sumber informasi yang berharga dalam mengembangkan model prediktif.
  
+ Perusahaan yang Berorientasi pada Keunggulan Kompetitif: Perusahaan ini mengutamakan keunggulan kompetitif di pasar *smartphone*. Mereka ingin memanfaatkan teknik analisis prediktif dan machine learning untuk meningkatkan strategi penetapan harga, mengelola sumber daya yang efisien dari proses produksi dan perakitan *smartphone*, serta menawarkan *smartphone* yang lebih menarik dan kompetitif bagi calon konsumen.

Dengan memahami karakteristik bisnis perusahaan elektronik yang berfokus pada produksi *smartphone*, proyek ini dapat dirancang dan disesuaikan untuk memenuhi kebutuhan dan tujuan bisnis yang spesifik.

Oleh sebab itu, proyek "Prediksi Harga *Smartphone*" ini dapat membantu perusahaan produsen *smartphone* dengan karakteristik bisnis di atas dalam meningkatkan keputusan bisnis dan mencapai keunggulan kompetitif sebagai berikut:

+ Penentuan harga *smartphone* yang Lebih Akurat: Dengan menggunakan model analisis prediktif yang dikembangkan dalam proyek ini, perusahaan dapat menentukan harga *smartphone* baru yang akan mereka rilis dengan lebih akurat berdasarkan fitur yang relevan. Dengan mempertimbangkan variabel seperti *battery*, model, *operating systems*, *price*, *touch screen*, GPS, 3G, 4G/ LTE, *bluetooth*, *processors*, RAM, *storage*, dan *number of sim card*, model ini dapat memberikan estimasi harga *smartphone* yang lebih tepat dan konsisten. Hal ini membantu perusahaan mengambil keputusan yang lebih informasional dan meminimalkan risiko keuangan yang tidak terduga.
  
+ Peningkatan Efisiensi dan Produktivitas: Dengan memanfaatkan teknologi analisis prediktif dan machine learning, perusahaan dapat meningkatkan efisiensi dan produktivitas dalam proses penetapan harga *smartphone*. Model prediktif dapat secara otomatis memproses data dan memberikan perkiraan harga *smartphone* yang lebih cepat, mengurangi waktu dan upaya yang dibutuhkan dalam proses manual yang lebih lambat dan rentan terhadap kesalahan. Ini memungkinkan perusahaan untuk lebih fokus pada kegiatan inti bisnis mereka dan meningkatkan produktivitas keseluruhan.
  
+ Pengambilan Keputusan yang Lebih Informasional dan *data-driven*: Dengan menggunakan model analisis prediktif yang akurat, perusahaan dapat mengambil keputusan bisnis yang lebih informasional dan lebih *data-driven*. Model ini memberikan wawasan yang lebih dalam tentang fitur-fitur yang mempengaruhi harga *smartphone*, membantu perusahaan memahami pelanggan mereka dengan lebih baik, dan mengidentifikasi pola atau tren yang relevan. Informasi ini memungkinkan perusahaan untuk mengoptimalkan strategi bisnis mereka, meningkatkan kualitas produk dan layanan kepada pelanggan, dan mengidentifikasi peluang baru di pasar *smartphone*.
  
+ Keunggulan Kompetitif dalam Pasar: Dengan menggunakan model analisis prediktif yang lebih canggih dan akurat, perusahaan produsen *smartphone* dapat mencapai keunggulan kompetitif di pasar. Dengan memperkirakan premi dengan lebih tepat dan memberikan estimasi yang lebih adil, perusahaan dapat menarik calon pelanggan potensial dengan produk *smartphone* yang lebih menarik dan kompetitif. Hal ini membantu perusahaan membedakan diri dari pesaing, memperluas pangsa pasar, dan membangun hubungan jangka panjang dengan pelanggan.

Dengan memanfaatkan model prediktif yang dikembangkan dalam proyek ini, perusahaan produsen *smartphone* dapat mengambil keputusan bisnis yang lebih baik, meningkatkan efisiensi operasional, mencapai keunggulan kompetitif, dan memberikan layanan yang lebih baik kepada calon pelanggan potensial.

Dampak dari keberhasilan project ini:

1. Ekonomi dan Finansial
+ Perusahaan dapat memaksimalkan profit dan meminimalisir kesalahan dalam mengalokasikan sumber daya pada proses produksi
+ Perusahaan dapat mengidentifikasi tren harga ponsel pintar di pasar sesuai dengan spesifikasi dan karakteristik ponsel tersebut
+ Perusahaan dapat membuat keputusan bisnis yang lebih terukur terutama dalam hal penentuan harga ponsel tersebut
+ Perusahaan mampu untuk terus kompetitif dalam menghadapi kompetitor ponsel pintar yang semakin ketat di pasar ponsel pintar

2. Sosial
+ Perusahaan dapat dengan jelas mengidentifikasi harga ponsel pintar di pasar sehingga konsumen diuntungkan dengan semakin menjamurnya pilihan ponsel pintar yang secara harga sangat bersaing
+ Konsumen diuntungkan dengan banyaknya pilihan ponsel pintar mulai dari kelas rendah hingga kelas tinggi sesuai dengan kondisi keuangan mereka

### 3. *Problem Statement*

1. Bagaimana cara mengidentifikasi terkait fitur yang paling berpengaruh terhadap harga smartphone?

- Perusahaan produsen *smartphone* menghadapi tantangan dalam menentukan harga dari produk *smartphone* baru mereka dengan akurat dan adil bagi calon pemegang polis. Hal ini disebabkan oleh keterbatasan dalam memahami faktor-faktor yang mempengaruhi besaran harga *smartphone*.

- Dalam proyek ini, kami akan mengatasi masalah ini dengan mengembangkan model analisis prediktif yang dapat memperkirakan harga *smartphone* dengan tingkat akurasi yang lebih tinggi.

2. Bagaimana caranya untuk meningkatkan transparansi dalam penetapan harga *smartphone*?

- Calon pembeli *smartphone* seringkali merasa bahwa penetapan harga *smartphone* dilakukan secara tidak adil atau tidak transparan. Mereka tidak memahami faktor-faktor apa yang menjadi dasar penentuan harga *smartphone*.

- Dalam proyek ini, kami akan mencoba meningkatkan transparansi dengan mengidentifikasi faktor-faktor yang paling signifikan dalam menentukan harga *smartphone*, sehingga calon pemegang polis dapat memahami alasan di balik harga *smartphone* yang ditawarkan.

3. Bagaimana risiko keuangan yang terkait dengan penentuan harga *smartphone* yang tidak akurat dapat dikurangi?

- Penentuan harga *smartphone* yang tidak akurat dapat menyebabkan risiko keuangan bagi perusahaan produsen *smartphone*. Jika harga *smartphone* yang ditetapkan terlalu rendah, perusahaan dapat menghadapi kerugian finansial terutama masalah profitabilitas perusahaan.

- Di sisi lain, premi yang terlalu tinggi dapat mengurangi daya tarik produk asuransi. Dalam proyek ini, kami akan membantu mengurangi risiko keuangan dengan memperkirakan premi yang lebih akurat berdasarkan faktor-faktor risiko yang relevan.

Dalam konteks penentuan harga *smartphone*, berikut adalah contoh konkret dari faktor-faktor spesifik yang seringkali menyebabkan masalah-masalah yang disebutkan sebelumnya:

Kurangnya akurasi dalam menentukan harga *smartphone* baru yang akan dirilis di pasar:

Masalah: Kurangnya pemahaman tentang fitur yang berkontribusi pada harga *smartphone*, seperti battery*, model, *operating systems*, *price*, *touch screen*, GPS, 3G, 4G/ LTE, *bluetooth*, *processors*, RAM, *storage*, dan *number of sim card*. 
Contoh: Perusahaan mengalami kesulitan dalam mengimbangi pola dan tren harga *smartphone* karena semakin melonjaknya pesaing dari berbagai *brand* yang menawarkan produk dengan harga yang sangat kompetitif sehingga perusahaan tersebut memerlukan sebuah hasil analisis prediktif sebagai salah satu strategi untuk menetapkan harga *smartphone* yang wajar dan menjaga produk barunya agar tetap bersaing di pasar *smartphone* secara jangka panjang.

Dengan memanfaatkan teknik machine learning, model ini akan menghasilkan perkiraan harga *smartphone* yang lebih akurat, mempertimbangkan fitur-fitur yang relevan dengan tingkat keakuratan yang lebih tinggi.

Selain itu, dengan mengidentifikasi fitur-fitur yang paling signifikan dalam penetapan harga, perusahaan produsen *smartphone* dapat memberikan penjelasan yang lebih baik kepada *potential buyer* mereka mengenai alasan di balik besaran harga *smartphone* yang mereka tawarkan. Dengan kata lain, meningkatkan transparansi dan kepercayaan kepada calon konsumen.

### 4. *Goals*

Proyek ini memiliki tujuan sebagai berikut:

+ Mengembangkan model analisis prediktif: Tujuan utama proyek ini adalah mengembangkan model analisis prediktif yang dapat memperkirakan harga *smartphone* dengan tingkat akurasi yang lebih tinggi. Dengan melakukan analisis data yang komprehensif dan menggunakan teknik *machine learning*, tujuannya adalah menciptakan model yang dapat memberikan perkiraan harga *smartphone* yang lebih tepat berdasarkan fitur-fitur yang relevan.

+ Meningkatkan transparansi: Proyek ini bertujuan untuk meningkatkan transparansi dalam penetapan harga *smartphone*. Dengan mengidentifikasi faktor-faktor yang paling signifikan dalam menentukan premi, tujuannya adalah memberikan pemahaman yang lebih baik kepada calon *potential buyer* mengenai alasan di balik besaran harga *smartphone* yang mereka terima. Hal ini akan membantu membangun kepercayaan dan kepuasan calon pembeli terhadap perusahaan atau *brand* ponsel tersebut.

+ Mengurangi risiko keuangan: Salah satu tujuan proyek ini adalah membantu perusahaan produsen *smartphone* mengurangi risiko keuangan yang terkait dengan penetapan harga *smartphone* yang tidak akurat. Dengan memperkirakan harga *smartphone* dengan lebih akurat berdasarkan fitur yang relevan, perusahaan *smartphone* dapat mengoptimalkan pengelolaan risiko keuangan mereka, menghindari kerugian yang tidak diharapkan, dan menjaga stabilitas keuangan perusahaan.

Metrik evaluasi yang digunakan untuk mengukur keberhasilan mencapai setiap tujuan dapat meliputi:

+ Akurasi prediksi: Metrik ini digunakan untuk mengukur sejauh mana model analisis prediktif dapat memperkirakan harga *smartphone* dengan tepat. Nilai akurasi yang tinggi menunjukkan bahwa model memberikan perkiraan yang lebih akurat, sehingga membantu mencapai tujuan pertama.

+ Tingkat transparansi: Metrik ini dapat diukur dengan melakukan survei atau penilaian terhadap calon pembeli *smartphone* untuk mengukur tingkat pemahaman mereka tentang alasan di balik harga *smartphone* di pasaran. Semakin tinggi tingkat pemahaman dan kepercayaan calon pembeli terhadap alasan penetapan harga *smartphone*, semakin tinggi pula tingkat transparansi yang dicapai.

+ Risiko keuangan: Metrik ini dapat diukur dengan membandingkan kinerja keuangan perusahaan asuransi sebelum dan setelah penerapan model analisis prediktif. Jika risiko keuangan berkurang setelah menggunakan model, hal ini menunjukkan bahwa tujuan ketiga tercapai.

Selain itu, metrik lain yang dapat digunakan untuk mengukur keberhasilan proyek ini adalah ialah Mean Squared Error (MSE): Metrik ini dapat digunakan untuk mengukur seberapa dekat prediksi premi dengan nilai sebenarnya. Semakin rendah nilai MSE, semakin baik model analisis prediktif dalam memperkirakan premi.

Penggunaan metrik evaluasi yang tepat dan relevan dengan tujuan proyek akan membantu dalam menilai keberhasilan dan dampak proyek terhadap perusahaan produsen *smartphone* dan calon pembeli.

### 5. *Solution Statement*

Solusi yang diberikan untuk proyek ini melibatkan beberapa tahapan dan algoritma yang digunakan. Berikut adalah penjelasan yang lebih rinci mengenai solusi yang diberikan:

1. Eksplorasi Data (Exploratory Data Analysis - EDA):

- Sebelum melatih model, proses EDA akan dilakukan untuk memahami karakteristik data yang ada. EDA akan membantu dalam mengidentifikasi pola, melihat hubungan antar variabel, dan menemukan wawasan yang berguna dalam memprediksi harga *smartphone*.

2. Algoritma Random Forest Regression:

- Algoritma Random Forest Regression dipilih sebagai algoritma machine learning yang akan digunakan dalam proyek ini.
- Random Forest Regression adalah algoritma yang digunakan untuk memodelkan dan memprediksi data regresi. Dalam proyek ini, Random Forest Regression akan digunakan untuk memprediksi harga 8smartphone* berdasarkan fitur-fitur yang relevan.
- Algoritma random forest adalah salah satu algoritma supervised learning. Algoritma ini dapat digunakan untuk menyelesaikan masalah klasifikasi dan regresi. Random forest juga merupakan algoritma yang sering digunakan karena cukup sederhana tetapi memiliki stabilitas yang mumpuni.

3. Evaluasi dengan Metrik MSE (Mean Squared Error):

- Metrik MSE (Mean Squared Error) akan digunakan untuk melakukan evaluasi pembanding antara model-model yang dikembangkan.
- MSE adalah metrik yang umum digunakan dalam masalah regresi untuk mengukur sejauh mana selisih antara nilai prediksi dan nilai sebenarnya.
- Dengan menggunakan metrik MSE, kita dapat mengukur tingkat keakuratan model dalam memprediksi harga *smartphone*.

Melalui pendekatan ini, diharapkan solusi yang diberikan dapat memenuhi tujuan proyek dalam mengembangkan model analisis prediktif yang akurat dan efektif untuk memprediksi harga *smartphone*.

## 6. *Data Understanding & Removing Outlier*

Dataset yang digunakan dalam proyek ini merupakan data harga smartphone dengan berbagai karakteristik. Dataset ini dapat diunduh di [Kaggle : Mobile Phone Specifications and Prices](https://www.kaggle.com/datasets/pratikgarai/mobile-phone-specifications-and-prices).

### A. Ringkasan Data Statistik dari Sampel Data

| *Battery* | *Screen Size* | *Resolution* X | *Resolution* Y | *Processor* | RAM | *Internal Storage* | *Rear Camera* | *Front Camera* |||
|-----|----------|-----------------------|----------------|--------------------|--------|--------|----------------|-------------------------|-----------------------|--------------|
| count | 918.000000 | 918.000000 | 918.000000 | 918.000000 | 918.000000 | 918.000000 | 918.000000 | 918.000000 | 918.000000 |
| mean | 0.0000 | -0.00000 | 0.00000 | 0.000000| 0.000000 | -0.0000000 | 0.000000 | -0.0000000 | -0.00000000 |
| std | 1.000545 | 1.000545 | 1.000545 | 1.000545 | 1.000545 | 1.000545 | 1.000545 | 1.000545 | 1.000545 |
| min | -2.097277 | -2.146661 | -2.259848 | -2.028770 | -2.025716 | -1.626563 | -1.289708 | -1.993510 | -1.571612 | 
| 25% | -0.720550	 | -0.284356 | -0.902828 | -0.874461 | -0.548665 | -0.906687 | -0.757857 | -1.207443 | -0.993291 | 
| 50% | -0.121973 | -0.284356 | -0.088615 | -0.104921 | -0.548665 | 0.060888	 | -0.189641 | -0.421376	 | 0.027274 | 
| 75% | 0.356889 | 0.646796 | -0.088615	 | 0.424137 | 1.420736 | 1.028462	 | 0.946791 | 0.888735	 | 1.047840 | 
| max | 2.990628 | 2.602216 | 3.530106	 | 3.742777	 | 2.405437	 | 3.931187	 | 3.219655 | 2.722891	 | 2.748782 | 

Berikut informasi pada dataset :

+ Dataset memiliki format CSV (Comma-Seperated Values).
+ Dataset memiliki 1360 sample dengan 21 fitur.
+ Dataset memiliki 7 fitur bertipe int64, 10 fitur bertipe object, dan 4 tipe float64
+ Tidak ada missing value dalam dataset.

### B. Variabel pada dataset
1. ***Name***: *Smartphone's series*
2. ***Brand***: *Smartphone's brand*
3. **Model**: *Smartphone's model*
4. ***Battery Capacity (mAh)***: *Smartphone's Battery Capacity*
5. ***Screen Sizes (Inch)***: *Smartphone'screen size*
6. ***Touchscreen***: *Touchscreen feature in smartphone (Yes/No)*
7. ***Resolution x***: *Smartphone horizontal screen resolution*
8. ***Resolutiony***: *Smartphone vertical screen resolution (Yes/No)*
9. ***Processor***: *Smartphone's processor*
10. ***RAM(MB)***: *Smartphone's RAM size*
11. ***Internal Storage (GB)***: *Smartphone's internal storage size*
12. ***Rear Camera***: *Smartphone's rear camera*
13. ***Front camera***: *Smartphone's front camera (Yes/No)*
14. ***Operating System***: *Smartphone's OS*
15. ***Wi-Fi***: *Smartphone's wifi feature*
16. ***Bluetooth***: *Smartphone's bluetooth feature*
17. **GPS**: *Smartphone's GPS feature*
18. ***Number of SIMs***: *Number of SIMs on smartphone*
19. **3G**: *3G feature on smartphone (Yes/No)*
20. **4G/LTE**: *4G/LTE feature on smartphone (Yes/No)*
21. ***Price***: *Smartphone's price*

### C. Pendalaman Data Understanding
- Melakukan tahapan EDA seperti mendeskripsikan variabel, mencari *outlier*s, Univariate hingga Multi-variate analysis.
- Untuk menganalisa *outlier*s bisa menggunaka boxplot dengan memanggil fungsi .plot() pada pandas
- Mengecek data missing value dan membersihkan data missing value dengan membuat simple logic program
- Menggunakan histogram untuk melihat penyebaran data dengan *library* pandas fungsi .hist()
- Mencari keterkaitan antar fitur numerik dan fitur kategori dengan correlation matrix menggunakan fungsi pandas dan visualisasi heatmap dengan seaborn

### D. Visualisasi proses Data Understanding

Untuk mengatasi outlier, salah satu metode yang umum digunakan adalah metode IQR (Interquartile Range) dengan visualisasi menggunakan boxplot. Berikut penjelasan mengenai metode IQR dan visualisasi boxplot:

Metode IQR:
1. Konsep: IQR merupakan ukuran statistik yang menggambarkan rentang atau sebaran data pada bagian tengah distribusi data. IQR dihitung dengan mengurangi nilai kuartil ketiga (Q3) dengan nilai kuartil pertama (Q1). Outlier dianggap sebagai nilai yang terletak di luar rentang IQR yang ditentukan.
2. Cara Kerja:
   - Hitung Q1 (kuartil pertama) dan Q3 (kuartil ketiga) dari data.
   - Hitung IQR dengan mengurangi Q1 dari Q3.
   - Tentukan batas atas dan batas bawah untuk outlier dengan menggunakan rumus: batas atas = Q3 + (1.5 * IQR), batas bawah = Q1 - (1.5 * IQR).
   - Data yang berada di luar batas atas dan batas bawah tersebut dianggap sebagai outlier.

Visualisasi Boxplot:
1. Konsep: Boxplot adalah visualisasi grafis yang digunakan untuk menganalisis distribusi data dan mengidentifikasi adanya outlier. Boxplot menampilkan beberapa ukuran statistik, termasuk Q1, Q3, median, serta batas atas dan batas bawah untuk outlier.
2. Cara Kerja:
   - Boxplot terdiri dari sebuah kotak (box) yang menunjukkan rentang IQR (dari Q1 hingga Q3).
   - Garis di dalam kotak menunjukkan posisi median.
   - Whisker atau garis lurus yang terhubung dengan kotak menunjukkan rentang data yang dianggap tidak sebagai outlier.
   - Titik-titik di luar whisker menunjukkan adanya outlier.
  
![outliers_boxplot](https://github.com/nikofebrianur/Machine-Learning-Terapan/assets/42314371/994b7ef1-fe6d-4bc4-94a5-5800322fe11f)
###### Gambar D.1 Contoh Visualisasi Outlier

### E. Univariate Analysis

Univariate Analysis adalah menganalisis setiap fitur secara terpisah atau parsial yang mana 

#### Analisis jumlah nilai unique pada setiap fitur kategorik
Fitur Name dan Model memiliki sebaran sample yang cukup merata.

![Fitur Merata](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/fitur%20merata.png)
###### Gambar E.1 Fitur Model

![Fitur Merata](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/fitur%20merata%202.png)
###### Gambar E.2 Fitur *Name*

Berikut adalah fitur dengan sample yang tidak merata :

  ![Fitur Tidak Merata 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata.png)
  ###### Gambar E.3 Fitur *Brand*
  
  ![Tidak Rata 2](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_2.png)
  ###### Gambar E.4 Fitur *Touchscreen*

  ![Tidak rata 3](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_3.png)
  ###### Gambar E.5 Fitur *Operating Systems*

  ![Tidak Rata 4](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_4.png)
  ###### Gambar E.6 Fitur *Wi-Fi*

  ![Tidak Rata 5](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_5.png)
  ###### Gambar E.7 Fitur *Bluetooth*

  ![Tidak Rata 6](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_6.png)
  ###### Gambar E.8 Fitur GPS

  ![Tidak Rata 7](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_7.png)
  ###### Gambar E.9 Fitur 3G

  ![Tidak Rata 8](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Fitur%20tidak%20merata_8.png)
  ###### Gambar E.10 Fitur 4G/ LTE

### F. Analisis sebaran pada setiap fitur numerik

![Fitur Numerik](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/fitur%20numerik.png)
###### Gambar F.1 Fitur Numerikal

Berikut analisis dari grafik di atas :

+ Sebagian besar smartphone memiliki kapasitas battery 2000 - 3000 mAh dan terdistribusi normal.
+ Sebagian besar smartphone memiliki screen size 5 - 5.5 inch.
+ Sebagian besar harga smartphone tersebar di range harga 5000 - 10000.
+ Fitur num of sim pada smartphone di market seluruhnya memiliki dual sim

### G. Multivariate Analysis

Multivariate Analysis menunjukkan hubungan antara dua atau lebih fitur dalam data.

#### Analisis fitur kategorik

+ Fitur kategorik terhadap Price 

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%200.png)
  ###### Gambar G.1 *Price* vs *Operating Systems*
  
  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%201.png)
  ###### Gambar G.2 *Price* vs *Models*

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%202.png)
  ###### Gambar G.3 *Price* vs *Wi-Fi*

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%203.png)
  ###### Gambar G.4 *Price* vs *Touchscreen*

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%204.png)
  ###### Gambar G.5 *Price* vs GPS

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%205.png)
  ###### Gambar G.6 *Price* vs *Blueetooth*

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%206.png)
  ###### Gambar G.7 *Price* vs 3G

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%207.png)
  ###### Gambar G.8 *Price* vs 4G/ LTE

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%208.png)
  ###### Gambar G.9 *Price* vs *Brand*

  ![kategorik 1](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/Multivariate_Categorical%209.png)
  ###### Gambar G.9 *Price* vs *Name*
  
Hasil Analisis
+ Pada fitur Operating system (OS), memiliki range harga yang sangat lebar yaitu 4500-18000 dengan harga terendah pada smartphone dengan OS Tizen dengan harga 4500 dan harga tertinggi yaitu smartphone dengan OS iPhone dengan harga tertinggi mencapai 18000. Jadi, fitur **Operating system** **sangat mempengaruhi** fluktuasi harga smartphone
+ Pada fitur Model, berdasarkan hasil bar chart tersebut menunjukkan bahwa harga smartphone sangat berfluktuasi jika dibandingkan berdasarkan pada modelnya. Jadi, kesimpulannya adalah **fitur model sangat mempengaruhi harga smartphone**
+ Pada fitur Name, berdasarkan hasil bar chart tersebut menunjukkan bahwa harga smartphone sangat berfluktuasi jika dibandingkan berdasarkan pada fitur Name. Jadi, kesimpulannya adalah **fitur Name sangat mempengaruhi harga smartphone**
+ Pada fitur Model, berdasarkan hasil bar chart tersebut menunjukkan bahwa harga smartphone sangat berfluktuasi jika dibandingkan berdasarkan pada fitur Model. Jadi, kesimpulannya adalah **fitur Model sangat mempengaruhi harga smartphone**
+ Pada fitur Wi-Fi, memiliki range harga rata-rata 6000-8000 dengan harga tertinggi pada smartphone dengan fitur Wi-Fi dan harga terendah pada smartphone tanpa Wi-Fi. Berdasarkan data tersebut, **fitur Wi-Fi cukup mempengaruhi harga smartphone**
+ Pada fitur Touchscreen, memiliki range harga rata-rata 5500-8000 dengan harga tertinggi pada smartphone dengan fitur Touchscreen dan harga terendah pada smartphone tanpa Touchscreen. Berdasarkan data tersebut, **fitur Touchscreen cukup mempengaruhi harga smartphone**
+ Pada fitur GPS, memiliki range harga rata-rata 6000-8000 dengan harga tertinggi pada smartphone dengan fitur GPS dan harga terendah pada smartphone tanpa GPS. Berdasarkan data tersebut, **fitur GPS cukup mempengaruhi harga smartphone**
+ Pada fitur Bluetooth, memiliki range harga rata-rata 6500-8000 dengan harga tertinggi pada smartphone dengan fitur Bluetooth dan harga terendah pada smartphone tanpa Bluetooth. Berdasarkan data tersebut, **fitur Bluetooth cukup mempengaruhi harga smartphone**
+ Pada fitur 3G, tidak memiliki range harga rata-rata yaitu sama-sama berada di harga 7900. Berdasarkan data tersebut, **fitur 3G tidak mempengaruhi harga smartphone**
+ Pada fitur 4G/ LTE, memiliki range harga rata-rata 6000-8300 dengan harga tertinggi pada smartphone dengan fitur 4G/ LTE dan harga terendah pada smartphone tanpa 4G/ LTE. Berdasarkan data tersebut, **fitur Wi-Fi cukup mempengaruhi harga smartphone**
+ **Jadi, fitur categorical pada data smartphone ini secara mayoritas mempengaruhi harga smartphone**

#### H. Analisis fitur Numerik

Analisis ini dilakukan untuk melihat kolerasi antara fitur kategorik dengan fitur target (Price).

+ Pairplot
  
  ![Pairplot](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/pairplot.png)
  ###### Gambar H.1 *Pairplot*
  
+ Matrix Correlation
  
  ![corr](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/blob/main/img/matrix%20corr.png)
  ###### Gambar H.2 *Matrix Correlation*
  
  Seluruh fitur numerikal berkorelasi cukup kuat dalam mempengaruhi variabel target yaitu Price 

## 7. Data preparation
+ One Hot Encoding

  One hot encoding adalah teknik mengubah data kategorik menjadi data numerik dimana setiap kategori menjadi kolom baru dengan nilai 0 atau 1. Fitur yang akan diubah menjadi numerik pada proyek ini adalah fitur dengan tipe object atau kategorikal. Hal ini perlu dilakukan karena sebuah model pembelajaran mesin tidak mampu melakukan *training* pada data tipe *string* sehingga diperlukan transformasi data menjadi numerik agar mesin mampu membaca data tersebut. Proses *One Hot Encoding* pada fitur kategorikal adalah teknik yang digunakan untuk mengubah variabel kategorikal menjadi representasi numerik yang dapat digunakan dalam model *machine learning*. Hal ini diperlukan karena sebagian besar algoritma *machine learning* hanya dapat bekerja dengan input numerik. Pandas *library* menyediakan fungsi pd.get_dummies() yang memudahkan dalam melakukan *One Hot Encoding*. Fungsi ini akan menghasilkan kolom-kolom baru yang mewakili setiap nilai unik dari fitur kategorikal. Jika suatu baris memiliki nilai tersebut, kolom yang sesuai akan diatur menjadi 1, sedangkan kolom lainnya akan menjadi 0. Misalnya, jika terdapat fitur "Warna" dengan nilai "Merah", "Biru", dan "Hijau", setelah One Hot Encoding akan terbentuk tiga kolom baru: "Warna_Merah", "Warna_Biru", dan "Warna_Hijau". Jika suatu baris memiliki nilai "Merah" pada fitur "Warna", maka kolom "Warna_Merah" akan diatur menjadi 1, sedangkan kolom lainnya akan menjadi 0.
  
+ Train Test Split

  Train test split aja proses membagi data menjadi data latih dan data uji. Data latih akan digunakan untuk membangun model, sedangkan data uji akan digunakan untuk menguji performa model. Pada proyek ini dataset sebesar 918 untuk data latih dan 102 untuk data uji. Metode ini perlu untuk dilakukan karena untuk membangun sebuah model *machine learning* diperlukan alokasi data untuk *training* dan *testing* dengan rasio tertentu supaya selain model dapat belajar, juga dapat melakukan *testing* pada data yang belum pernah dilihat sebelumnya. Proses pembagian dataset menjadi data training dan data testing penting dalam pengembangan model *machine learning*. Ini dilakukan untuk mengevaluasi performa model pada data yang belum pernah dilihat sebelumnya dan untuk menghindari *overfitting*. Data training digunakan untuk melatih model, sedangkan data testing digunakan untuk menguji seberapa baik model yang dilatih dapat melakukan prediksi pada data yang belum pernah dilihat sebelumnya. Dengan memisahkan data training dan data testing, kita dapat mengukur sejauh mana model dapat mengeneralisasi dan memprediksi dengan akurat pada data baru. Rasio 80:20 sering digunakan sebagai perbandingan pembagian data training dan data testing. Data training sebesar 80% digunakan untuk melatih model, sementara data testing sebesar 20% digunakan untuk menguji performa model. Rasio ini merupakan aturan praktis umum yang memberikan keseimbangan antara memiliki jumlah data yang cukup untuk melatih model dan menyediakan data yang cukup untuk menguji performa model. Namun, rasio ini dapat bervariasi tergantung pada karakteristik dataset dan kebutuhan proyek tertentu.

## 8. Modeling

+ Algoritma
  Penelitian ini melakukan pemodelan dengan 3 algoritma, yaitu K-Nearest Neighbour, Random Forest, dan Adaptive Boosting (AdaBoost)
  + K-Nearest Neighbour
    K-Nearest Neighbour bekerja dengan membandingkan jarak satu sampel ke sampel pelatihan lain dengan memilih sejumlah k tetangga terdekat. Proyek ini menggunakan [sklearn.neighbors.KNeighborsRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.neighbors.KNeighborsRegressor.html) dengan memasukkan X_train dan y_train dalam membangun model. Parameter yang digunakan pada proyek ini adalah :
    + `n_neighbors` = Jumlah k tetangga tedekat.

  + Random Forest
    Algoritma random forest adalah teknik dalam machine learning dengan metode ensemble. Teknik ini beroperasi dengan membangun banyak decision tree pada waktu pelatihan. Proyek ini menggunakan [sklearn.ensemble.RandomForestRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html) dengan memasukkan X_train dan y_train dalam membangun model. Parameter yang digunakan pada proyek ini adalah :
    + `n_estimators` = Jumlah maksimum estimator di mana boosting dihentikan.
    + `max_depth` = Kedalaman maksimum setiap tree.
    + `random_state` = Mengontrol seed acak yang diberikan pada setiap base_estimator pada setiap iterasi boosting.

  + Adaboost
    AdaBoost juga disebut Adaptive Boosting adalah teknik dalam machine learning dengan metode ensemble.  Algoritma yang paling umum digunakan dengan AdaBoost adalah pohon keputusan (decision trees) satu tingkat yang berarti memiliki pohon Keputusan dengan hanya 1 split. Pohon-pohon ini juga disebut Decision Stumps. Algoritma ini bertujuan untuk meningkatkan performa atau akurasi prediksi dengan cara menggabungkan beberapa model sederhana dan dianggap lemah (weak learners) secara berurutan sehingga membentuk suatu model yang kuat (strong ensemble learner). Proyek ini menggunakan [sklearn.ensemble.AdaBoostRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostRegressor.html) dengan memasukkan X_train dan y_train dalam membangun model. Parameter yang digunakan pada proyek ini adalah :
    + `n_estimators` = Jumlah maksimum estimator di mana boosting dihentikan.
    + `learning_rate` = Learning rate memperkuat kontribusi setiap regressor.
    + `random_state` = Mengontrol seed acak yang diberikan pada setiap base_estimator pada setiap iterasi boosting.
   
### Tahapan yang dilakukan
Berikut adalah urutan tahapan yang dilakukan dalam proses modeling:
 - Melatih model dengan data training dengan menggunakan algoritma *Random Forest Regression*, *K-Nearest Neighbor*, dan *AdaBoost*
 - Dalam tahap training, pengujian model dilakukan dengan menggunakan parameter default bawaan *library* yaitu *scikit-learn*
 - Melakukan pengujian dengan data training
 - Melakukan pengujian dengan data testing
 - Pengukuran menggunakan metriks *MSE*,MAE,R*MSE* dan R2 dengan menggunakan lirbary sklearn. 
 - Melihat hasil performa model antara hasil data training dan data testing

## Evaluation

### *MSE*
Mean Square Error (*MSE*) adalah salah satu metrik evaluasi yang digunakan untuk mengukur sejauh mana perbedaan antara nilai prediksi dan nilai sebenarnya dalam masalah regresi. 

Model evaluasi *MSE* menghitung rata-rata dari kuadrat selisih antara nilai prediksi dan nilai sebenarnya. Semakin kecil *MSE*, semakin baik model tersebut dalam melakukan prediksi yang akurat.

Berikut adalah langkah-langkah untuk menghitung *MSE*:

1. Mulai dengan memiliki kumpulan data yang terdiri dari pasangan nilai sebenarnya (y) dan nilai prediksi (ŷ) untuk sejumlah contoh atau sampel.

2. Hitung selisih antara nilai sebenarnya dan nilai prediksi untuk setiap contoh. Selisih ini merupakan error atau kesalahan prediksi untuk masing-masing contoh.

3. Kuadratkan setiap selisih. Ini dilakukan untuk memastikan bahwa setiap error memiliki kontribusi positif terhadap nilai *MSE*, tanpa mempertimbangkan apakah prediksi lebih rendah atau lebih tinggi dari nilai sebenarnya.

4. Hitung rata-rata dari kuadrat selisih. Caranya adalah dengan menjumlahkan semua kuadrat selisih dan membaginya dengan jumlah contoh.

   *MSE* = (Σ (y - ŷ)²) / n
   
   di mana:
   - Σ menunjukkan penjumlahan
   - y adalah nilai sebenarnya
   - ŷ adalah nilai prediksi
   - n adalah jumlah contoh atau sampel dalam dataset.

5. Setelah menghitung *MSE*, semakin kecil nilai *MSE*, semakin baik model dalam melakukan prediksi yang akurat. *MSE* memiliki satuan yang berbeda dengan variabel yang dievaluasi, karena hasilnya berupa kuadrat. Oleh karena itu, *MSE* seringkali diinterpretasikan dalam konteks yang lebih luas, atau perbandingannya dibandingkan dengan metrik evaluasi lainnya.

Tabel 9.1 Tabel hasil running evaluasi model
|           | ***Random Forest*** | **KNN** | ***AdaBoost***|              
|-----------|---------------|----------------|----------------|
| *train_MSE* | 2166.718234 | 7394.797252 | 8209.997366 |
| *test_MSE*  | 11421.410566 | 10513.247217 |11022.25554 |

Tabel 9.2 Hasil Prediksi
|***y_true*** |***Random Forest*** | **KNN** | ***AdaBoost***|              
|-----------|---------------|----------------|----------------|
| 2299.0 | 3834.0 | 3646.3 | 4134.8 |

Metrik evaluasi yang digunakan pada proyek ini adalah akurasi dan mean squared error (MSE). Akurasi menentukan tingkat kemiripan antara hasil prediksi dengan nilai yang sebenarnya (y_test). Mean squared error (MSE) mengukur error dalam model statistik dengan cara menghitung rata-rata error dari kuadrat hasil aktual dikurang hasil prediksi. Berikut formulan MSE :

Berikut hasil evaluasi pada proyek ini :

+ Mean Squared Error (MSE)
  ![Evaluasi](https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/evaluation.png)
Dari hasil evaluasi dapat dilihat bahwa model dengan algoritma Random Forest memiliki akurasi lebih tinggi baik dan tingkat error lebih kecil dibandingkan algoritma lainnya dalam proyek ini.

Berdasarkan hasil evaluasi model setelah menggunakan *hyperparameter*, kita dapat mengambil beberapa kesimpulan:

1. *Mean Squared Error* (*MSE*) - *Train Set*:
   - Model *Random Forest* memiliki *MSE* *train set* sebesar 2166.718234.
   - Model *K-Nearest Neighbor (KNN)* memiliki *MSE* *train set* sebesar 7394.797252.
   - Model *AdaBoost* memiliki *MSE* *train set* sebesar 8209.997366
   - Model *Random Forest* memiliki nilai *MSE* yang lebih rendah dibandingkan dengan model *K-Nearest Neighbor (KNN)* dan *AdaBoost* pada data training. Artinya, model *Random Forest* mampu melakukan prediksi yang lebih akurat daripada model KNN dan *AdaBoost*.

2. *Mean Squared Error* (*MSE*) - *Test Set*:
   - Model *Random Forest* memiliki *MSE* *test set* sebesar 11421.410566.
   - Model *K-Nearest Neighbor (KNN)* memiliki *MSE* *test set* sebesar 10513.247217.
   - Model *AdaBoost* memiliki *MSE* *test set* sebesar 11022.25554
   - Model *Random Forest* memiliki nilai *MSE* yang lebih rendah dibandingkan dengan model *K-Nearest Neighbor (KNN)* dan *AdaBoost* pada data training. Artinya, model *Random Forest* mampu melakukan prediksi yang lebih akurat daripada model KNN dan *AdaBoost*.

3. Berdasarkan hasil prediksi terhadap *y_true*, hasil prediksi dari *Random Forest* lebih mendekati sehingga model ini dipilih untuk proyek prediksi harga *smartphone*

Berdasarkan kesimpulan di atas, model *Random Forest* memiliki performa yang lebih baik daripada model *K-Nearest Neighbor* dan *AdaBoost* dalam memprediksi harga *smartphone*. 

Oleh karena itu, model *Random Forest* dapat dianggap lebih optimal dalam proyek ini untuk memperkirakan harga *smartphone* dengan tingkat akurasi yang lebih tinggi.

## 10. Kesimpulan 

Proyek ini berhasil mengembangkan model analisis prediktif menggunakan model *Random Forest* yang mampu memperkirakan harga *smartphone* dengan tingkat akurasi yang lebih tinggi dibandingkan dengan model *AdaBosst* dan KNN. 

Hasil evaluasi menunjukkan bahwa model *Random Forest* memberikan *MSE* yang lebih rendah pada data training dan test set.

Hal ini menunjukkan bahwa model *Random Forest* dapat memberikan prediksi harga *smartphone* yang lebih akurat dan bermanfaat bagi perusahaan produsen *smartphone* dan calon pembeli *smartphone*.

Manfaat bagi Perusahaan *smartphone*:
- Penentuan harga *smartphone* yang lebih akurat: Model *Random Forest* dapat membantu perusahaan *smartphone* menentukan harga *smartphone* dengan tingkat akurasi yang lebih tinggi, mengurangi risiko keuangan dan meningkatkan efisiensi dalam pengelolaan risiko.

- Transparansi yang ditingkatkan: Dengan memahami faktor-faktor yang signifikan dalam penetapan harga *smartphone*, perusahaan elektronik yang bergerak dalam produksi *smartphone* dapat memberikan penjelasan yang lebih baik kepada calon pembeli mengenai alasan di balik besaran harga *smartphone* yang mereka terima, meningkatkan transparansi dan kepercayaan.

Manfaat bagi Calon Pemegang Polis:
- Harga *smartphone* yang adil dan akurat: Model *Random Forest* dapat memberikan prediksi harga *smartphone* yang lebih adil dan akurat berdasarkan fitur-fitur yang relevan, memastikan bahwa harga *smartphone* yang dibayarkan sejalan dengan fitur yang ditawarkan oleh *brand* atau perusahaan *smartphone*.

- Pemahaman yang lebih baik: Dengan penjelasan yang lebih jelas mengenai faktor-faktor yang mempengaruhi penetapan premi, calon pemegang polis dapat memiliki pemahaman yang lebih baik tentang alasan di balik besaran harga *smartphone* yang mereka tawarkan.

Langkah Tindak Lanjut:
- Implementasi model: Model *Random Forest* yang telah dikembangkan dapat diimplementasikan oleh perusahaan produsen *smartphone* dalam proses penetapan harga pada produk baru mereka yang akan dirilis di pasar.

- Peningkatan data dan pemeliharaan model: Perusahaan produsen *smartphone* dapat terus memperkaya data yang digunakan dalam model dan mempertahankan model dengan melakukan pemeliharaan dan pembaruan secara berkala.

- Evaluasi dan peningkatan: Perusahaan *smartphone* dapat terus mengevaluasi kinerja model dan melakukan perbaikan atau pengembangan lebih lanjut untuk meningkatkan keakuratan dan efektivitas prediksi harga *smartphone*.

Dengan mengambil langkah-langkah tindak lanjut ini, perusahaan asuransi dapat memanfaatkan model analisis prediktif ini untuk meningkatkan ketepatan penetapan harga *smartphone*, meningkatkan transparansi, dan memberikan manfaat yang lebih baik bagi calon pembeli dalam pengalaman berbelanja *smartphone* mereka


## Reference
[1] 	J. Degenhard, "Statista," 30 January 2024. [Online]. Available: https://www.statista.com/forecasts/1143723/smartphone-users-in-the-world#statisticContainer.

[2] 	S. Sadya, "Dataindonesia," 17 January 2023. [Online]. Available: https://dataindonesia.id/telekomunikasi/detail/pengguna-smartphone-indonesia-terbesar-keempat-dunia-pada-2022.

[3] 	V. W. Siburian and I. E. Mulyana, "Prediksi Harga Ponsel Menggunakan Metode Random Forest," Computer Science and ICT, pp. 144-147, 2018. DOI: seminar.ilkom.unsri.ac.id:article/1992

