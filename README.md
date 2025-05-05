# Proyek Klasifikasi Gambar

## Deskripsi Proyek
Proyek ini bertujuan untuk mengklasifikasikan gambar ke dalam tiga kategori: **Plastic Bag**, **Paper Bag**, dan **Garbage Bag** menggunakan model deep learning berbasis **Convolutional Neural Networks (CNN)**. Model ini dilatih menggunakan dataset yang terdiri dari 15.000 gambar, dengan pembagian dataset menjadi **80% untuk training**, **10% untuk validasi**, dan **10% untuk testing**. Proyek ini juga mencakup beberapa format penyimpanan model seperti **SavedModel**, **TensorFlow Lite (TF-Lite)**, dan **TensorFlow.js (TFJS)** untuk memungkinkan penggunaan model di berbagai platform.

## Kriteria Submission
1. **Dataset**:
   - Dataset yang digunakan terdiri dari 15.000 gambar yang memiliki 3 kelas: **Plastic Bag**, **Paper Bag**, dan **Garbage Bag**. Dataset ini diunduh dari Kaggle dan merupakan dataset yang belum pernah digunakan sebelumnya.

2. **Pembagian Dataset**:
   - Dataset dibagi menjadi tiga bagian utama:
     - **80% untuk Training Set**
     - **10% untuk Validation Set**
     - **10% untuk Test Set**
     - Pembagian ini memastikan model dilatih dengan baik dan dapat dievaluasi secara objektif.

3. **Arsitektur Model**:
   - Model yang digunakan adalah **Sequential Model** dengan **Conv2D** (Convolutional Layer) dan **MaxPooling Layer**, sesuai dengan kriteria.
   - Model dibangun menggunakan Keras dengan TensorFlow sebagai backend.

4. **Akurasi**:
   - Model mencapai lebih dari **98% akurasi** pada **training set** dan **testing set**, memenuhi kriteria minimal 85%.

5. **Plot Akurasi dan Loss**:
   - Visualisasi akurasi dan loss selama proses pelatihan untuk menunjukkan performa model. Plot ini memberikan gambaran mengenai peningkatan akurasi dan penurunan loss selama training.

6. **Format Model**:
   - Model disimpan dalam tiga format berikut:
     - **SavedModel**: Format standar untuk deployment di server atau cloud.
     - **TensorFlow Lite (TF-Lite)**: Format yang dioptimalkan untuk perangkat mobile dan embedded.
     - **TensorFlow.js (TFJS)**: Format untuk menjalankan model di browser dan aplikasi berbasis JavaScript.

7. **Callback**:
   - **Callback** diimplementasikan untuk menghentikan pelatihan otomatis jika akurasi mencapai lebih dari **98%** pada **training set** dan **validation set**, sehingga menghemat waktu komputasi.

8. **Preprocessing Gambar**:
   - Resolusi gambar yang tidak seragam pada dataset telah disesuaikan terlebih dahulu menjadi ukuran **150x150 piksel** untuk memastikan model dapat memproses gambar secara konsisten.

9. **Inference**:
   - Inference dilakukan menggunakan dua model yang berbeda: **SavedModel** dan **TensorFlow Lite (TF-Lite)**.
   - Hasil prediksi menggunakan kedua model menunjukkan performa yang konsisten dan akurat dalam mengklasifikasikan gambar ke dalam kategori yang tepat.

## Langkah-langkah Implementasi

### 1. Persiapan Dataset
Dataset digunakan terdiri dari 15.000 gambar yang telah dibagi menjadi tiga kelas utama: **Plastic Bag**, **Paper Bag**, dan **Garbage Bag**. Dataset ini diunduh dari Kaggle.

### 2. Pembagian Dataset
Dataset dibagi menjadi tiga bagian:
- **Training Set**: 80% dari dataset
- **Validation Set**: 10% dari dataset
- **Test Set**: 10% dari dataset

### 3. Pembuatan Model
Model dibangun menggunakan arsitektur **Sequential** dengan beberapa lapisan **Conv2D**, **MaxPooling**, dan **Dense** untuk klasifikasi gambar. Dropout digunakan untuk mengurangi overfitting. Fungsi aktivasi yang digunakan adalah **ReLU** untuk lapisan konvolusional dan **Softmax** untuk lapisan output.

### 4. Pelatihan Model
Model dilatih dengan menggunakan **Adam Optimizer** dan **Categorical Crossentropy** sebagai fungsi loss. Akurasi diukur selama pelatihan dan evaluasi untuk memastikan model mencapai lebih dari 98% pada **training set** dan **testing set**.

### 5. Penyimpanan Model
Model disimpan dalam tiga format yang berbeda:
- **SavedModel**: Untuk penggunaan di server dan cloud.
- **TensorFlow Lite (TF-Lite)**: Untuk perangkat mobile dan embedded.
- **TensorFlow.js (TFJS)**: Untuk aplikasi berbasis browser.

### 6. Callback
Callback digunakan untuk menghentikan pelatihan secara otomatis jika akurasi model mencapai lebih dari 98%.

### 7. Preprocessing Gambar
Gambar dari dataset yang memiliki resolusi tidak seragam diubah ukurannya menjadi **150x150 piksel** sebelum dimasukkan ke dalam model untuk memastikan konsistensi.

### 8. Inference
Inference dilakukan menggunakan model yang disimpan dalam format **SavedModel** dan **TensorFlow Lite** untuk melihat hasil prediksi gambar. Kedua model menghasilkan prediksi yang akurat.

## Kesimpulan
Proyek ini berhasil mengklasifikasikan gambar ke dalam tiga kategori dengan akurasi lebih dari 98%. Semua kriteria yang ditentukan telah dipenuhi, termasuk pembagian dataset, arsitektur model, dan format penyimpanan model yang memungkinkan penggunaan model di berbagai platform. Proyek ini juga berhasil mengimplementasikan semua saran penilaian termasuk callback untuk menghentikan pelatihan otomatis jika akurasi mencapai lebih dari 98%, gambar pada dataset asli memiliki resolusi yang tidak seragam, dataset terdiri lebih dari 10000 gambar lebih tepatnya 15000 gambar, terdiri dari 3 kelas, akurasi >95% lebih tepatnya 98%, serta melakukan inference dengan dua model yang berbeda: **SavedModel** dan **TensorFlow Lite**.

