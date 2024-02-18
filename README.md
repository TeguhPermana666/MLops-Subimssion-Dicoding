# Submission 1: Machine Learning Pipeline - Human Stress Prediction
Nama: I Gede Teguh Permana

Username dicoding: teguhpermana666

![human resources problems](https://user-images.githubusercontent.com/58927608/232183728-df31ce54-b58c-4163-a563-5df9d3daf167.jpg)

[Sumber Gambar](https://blog.peoplespheres.com/en-us/what-problems-do-human-resources-managers-face-every-day)

| | Deskripsi |
| ----------- | ----------- |
| Dataset | [Human Stress Prediction](https://www.kaggle.com/datasets/kreeshrajani/human-stress-prediction) |
| Masalah | Proyek Human Stress Prediction bertujuan untuk memprediksi tingkat stres yang dialami oleh individu berdasarkan pada berbagai faktor seperti aktivitas fisik, jumlah tidur, interaksi sosial, dan lainnya. Masalah yang mendasari proyek ini adalah meningkatnya kesadaran akan pentingnya kesejahteraan mental di kalangan masyarakat. Stres merupakan salah satu masalah kesehatan mental yang umum dihadapi oleh banyak orang dan dapat memiliki dampak negatif pada kesehatan fisik dan mental seseorang. Oleh karena itu, dengan memprediksi tingkat stres, kita dapat memberikan solusi atau intervensi yang sesuai untuk membantu individu mengelola stres mereka dengan lebih efektif. Dataset yang digunakan dalam proyek ini berisi informasi tentang berbagai variabel yang berpotensi memengaruhi tingkat stres seseorang. Ini termasuk data tentang aktivitas fisik harian, pola tidur, interaksi sosial, faktor lingkungan, dan mungkin juga informasi demografis seperti usia, jenis kelamin, dan tingkat pendidikan. Setiap entri dalam dataset mungkin mencakup pengukuran atau estimasi dari faktor-faktor ini untuk seorang individu pada suatu waktu tertentu. Dataset ini relevan dengan deskripsi masalah karena berisi informasi yang diperlukan untuk memprediksi tingkat stres seseorang. Dengan menganalisis data dari berbagai faktor yang memengaruhi stres, kita dapat mengembangkan model machine learning yang dapat memprediksi tingkat stres seseorang berdasarkan pada faktor-faktor tersebut. Ini akan memungkinkan kita untuk memberikan solusi atau intervensi yang sesuai untuk membantu individu mengelola stres mereka.|
| Solusi machine learning | Stress susah dilihat dari keseharian seseorang, oleh karena itu dengan machine learning dapat mengetahui apakah seseorang stress hanya dari ketikan seseorang yang dilakukan dimedia sosial. Solusi machine learning dapat di segmentasi kedalam tiga hal, diantaranya Pengelolaan Stres yang Lebih Efekti: Dengan memiliki model yang dapat memprediksi tingkat stres, individu dapat lebih memahami faktor-faktor apa yang berkontribusi terhadap stres mereka dan mengambil langkah-langkah untuk mengelola stres tersebut dengan lebih efektif. Misalnya, mereka dapat mengubah pola tidur atau rutinitas aktivitas fisik mereka untuk mengurangi tingkat stres.
Pencegahan Masalah Kesehatan: Stres yang tidak dikelola dengan baik dapat berdampak negatif pada kesehatan fisik dan mental. Dengan menggunakan model ini, individu dapat mengambil tindakan preventif untuk menghindari masalah kesehatan yang dapat timbul akibat stres.
Penyesuaian Perilaku: Model ini juga dapat membantu individu untuk membuat perubahan perilaku yang positif. Misalnya, jika model menunjukkan bahwa tingkat stres lebih tinggi setelah kurang tidur, individu dapat lebih memprioritaskan tidur yang cukup.|
| Metode pengolahan | Pada data Human Stress Prediction, terdapat tujuh feature, tetapi yang digunakan pada proyek ini hanya feature text dan label, sehingga features selain itu akan dihapus, kemudian dilakukan split data training dan eval menjadi rasio 80:20, dan mengubah data feature menjadi lowercase serta feature label menjadi integer. Adapun tahapan metode pengolahan pipeline diantaranya
- Data Ingestion:
Data dikumpulkan dari berbagai sumber seperti survei, sensor wearable, dan rekaman aktivitas harian.
Data kemudian dibersihkan dan dipersiapkan untuk analisis lebih lanjut. Ini termasuk langkah-langkah seperti penghapusan nilai yang hilang, normalisasi data, dan pengkodean kategori jika diperlukan.

- Exploratory Data Analysis (EDA):
Data dieksplorasi untuk memahami karakteristiknya, korelasi antar variabel, dan pola yang mungkin ada.
Visualisasi data sering digunakan di sini untuk membantu pemahaman.

- Pemodelan Machine Learning:
Data dibagi menjadi set pelatihan dan pengujian.
Model machine learning dikembangkan dan dilatih menggunakan set pelatihan.
Model kemudian diuji menggunakan set pengujian untuk mengevaluasi kinerjanya.

- Evaluasi Model:
Kinerja model dievaluasi menggunakan metrik yang relevan seperti akurasi, presisi, recall, atau F1-score, tergantung pada kebutuhan proyek.
Model dapat disesuaikan dan dievaluasi kembali jika diperlukan untuk meningkatkan kinerjanya.

- Implementasi dan Penyesuaian:
Setelah model dianggap memadai, itu dapat diimplementasikan dalam lingkungan produksi atau digunakan untuk memberikan rekomendasi dan solusi kepada pengguna akhir.Ada juga proses penyesuaian dan pemeliharaan model secara berkala untuk memastikan bahwa itu tetap relevan dan akurat seiring waktu.|
| Arsitektur model | Arsitektur model yang digunakan yaitu model embedding dimana terdiri dari vectorize_layer, kemudian layer embedding dengan dimensi embedding yaitu 16, setelah itu layer AveragePooling1D karena data merupakan bentuk text, kemudian layer dense 64, 32 dengan activation relu dan sigmoid karena akan dilakukan klasifikasi antar dua label. Loss yang digunakan binary_crossentropy dengan optimizer Adam dan metrik BinaryAccuray |
| Metrik evaluasi | Metrik evaluasi yang digunakan yaitu ExampleCount, AUC, FalsePositives, TruePositives, FalseNegatives, TrueNegatives, dan BinaryAccuracy |
| Performa model | Evaluasi model diperoleh yaitu AUC sebesar 82%, kemudian example_count 575, dengan BinaryAccuracy 75%, dan loss sebesar 1.364. Untuk False Negatives 68, False Positive 75, True Negative 201 dan True Positive 231. Model yang telah dibuat dapat dilakukan peningkatan performa, karena model belum cukup baik karena BinaryAccuracy masih dibawah 80% |
