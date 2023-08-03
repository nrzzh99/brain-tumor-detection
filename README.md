# brain-tumor-detection
Objective : Brain Tumor Detection

# Latar Belakang Masalah :
Deteksi dini tumor otak sangat penting untuk mendapatkan pengobatan yang efektif. Semakin cepat tumor otak terdeteksi, semakin baik peluang kesembuhan dan pengurangan risiko komplikasi. Proyek ini bertujuan untuk memastikan deteksi dini dan akurat sehingga pasien dapat segera mendapatkan pengobatan yang tepat.

# Data yang Digunakan :
Pada project kali ini, dataset yang digunakan berasal dari kaggle dengan judul Brain MRI Images for Brain Tumor Detection. Jumlah masing2 data gambar antara data yes dan no adalah 155 untuk data yes, dan 98 untuk data no

# Metode yang Digunakan :
Model Sequential API digunakan karena kemudahannya dalam membangun model dengan layer yang ditambahkan secara berurutan. Hal ini membuat model ANN yang dihasilkan memiliki struktur yang terstruktur dan mudah diimplementasikan.

Model Functional API digunakan untuk menciptakan arsitektur jaringan yang lebih kompleks yang tidak dapat dicapai dengan menggunakan model Sequential API. Hal ini memungkinkan penggunaan layer-layer yang lebih kompleks dan lebih fleksibel dalam merancang model.

Augmentasi data menggunakan ImageDataGenerator membantu memperluas jumlah data dengan melakukan transformasi pada gambar seperti rotasi, pergeseran, zoom, dan lainnya. Hal ini meningkatkan variasi data yang digunakan dalam proses pelatihan dan dapat membantu mengatasi masalah overfitting.

Transfer Learning digunakan dengan menggunakan arsitektur VGG16 sebagai base model. Layer-layer pada base model dibekukan agar tidak dilatih ulang, dan lapisan-lapisan baru ditambahkan untuk disesuaikan dengan tugas deteksi tumor otak. Transfer learning memungkinkan pemanfaatan pengetahuan yang sudah ada dari arsitektur yang telah dilatih sebelumnya untuk tugas lain.

Model dikompilasi dengan menggunakan optimizer Adam dan loss function categorical_crossentropy. Optimizer Adam merupakan optimizer yang populer dalam pelatihan jaringan saraf karena efisien dan efektif. Loss function categorical_crossentropy cocok untuk masalah klasifikasi multikelas seperti deteksi tumor otak.

Evaluasi model menggunakan metrik akurasi (accuracy), yang mengukur sejauh mana model dapat mengklasifikasikan data dengan benar. Akurasi adalah salah satu metrik yang paling umum digunakan untuk mengevaluasi kinerja model klasifikasi.

# Kelebihan dan Kekurangan project :
Secara kelebihan, model dapat memprediksi gambar baru dengan benar sekitar 76.2%, ini cukup baik untuk mengetahui apakah digambarnya terdapat tumor atau tidak.

kelemahannya, model bisa saja salah memprediksi, karena datanya imbalance, diperlukan data lebih benyak agar model dapat memprediksi dengan baik
