# Klasifikasi-Bunga-Menggunakan-Convolutional-Neural-Network-CNN-_ML
Proyek ini mendemonstrasikan pembangunan dan evaluasi model Convolutional Neural Network (CNN) untuk mengklasifikasikan gambar bunga ke dalam beberapa kategori. Model dilatih menggunakan dataset `tf_flowers` dari TensorFlow Datasets.

## Daftar Isi
- [Gambaran Umum Proyek](#gambaran-umum-proyek)
- [Dataset](#dataset)
- [Struktur Model](#struktur-model)
- [Hasil Pelatihan](#hasil-pelatihan)
- [Evaluasi Model](#evaluasi-model)
- [Prediksi Gambar Baru](#prediksi-gambar-baru)
- [Persyaratan](#persyaratan)
- [Cara Menjalankan](#cara-menjalankan)

## Gambaran Umum Proyek

Proyek ini bertujuan untuk membangun sistem klasifikasi gambar yang dapat membedakan berbagai jenis bunga. Kami menggunakan arsitektur CNN yang sederhana namun efektif untuk mempelajari fitur-fitur dari gambar bunga dan mengklasifikasikannya ke dalam kategori yang sesuai.

## Dataset

Dataset yang digunakan adalah `tf_flowers` yang tersedia di TensorFlow Datasets. Dataset ini berisi gambar-gambar dari 5 kelas bunga:
- `dandelion`
- `daisy`
- `tulips`
- `sunflowers`
- `roses`

Dataset dibagi menjadi 80% untuk pelatihan dan 20% untuk validasi.

## Struktur Model

Model CNN dibangun menggunakan `tf.keras.Sequential` dengan lapisan-lapisan berikut:

-   **`Conv2D`**: Lapisan konvolusi pertama dengan 32 filter berukuran (3,3) dan fungsi aktivasi ReLU. Menerima input gambar berukuran 128x128x3 (tinggi, lebar, saluran warna).
-   **`MaxPooling2D`**: Lapisan max-pooling dengan ukuran (2,2) untuk mengurangi dimensi spasial.
-   **`Conv2D`**: Lapisan konvolusi kedua dengan 64 filter berukuran (3,3) dan fungsi aktivasi ReLU.
-   **`MaxPooling2D`**: Lapisan max-pooling kedua dengan ukuran (2,2).
-   **`Flatten`**: Lapisan untuk meratakan output dari lapisan konvolusi menjadi satu vektor tunggal.
-   **`Dense`**: Lapisan fully connected (Dense) dengan 128 unit dan fungsi aktivasi ReLU.
-   **`Dense`**: Lapisan output fully connected dengan jumlah unit sama dengan jumlah kelas bunga (5 kelas) dan fungsi aktivasi Softmax untuk probabilitas kelas.

Model dikompilasi dengan optimizer `adam`, fungsi loss `sparse_categorical_crossentropy`, dan metrik `accuracy`.

## Hasil Pelatihan
Model dilatih selama 10 epoch.

## Evaluasi Model
Setelah pelatihan, model dievaluasi menggunakan data validasi.

Persyaratan
Pastikan Anda telah menginstal pustaka-pustaka berikut:
tensorflow
numpy
matplotlib
seaborn
tensorflow_datasets
scikit-learn
Pillow (PIL)

Anda dapat menginstalnya menggunakan pip
