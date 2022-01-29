# Machine Learning 234-244
# Klasifikasi Alzheimer's Berdasarkan Citra MRI Menggunakan Convolutional Neural Networks

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

### Model 1 (Base CNN)
#### Summary

![summary 1](https://user-images.githubusercontent.com/49244704/145957141-0f1f8d2b-50bb-496a-81ea-5ca0328980e6.PNG)

#### Akurasi dan Loss

![Model 1 akurasi](https://user-images.githubusercontent.com/49244704/151637382-127b96b6-a7cb-4fa6-9e4b-e59b3ac1cf24.png)

#### Classification Report

![Model 1 report](https://user-images.githubusercontent.com/49244704/151637468-1d5f63af-48e6-475d-b711-2bec839171ea.png)

### Model 2 (CNN + VGG19)
#### Summary

![summary 2](https://user-images.githubusercontent.com/49244704/145958511-2c481a75-db12-4002-b055-36989eac5f52.PNG)

#### Akurasi dan Loss

![model 2 akurasi](https://user-images.githubusercontent.com/49244704/151637506-90c12de2-4f98-45a5-9a1e-6e0e021a59bd.png)

#### Classification Report

![model 2 report](https://user-images.githubusercontent.com/49244704/151637535-c28b5c04-3b33-4784-b813-5e9271a7663a.png)

### Model 3 (CNN + Inception-V3)
#### Summary

![summary3](https://user-images.githubusercontent.com/49244704/151637617-f29b8f69-a05d-4366-87be-e4898f504f81.PNG)

#### Akurasi dan Loss

![model 3 akurasi](https://user-images.githubusercontent.com/49244704/151637662-6c2e321a-c875-4129-944d-57f020991d6e.png)

#### Classification Report

![model 3 report](https://user-images.githubusercontent.com/49244704/151637680-e1b9a2ff-84e0-4d6e-a213-db83fef5291c.png)

### Deployment
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
4. Model 3            : Done
5. Augmentasi Data    : Done
6. Pretrained Model   : Done
7. Model Deployment   : Done
