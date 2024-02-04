# Proyek Prediksi Harga Ponsel Pintar
### Disusun Oleh : Putra Andika Pradana

Ini adalah proyek pertama untuk memenuhi tugas dicoding. Proyek ini membangun model machine learning yang dapat memprediksi harga ponsel pintar berdasarkan fitur-fitur spesifikasi dari ponsel tersebut.

## Domain Proyek
### Latar Belakang
Kebutuhan akan ponsel pintar pada saat ini bukanlah menjadi kebutuhan tersier melainkan telah menjadi kebutuhan pokok setiap orang. Ponsel pintar kini telah menjadi barang yang sifatnya vital dalam mendukung fungsi dari kehidupan manusia seperti membantu dalam bekerja dan untuk menjadi lebih produktif. Menurut J. Degenhard (2024) bahwa Kebutuhan akan ponsel pintar yang masif juga merupakan dampak dari kemajuan teknologi yang tiada henti sehingga manusia dipaksa untuk terus mengikuti perkembangan zaman untuk tetap kompetitif. Fenomena tersebut tentu perusahaan elektronik khususnya produsen ponsel pintar perlu untuk terus memenuhi permintaan pasar smartphone yang meningkat [1](https://www.statista.com/forecasts/1143723/smartphone-users-in-the-world#statisticContainer). Hal ini tentunya perusahaan juga perlu untuk tetap kompetitif dalam bersaing dengan kompetitornya. Selain itu, pengguna ponsel pintar di Indonesia juga mengalami peingkatan secara signifikan dan menjadi yang terbanyak keempat di dunia pada tahun 2022 [2](https://dataindonesia.id/telekomunikasi/detail/pengguna-smartphone-indonesia-terbesar-keempat-dunia-pada-2022). Oleh karena itu, analisis ini dilakukan untuk membantu perusahaan produsen ponsel pintar di Indonesia dalam menjaga sustainability bisnisnya agar tetap kompetitif di pasar ponsel pintar dan tidak salah dalam membuat keputusan terkait harga ponsel pintar ketika produk barunya akan dirilis di pasar ponsel Indonesia. 
![image](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/assets/133973000/f679c9ca-abbe-42e6-a4e5-e7f3627a89d2)


[Referensi gambar](https://chatnews.id/read/harga-smartphone-5g-mulai-terjangkau)


Harga dari setiap ponsel pintar diukur dari nilai yang dimiliki oleh ponsel tersebut. Namun, harga ini tidak selalu pasti dan sulit untuk melakukan prediksi akurat secara manual. Faktor ketidakpastian perlu dikurangi oleh perusahaan yang memproduksi ponsel pintar dengan membangun sistem prediksi yang dapat menentukan berapa harga pasaran ponsel pintar tersebut yang pantas untuk spesifikasi ponsel pintar tertentu.

Dalam mencapai hal tersebut, maka dilakukan penelitian untuk memprediksi harga ponsel pintar menggunakan model pembelajaran mesin. Diharapkan model ini mampu memprediksi harga ponsel pintar yang sesuai dengan harga pasar. Prediksi ini nantinya dijadikan acuan bagi perusahaan dalam mengedarkan ponsel pintar dan mengatur harga pasar tepat dan kompetitif sehingga mampu meningkatkan profit lebih baik lagi bagi perusahaan.

Referensi : [3](https://core.ac.uk/download/pdf/235044836.pdf)

## *Business Understanding*

Proyek ini dibangun untuk perusahaan dengan karakteristik bisnis sebagai berikut :

+ Perusahaan elektronik yang berfokus sebagai produsen smartphone dengan tipe ponsel pintar mulai kelas rendah hingga atas

Dampak dari keberhasilan project ini:

A. Ekonomi dan Finansial
+ Perusahaan dapat memaksimalkan profit dan meminimalisir kesalahan dalam mengalokasikan sumber daya pada proses produksi
+ Perusahaan dapat mengidentifikasi tren harga ponsel pintar di pasar sesuai dengan spesifikasi dan karakteristik ponsel tersebut
+ Perusahaan dapat membuat keputusan bisnis yang lebih terukur terutama dalam hal penentuan harga ponsel tersebut
+ Perusahaan mampu untuk terus kompetitif dalam menghadapi kompetitor ponsel pintar yang semakin ketat di pasar ponsel pintar

B. Sosial
+ Perusahaan dapat dengan jelas mengidentifikasi harga ponsel pintar di pasar sehingga konsumen diuntungkan dengan semakin menjamurnya pilihan ponsel pintar yang secara harga sangat bersaing
+ Konsumen diuntungkan dengan banyaknya pilihan ponsel pintar mulai dari kelas rendah hingga kelas tinggi sesuai dengan kondisi keuangan mereka

C. Lingkungan
+ Project ini juga dapat digunakan untuk pertimbangan perusahaan dalam mengambil sebuah keputusan dalam alokasi sumber daya pada proses perakitan ponsel pintar dengan beberapa fitur tertentu sehingga meminimalisir pemborosan sumber daya yang dapat mengurangi potensi depresiasi lingkungan seperti terlalu berlebihan dalam penggunaan timah yang dapat berpotensi pada lingkungan

### Problem Statement

1. Bagaimana cara mengidentifikasi terkait fitur yang paling berpengaruh terhadap harga smartphone?
2. Bagaimana cara mengidentifikasi harga smartphone yang tepat di pasaran berdasarkan karakteristik atau spesifikasi tertentu?

### Goals

+ Perusahaan produsen *smartphone* dapat mengidentifikasi fitur ponsel pintar yang paling mempengaruhi performa harga smartphone di pasaran.
+ Perusahaan produsen *smartphone* mampu mengatur *product competitiveness* mereka dengan harga yang sesuai pada setiap lini dan spesifikasi produk mereka yaitu tingkat harga yang selaras dengan fitur yang diterapkan pada sebuah *smartphone* tersebut sehingga sesuai dengan kondisi pasar yaitu setara antara spesifikasi yang ditawarkan dengan tren harga pasar sehingga tidak terlalu berlebihan atau sebaliknya dalam menentukan sebuah harga ponsel tersebut. Hal ini tentunya juga dapat digunakan perusahaan untuk menjaga tingkat persaingan produk mereka agar tetap berkelanjutan.
+ Berhasilnya proyek ini diukur dari tingkat keberhasilan model dalam membantu perusahaan dalam mengambil sebuah keputusan untuk memprediksi harga pasar dari *smartphone* tersebut berdasarkan fitur yang telah ditanamkan pada *smartphone* tersebut sehingga perusahaan mampu mengurangi kesalahan dalam menetapkan harga serta tujuan terkait menjaga *product competitiveness* dapat dipenuhi.

### Solution Statement

1. Menganalisis data dengan melakukan univariate analysis dan multivariate analysis. Memahami data juga dapat dilakukan dengan visualisasi. Memahami data dapat membantu untuk mengetahui kolerasi antar fitur dan mendeteksi outlier.
2. Menyiapkan data agar bisa digunakan dalam membangun model dengan mendeteksi missing-value, dan melakukan one-hot-encoding untuk fitur kategorikal.
3. Melakukan model evelopment dengan ALgoritma msupervised machine learning yaitu linear regression yang dipakai dalam proyek ini adalah K-Nearest Neighbour, Random Forest, dan Booosting.

## Data Understanding & Removing Outlier

Dataset yang digunakan dalam proyek ini merupakan data harga smartphone dengan berbagai karakteristik. Dataset ini dapat diunduh di [Kaggle : Mobile Phone Specifications and Prices](https://www.kaggle.com/datasets/pratikgarai/mobile-phone-specifications-and-prices).

Berikut informasi pada dataset :

+ Dataset memiliki format CSV (Comma-Seperated Values).
+ Dataset memiliki 1360 sample dengan 21 fitur.
+ Dataset memiliki 7 fitur bertipe int64, 10 fitur bertipe object, dan 4 tipe float64
+ Tidak ada missing value dalam dataset.

### Variable - variable pada dataset
1. **Name**: Smartphone's series
2. **Brand**: Smartphone's brand
3. **Model**: Smartphone's model
4. **Battery Capacity (mAh)**: Smartphone's Battery Capacity
5. **Screen Sizes (Inch)**: Smartphone'screen size
6. **Touchscreen**: Touchscreen feature in smartphone (Yes/No)
7. **Resolution x**: Smartphone horizontal screen resolution
8. **Resolutiony**: Smartphone vertical screen resolution (Yes/No)
9. **Processor**: Smartphone's processor
10. **RAM(MB)**: Smartphone's RAM size
11. **Internal Storage (GB)**: Smartphone's internal storage size
12. **Rear Camera**: Smartphone's rear camera
13. **Front camera**: Smartphone's front camera (Yes/No)
14. **Operating System**: Smartphone's OS
15. **Wi-Fi**: Smartphone's wifi feature
16. **Bluetooth**: Smartphone's bluetooth feature
17. **GPS**: Smartphone's GPS feature
18. **Number of SIMs**: Number of SIMs on smartphone
19. **3G**: 3G feature on smartphone (Yes/No)
20. **4G/LTE**: 4G/LTE feature on smartphone (Yes/No)
21. **Price**: Smartphone's price

### Univariate Analysis

Univariate Analysis adalah menganalisis setiap fitur secara terpisah atau parsial.

#### Analisis jumlah nilai unique pada setiap fitur kategorik
Fitur Name dan Model memiliki sebaran sample yang cukup merata.
<div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%201.png" width="1000"/></div> <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%202.png" width="1000"/></div>

Berikut adalah fitur dengan sample yang tidak merata :

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata_8.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata_7.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata_6.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata_5.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata_4.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/Fitur%20tidak%20merata_3.png" width="1000"/></div>

#### Analisis sebaran pada setiap fitur numerik

<div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/fitur%20numerik.png" width="1000"/></div><br />
Berikut analisis dari grafik di atas :

+ Sebagian besar smartphone memiliki kapasitas battery 2000 - 3000 mAh dan terdistribusi normal.
+ Sebagian besar smartphone memiliki screen size 5 - 5.5 inch.
+ Sebagian besar harga smartphone tersebar di range harga 5000 - 10000.
+ Fitur num of sim pada smartphone di market seluruhnya memiliki dual sim

### Multivariate Analysis

Multivariate Analysis menunjukkan hubungan antara dua atau lebih fitur dalam data.

#### Analisis fitur kategorik

+ Fitur Size dan BHK (Menghapus BHK Outlier)

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/kat_multi.png" width="1000"/></div>
  
  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_10.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_2.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_3.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_4.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_5.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_6.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_7.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_8.png" width="1000"/></div>

  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/mv_kat_9.png" width="1000"/></div>

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

#### Analisis fitur Numerik

Analisis ini dilakukan untuk melihat kolerasi antara fitur kategorik dengan fitur target (Price).

+ Pairplot
  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/num_multi.png" width="1000"/></div>
+ Matrix Correlation
  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/matrix%20corr.png" width="1000"/></div>
  Seluruh fitur numerikal berkorelasi cukup kuat dalam mempengaruhi variabel target yaitu Price 

## Data preparation
+ One Hot Encoding

  One hot encoding adalah teknik mengubah data kategorik menjadi data numerik dimana setiap kategori menjadi kolom baru dengan nilai 0 atau 1. Fitur yang akan diubah menjadi numerik pada proyek ini adalah fitur dengan tipe object atau kategorikal. Hal ini perlu dilakukan karena sebuah model pembelajaran mesin tidak mampu melakukan *training* pada data tipe *string* sehingga diperlukan transformasi data menjadi numerik agar mesin mampu membaca data tersebut. 
  
+ Train Test Split

  Train test split aja proses membagi data menjadi data latih dan data uji. Data latih akan digunakan untuk membangun model, sedangkan data uji akan digunakan untuk menguji performa model. Pada proyek ini dataset sebesar 918 untuk data latih dan 102 untuk data uji. Metode ini perlu untuk dilakukan karena untuk membangun sebuah model *machine learning* diperlukan alokasi data untuk *training* dan *testing* dengan rasio tertentu supaya selain model dapat belajar, juga dapat melakukan *testing* pada data yang belum pernah dilihat sebelumnya. 

## Modeling

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

## Evaluation

Metrik evaluasi yang digunakan pada proyek ini adalah akurasi dan mean squared error (MSE). Akurasi menentukan tingkat kemiripan antara hasil prediksi dengan nilai yang sebenarnya (y_test). Mean squared error (MSE) mengukur error dalam model statistik dengan cara menghitung rata-rata error dari kuadrat hasil aktual dikurang hasil prediksi. Berikut formulan MSE :
<div><img src="https://user-images.githubusercontent.com/107544829/188412654-f5dc0ae1-901b-470e-aae5-1f6b5fb68b4d.png" width="1000"/></div>

Berikut hasil evaluasi pada proyek ini :

+ Mean Squared Error (MSE)
  <div><img src="https://github.com/PutraAndika88/Smartphone-Predictive-Analysis/blob/main/evaluation.png" width="300"/></div>

Dari hasil evaluasi dapat dilihat bahwa model dengan algoritma Random Forest memiliki akurasi lebih tinggi baik dan tingkat error lebih kecil dibandingkan algoritma lainnya dalam proyek ini.

## Reference
[1] 	J. Degenhard, "Statista," 30 January 2024. [Online]. Available: https://www.statista.com/forecasts/1143723/smartphone-users-in-the-world#statisticContainer.

[2] 	S. Sadya, "Dataindonesia," 17 January 2023. [Online]. Available: https://dataindonesia.id/telekomunikasi/detail/pengguna-smartphone-indonesia-terbesar-keempat-dunia-pada-2022.

[3] 	V. W. Siburian and I. E. Mulyana, "Prediksi Harga Ponsel Menggunakan Metode Random Forest," Computer Science and ICT, pp. 144-147, 2018. DOI: seminar.ilkom.unsri.ac.id:article/1992

