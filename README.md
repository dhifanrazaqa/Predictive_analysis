# Laporan Proyek Machine Learning - Dhi'fan Razaqa

## Domain Proyek
Pasar energi mulai mengalami tekanan sejak 2021 akibat pemulihan ekonomi yang cepat pasca pandemi. Situasi ini semakin memburuk setelah invasi Rusia ke Ukraina pada Februari 2022, yang menyebabkan lonjakan harga gas alam dan listrik serta kenaikan harga minyak ke level tertinggi sejak 2008. Kenaikan harga energi ini memicu inflasi tinggi, meningkatkan angka kemiskinan, memperlambat pertumbuhan ekonomi, dan bahkan memaksa beberapa pabrik untuk mengurangi produksi atau tutup. Eropa, yang sangat bergantung pada pasokan gas dari Rusia, menghadapi ancaman pembatasan gas, sementara negara berkembang mengalami lonjakan biaya impor energi dan kelangkaan bahan bakar.

Berbeda dengan krisis minyak pada 1970-an yang hanya melibatkan minyak bumi, krisis saat ini mencakup semua bahan bakar fosil. Dengan ekonomi global yang semakin terhubung, dampaknya semakin luas dan menjadikannya krisis energi global pertama yang benar-benar menyeluruh. Beberapa pabrik di Eropa terpaksa mengurangi produksi karena mahalnya biaya operasional. Negara berkembang yang sudah menghadapi tekanan ekonomi akibat tingginya biaya energi dan pangan kini mengalami peningkatan kemiskinan ekstrem. Bahkan di negara maju, kenaikan harga energi berdampak pada rumah tangga rentan dan menyebabkan ketegangan ekonomi, sosial, serta politik.

### Mengapa Masalah Ini Penting?
Kenaikan harga energi menyebabkan inflasi tinggi, meningkatnya angka kemiskinan, dan perlambatan pertumbuhan ekonomi. Banyak industri, terutama di Eropa dan negara berkembang, mengalami penurunan produksi akibat mahalnya biaya energi, yang pada akhirnya berdampak pada ketahanan ekonomi global. Harga energi yang tinggi membebani rumah tangga, terutama yang berpenghasilan rendah. Ini dapat memicu ketegangan sosial dan politik di banyak negara, terutama jika pemerintah tidak mampu memberikan subsidi atau alternatif yang terjangkau.

### Bagaimana Masalah Ini Harus Diselesaikan?
Mengurangi ketergantungan pada bahan bakar fosil dengan meningkatkan investasi dalam energi terbarukan seperti tenaga surya, angin, dan hidro untuk memastikan pasokan energi yang lebih stabil. Negara-negara perlu bekerja sama untuk mengamankan pasokan energi global dan menghindari ketegangan geopolitik yang memperburuk krisis. Mengembangkan infrastruktur yang lebih efisien, seperti bangunan hemat energi dan transportasi berbasis listrik. Menerapkan sistem manajemen energi yang cerdas menggunakan model prediktif untuk mengoptimalkan konsumsi energi di berbagai sektor.

[Global Energy Crisis](https://www.iea.org/topics/global-energy-crisis)  
[World Energy Outlook 2022](https://www.iea.org/reports/world-energy-outlook-2022) 

## Business Understanding
Pada era digital saat ini, konsumsi energi menjadi salah satu faktor utama yang mempengaruhi efisiensi operasional di berbagai sektor. Prediksi konsumsi energi yang akurat dapat membantu pengambilan keputusan dalam mengurangi biaya operasional, meningkatkan efisiensi energi, dan mengurangi dampak lingkungan.
### Problem Statements
- **Perubahan Konsumsi Energi**  
  Konsumsi energi dipengaruhi oleh berbagai faktor seperti suhu, kelembaban, waktu penggunaan, dan keberadaan sistem HVAC serta pencahayaan. Ketidakmampuan dalam memprediksi konsumsi energi dapat menyebabkan pemborosan atau kekurangan daya yang mengganggu operasional bisnis.

- **Ketergantungan pada Sumber Energi Tidak Terbarukan**  
  Sebagian besar konsumsi energi masih bergantung pada bahan bakar fosil. Dengan lonjakan harga energi global, bisnis perlu mengoptimalkan pemanfaatan sumber energi terbarukan agar lebih efisien dan berkelanjutan.

### Goals
- **Mengembangkan Model Prediksi Konsumsi Energi**  
  Menggunakan teknik machine learning untuk memprediksi konsumsi energi berdasarkan variabel-variabel seperti suhu, kelembaban, waktu, dan penggunaan sistem HVAC serta pencahayaan.

- **Meningkatkan Efisiensi Energi dengan Pemanfaatan Energi Terbarukan**  
  Mengidentifikasi pola konsumsi energi dan bagaimana energi terbarukan dapat dimanfaatkan lebih optimal untuk mengurangi ketergantungan pada sumber energi konvensional.

### Solution statements
- **Penerapan Model Machine Learning**  
  Menggunakan Linear Regression dan Random Forest Regressor sebagai baseline model untuk melihat hubungan antara variabel independen dengan konsumsi energi.

- **Hyperparameter Tuning**  
  Meningkatkan performa model dengan optimasi hyperparameter menggunakan GridSearchCV untuk mendapatkan kombinasi parameter terbaik.

- **Evaluasi Model**  
  Menilai performa model menggunakan metrik Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), dan R² Score untuk memastikan akurasi dan efektivitas prediksi.

## Data Understanding
Dataset yang digunakan adalah dataset [Energy Consumption Prediction](https://www.kaggle.com/datasets/ajinilpatel/energy-consumption-prediction) yang merupakan dataset time-series yang menunjukkan pola konsumsi energi setiap jam dan setiap hari selama satu tahun. Dataset ini awalnya berisi 1000 baris yang bersumber dari Kaggle, dengan beberapa kesalahan dan ketidakkonsistenan. Setelah pembersihan dan praproses menyeluruh, 4000 baris tambahan data sintetis dihasilkan untuk mencocokkan distribusi dataset asli sehingga menghasilkan total 5000 baris. Dataset yang diperluas mempertahankan statistik yang sama seperti aslinya sehingga cocok untuk berbagai tugas analitis dan prediktif yang terkait dengan konsumsi energi.

### Variabel-variabel pada Energy Consumption Prediction dataset adalah sebagai berikut:
- Month: Mewakili bulan dalam setahun (1–12). Berguna untuk mengkategorikan data bulan ke dalam musim.
- Hour: Pembacaan per jam dalam sehari (0–23), berguna untuk mengkategorikan data waktu ke dalam pagi, siang, sore, dan malam.
- DayOfWeek: Variabel kategoris yang menunjukkan hari dalam seminggu
- Holiday: Variabel kategoris Boolean yang menunjukkan apakah hari tersebut adalah hari libur.
- Temperature: Variabel numerik yang mewakili suhu dalam derajat Celsius.
- Humidity: Variabel numerik yang menunjukkan tingkat kelembaban sebagai persentase.
- SquareFootage: Variabel numerik yang mengukur luas bangunan atau ruang.
- Occupancy: Variabel numerik yang mewakili jumlah orang di area tersebut.
- HVACUsage: Variabel kategoris yang menunjukkan penggunaan sistem Pemanas, Ventilasi, dan Pendingin Udara.
- LightingUsage: Variabel kategoris yang menunjukkan penggunaan sistem pencahayaan.
- RenewableEnergy: Variabel numerik yang mewakili persentase kontribusi sumber energi terbarukan.
- EnergyConsumption: Variabel target numerik yang mewakili total energi yang dikonsumsi.

### Exploratory Data Analysis (EDA)
- **Distribusi Konsumsi Energi**
  ![download](https://github.com/user-attachments/assets/8cb638cc-abfd-48c9-8761-179d7f3ce4cb)
  Nilai konsumsi energi paling banyak ada di rentang 70-80. Hal ini menunjukkan tren konsumsi energi yang tidak terlalu tinggi atau rendah, tetapi berada di tengah-tengah.

- **Distribusi Penggunaan HVAC**
  ![download](https://github.com/user-attachments/assets/6c24fc68-7dba-4263-b9df-d15262782f70)
  Distribusi penggunaan HVAC (Heating, Ventilation, and Air Conditioning systems) cukup merata, jumlah nilai on dan off pada penggunaan HVAC bisa dibilang sama.
  
- **Distribusi Penggunaan Pencahayaan**
  ![download](https://github.com/user-attachments/assets/a92b593d-e793-408f-9804-cfbb96d7837f)
  Distribusi penggunaan pencahayaan atau lampu juga cukup merata, jumlah nilai on dan off pada penggunaan pencahayaan bisa dibilang hampir sama.
  
- **Konsumsi Energi Berdasarkan Bulan**
  ![download](https://github.com/user-attachments/assets/3441a00f-4ffd-4cce-be5c-3b3cf648d433)
  Menunjukkan tren konsumsi energi setiap bulannya, bulan ke-4 atau bulan April menjadi bulan dengan rata-rata konsumsi energi yang paling tinggi. Bulan Juni menduduki posisi sebagai bulan dengan konsumsi energi yang paling rendah.
  
- **Konsumsi Energi Berdasarkan Hari dalam Seminggu**
  ![download](https://github.com/user-attachments/assets/879e1e18-3fd3-433f-bcd4-235dbab1b219)
  Tren menunjukkan hari Sabtu menjadi hari dengan konsumsi energi paling banyak, hal ini mungkin disebabkan oleh weekend sehingga lebih banyak orang di rumah. Hari Senin menjadi hari dengan konsumsi energi terendah, biasanya orang berada di luar rumah ketika hari Senin.
  
- **Hubungan antara Suhu dan Konsumsi Energi**
  ![download](https://github.com/user-attachments/assets/2e61570a-484a-44b0-840c-ab4448baf277)
  Terdapat hubungan yang menarik antara suhu dengan konsumsi energi, dimana dengan naiknya suhu meningkat juga konsumsi energinya. Hubungan ini didapatkan melalui penggunaan HVAC (Heating, Ventilation, and Air Conditioning systems) yang akan "On" saat suhu meningkat atau panas.

## Data Preparation
Tahapan ini bertujuan untuk mempersiapkan data agar siap digunakan pada proses model development. Tahapan ini meliputi Encoding, Data Splitting, dan Standarisasi. Hal-hal yang dilakukan pada tahap ini sangat krusial untuk performa model. Sebelum melaju ke tahap berikutnya data fitur dan target harus dipisahkan terlebih dahulu, biasanya data fitur disimpan dalam variabel X dan data target disimpan dalam variabel y. **Perlu diingat semua proses data preparation hanya dilakukan untuk data fitur atau variabel X saja**.
### Encoding Fitur Kategori
- **Apa itu?**  
Proses yang pertama dilakukan adalah encoding fitur kategori, seperti yang kita ketahui komputer tidak dapat memahami sebuah data kategori sehingga kita perlu mengubah nya menjadi data numerik. Salah satu teknik encoding adalah **One-Hot Encoding** yang mengubah data kategorikal menjadi numerik tanpa menganggap ada hubungan ordinal antar kategori sehingga dapat digunakan dalam model machine learning. Setiap kategori dalam fitur kategorikal diubah menjadi vektor biner, di mana hanya satu elemen yang bernilai **1** dan sisanya **0**. Misalnya, jika ada dua kategori ("On", "Off"), masing-masing akan diwakili sebagai `[1,0]` dan `[0,1]`.
- **Mengapa Perlu?**  
Teknik ini diperlukan karena algoritma machine learning umumnya tidak dapat bekerja langsung dengan data kategorikal dan membutuhkan data numerik agar dapat memahami pola dan hubungan dalam data.

### Data Splitting
- **Apa itu?**   
**Data Splitting** adalah teknik yang digunakan dalam machine learning untuk membagi dataset menjadi dua bagian, dalam kasus ini **80% untuk training** dan **20% untuk testing**. Data **training** digunakan untuk melatih model agar memahami pola dalam data, sementara data **testing** digunakan untuk mengevaluasi performa model terhadap data yang belum pernah dilihat sebelumnya. Rasio ini populer karena memberikan cukup data untuk pembelajaran sekaligus mempertahankan sejumlah data untuk validasi, sehingga model dapat diuji dengan lebih akurat sebelum diterapkan dalam skenario dunia nyata.
- **Mengapa Perlu?**   
Data splitting diperlukan dalam machine learning untuk memastikan bahwa model dapat belajar dari data dengan baik tanpa mengalami overfitting atau terlalu bergantung pada satu dataset. Jika model hanya diuji menggunakan data training, ia mungkin bekerja sangat baik di dataset itu tetapi gagal mengenali pola dalam data baru.

### Standarisasi
- **Apa itu?**   
Standarisasi adalah teknik dalam preprocessing data yang bertujuan untuk menyelaraskan skala fitur numerik sehingga memiliki mean = 0 dan standard deviation = 1. Ini dilakukan dengan mengurangi mean dari setiap nilai dan membaginya dengan standard deviation, sehingga distribusi data menjadi lebih seimbang dan tidak berat sebelah. Perlu dicatat, untuk mencegah **data leakage** proses standarisasi harus dilakukan setelah dataset dibagi menjadi data train dan test.
- **Mengapa Perlu?**   
Standarisasi diperlukan karena banyak algoritma machine learning, seperti regresi lebih sensitif terhadap skala fitur. Dengan standarisasi, model dapat belajar lebih stabil dan menghasilkan prediksi yang lebih akurat.

## Modeling
Model machine learning yang digunakan pada proyek ini adalah Random Forest Regressor dan Linear Regression. Keduanya akan digunakan untuk memecahkan masalah regresi untuk prediksi konsumsi energi.

### Random Forest Regressor Base & Hyperparameter Tuning   
Random Forest Regressor adalah algoritma regresi berbasis Decision Tree yang menggunakan banyak pohon (ensemble learning) untuk membuat prediksi yang lebih akurat dan stabil dibandingkan satu Decision Tree. Model ini bekerja dengan membangun beberapa Decision Tree dan menggabungkan hasilnya dengan rata-rata prediksi dari semua pohon.   
#### **Kelebihan:**   
- Lebih akurat karena merupakan ensemble learning
- Lebih toleran terhadap outlier karena menggunakan banyak Decision Tree          
#### **Kekurangan:**   
- Training lambat karena menggunakan banyak Decision Tree
- Kurang optimal untuk dataset kecil   
#### **Parameter:**   
- Pada base model tidak dilakukan penyesuaian hyperparameter, semua hyperparameter yang digunakan adalah default.
- Pada Tuned model parameter seperti n_estimator, max_depth, min_samples_split, dan min_samples_leaf diatur nilainya mengikuti hasil dari Hyperparameter Tuning.   
#### **Improvement Hyperparameter Tuning:**   
Proses Hyperparameter Tuning yang dilakukan menggunakan teknik GridSearchCV yang akan mencoba satu-persatu semua kemungkinan parameter terbaik, hasil akhirnya adalah sekumpulan parameter yang menghasilkan performa model paling baik.   
Setelah proses GridSearchCV hasil parameter terbaiknya adalah:   
`{'max_depth': 10, 'min_samples_leaf': 4, 'min_samples_split': 10, 'n_estimators': 300}`

### Linear Regression    
Linear Regression adalah algoritma machine learning yang digunakan untuk memodelkan hubungan antara variabel independen (features) dan variabel dependen (target) menggunakan garis lurus. Model ini mencoba menemukan koefisien terbaik yang meminimalkan selisih antara prediksi dan nilai sebenarnya dengan metode Least Squares.
#### **Kelebihan:**   
- Sederhana dan mudah dipahami
- Cepat dan efisien untuk dataset besar        
#### **Kekurangan:**   
- Sensitif terhadap outlier
- Kurang akurat untuk data yang tidak benar-benar linear     
#### **Parameter:**   
- Pada model tidak dilakukan penyesuaian hyperparameter, semua hyperparameter yang digunakan adalah default.

### Memilih Model Terbaik
Tanpa melihat hasil dari evaluasi model, algoritma yang akan dipilih sebagai solusi adalah Linear Regression karena sangat cocok dengan karateristik dataset yang digunakan. Linear Regression sensitif terhadap outlier dan pada dataset yang digunakan tidak terdapat outlier. Selain itu, Linear Regression juga efektif untuk dataset yang besar, dataset yang digunakan memang tidak terlalu besar tetapi sangat cocok untuk algoritma ini. 

## Evaluation
Metrik evaluasi yang digunakan dalam kasus ini adalah Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), dan R² Score. Keempat metrik ini sesuai digunakan dengan konteks data, problem statement, dan solusi yang diinginkan untuk kasus prediksi tingkat konsumsi energi.
### Mean Squared Error
![dos-b717066bbe42ad8d092945ed8a1b152420241016110235](https://github.com/user-attachments/assets/317a7533-2001-4d9d-abb6-8503b3507c15)    
Mean Squared Error (MSE) adalah metrik yang menghitung rata-rata kuadrat selisih antara nilai aktual dan nilai prediksi. Dengan mengkuadratkan selisih tersebut, MSE memberikan bobot lebih besar terhadap kesalahan yang lebih besar, sehingga lebih sensitif terhadap outlier. Metrik ini sering digunakan dalam regresi karena memberikan gambaran seberapa jauh prediksi menyimpang dari nilai sebenarnya, tetapi satuannya adalah kuadrat dari variabel target, yang bisa membuat interpretasi menjadi kurang intuitif.

### Root Mean Squared Error
![image](https://github.com/user-attachments/assets/05249e0c-ac49-48f6-a13d-2ddc98c42856)    
Root Mean Squared Error (RMSE) adalah akar dari MSE, yang mengembalikan kesalahan ke skala asli variabel target, sehingga lebih mudah diinterpretasikan dibandingkan MSE. Karena RMSE masih berbasis kuadrat, ia tetap sensitif terhadap outlier, tetapi lebih intuitif dalam memahami seberapa besar rata-rata kesalahan prediksi dalam satuan yang sama dengan target. RMSE sering digunakan ketika model harus menangani variasi data yang besar dan di mana penalti untuk kesalahan yang lebih besar perlu diperhatikan.

### Mean Absolute Error
![dos-11feda41b23139f0de73ed8c634dc6e920241016110235](https://github.com/user-attachments/assets/8bb43129-3aa0-4fb7-bda6-2fe0fc75b149)    
Mean Absolute Error (MAE) mengukur rata-rata selisih absolut antara nilai aktual dan prediksi tanpa mengkuadratkan error, sehingga tidak terlalu dipengaruhi oleh outlier dibandingkan MSE atau RMSE. MAE lebih mudah diinterpretasikan karena nilainya dalam skala yang sama dengan variabel target. Namun, MAE tidak menangkap perbedaan besar dalam kesalahan dengan cara yang sama seperti MSE atau RMSE, sehingga tidak memberikan bobot lebih pada kesalahan besar.

### R² Score
![dos-f54b3a820aa37b345729c961c3e01f4f20241016110235](https://github.com/user-attachments/assets/ec3615f4-96cd-4852-b816-b5b2dd664c67)    
R² juga dikenal sebagai coefficient of determination adalah salah satu metrik yang digunakan untuk mengevaluasi seberapa baik model regresi linear menjelaskan variasi dalam data. R² memberikan ukuran proporsi variasi dalam variabel dependen (output) yang dapat dijelaskan oleh variabel independen (input) dalam model. R² dihitung dengan menggunakan perbandingan antara variasi total dalam data dan variasi yang dapat dijelaskan oleh model regresi.




Pada bagian ini anda perlu menyebutkan metrik evaluasi yang digunakan. Lalu anda perlu menjelaskan hasil proyek berdasarkan metrik evaluasi yang digunakan.

Sebagai contoh, Anda memiih kasus klasifikasi dan menggunakan metrik **akurasi, precision, recall, dan F1 score**. Jelaskan mengenai beberapa hal berikut:
- Penjelasan mengenai metrik yang digunakan
- Menjelaskan hasil proyek berdasarkan metrik evaluasi

Ingatlah, metrik evaluasi yang digunakan harus sesuai dengan konteks data, problem statement, dan solusi yang diinginkan.

**Rubrik/Kriteria Tambahan (Opsional)**: 
- Menjelaskan formula metrik dan bagaimana metrik tersebut bekerja.

**---Ini adalah bagian akhir laporan---**

_Catatan:_
- _Anda dapat menambahkan gambar, kode, atau tabel ke dalam laporan jika diperlukan. Temukan caranya pada contoh dokumen markdown di situs editor [Dillinger](https://dillinger.io/), [Github Guides: Mastering markdown](https://guides.github.com/features/mastering-markdown/), atau sumber lain di internet. Semangat!_
- Jika terdapat penjelasan yang harus menyertakan code snippet, tuliskan dengan sewajarnya. Tidak perlu menuliskan keseluruhan kode project, cukup bagian yang ingin dijelaskan saja.

