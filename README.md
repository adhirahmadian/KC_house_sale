# KC_house_sale

# Overview
Dataset ini berisi harga jual rumah untuk King County hingga mencakup Seattle, USA. Data ini mencakup rumah yang dijual antara Mei 2014 dan Mei 2015. 

Pada _project_ ini saya akan mengevaluasi model regresi untuk memprediksi harga rumah berdasarkan spesifikasi tertentu.

# Code Resources

Python Version: 3.7

Packages: pandas, numpy, sklearn, matplotlib, seaborn, keras.

https://www.kaggle.com/harlfoxem/housesalesprediction

# EDA

Saya melakukan beberapa analisis data harga rumah, serta hubungannya terhahap luas tanah.

>![Harga Rumah](/harga_rumah.png)
>![Harga Rumah Luas](/luas_harga.png)
>![Harga Tahun](/harga_tahunan.png)

Berdasarkan kurva bisa kita lihat bahwa sebagian besar harga rumah berada dibawah 1 juta dollar dengan luas dibawah 6000 meter persegi.
Harga lebih variatif pada tahun 2014 dibanding tahun 2015.

# Model Building
Dengan metode deep learning keras, saya menggunakan Neural Network dengan _input layer_ dan _hidden layer_ sebanyak 19 sel dengan metode aktivasi ReLU (Rectified Linear Unit), output layernya 1, serta optimasi 'adam' dan loss 'mse'. Metode ini digunakan karena pada kasus ini saya akan memprediksi besar eror terhadap nilai aktual.

>![model](/model.png)

model menunjukan kurva loss dan val_loss yang dimana kurva sangat fit dan mulai _overfitting_. Model tersebut akan saya coba gunakan.

# Model Performance
Hasil _modelling_ ternyata bisa memprediksi dengan ketepatan >80% dan akan lebih baik bila data yang digunakan adalah untuk rumah dengan harga dibawah 2 juta dollar.

>![model](/prediksi_harga.png)

terakhir saya mencoba memprediksi harga rumah dengan data random, rumah yang dijual dengan harga 383.000 dollar saya berhasil memprediksi harga rumah tersebut 381.728 dollar
