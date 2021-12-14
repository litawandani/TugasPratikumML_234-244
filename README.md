# TugasPratikumML_234-244
# Klasifikasi Alzheimer's Berdasarkan Hasil MRI Menggunakan Convolutional Neural Networks

### Team:
+ Andhika Dwija Bagaskara_201810370311234
+ Lulita Ria Wandani_201810370311244
    
### Overview Jurnal
Jurnal yang digunakan pada project ini berjudul "Convolutional neural networks for classification of Alzheimer’s disease: Overview and reproducible evaluation" yang ditulis oleh Junhao Wen, Elina Thibeau-Sutre, Mauricio Diaz-Melo, Jorge Samper-González, Alexandre Routier, Simona Bottani, Didier Dormont, Stanley Durrleman, Ninon Burgos, Olivier, pada tahun 2020. Adapun rincian jurnal sebagai berikut:
+ DOI: https://doi.org/10.1016/j.media.2020.101694
+ Dataset: ADNI (Alzheimers Disease Neuroimaging Initiative)
+ Preprocessing:
+ Model:
+ Akurasi:

### Overview Dataset
Dataset yang digunakan merupakan dataset citra MRI dengan judul "Alzheimer's Dataset (4 class of Images)". Adapun rincian dataset sebagai berikut:

Link sumber: https://www.kaggle.com/tourist55/alzheimers-dataset-4-class-of-images. Dataset terdiri dari 6400 gambar yang terbagi menjadi 4 kelas dengan rincian sebagai berikut:
1. Non-Demented: 3200 gambar
2. Verry Mild Demented: 2240 gambar
3. Moderate Demented: 64 gambar 
4. Mild Demented: 896 gambar


Dataset dibagi menjadi data train, val, test dengan perbandingan 80:19:1. Jumlah data setelah dibagi menjadi 5119 train, 1215 val, dan 66 test

### Prepocessing
+ Size (150, 150)
+ Horizontal flip: True
+  Shuffle: False
+  Color Mode: rgb
+  Batch Size: 32
+  Class: Categorical
+  Learning Rate: 0.001

### Model 1



### Model 2:



### Library
+ Tensorflow
+ Keras
+ Matplotlib
+ Numpy

### Status Project
1. Preprocessing Data : Done 
2. Model 1            : Done
3. Model 2            : Done
4. Augmentasi Data    : Done
