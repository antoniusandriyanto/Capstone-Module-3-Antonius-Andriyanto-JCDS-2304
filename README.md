# California Housing Price

# Business Problem

**Context**

California Housing Price merupakan dataset yang berisi informasi mengenai harga rumah di California. Rumah merupakan aset yang sangat berharga dikarenakan rumah selain berfungsi sebagai tempat tinggal akan tetapi dapat menjadi suatu investasi yang dimiliki seseorang. Harga rumah dipengaruhi oleh berbagai faktor seperti lokasi, ukuran serta fasilitas yang ditawarkan. Menjual dan membeli rumah merupakan suatu keputusan finansial yang kompleks di mana penjual rumah perlu menentukan harga jual yang sesuai agar mendapatkan pembeli secepatnya dengan mendapatkan keuntungan yang besar dan sebaliknya pembeli rumah juga perlu mendapatkan nilai yang sesuai dengan uang yang dikeluarkan.

**Problem Statement**

Stakeholder : Agen Properti Rumah California

Di California, pasar perumahannya dikenal memiliki fluktuasi harga yang signifikan serta permintaannya juga tinggi. Dalam menentukan harga jual rumah yang tepat khususnya di California menjadi tantangan besar bagi para agen properti di mana harga yang terlalu tinggi dapat membuat agen properti mendapatkan keuntungan yang maksimal tetapi jika terlalu mahal maka akan sulit untuk mendapatkan pembeli sehingga agen properti harus cukup bijak untuk menentukan harga sehingga harga tersebut dapat menarik pembeli potensial. Oleh karena itu dibutuhkan alat yang dapat memprediksi harga rumah berdasarkan fitur yang ada dalam dataset California Housing Price.

**Goals**

Berdasarkan problem statement, agen properti memerlukan alat yang dapat memprediksi harga rumah berdasarkan fitur yang ada di dalam dataset California Housing Price. Alat ini diharapkan dapat membantu agen properti dalam menentukan harga yang kompetitif yang sesuai dengan fitur yang didapatkan oleh pembeli serta pembeli juga dapat terbantu dengan menilai apakah harga yang diberikan sudah sesuai dengan nilai properti.

**Analytic Approach**

Untuk membuat alat prediktif harga rumah di California maka kita akan melakukan analisis data dari fitur-fitur yang tersedia untuk mengetahui pembeda antara satu properti dengan yang lainnya. Oleh karena itu yang dilakukan adalah:
- Exploratory Data Analysis (EDA) : Untuk memahami distribusi serta hubungan antara berbagai fitur.
- Data Preprocessing : Mengidentifikasi nilai yang kosong, outlier atau data yang tidak sesuai untuk menciptakan prediksi yang lebih akurat pada alat prediktif.
- Feature Engineering : Menciptakan fitur baru yang dapat meningkatkan akurasi model.
- Modelling Machine Learning : Membangun model-model regresi dan memilih model yang terbaik.
- Model Evaluation : Mengevaluasi model menggunakan metrik.

Metrik sendiri terdiri atas:
- Root Mean Squared Error (RMSE) adalah metrik yang sangat umum digunakan untuk mengukur kinerja model regresi. RMSE memberikan estimasi seberapa jauh, rata-rata, prediksi dari model berada dari nilai sebenarnya.
- Mean Absolute Error (MAE) untuk menghitung rata-rata selisih absolut antara nilai yang diprediksi oleh model dengan nilai aktual.
- Mean Absolute Percentage Error (MAPE) untuk mengukur rata-rata persentase kesalahan prediksi relatif terhadap nilai aktual.

# Conclusion
1. Berdasarkan modelling yang telah dilakukan dan analisa featuring importance dengan 2 metode yang berbeda yaitu XGBoost dan SHAP menghasilkan 2 hasil yang berbeda juga di mana dapat disimpulkan jika menggunakan XGBoost maka feature importancenya yang paling besar adalah median income sedangkan jika menggunakan SHAP didapatkan fitur latitude dan longitude. Hal ini dikarenakan:
- Feature importance dari XGBoost untuk gambaran global tentang fitur mana yang paling sering digunakan dan memberikan informasi paling banyak.
- Feature importance dari SHAP values untuk memahami kontribusi spesifik fitur terhadap prediksi individual dan untuk analisis yang lebih mendalam serta adil tentang kontribusi fitur.

2. Metrik evaluasi yang digunakan MSE, MAE dan RMSE. Model terbaik yang dapat dihasilkan adalah model XGBoost Regression tanpa dilakukan hyperparameter tuning dengan RMSE sebesar 45695.001622, MAE sebesar 29834.33225 dan MAPE sebesar 0.167691. Artinya prediksi harga yang dilakukan model memiliki rata-rata errornya sebesar 16,77% dari harga seharusnya.

3. Jika dibandingkan antara alat prediktif tanpa machine learning (menggunakan mean price) dengan menggunakan machine learning maka prediksi dengan menggunakan alat machine learning yang telah dirancang dapat memberikan prediksi harga yang lebih akurat sebesar 43.18%.

# Recommendation
#### Recommendation Model
1. Mengupdate dataset pada tahun 2024 sehingga nantinya dapat digunakan untuk memprediksi harga rumah sesuai dengan tren harga tahun saat ini.
2. Penarikan data yang dilakukan oleh sensus dapat menambahkan fitur-fitur yang memiliki pengaruh yang kuat terhadap harga rumah seperti luas rumah per rumah, lokasi perumahan apakah berada di jalan utama / perkomplekan dan apakah letak rumahnya berada di dekat fasilitas umum seperti jalan tol, transportasi umum, tempat rekreasi, sekolah dikarenakan semua itu mempengaruhi harga rumah.
3. Dapat mencoba untuk menciptakan fitur-fitur baru yang dapat dibuat berdasarkan data yang telah ada yang memiliki pengaruh lebih besar terhadap prediksi nilai harga rumah di California selain dari fitur baru (population per house, bedroom per house, rooms per house) yang sudah dibuat pada machine learning ini.
4. Dapat menggunakan modeling lain yang belum dicoba seperti deep learning

#### Recommendation Business
1. Median income menjadi fitur yang sangat berpengaruh terhadap harga rumah. Oleh karena itu kelompok dengan pendapatan yang tinggi dapat difokuskan dengan menawarkan promosi-promosi seperti down payment yang lebih rendah dikarenakan kelompok dengan pendapatan yang tinggi lebih memungkinkan untuk menjadi pembeli potensial.
2. Untuk pengelompokan umur rumah yang sudah Old dapat ditawarkan program renovasi untuk meningkatkan fasilitasnya sehingga dapat menarik pembeli potensial.
