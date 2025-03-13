# Laporan Proyek Machine Learning - Abiyyu Rasyiq Muhadzzib

## Domain Proyek

Dalam industri gaming yang berkembang pesat, memahami perilaku pemain dan engagement mereka terhadap sebuah game menjadi hal yang sangat penting bagi pengembang game. Engagement level pada pemain mencerminkan loyalitas, kepuasan, dan retensi pemain terhadap game tersebut. Menurut Vasalou et al., terdapat banyak faktor yang mempengaruhi engagement, seperti waktu bermain, banyaknya sesi permainan, jenis permainan yang dimainkan, serta interaksi sosial di dalam game [1].

Masalah utama yang dihadapi oleh industri game adalah kurangnya kemampuan industri game dalam menganalisis perilaku pemain secara mendalam. Menurut Deterding (2013), kurangnya kemampuan untuk menganalisis perilaku pemain dapat menghambat retensi pemain retensi pemain, sehingga berisiko menurunkan tingkat engagement serta loyalitas pemain [2]. Oleh karena itu, kemampuan analisis perilaku pemain yang tepat dapat membantu pengembang game merumuskan strategi yang efektif dan mempertahankan loyalitas pemain [3].

Salah satu solusi yang diusulkan untuk mengatasi masalah ini adalah dengan memanfaatkan machine learning untuk menganalisis dan memprediksi engagement level pemain. Hal ini dibukti dengan penelitian yang dilakukan oleh A. A. R. Alzahrani et a., menunjukkan bahwa machine learning dapat secara efektif memprediksi tingkat engagement pemain berdasarkan aktivitas mereka, yang mencakup frekuensi sesi dan pembelian dalam game [4]. Penelitian lain yang dilakukan oleh M. Hussain et al., juga dapat diterapkan dalam konteks game untuk menganalisis perilaku pemain dan memprediksi engagement dengan akurasi tinggi [5]. Dengan memanfaatkan pendekatan ini, industri game dapat memahami perilaku pemain secara lebih mendalam dan merumuskan strategi yang lebih baik untuk meningkatkan engagement dan loyalitas pemain. 

## Business Understanding

Industri gaming saat ini menghadapi tantangan signifikan akibat kurangnya kemampuan dalam menganalisis perilaku pemain secara mendalam, yang berpotensi mengurangi efektivitas strategi untuk meningkatkan engagement dan retensi pemain. Keterbatasan ini dapat mengakibatkan penurunan loyalitas pemain, sehingga memperburuk keberhasilan dan keberlangsungan game di pasar yang kompetitif.

Dalam proyek ini, tujuan utama adalah menerapkan analisis prediktif untuk mendeteksi engagement level pada pemain dengan mamanfaatkan beberapa faktor seperti, durasi bermain, banyaknya bermain dalam per minggu, level pemain, jenis permainan, dan faktor lainnya.

### Problem Statements

- Bagaimana memprediksi level engagement pemain berdasarkan perilaku bermain mereka?

Banyak fitur terkait perilaku pemain, seperti waktu bermain, frekuensi login, dan pembelian in-game, memerlukan analisis mendalam untuk mengidentifikasi fitur yang paling berpengaruh terhadap engagement. Tantangannya adalah mengekstraksi pola dari perilaku pemain, karena tidak semua fitur memberikan hasil yang sama.

- Bagaimana model machine learning dapat digunakan untuk menganalisis dan memprdiksi engagement level pemain secara akurat?

Penting untuk memilih dan membangun model machine learning yang tepat untuk menganalisis dan memprediksi level engagement pemain. Beberapa algoritma yang dapat digunakan termasuk Random Forest, XGBoost, dan Neural Networks.

### Goals

- Mengidentifikasi fitur-fitur utama yang mempengaruhi engagement level pemain untuk membantu pengambilan keputusan dalam pengembangan game.

Dengan menggunakan teknik analisis data, seperti analisis korelasi dan feature importance, kita dapat menentukan fitur-fitur signifikan yang mempengaruhi tingkat engagement pemain, seperti waktu bermain, jenis permainan, dan interaksi sosial. Wawasan ini akan membantu pengembang game dalam membuat keputusan strategis, seperti menambahkan fitur baru dan merancang konten yang lebih menarik.

- Memilih model prediktif yang mampu mengklasifikasikan engagement level pemain secara akurat, dengan menggunakan data perilaku bermain.

Model akan menggunakan data perilaku bermain, termasuk fitur seperti waktu bermain, frekuensi login, dan interaksi sosial, dan dievaluasi berdasarkan metrik seperti akurasi, precision, dan recall. Model yang efektif memungkinkan pengembang mengidentifikasi pemain yang membutuhkan perhatian lebih atau yang berisiko kehilangan minat, sehingga dapat melakukan intervensi untuk meningkatkan retensi pemain.

### Solution statements

- Melakukan Exploratory Data Analysis (EDA) pada dataset untuk menganalisis fitur yang mempengaruhi engagement level pada pemain

Dengan memahami struktur dataset, analisis distribusi, dan analisis korelasi antar fitur dapat memberikan memberikan wawasan yang lebih dalam tentang faktor-faktor yang memengaruhi engagement level pemain. Hal ini juga dapat membantu dalam melakukan seleksi fitur pada preparation dataset


- Menerapkan tiga algoritma prediksi, yaitu Random Forest, Logistic Regression,dan Gradient Boosting

Menerapkan 3 algoritma machine learning untuk kalasifikasi engagement level, yaitu Random Forest, Logistic Regression, dan Gradient Boosting. Setelah model dilatih, memilih model terbaik dengan melakukan evaluasi menggunakan metrik yang relevan, seperti akurasi, precision, recall, dan F1 score.


## Data Understanding

### About Dataset

Dataset yang digunakan adalah Online Gaming Behavior Dataset. Dataset ini berfokus perilaku pemain dalam lingkungan game online. Dataset ini memiliki 40034 data, mencangkup berbagai matriks dan demografis yang berhubungan dengan engagement pemain. menurut informasi dari dataset langsung, dataset ini dapat digunakan untuk memprediksi pola perilaku pemain dan mengidentifikasi faktor-faktor yang mempengaruhi engagement dan retensi dari pemain. 

Dataset ini bersifat sintetis, karena itulah dataset ini tidak ada jaminan tertentu terkait kesempurnaan datanya. Namun, dataset ini ideal untuk proyek-proyek data science dan machine learning diciptakan untuk  tujuan edukasi. Dibuat oleh Rabie El Kharoua, dataset ini tersedia di bawah lisensi CC BY 4.0, sehingga bebas digunakan selama memberikan atribusi yang tepat kepada pembuatnya. Dataset ini didapat melalu website kaggel. Berikut merupakan link dari dataset tersebut:

https://www.kaggle.com/datasets/rabieelkharoua/predict-online-gaming-behavior-dataset

### Variabel-variabel pada Online Gaming Behavior Dataset adalah sebagai berikut:
- PlayerID: Pengenal unik untuk setiap pemain.
- Age: Usia pemain.
- Gender: Jenis kelamin pemain.
- Location: Lokasi geografis pemain.
- GameGenre: Genre permainan yang dimainkan oleh pemain.
- PlayTimeHours: Rata-rata waktu bermain dalam jam per sesi.
- InGamePurchases: Menunjukkan apakah pemain melakukan pembelian dalam game (0 = Tidak, 1 = Ya).
- GameDifficulty: Tingkat kesulitan permainan.
- SessionsPerWeek: Jumlah sesi permainan per minggu.
- AvgSessionDurationMinutes: Rata-rata durasi setiap sesi permainan dalam menit.
- PlayerLevel: Level pemain saat ini dalam permainan.
- AchievementsUnlocked: Jumlah pencapaian yang telah dibuka oleh pemain.
- EngagementLevel: Tingkat keterlibatan yang mencerminkan retensi pemain ('Tinggi', 'Sedang', 'Rendah').

### Statistical Analysis of Numerical Variables

Melakukan analisi data menggunakan fungsi ```describe()``` untuk menganalisi statistik variabel numerik.fungsi ini akan memperlihatkan mean, standar deviasi, median, nilai minimum dan nilai maksimal.

|index|PlayerID|Age|PlayTimeHours|InGamePurchases|SessionsPerWeek|AvgSessionDurationMinutes|PlayerLevel|AchievementsUnlocked|
|---|---|---|---|---|---|---|---|---|
|count|40034\.0|40034\.0|40034\.0|40034\.0|40034\.0|40034\.0|40034\.0|40034\.0|
|mean|29016\.5|31\.9925313483539|12\.024365373325825|0\.20085427386721286|9\.471773992106709|94\.79225158615178|49\.65556776739771|24\.52647749412999|
|std|11556\.964675034704|10\.043226791634499|6\.914637905333817|0\.40064428614987424|5\.763667125348743|49\.01137453870166|28\.588379140405436|14\.430726177622933|
|min|9000\.0|15\.0|0\.0001146866199155|0\.0|0\.0|10\.0|1\.0|0\.0|
|25%|19008\.25|23\.0|6\.067500507750126|0\.0|4\.0|52\.0|25\.0|12\.0|
|50%|29016\.5|32\.0|12\.00800215801307|0\.0|9\.0|95\.0|49\.0|25\.0|
|75%|39024\.75|41\.0|17\.963831138295756|0\.0|14\.0|137\.0|74\.0|37\.0|
|max|49033\.0|49\.0|23\.999591633580454|1\.0|19\.0|179\.0|99\.0|49\.0|

berikut merupakan informasi yang didapatkan:
*  Pada kolom 'Age' rata-rata player adalah 32 tahun, dengan umur paling muda 15 tahun dan paling tua 49 tahun.
*   Pada kolom 'PlayTimeHours' rata-rata player bermain selama 12 jam dengan paling singkat selama >1 jam dan paling lama 24 jam.
*   Pada kolom 'InGamePurchases' rata-rata player tidak melakukan pembelian dalam game.
*  Pada kolom 'SessionPerWeek' rata-rata player bermain 9 sesi per minggu , dengan 19 sesi paling banyak.
* Pada 'AvgSessionDurationMinutes' rata-rata bermain selama 94 menit, dengan 10 menit paling cepat dan 179 menit paling lama.
* Pada 'Playerlevel' rata-rata player mencapai level 49
* Pada 'AchievementsUnlocked' rata-rata player telah membuka 24 Achievement.

### Data Condition

Melakukan pemerikasaan kondisi data, apakah data memiliki nilai null atau tidak. Dengan fungsi `Isnull()`. Berikut ini adalah hasil kondisi dataset

![null_value](https://github.com/user-attachments/assets/48bd4475-91b2-460d-84e5-1bdd92c46f5a)

Hasil tersebut memberikan informasi bahwa dataset bersih dari nilai null. 

selanjutnya, melakukan pemerikasaan apakah dataset memiliki outlier pada variabel numerik. Pemeriksaan ini menggunakan plotbox yang tersedia pada library seaborn. Berikut ini merupakan output yang ditampilkan

![Box_plot](https://github.com/user-attachments/assets/b86177ee-3536-4396-ba19-92afeeea07cb)


Output tersebut memberikan informasi, bahwa dataset bersih dari outlier.

Informasi diatas memberitahukan kita bahwa dataset bersih dari noise seperti nilai null dan outlier. Hal tersebut kemungkinan disebabkan oleh dataset yang dibuat untuk tujuan proyek-proyek data science dan machine learning diciptakan untuk  tujuan edukasi.

### Univariate Analysis
Selanjutnya, melakukan analisis data dengan melihat distribusi dataset dari masing masing variabel/fiturnya. Pertama memeriksa distribusi masing-masing dari fitur kategori.

#### Gender
![Gender](https://github.com/user-attachments/assets/36cb9576-3450-42e8-9d6e-56569038fea0)

Distribusi gender pada dataset tidak seimbang, dengan didominasi oleh laki-laki 59% sedangkan untuk perempuan hanya 40%. Dapat disimpulkan bahwa laki-laki memiliki keterlibatan yang tinggi dengan game

#### Location

![Location](https://github.com/user-attachments/assets/86ba8f46-2579-4228-9f7c-dd0e5c05c284)

Pada fitur lokasi terdapat 4 lokasi pada dataset, yaitu USA, Europe, Asia, dan lain-lain. Distribusi juga tidak seimbang dengan USA 40%, sementara untuk eropa dan asia hanya 30% dan 20%, dan untuk lokasi lain hanya 9.8%. Dapat disimpulkan USA menjadi lokasi pemain paling banyak disusul dengan eropa dan asia.

#### Game Genre

![GameGenre](https://github.com/user-attachments/assets/79a593df-1bbe-4463-87ad-3c778cfc0a29)

Fitur 'GameGenre' terdiri dari 5 genre terdiri dari, Sport, Action, Strategy, Simulation, RPG. Distribusi fitur 'GameGenre' pada dataset juga seimbang. Dapat disimpulkan genre game tidak memiliki pengaruh yang signifikan, terlihat tidak ada perbedaan antara satu genre dengan genre yang lainnya.

#### Game Difficulty

![GameDifficulty](https://github.com/user-attachments/assets/8d5cd21e-c8dd-4caa-bd06-135032eefef7)

Pada fitu 'GameDifficulty' terdiri dari 3 macam kesulitan, yaitu Easy, Medium, Hard. Distribusi fitur ini juga tidak seimbang dengan Easy 50% sementara Medium 30% dan Hard 20%. Hal tersebut dapat disimpulkan bahwa banyak pemain bermain dengan difficulty Easy.

#### Engagement Level

![EngagementLevel](https://github.com/user-attachments/assets/d234b42b-ebab-481d-bdfe-798c0f51f5ea)

Pada fitur 'EngagementLevel' merupakan fitur target dari projek ini. Distribus yang dapat terlihat tidak seimbang dengan level medium mencapai 48%, sedangkan untuk level High dan Low hanya 25.8%. Hal ini dapat disimpulkan bahwa banyak pemain yang memiliki engagement level Medium

Setelah melakukan analisis distribusi pada fitur kategori, selanjutnya melakukan analisis pada fitur numerik.

#### Univariate Numerical

![Univariate_Numerical](https://github.com/user-attachments/assets/cc5075b1-fecd-416f-a1ab-d5dc03dd67d5)

Pada gambar tersebut memberikan informasi berikut:
* Pada distribusi fitur numerik variabel 'Age', 'PlayTimeHours', 'SessionPerWeek', 'AchievementsUnlcoked' memiliki distribusi yang cukup seimbang.
* Untuk fitur 'InGamePurchases' didominasi oleh player yang tidak melakukan pembelian di dalam game
* Untuk kedua fitur 'AvgSessionDurationMinutes' dan 'PlayerLavel' terdapat perbedaan distribusi yang mencolok.

### Multivariate Analysis

Multivariate EDA menunjukkan hubungan antara dua atau lebih variabel pada data. Multivariate EDA yang menunjukkan hubungan antara dua variabel biasa disebut sebagai bivariate EDA. Pada tahap ini akan dilakukan analisis data pada fitur kategori dan numerik.

#### Categorical Features

Pada tahap ini akan memeriksa hubungan 'EngagementLevel' dengan fitur kategori yang lain.

![Engagement_Level_Gender](https://github.com/user-attachments/assets/8f398e2b-d59d-4c99-8719-9c318ff2a4eb)
![Engagement_Level_Location](https://github.com/user-attachments/assets/8887a7b9-669e-4615-a31f-7402b6f2e148)
![Engagement_Level_GameGenre](https://github.com/user-attachments/assets/2414f45c-a768-454a-8a28-395981edc5e9)
![Engagement_Level_GameDifficulty](https://github.com/user-attachments/assets/394f8490-d608-4648-856f-f25cba843f06)

Dari EDA ada beberapa insight sebagai berikut:
* untuk semua fitur kategori memiliki kesamaan yaitu engagement level medium mendominasi/memiliki jumlah paling banyak diantara level yang lain.
* Untuk lebel high dan low juga memiliki kesamaan atau perbedaan yang tidak terlalu jauh pada fitur kategori

#### Numerical Features

Tahap ini untuk memeriksa hubungan antara 'EngagementLevel' dengan fitur numerik

![Multivariate_Numerical_Age](https://github.com/user-attachments/assets/196cec6f-5b7e-4996-8b89-c78f7bf75bd7)
![Multivariate_Numerical_PlayTimeHours](https://github.com/user-attachments/assets/4795cdbd-0569-492b-8b3b-4ff8cb4ae923)
![Multivariate_Numerical_SessionsPerWeek](https://github.com/user-attachments/assets/af668d0d-4938-45ad-949c-9326681bb530)
![Multivariate_Numerical_AvgSessionDurationMinutes](https://github.com/user-attachments/assets/9700d82e-1258-4bea-ad17-fa47416cc4d8)
![Multivariate_Numerical_PlayerLevel](https://github.com/user-attachments/assets/d9fc2ec0-fd49-4e87-8dc9-ca1509143116)
![Multivariate_Numerical_AchievementsUnlocked](https://github.com/user-attachments/assets/3dd5bc08-21ce-4845-8295-450ee248ef0a)

Dari EDA ada beberapa insight:
* Pada 'SessionPerWeek' terhadap 'EngagementLevel' memiliki perbedaan yang jelas. Player  dengan tingkat engagement yang tinggi cenderung memiliki sesi mingguan yang lebih banyak. Akan tetapi, pada engagement level rendah dan tinggi bervariasi dalam jumlah sesi per minggu, ada beberapa player yang memiliki sesi tinggi tetapi tingkat engagement mereka dianggap rendah dan begitu sebaliknya.
* Pada 'AvgSessionDurationMinutes' juga memiliki beberapa hal menarik seperti perbedaan yang jelas antara rata-rata durasi menit player dengan engagement mereka. Akan tetapi untuk tingkat tinggi memiliki outlier dimana beberapa pemain dengan durasi menit yang rendah memiliki tingkat engagement yang tinggi.

Selain itu, pada tahap ini menggunakan Mean Value dari fitur numerik. Hal ini dilakukan untuk melihat rata-rata nilai hubungan fitur numerik terhadapa 'EngagementLevel'.

![Multivariate_Heatmap](https://github.com/user-attachments/assets/b9c44a6b-355f-4e8d-ab48-d986d20c004a)

Dari visualisasi diatas ada beberapa insight berikut ini:
* Pada fitur 'SessionsPerWeek' player dengan sesi terbanyak dalam per minggu memiliki engagement level yang tinggi. sedangkan, untuk sesi sedikit memiliki engagement level yang rendah.
* Pada fitur'AvgsessionDurationMinutes' player dengan rata-rata durasi tertinggi mencapai 130 menit per sesi memiliki engagement yang tinggi, sedangkan untuk rata-rata durasi 67 menit per sesi memiliki engagement yang rendah.

## Data Preparation

Pada tahap selanjutnya dilakukan data preparation. Data preparation merupakan tahapan penting dalam proses pengembangan model machine learning. Ini adalah tahap dimana dilakukan proses transformasi pada data sehingga menjadi bentuk yang cocok untuk proses pemodelan. Ada beberapa tahapan yang umum dilakukan pada data preparation, antara lain, seleksi fitur, transformasi data, feature engineering, dan dimensionality reduction.  

Pada projek ini dilakukan beberapa tahap yaiut:
1. Seleksi fitur
2. Encoding fitur kategori
3. Pembagian dataset
4. Standarisasi

### Seleksi fitur

Tahap ini dilakukan untuk menyeleksi fitur yang tidak berhubungan/korelasi terhadap fitur target. Untuk itulah fitur PlayerID dipilih untuk dihapus dari dataset.

PlayerID dipilih karena fitur ini hanya memberikan identitas unik pada setiap pemain. Hal inilah menjadikan PlayerID tidak memiliki hubungan/korelasi pada fitur target yaitu 'EngegementLevel'.

```
new_df = df.drop(['PlayerID'], axis=1, inplace=False)
new_df.head()
```

Dengan code diatas fitur PlayerID dihapus. Lalu, melakukan pengecekan apakah fitur bener-bener telah terhapus dengan `new_df.head()`, berikut outputnya:

|index|Age|Gender|Location|GameGenre|PlayTimeHours|InGamePurchases|GameDifficulty|SessionsPerWeek|AvgSessionDurationMinutes|PlayerLevel|AchievementsUnlocked|EngagementLevel|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|43|Male|Other|Strategy|16\.271118760553215|0|Medium|6|108|79|25|Medium|
|1|29|Female|USA|Strategy|5\.525961380570566|0|Medium|5|144|11|10|Medium|
|2|22|Female|USA|Sports|8\.223755243499511|0|Easy|16|142|35|41|High|
|3|35|Male|USA|Action|5\.265351277318268|1|Easy|9|85|57|47|Medium|
|4|33|Male|Europe|Action|15\.53194452113429|0|Medium|2|131|95|37|Medium|

kolom PlayerID telah dihapus.

### Encoding Fitur Kategori

Pada tahap ini dilakukan untuk merubah fitur kategori menjadi nilai numerik. Hal ini perlu dilakukan untuk mengefisiensikan kinerja model yang akan dibuat.

Pada tahap ini akan dilakukan dua encoding berbeda. Pertama menggunakan fitur get_dummies untuk encoding fitur kategori selain fitur target. Berikut merupakan code yang akan dijalankan
```
new_df = pd.concat([new_df, pd.get_dummies(new_df['Gender'], prefix='Gender')], axis=1)
new_df = pd.concat([new_df, pd.get_dummies(new_df['Location'], prefix='Location')], axis=1)
new_df = pd.concat([new_df, pd.get_dummies(new_df['GameGenre'], prefix='GameGenre')], axis=1)
new_df = pd.concat([new_df, pd.get_dummies(new_df['GameDifficulty'], prefix='GameDifficulty')], axis=1)
new_df.drop(['Gender', 'Location', 'GameGenre', 'GameDifficulty'], axis=1, inplace=True)
new_df = new_df.applymap(lambda x: int(x) if isinstance(x, bool) else x)
```

Pada code diatas, fitur yang telah dilakukan encoding dapat dihapus. Kemudian, langkah kedua melakukan encoding pada fitur target, yaitu 'EngagementLevel'.

Pada langkah ini, menggunakan teknik Ordinal-Encoder. Hal ini diperlukan karena fitur engagement memiliki sifat ordinal atau tingkatan. Jadi, teknik Ordinal-Encoder sangat cocok digunakan pada langah ini. Berikut adalah code yang dijalankan:

```
from sklearn.preprocessing import OrdinalEncoder

label_encoder = OrdinalEncoder(categories=[['Low', 'Medium', 'High']])
new_df['EngagementLevel'] = label_encoder.fit_transform(new_df[['EngagementLevel']])

new_df.head()
```

Setelah semua langkah dilakukan, Periksa ulang dataset menggunakan `new_df.head()`. hal ini untuk memastikan bahwa fitur kategori telah dirubah menjadi nilai numerik. Berikut adalah outputnya:

|index|Age|PlayTimeHours|InGamePurchases|SessionsPerWeek|AvgSessionDurationMinutes|PlayerLevel|AchievementsUnlocked|EngagementLevel|Gender\_Female|Gender\_Male|Location\_Asia|Location\_Europe|Location\_Other|Location\_USA|GameGenre\_Action|GameGenre\_RPG|GameGenre\_Simulation|GameGenre\_Sports|GameGenre\_Strategy|GameDifficulty\_Easy|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|43|16\.271118760553215|0|6|108|79|25|1\.0|0|1|0|0|1|0|0|0|0|0|1|0|
|1|29|5\.525961380570566|0|5|144|11|10|1\.0|1|0|0|0|0|1|0|0|0|0|1|0|
|2|22|8\.223755243499511|0|16|142|35|41|2\.0|1|0|0|0|0|1|0|0|0|1|0|1|
|3|35|5\.265351277318268|1|9|85|57|47|1\.0|0|1|0|0|0|1|1|0|0|0|0|1|
|4|33|15\.53194452113429|0|2|131|95|37|1\.0|0|1|0|1|0|0|1|0|0|0|0|0|

Fitur kategori sudah berubah menjadi fitur numerik, begitu juga dengan fitur target 'EngagementLevel' dengan memiliki tingkatan. Berikut penjelasannya
* 0 = Low
* 1 = Medium
* 3 = High

### Pembagian Dataset

Pada tahap ini dilakukan pembagian dataset menjadi dataset untuk melatih model (Data Training) dan data untuk melakukan menguji model (Data Testing). Tahap ini diperlukan untuk mempertahankan data sebagai data uji untuk melihat peforma model pada data baru. 

```
from sklearn.model_selection import train_test_split

X = new_df.drop(['EngagementLevel'], axis=1)
y = new_df['EngagementLevel']

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.1, random_state=42)
```

Pada tahap ini digunakan fungsi `train_test_split()` untuk membagi dataset. Lalu, menggunakan perbandingan 90:10, hal tersebut dikarenakan dataset yang digunakan memiliki jumlah 40034 data. Dengan perbandingan ini, dataset latih berjumlah 36030 dan dataset test berjumlah 4004. Kemudian, parameter `random_state=42` digunakan untuk memastikan bahwa setiap kali kode ini dijalankan, pembagian dataset antara training dan testing akan sama.

### Standarisasi

Tahap selanjutnya adalah standarisasi. Standardisasi adalah teknik transformasi yang paling umum digunakan dalam tahap persiapan pemodelan. Pada tahap ini menggunakan teknik StandarScaler dari library Scikitlearn.

StandardScaler melakukan proses standarisasi fitur dengan mengurangkan mean kemudian membaginya dengan standar deviasi untuk menggeser distribusi.  StandardScaler menghasilkan distribusi dengan standar deviasi 1 dan mean 0. Sekitar 68% dari nilai akan berada di antara -1 dan 1.

Hal ini perlu dilakukan untuk meningkatkan performa dan konvergen lebih cepat pada machine learning karena data memiliki skala relatif sama atau mendekati distribusi normal. Standarisasi membantu untuk membuat fitur data menjadi bentuk yang lebih mudah diolah oleh algoritma. 

```
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```

Pada tahap ini standarisasi dilakukan setelah melakukan pembagian dataset. Hal ini dilakukan agar tidak mengotori data uji dengan informasi yang kita dapat dari data latih. 

## Modeling
Tahap modeling adalah tahap membangun dan mengembangkan model machine learning untuk menjadi solusi dari permasalahan yang dihadapi. 

Pada tahap ini akan dikembangkan model machine learning dengan 3 algoritma. Kemudian model tersebut akan dilakukan evaluasi dengan metrik klasifikasi untuk menguji performa dari masing-masing algortima. Algoritma yang memiliki performa terbaik akan dipilih untuk menjadi solusi dari problem statement pada business understanding. 

Algoritma yang akan digunakan adalah:
1. Random Forest
2. Logistic Regression
3. XGBoost

### Random Forest

Random forest merupakan algoritma machine learning yang terdiri dari banyak decision tree yang digabungkan untuk membuat prediksi lebih akurat. Algoritma ini bekerja dengan cara membangun beberapa decision tree. kemudian decision tree tersebut dilatih dengan subset data dan fitur yang berbeda menggunakan teknik bagging, yaitu pengambilan secara acak dengan bergantian, sehingga setiap tree dapat membuat keputusan yang berbeda. Setelah semua tree telah dilatih, algoritma mengambil prediksi dari masing-masing tree dan menggabungkannya dengan cara "voting mayoritas." Prediksi yang paling sering dipilih oleh tree dianggap sebagai hasil akhir. 

Parameter yang digunakan, yaiut:

| Parameter | Value |
|---|---|
| n_estimator | 400 |
| max_depth | 20
| random_state | 42 |
| n_jobs | -1 |

* `n_estimator` : jumlah trees (pohon) di forest. Set value `n_estimator=400`.
* `max_depth` : kedalaman atau panjang pohon. Ia merupakan ukuran seberapa banyak pohon dapat membelah (splitting) untuk membagi setiap node ke dalam jumlah pengamatan yang diinginkan. Set value `max_depth=20`.
* `random_state` : digunakan untuk mengontrol random number generator yang digunakan. Set value `random_state=42`. 
* `n_jobs` : jumlah job (pekerjaan) yang digunakan secara paralel. Ia merupakan komponen untuk mengontrol thread atau proses yang berjalan secara paralel. set value `n_jobs=-1`. 

berikut adalah codenya:

```
from sklearn.ensemble import RandomForestClassifier

rf_classifier = RandomForestClassifier(n_estimators=400, max_depth=20, random_state=42, n_jobs=-1)
rf_classifier.fit(X_train, y_train)
```

**Kelebihan Random Forest**

1. Robust terhadap Overfitting: Karena Random Forest menggabungkan banyak decision tree, algoritma ini kurang rentan terhadap overfitting dibandingkan decision tree tunggal.

2. Akurasi yang Baik: Algoritma ini biasanya memberikan akurasi yang lebih tinggi dibandingkan model sederhana seperti decision tree atau regresi logistik.

3. Bisa Menangani Data yang Kompleks: Mampu menangani dataset yang besar dengan fitur-fitur yang banyak dan bervariasi.

4. Tahan terhadap Outlier dan Noise: Karena keputusan didasarkan pada voting banyak tree, outlier dan noise dalam data tidak terlalu mempengaruhi hasil akhir.

5. Mengukur Pentingnya Fitur: Random Forest dapat memberikan peringkat fitur berdasarkan seberapa besar kontribusi mereka terhadap keputusan akhir, yang sangat membantu dalam analisis data.

**Kekurangan Random Forest**

1. Memerlukan Sumber Daya yang Lebih Besar: Karena algoritma membangun banyak tree, ini memerlukan lebih banyak waktu komputasi dan memori dibandingkan decision tree tunggal.

2. Sulit Diinterpretasi: Meskipun menghasilkan prediksi yang akurat, hasil dari Random Forest sulit dijelaskan karena melibatkan banyak decision tree yang berbeda.

3. Tidak Optimal untuk Data dengan Fitur yang Sangat Banyak: Ketika jumlah fitur sangat besar, ada risiko beberapa fitur dominan lebih sering dipilih, sehingga model dapat sedikit bias.

4. Waktu Inferensi Lebih Lama: Proses inferensi atau prediksi bisa lebih lambat dibandingkan model lain seperti decision tree tunggal atau model linier.

### Logistic Regression

Logistic Regression adalah algoritma yang digunakan untuk klasifikasi biner (dua kelas) dan bisa diperluas untuk multi-class. Algoritma ini bekerja dengan menghitung peluang suatu sampel berada dalam satu kelas dibandingkan kelas lainnya. Logistic Regression menggunakan fungsi sigmoid untuk mengubah prediksi menjadi probabilitas antara 0 dan 1. Untuk klasifikasi multi-class, Logistic Regression menggunakan teknik seperti One-vs-Rest (OvR) atau multinomial.

Parameter yang digunakan, yaiut:

| Parameter | Value |
|---|---|
| multi_class | multinomial |
| solver | lbfgs |
| max_iter | 300 |
| random_state | 42 |

* `multi_class='multinomial'` digunakan untuk klasifikasi multi-kelas dengan model softmax regression. Ini berarti Logistic Regression menangani semua kelas secara bersamaan, dan setiap kelas diberikan probabilitas.

* `solver` : algoritma optimasi yang digunakan untuk menemukan bobot terbaik. Set value `solver='lbfgs'` untuk data yang besar dan multi-class.

* `max_iter` :  jumlah maksimum iterasi yang akan dijalankan solver untuk menyelesaikan masalah optimasi. Set velue `max_iter=300`.

* `random_state` : menetapkan seed untuk pengacakan, sehingga hasilnya dapat direproduksi. Ste value `random_state=42`.

Berikut codenya:
```
from sklearn.linear_model import LogisticRegression

lr_classifier = LogisticRegression(multi_class='multinomial', solver='lbfgs', max_iter=300, random_state=42)
lr_classifier.fit(X_train, y_train)
```

**Kelebihan Logistic Regression**

1. Sederhana dan Mudah Diinterpretasi: Logistic Regression adalah salah satu algoritma paling sederhana yang hasilnya mudah diinterpretasi (koefisien bisa menunjukkan pengaruh fitur).

2. Efisien untuk Data Kecil: Sangat cepat dalam hal waktu komputasi dan cocok untuk dataset yang tidak terlalu besar.

3. Probabilitas Output: Memberikan output berupa probabilitas, yang berguna jika kamu ingin mendapatkan probabilitas, bukan hanya prediksi kelas.

4. Tidak Memerlukan Banyak Parameter: Logistic Regression tidak memiliki banyak hyperparameter yang perlu diatur, sehingga lebih mudah diterapkan.

5. Tidak Memerlukan Scaling yang Kompleks: Algoritma ini bekerja baik dengan data yang sudah di-normalisasi atau distandarisasi.

**Kekurangan Logistic Regression**

1. Hanya Linear Boundary: Logistic Regression mengasumsikan bahwa data bisa dipisahkan oleh garis lurus (linear). Jika data tidak linear, performa algoritma bisa sangat rendah.

2. Kurang Efektif pada Data yang Kompleks: Jika data memiliki banyak fitur yang kompleks atau hubungan non-linear, Logistic Regression biasanya kurang efektif dibandingkan metode lain seperti Random Forest atau Neural Network.

3. Sensitif terhadap Outlier: Logistic Regression bisa dipengaruhi oleh outlier, karena outlier dapat menyebabkan model untuk memperhitungkan outlier secara signifikan dalam menentukan garis pemisah.

4. Kurang Efisien untuk Dataset Besar: Walaupun sederhana dan cepat untuk dataset kecil, Logistic Regression bisa lambat jika diterapkan pada dataset yang sangat besar, terutama dalam kasus multi-class.

### XGBoost

XGBoost (Extreme Gradient Boosting) adalah algoritma boosting berbasis pohon keputusan yang sangat kuat untuk tugas klasifikasi dan regresi. XGBoost adalah varian dari algoritma Gradient Boosting yang dirancang agar lebih cepat dan efisien.

Cara kerja XGBoost adalah membuat serangkaian decision tree bertahap. Setiap tree baru mencoba memperbaiki kesalahan yang dibuat oleh tree sebelumnya. Kemudian, Model ini menambahkan tree baru secara iteratif. Setiap tree yang ditambahkan memberikan kontribusi kecil untuk memperbaiki prediksi keseluruhan. Proses ini disebut boosting karena model terus ditingkatkan dengan menambahkan prediksi dari tree baru. Selanjutnya, XGBoost menggunakan berbagai teknik optimasi seperti shrinkage (pembobotan setiap tree baru) dan regularisasi (L1 dan L2) untuk mencegah overfitting dan membuat model lebih general.

Parameter yang digunakan, yaitu: 

| Parameter | Value |
|---|---|
| objective | multi |
| num_class | 3 |
| n_estimators | 250 |
| max_depth | 24 |
| n_jobs | -1 |
| random_state | 42 |

* `objective` : menentukan jenis masalah yang ingin diselesaikan oleh model. Set value `objective='multi` digunakan untuk klasifikasi multi-class dengan keluaran prediksi berupa label kelas.

* `num_class` : model menangani masalah klasifikasi dengan kelas yang berbeda. Set value `num_class=3` artinya klasifikasi 3 kelas yang berbeda.

* `n_estimators` : Jumlah tree yang akan dibangun oleh model. Set value `n_estimators=250` artinya XGBoost membangun 250 decision tree untuk mempelajari pola dari data.

* `max_depth` :  kedalaman maksimal dari setiap decision tree. Set value `max_depth=24`

* `n_jobs` : untuk memanfaatkan multithreading. Set value `n_jobs=-1`  

* `random_state` : menetapkan seed untuk pengacakan. Set value `random_state=42`

Berikut codenya:

```
import xgboost as xgb

xgb_classifier = xgb.XGBClassifier(objective='multi:softmax', num_class=3, n_estimators=250,
                                   max_depth=24, n_jobs=-1, random_state=42)
xgb_classifier.fit(X_train, y_train)
```

**Kelebihan XGBoost**

1. Kecepatan dan Efisiensi: XGBoost dirancang untuk lebih cepat dibandingkan metode boosting tradisional, menggunakan optimasi paralel untuk meningkatkan efisiensi.

2. Akurasi Tinggi: XGBoost terkenal karena akurasinya yang tinggi pada banyak tugas klasifikasi dan regresi, bahkan dengan data yang kompleks.

3. Penanganan Overfitting: Algoritma ini memiliki parameter regularisasi (L1 dan L2) yang mengurangi overfitting, membuatnya lebih robust dibandingkan model boosting lainnya.

4. Menangani Data yang Hilang: XGBoost dapat menangani missing values dengan baik, dan bisa bekerja dengan data yang memiliki nilai hilang tanpa harus melakukan imputasi manual.

5. Fleksibel: XGBoost mendukung berbagai fungsi loss (seperti regresi dan klasifikasi), serta bekerja dengan baik untuk tugas multi-class.

**Kekurangan XGBoost**

1. Sulit Diinterpretasi: Karena XGBoost menggabungkan banyak pohon keputusan, hasilnya sulit diinterpretasi dibandingkan dengan model yang lebih sederhana seperti Logistic Regression.
2. Waktu dan Sumber Daya Besar: Walaupun cepat dibandingkan dengan boosting tradisional, XGBoost bisa memerlukan banyak waktu untuk melatih model pada dataset yang sangat besar, terutama jika parameter dioptimalkan.
3. Memerlukan Tuning Parameter: Untuk mendapatkan performa terbaik, XGBoost sering memerlukan tuning parameter yang signifikan, yang bisa menjadi proses yang memakan waktu.
4. Rentan terhadap Noise: Jika tidak diatur dengan baik (misalnya, tanpa regularisasi yang cukup), XGBoost dapat overfit pada data yang noisy.

Setelah membangun model dengan ketiga algortima tersebut, selanjutnya membandingkan kinerja dan performa model. Model dengan performa terbaik akan menjadi model solution untuk business understanding. Berikut merupakan hasilnya.

### Random Forest

Hasil akurasi random fores mencapai 90%. Berikut hasil dengan klasifikasi dengan metrik precision, recall, dan f1-score

| Label | Precision | Recall | F1-Score |
|-|-|-|-|
| Low |  91% | 86% | 88% |
| Medium | 89% | 94% | 92% |
| High | 91% | 85% | 88% |

Secara keseluruhan, model Random Forest menunjukkan performa yang baik dengan akurasi yang tinggi. Setiap kelas memiliki precision, recall, dan f1-score yang cukup tinggi, meskipun kelas 'Medium' sedikit lebih baik dalam recall dan f1-score dibandingkan kelas lainnya.

### Logistic Regression

Hasil akurasi logistic regression mencapai 82%.Berikut hasil dengan klasifikasi dengan metrik precision, recall, dan f1-score

| Label | Precision | Recall | F1-Score |
|-|-|-|-|
| Low |  80% | 70% | 75% |
| Medium | 80% | 89% | 82% |
| High | 89% | 82% | 86% |

Model Logistic Regression menunjukkan performa yang baik. Precision dan recall untuk kelas 'Medium' dan 'High' lebih tinggi dibandingkan kelas 'Low', menunjukkan bahwa model lebih baik dalam mendeteksi sampel kelas 'Medium' dan 'High'. Namun, performa pada kelas 'Low' dengan recall hanya 70%

### XGBoost

Hasil akurasi XGBoost mencapai 91%.Berikut hasil dengan klasifikasi dengan metrik precision, recall, dan f1-score

| Label | Precision | Recall | F1-Score |
|-|-|-|-|
| Low |  90% | 88% | 89% |
| Medium | 92% | 94% | 93% |
| High | 91% | 89% | 90% |

Model XGBoost menunjukkan performa yang sangat baik dengan akurasi tinggi (91.2%) dan nilai precision, recall, serta f1-score yang stabil di semua kelas. Kelas 'Low' memiliki performa terbaik dengan recall dan f1-score yang tertinggi, menunjukkan bahwa model sangat baik dalam mendeteksi sampel kelas ini.

Dengan hasil diatas, dipilihlah model XGBoost untuk menjadikan model solution untuk business understanding. Model ini dipilih karena performa akurasi yang paling tinggi diantara model lain yaitu 91%. Model juga memiliki performa yang stabil pada precision, recall, serta f1-score dalam mengklasifikasi semua kelas pada dataset.

Model lain yang memiliki performa yang kompetitif adalah Random Forest. Model ini memiliki akurasi yaitu 90% berbeda 1% dengan model GXBoost. Performa pada metrik precision, recall, serta f1-score pada setiap kelas juga tinggi. Akan tetapi, model XGBoost memiliki performa diatas Random Forest.

## Evaluation

Berikut merupakan penjelasan dari metrik yang digunakan untuk projek ini untuk mengukur dan membandingkan model yang telah dikembangkan.

### Akurasi

Formula:

$$` 
 Akurasi = \frac{Jumlah Prediksi Benar}{Total Prediksi} 
`$$

Cara kerja dari akurasi adalah mengukur proporsi dari prediksi yang benar terhadap keseluruhan prediksi yang dilakukan model.

### Precesion

Formula:

$$`
Presicion = \frac{True \ Positives}{True \  Positives + False \ Positives}
`$$

Cara kerja dari presicion adalah precision menunjukkan berapa banyak dari prediksi kelas positif yang benar-benar positif. Jika precision tinggi, berarti model jarang salah mengklasifikasikan sampel negatif sebagai positif. 

### Recall

Formula: 

$$`
Recall = \frac{True \ Positives}{True \ Positives + False \ Negatives}
`$$

Cara kerja recall adalah dengan mengukur seberapa banyak sampel positif yang dapat ditemukan oleh model dari semua sampel yang sebenarnya positif.

### F1 Score

Formula:

$$`
F1 \ Score = 2 \times \frac{Precision \times Recall}{Precision + Recall}
`$$

F1 score adalah harmonisasi dari precision dan recall. Metrik ini lebih baik digunakan ketika mempertimbangkan keseimbangan antara precision dan recall penting, terutama jika data tidak seimbang.

### Dampak model pada Business Understanding.
Model sudah menjawab problem statemen. Dengan pendekatan tiga algoritma machine learning seperti, Random Forest, Logistic Regression, dan XGBoost, model-model ini dapat memprediksi engagment level pemain berdasarakan perilaku bermain.

Hasil evaluasi XGBoost menjunjukan hasil terbaik diantara semua model dengan 91%. Model ini juga mendapatkan performa stabil pada precision, recall, dan f1-score terhadap semua kelas. Model ini menjawab problem statemen yang menginginkan model yang dapat memprediksi engagement level secara akurat. 

Model juga berhasil mencapai kedua goals yang ditentukan. 

1. **Mengidentifikasi Fitur yang Mempengaruhi Engagement Level** 
Dengan dilakukannya exploratory data analysi (EDA) dapat memahami fitur-fitur utama yang mempengaruhi engagement level. Pemahaman ini berkontribusi pada insight penting untuk pengembangan game yang lebih tepat sasaran dan sesuai kebutuhan pemain.

2. **Memilih Model Prediktif dengan Akurasi Tinggi** 
Hasil evaluasi menunjukkan bahwa XGBoost, dengan akurasi 91%, merupakan model terbaik di antara pilihan yang ada. Ini memenuhi goal untuk memilih model yang dapat mengklasifikasikan engagement level secara akurat.

Solusi statement yang direncanakan juga memiliki dampak yang signifikan untuk mencapai goals. Berikut merupakan penjelasannya.
1. EDA memberikan wawasan penting tentang perilaku pemain, membantu tim pengembang game fokus pada fitur atau aspek game yang berkontribusi paling besar terhadap engagement. Hal ini sangat berguna untuk strategi retensi pemain.

2. Implementasi Model Prediksi memungkinkan identifikasi level engagement secara otomatis, memberikan insight kepada tim pengembang untuk menyesuaikan atau menambahkan elemen game yang dapat meningkatkan engagement di setiap level. Algoritma yang dipilih (terutama XGBoost dan Random Forest) memberikan performa yang cukup memadai, sehingga model ini dapat digunakan dengan tingkat kepercayaan yang tinggi.

Secara keseluruhan, evaluasi model ini menunjukkan bahwa model sudah memenuhi ekspektasi awal dengan dampak nyata yang relevan pada pengambilan keputusan dalam pengembangan game, sejalan dengan goals yang ditetapkan.

## Referensi

[1] Vasalou, A., Joinson, A. N., Bänziger, T., & Bächtiger, A. (2008). “Player Engagement in Video Games: A Review of the Literature,” *International Journal of Human-Computer Studies*, 66(11), 811–825.

[2] Deterding, T. (2013). "The Gameful World: Approaches, Issues, Applications." MIT Press.

[3] Bärtsch, M. K. (2021). "The Role of Data Analytics in Enhancing Player Engagement and Retention." *International Journal of Information Management*, 57, 102-110.

[4] Alzahrani, A. A. R., Alharthi, A., & Alshahrani, M. (2024). "Predicting Online Gaming Behaviour Using Machine Learning Techniques". *Indonesian Journal of Data and Science*, 5(2), 133-143.

[5] Hussain, M., Zhu, W., Zhang, W., & Abidi, S.M.R. (2023). "Student Engagement Predictions in an e-Learning System and Their Impact on Student Course Assessment Scores". *Computational Intelligence and Neuroscience*, 2018, 1–21.

