# TugasPratikumML_234-244
# Klasifikasi Alzheimer's Berdasarkan Hasil MRI Menggunakan Convolutional Neural Networks

### Team:
+ Andhika Dwija Bagaskara_201810370311234
+ Lulita Ria Wandani_201810370311244
    
### Overview Jurnal
Jurnal yang digunakan pada project ini berjudul "Convolutional neural networks for classification of Alzheimer’s disease: Overview and reproducible evaluation" yang ditulis oleh Junhao Wen, Elina Thibeau-Sutre, Mauricio Diaz-Melo, Jorge Samper-González, Alexandre Routier, Simona Bottani, Didier Dormont, Stanley Durrleman, Ninon Burgos, Olivier, pada tahun 2020. Adapun rincian jurnal sebagai berikut:
#### DOI: https://doi.org/10.1016/j.media.2020.101694
#### Dataset: ADNI (Alzheimers Disease Neuroimaging Initiative)
#### Preprocessing:
169 × 208 × 179 with 1 mm3 isotropic voxels.
#### Model 1 (3D subject-level CNN)

![model1](https://user-images.githubusercontent.com/49244704/145960549-fef94a6d-f0a4-4097-8eaf-2a9d569aa70b.PNG)

#### Model 2 (3D ROI-based CNN)

![model2](https://user-images.githubusercontent.com/49244704/145960690-acf360a1-7043-4994-a7cc-b772a9ddc166.PNG)

#### Model 3 (2D slice-level CNN)

![model3](https://user-images.githubusercontent.com/49244704/145960798-e245592e-7f7b-434b-9842-2269574f1930.PNG)

#### Akurasi:
+ Model 1 (3D subject-level CNN) : 0.86
+ Model 2 (3D ROI-based CNN) : 0.90
+ Model 3 (2D slice-level CNN) : 0.81

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

### Model 1 (CNN + Inception V3)
#### Summary

![summary 1](https://user-images.githubusercontent.com/49244704/145957141-0f1f8d2b-50bb-496a-81ea-5ca0328980e6.PNG)

#### Akurasi

![acc 1](https://user-images.githubusercontent.com/49244704/145958043-b12d30f2-12c0-47d9-ad97-148122eea7fe.PNG)

#### Loss

![loss 2](https://user-images.githubusercontent.com/49244704/145958105-242500b6-0d31-4862-8b38-088484a47707.PNG)

#### Classification Report

![report 1](https://user-images.githubusercontent.com/49244704/145958285-3359ded9-d4f9-4c63-bc91-f794e69118d6.PNG)

### Model 2 (CNN + VGG16)
#### Summary

![summary 2](https://user-images.githubusercontent.com/49244704/145958511-2c481a75-db12-4002-b055-36989eac5f52.PNG)

#### Akurasi

![Capture](https://user-images.githubusercontent.com/49244704/145958609-7da9084b-a20e-4dc6-929a-d0888a4e8fca.PNG)

#### Loss

![mode loss 2](https://user-images.githubusercontent.com/49244704/145958665-bc38dac0-0436-4e84-b1c0-11923a83f0e7.PNG)

#### Classification Report

![report 2](https://user-images.githubusercontent.com/49244704/145958754-dad1f666-7428-4f59-bf2a-6faa6c5773e3.PNG)

#### Tampilan awal Deployment

![www](https://user-images.githubusercontent.com/49264864/147601792-a9be94f9-7ba0-4d37-9eca-a13a164a1ca5.jpg)

#### Tampilan Hasil Prediksi Beserta Nilai Confidence

![www](https://user-images.githubusercontent.com/49264864/147602001-3767a86e-0a4f-472c-a2b1-3a737c196bb9.jpg)

#### Hasil Prediksi Model terbaik dan Waktu Prediksi

![www](https://user-images.githubusercontent.com/49264864/147602137-bfc3d512-cb9a-4b96-8a2f-b804e2da8c43.jpg)

### Library
+ Tensorflow
+ Keras
+ Matplotlib
+ Numpy
+ OpenCV

### Status Project
1. Preprocessing Data : Done 
2. Model 1            : Done
3. Model 2            : Done
4. Augmentasi Data    : Done
5. Pretrained Model   : Done
6. Model Deployment   : Done
