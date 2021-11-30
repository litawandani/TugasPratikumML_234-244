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
+ Link sumber: https://www.kaggle.com/tourist55/alzheimers-dataset-4-class-of-images. Dataset terdiri dari 6400 gambar yang terbagi menjadi 4 kelas dengan rincian sebagai berikut:
1. Non-Demented: 3200 gambar
2. Verry Mild Demented: 2240 gambar
3. Moderate Demented: 64 gambar 
4. Mild Demented: 896 gambar
Dataset dibagi menjadi data train, val, test dengan perbandingan 80:19:1. Jumlah data setelah dibagi menjadi 5119 train, 1215 val, dan 66 test

### Prepocessing
1. Size (150, 150)
2. Horizontal flip: True
3. Shuffle: False

### Model
+ Model yang digunakan: CNN
+ Summary model 1: 

Model: "sequential_1"
_______________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d_3 (Conv2D)           (None, 150, 150, 64)      1792      
                                                                 
 max_pooling2d_3 (MaxPooling  (None, 75, 75, 64)       0         
 2D)                                                             
                                                                 
 batch_normalization_3 (Batc  (None, 75, 75, 64)       256       
 hNormalization)                                                 
                                                                 
 conv2d_4 (Conv2D)           (None, 75, 75, 128)       73856     
                                                                 
 max_pooling2d_4 (MaxPooling  (None, 38, 38, 128)      0         
 2D)                                                             
                                                                 
 batch_normalization_4 (Batc  (None, 38, 38, 128)      512       
 hNormalization)                                                 
                                                                 
 conv2d_5 (Conv2D)           (None, 38, 38, 256)       295168    
                                                                 
 max_pooling2d_5 (MaxPooling  (None, 19, 19, 256)      0         
 2D)                                                             
                                                                 
 batch_normalization_5 (Batc  (None, 19, 19, 256)      1024      
 hNormalization)                                                 
                                                                 
 dropout_1 (Dropout)         (None, 19, 19, 256)       0         
                                                                 
 flatten_1 (Flatten)         (None, 92416)             0         
                                                                 
 dense_4 (Dense)             (None, 256)               23658752  
                                                                 
 dense_5 (Dense)             (None, 128)               32896     
                                                                 
 dense_6 (Dense)             (None, 64)                8256      
                                                                 
 dense_7 (Dense)             (None, 4)                 260       
                                                                 
=================================================================
Total params: 24,072,772
Trainable params: 24,071,876
Non-trainable params: 896
_______________________
None

+ Summary model 2:

Model: "sequential"
_______________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 150, 150, 16)      448       
                                                                 
 max_pooling2d (MaxPooling2D  (None, 75, 75, 16)       0         
 )                                                               
                                                                 
 batch_normalization (BatchN  (None, 75, 75, 16)       64        
 ormalization)                                                   
                                                                 
 conv2d_1 (Conv2D)           (None, 75, 75, 32)        4640      
                                                                 
 max_pooling2d_1 (MaxPooling  (None, 38, 38, 32)       0         
 2D)                                                             
                                                                 
 batch_normalization_1 (Batc  (None, 38, 38, 32)       128       
 hNormalization)                                                 
                                                                 
 dropout (Dropout)           (None, 38, 38, 32)        0         
                                                                 
 conv2d_2 (Conv2D)           (None, 38, 38, 64)        18496     
                                                                 
 max_pooling2d_2 (MaxPooling  (None, 19, 19, 64)       0         
 2D)                                                             
                                                                 
 batch_normalization_2 (Batc  (None, 19, 19, 64)       256       
 hNormalization)                                                 
                                                                 
 dropout_1 (Dropout)         (None, 19, 19, 64)        0         
                                                                 
 flatten (Flatten)           (None, 23104)             0         
                                                                 
 dense (Dense)               (None, 512)               11829760  
                                                                 
 dense_1 (Dense)             (None, 128)               65664     
                                                                 
 dense_2 (Dense)             (None, 64)                8256      
                                                                 
 dense_3 (Dense)             (None, 4)                 260       
                                                                 
=================================================================
Total params: 11,927,972
Trainable params: 11,927,748
Non-trainable params: 224
_______________________
None

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
