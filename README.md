# Proyek Pertama Smartphone Price Prediction
### Disusun Oleh : Putra Andika Pradana

Ini adalah proyek pertama predictive analytics untuk memenuhi submission dicoding. Proyek ini membangun model machine learning yang dapat memprediksi harga smartphone berdasarkan fitur-fitur spesifikasi dari smartphone.

## Domain Proyek
### Latar Belakang
Kebutuhan akan smartphone pada saat ini bukanlah menjadi kebutuhan tersier melainkan telah menjadi kebutuhan pokok setiap orang. Smartphone kini telah menjadi barang yang sifatnya vital dalam mendukung fungsi dari kehidupan manusia seperti membantu dalam bekerja dan untuk menjadi lebih produktif. Kebutuhan akan smartphone yang masif juga merupakan dampak dari kemajuan teknologi yang tiada henti sehingga manusia dipaksa untuk terus mengikuti perkembangan zaman untuk tetap kompetitif. Fenomena tersebut tentu perusahaan elektronik khususnya produsen smartphone perlu untuk terus memenuhi permintaan pasar smartphone yang membludak dan tentunya perusahaan juga perlu untuk tetap kompetitif dalam bersaing dengan kompetitor. Oleh karena itu, analisis ini dilakukan untuk membantu perusahaan produsen samrtphone dalam menjaga sustainability bisnisnya agar tetap kompetitif di pasar smartphone dan tidak salah dalam memasang harga smartphone ketika produk barunya akan dirilis di pasar smartphone. 
![image](https://github.com/PutraAndika88/smartphone-prediction-machine-learning/assets/133973000/f679c9ca-abbe-42e6-a4e5-e7f3627a89d2)


[Referensi gambar](https://chatnews.id/read/harga-smartphone-5g-mulai-terjangkau)


Harga dari setiap smartphone diukur dari nilai yang dimiliki oleh smartphone tersebut. Namun, harga ini tidak selalu pasti dan sulit untuk melakukan prediksi akurat secara manual. Faktor ketidakpastian perlu dikurangi oleh perusahaan yang memproduksi smartphone dengan membangun sistem prediksi yang dapat menentukan berapa harga pasaran smartphone tersebut yang pantas untuk spesifikasi smartphone tertentu.

Dalam mencapai hal tersebut, maka dilakukan penelitian untuk memprediksi harga smartphone menggunakan model machine learning. Diharapkan model ini mampu memprediksi harga smartphone yang sesuai dengan harga pasar. Prediksi ini nantinya dijadikan acuan bagi perusahaan dalam mengedarkan smartphone dan mengatur harga pasar tepat dan kompetitif sehingga mampu meningkatkan profit lebih baik lagi bagi perusahaan.

Referensi : [Prediksi Harga Ponsel Menggunakan Metode Random Forest](https://core.ac.uk/download/pdf/235044836.pdf)

## Business Understanding

Proyek ini dibangun untuk perusahaan dengan karakteristik bisnis sebagai berikut :

+ Perusahaan elektronik yang berfokus sebagai produsen smartphone dengan tipe smartphone mulai kelas entry-level hingga flagship

### Problem Statement

1. Bagaimana cara mengidentifikasi terkait fitur yang paling berpengaruh terhadap harga smartphone?
2. Bagaimana cara mengidentifikasi harga smartphone yang tepat di pasaran berdasarkan karakteristik atau spesifikasi tertentu?

### Goals

1. Perusahaan produsen smartphone dapat mengidentifikasi fitur smartphone yang paling mempengaruhi performa harga smartphone di pasaran.
2. Perusahaan produsen smartphone mampu mengatur price pada setiap lini dan spesifikasi produk mereka sehingga sesuai dengan kondisi pasar untuk menjaga product competitiveness. 

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

  One hot encoding adalah teknik mengubah data kategorik menjadi data numerik dimana setiap kategori menjadi kolom baru dengan nilai 0 atau 1. Fitur yang akan diubah menjadi numerik pada proyek ini adalah fitur dengan tipe object atau kategorikal.
  
+ Train Test Split

  Train test split aja proses membagi data menjadi data latih dan data uji. Data latih akan digunakan untuk membangun model, sedangkan data uji akan digunakan untuk menguji performa model. Pada proyek ini dataset sebesar 918 untuk data latih dan 102 untuk data uji.

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
