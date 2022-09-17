# Rent price prediction
Roy Andhika Satria, [satriaroy70@gmail.com](mailto:satriaroy70@gmail.com).

## Regression
Sebuah proyek machine learning yang menggunakan algoritma regresi untuk memprediksi harga sewa hunian berdasarkan spesifikasi yang dimilikinya.

## Dataset
Data berisi informasi harga sewa rumah / apartemen / kos yang diambil dari [**magicbricks**](https://www.magicbricks.com/). Tiap hunian memiliki harga sewa yang berbeda dengan spesifikasi masing - masing yang unik.

## Tujuan
Ke depannya kita bisa memperkirakan sewa hunian sendiri, atau menggunakan hasil prediksi ini sebagai acuan harga untuk mencari / menjual hunian masing - masing.

### Problem Statement :
1. Kota apa yang memiliki biaya sewa paling mahal?
1. Sewa untuk keluarga dan bujangan lebih mahal mana?

## Penjelasan Dataset 
Dataset yang ada meliputi `4746` baris dengan `10` fitur dan 1 label (`Rent`)

| No | __Nama Fitur__ | __Penjelasan__ |
| - | - | - |
| 1 | BHK | Number of Bedrooms, Hall, Kitchen. | 
| 2 | Rent | Rent of the Houses/Apartments/Flats. |
| 3 | Size | Size of the Houses/Apartments/Flats in Square Feet. |
| 4 | Floor  | Houses/Apartments/Flats situated in which Floor and Total Number of Floors (Example: Ground out of 2, 3 out of 5, etc.) |
| 5 | Area Type | Size of the Houses/Apartments/Flats calculated on either Super Area or Carpet Area or Build Area. | 
| 6 | Area Locality | Locality of the Houses/Apartments/Flats. |
| 7 | City | City where the Houses/Apartments/Flats are Located. |
| 8 | Furnishing Status | Furnishing Status of the Houses/Apartments/Flats, either it is Furnished or Semi-Furnished or Unfurnished. |
| 9 | Tenant Preferred | Type of Tenant Preferred by the Owner or Agent. |
| 10 | Bathroom | Number of Bathrooms. | 
| 11 | Point of Contact | Whom should you contact for more information regarding the Houses/Apartments/Flats. | 

## Steps
1. Data Understanding
2. Exploratory Data Analysis (EDA)
3. Preprocessing 
4. Modeling & Conclusion 

### 1. Data Understanding
1. Terdapat 10 fitur dan 1 label pada dataset
2. Awalnya tidak ada null / missing value
3. Fitur **posted_on**, **area_locality**, dan **point_of_contact** dihapus karena dianggap terlalu random

### 2. Ringkasan Exploratory Data Analysis (EDA)
![graph](https://raw.githubusercontent.com/royandhika/rent-price-regression/main/assets/cityrent.png)
1. Kota Mumbai memiliki rerata harga sewa jauh lebih mahal dibandingkan kota lain.  
2. Kota lainnya memiliki harga kurang lebih setara.  
![graph](https://raw.githubusercontent.com/royandhika/rent-price-regression/main/assets/rent-city-furnish.png)
3. Di Delhi dan Hyderabad, hunian semi-furnish lebih mahal daripada hunian full-furnished.
4. Di Mumbai harga sewa unfurnished jauh di bawah semi dan full-furnished (hampir setengahnya) sehingga dapat dimasukkan pertimbangan.
![graph](https://raw.githubusercontent.com/royandhika/rent-price-regression/main/assets/city-rent-boxplot.png)
5. Ada 1 outlier di Bangalore dimana harga sewa mencapai 3.500.000 dengan ukuran 2500.
![graph](https://raw.githubusercontent.com/royandhika/rent-price-regression/main/assets/heatmap.png)
![graph](https://raw.githubusercontent.com/royandhika/rent-price-regression/main/assets/heatmap2.png)
6. Atas pertimbangan dan percobaan fitur **floor** dan **totalfloor** dihapus, dan hasilnya terjadi perubahan terhadap korelasi yang ditunjukkan dalam heatmap.
![graph](https://raw.githubusercontent.com/royandhika/rent-price-regression/main/assets/rent-city-tenant.png)
7. Sewa untuk bujangan, keluarga, atau campur tidak memiliki perbedaan signifikan.

### 3. Preprocessing
Saya menggunakan [regex101](https://regex101.com/r/Xy6zZs/1) untuk membantu *feature engineering*  
Kemudian dipilih menggunakan onehot encoding daripada labelencoder karena data merupakan data nominal 

### 4. Benchmarking


### 5. Learning Curve

