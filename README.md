# KC_house_sale

# Overview
This dataset contains the selling price of homes for King County to cover Seattle, USA. This data includes homes sold between May 2014 and May 2015.

In this project I will evaluate a regression model to predict house prices based on certain specifications.

# Code Resources

Python Version: 3

Packages: pandas, numpy, sklearn, matplotlib, seaborn, keras.

Dataset : https://www.kaggle.com/harlfoxem/housesalesprediction

# EDA

I did some data analysis on house prices and their relationship to land area.

>![Harga Rumah](/harga_rumah.png)
>![Harga Rumah Luas](/luas_harga.png)

Based on graph 1 and graph 2 we can see that most of the house prices in King County are under 1 million dollars with an area under 6000 square meters.

>![Harga Tahun](/harga_tahunan.png)

And for graph 3, it shows the comparison of price variants in 2014 and 2015.

# Model Building
With the _Deep learning_ method, I use the _Neural Network_. The _input layer_ and _hidden layer_ that I use are 19 cells with the _ReLU_ (_Rectified Linear Unit_) activation method. For _output layer_ 1 cells with _adam_ optimization and _mse_ loss. This methods are used because in this case I will predict the amount of error against the actual value.

>![model](/model.png)

The model curve shows the tangent of the _loss_ and _val_loss_ where the curve starts to overfitting, therefore I will try to use this model.
# Model Performance

The results of this _modeling_ is able to predict with accuracy above 80% and better if the data used were for houses with prices below 2 million dollars.

>![model](/prediksi_harga.png)

Finally, I tried to predict the price of the house with random data which was sold for 383,000 dollars and I managed to predict the price of that house was 381,728 dollars.
