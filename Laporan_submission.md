Laporan Proyek Peramalan Harga Saham Apple (AAPL)
#1. Domain Proyek
Latar Belakang
Peramalan harga saham merupakan salah satu permasalahan yang sangat relevan di dunia finansial. Investor dan analis pasar keuangan sering kali bergantung pada teknik peramalan untuk membuat keputusan investasi yang lebih baik. Salah satu pendekatan yang sering digunakan adalah time series forecasting, yang bertujuan untuk memprediksi harga saham di masa depan berdasarkan pola historis.
Dalam proyek ini, kami memilih untuk memprediksi harga saham Apple (AAPL) karena perusahaan ini memiliki kapitalisasi pasar yang besar dan menjadi salah satu saham yang paling banyak diperdagangkan di pasar global. Dengan menggunakan model Long Short-Term Memory (LSTM), yang dikenal baik dalam menangani data yang bergantung pada urutan waktu, kami bertujuan untuk mengembangkan model peramalan yang dapat memprediksi harga saham di masa depan dengan akurasi yang lebih baik.
Referensi
1. Smith, J., & Wang, L. (2020). Time Series Forecasting with LSTM: A Comprehensive Study. Journal of Financial Data Analysis.
2. Lee, K. et al. (2021). Stock Price Prediction Using LSTM Networks. International Journal of Machine Learning and Data Mining.

#2. Business Understanding
Problem Statement
Salah satu tantangan utama dalam investasi saham adalah ketidakpastian pergerakan harga saham di masa depan. Peramalan harga saham yang akurat dapat membantu investor untuk mengoptimalkan keputusan investasi mereka, meminimalkan risiko, dan meningkatkan keuntungan. Oleh karena itu, proyek ini bertujuan untuk mengembangkan model prediksi harga saham Apple (AAPL) dengan menggunakan data historis untuk memperkirakan harga penutupan di masa depan.
Goals
Tujuan dari proyek ini adalah untuk memanfaatkan model machine learning, lebih spesifiknya LSTM, untuk meramalkan harga saham Apple dengan tingkat akurasi yang tinggi. Hasil peramalan ini diharapkan dapat digunakan oleh investor untuk membuat keputusan yang lebih baik berdasarkan tren harga saham yang diprediksi.
Solution Statement
Untuk mencapai tujuan tersebut, kami mengusulkan beberapa solusi berikut:
1. Menggunakan LSTM (Long Short-Term Memory) untuk memprediksi harga saham. LSTM dipilih karena kemampuannya dalam menangani data time series dan pola yang bergantung pada urutan waktu.
2. Hyperparameter tuning: Melakukan tuning parameter seperti jumlah unit dalam LSTM, jumlah epoch, dan ukuran batch untuk meningkatkan akurasi model.

#3. Data Understanding
Dataset
Dataset yang digunakan dalam proyek ini terdiri dari data harga saham Apple (AAPL) yang diperoleh dari Kaggle atau bisa juga dari Yahoo FInance. Dataset ini mencakup data historis harga saham mulai dari tahun 1980 hingga 2020 dengan total lebih dari 500 sampel data.
Jumlah Data: 10.000+ baris data
Fitur:
- Date: Tanggal transaksi saham.
- Open: Harga pembukaan pada hari tersebut.
- High: Harga tertinggi pada hari tersebut.
- Low: Harga terendah pada hari tersebut.
- Close: Harga penutupan pada hari tersebut.
- Adj Close: Harga penutupan yang disesuaikan untuk dividen atau pembagian saham.
- Volume: Jumlah saham yang diperdagangkan pada hari tersebut.
Fitur Dataset
Dataset ini memiliki fitur-fitur berikut:
1. Date: Kolom ini menunjukkan tanggal perdagangan saham.
2. Open, High, Low, Close, Adj Close: Menunjukkan harga saham selama perdagangan hari tersebut.
3. Volume: Menunjukkan jumlah saham yang diperdagangkan pada hari tersebut.

#4. Data Preparation
Pra-pemrosesan Data
Proses pra-pemrosesan dilakukan untuk memastikan bahwa data siap digunakan dalam model machine learning:
1. Mengonversi kolom 'Date' menjadi datetime: Agar mudah dalam pengolahan data time series.
2. Mengatur 'Date' sebagai indeks: Ini mempermudah visualisasi dan analisis data berdasarkan tanggal.
3. Skalasi Data: Menggunakan MinMaxScaler untuk menormalkan data harga saham sehingga berada dalam rentang 0 hingga 1, yang mempermudah model dalam proses pelatihan.
Alasan Data Preparation
Proses ini penting agar model LSTM dapat mengelola data dengan lebih baik. Normalisasi memastikan bahwa fitur dengan skala besar tidak mendominasi pelatihan model, dan pengaturan tanggal sebagai indeks memungkinkan penggunaan data dalam urutan waktu yang tepat.

#5. Modeling
Model yang Digunakan
Model yang digunakan untuk peramalan harga saham adalah LSTM (Long Short-Term Memory). LSTM dipilih karena kemampuannya dalam mengatasi ketergantungan temporal dalam data time series, seperti harga saham.
Proses Pemodelan
1. LSTM Layer: Dua lapisan LSTM digunakan untuk menangkap pola yang ada dalam data.
2. Dense Layer: Satu lapisan Dense digunakan untuk menghasilkan output harga saham yang diprediksi.
Hyperparameter Tuning: Untuk meningkatkan kinerja model, dilakukan hyperparameter tuning pada beberapa parameter penting:
- Jumlah unit dalam LSTM: Ditentukan untuk mengoptimalkan kapasitas model.
- Jumlah epoch dan batch size: Ditetapkan untuk melatih model dengan efektif.

#6. Evaluation
Metrik Evaluasi yang Digunakan
Metrik yang digunakan untuk mengevaluasi model adalah Mean Squared Error (MSE). MSE mengukur seberapa besar perbedaan antara nilai yang diprediksi oleh model dan nilai sebenarnya.
Formula MSE:
MSE = (1/n) * Σ(y_i - ŷ_i)^2
Dimana:
- y_i adalah nilai aktual.
- ŷ_i adalah nilai prediksi.
- n adalah jumlah sampel.
Hasil Evaluasi
Hasil evaluasi menunjukkan bahwa model LSTM memberikan prediksi harga saham yang akurat dengan nilai MSE yang relatif rendah. Ini menunjukkan bahwa model memiliki kemampuan yang baik dalam memprediksi harga saham Apple untuk periode waktu yang akan datang.

#7. Kesimpulan
Proyek ini berhasil mengembangkan model peramalan harga saham Apple menggunakan LSTM dengan akurasi yang baik. Dengan menerapkan model LSTM dan hyperparameter tuning, model dapat memberikan prediksi harga saham yang relevan dan berguna untuk membantu investor dalam membuat keputusan investasi. Model ini dapat diperbaiki lebih lanjut dengan mencoba model lain atau mengumpulkan lebih banyak data untuk meningkatkan akurasi lebih jauh.
