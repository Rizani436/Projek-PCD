# Project Title
- Analisis Citra Digital untuk Identifikasi dan Klasifikasi Penyakit Daun Jagung				
## Dataset
- https://www.kaggle.com/datasets/smaranjitghose/corn-or-maize-leaf-disease-dataset
## Members
| Name | Student ID |
| --- | --- |
| DARA FINAS ELEN |F1D022038|
| PUTRA HERYAN GAGAH PERKASA |F1D022087|
| RAFLI RIZANI|F1D022088|
| RIZKA SAFITRI |F1D022092|
| KAYLA MIZANTI |F1D022127|

## Deskripsi Program
Program ini akan mengimplementasikan beberapa pengolahan citra digital yang diterapkan dalam proses pengklasifikasian daun sehat dan tidak sehat dari beberapa label. 

Proses dimulai dengan pemuatan gambar citra daun jagung berbagai label dari direktori bernama "data" menggunakan fungsi insertGambar, di mana setiap gambar diresize ke ukuran yang ditentukan dan latar belakangnya dihapus menggunakan algoritma penghapusan latar belakang. Berbagai proses preprocessing dilakukan. Gambar kemudian diubah menjadi citra grayscale dan diterapkan ekualisasi histogram untuk meningkatkan kontrasnya, dah proses yang lainnya.
Ekstraksi fitur dilakukan dengan menerapkan Gray Level Co-occurrence Matrix (GLCM) pada citra hasil preprocessing. GLCM dihitung untuk empat sudut (0°, 45°, 90°, 135°) menggunakan fungsi derajat dan GLCM. Hasil GLCM dijadikan dasar untuk menghitung statistik fitur tekstur seperti kontras, dissimilaritas, homogenitas, energi, korelasi, entropy, dan ASM menggunakan fungsi-fungsi terpisah seperti contrast, dissimilarity, homogeneity, energy, correlation, entropy, dan asm.

Seluruh hasil ekstraksi fitur disimpan dalam sebuah dataframe menggunakan pandas, dan kemudian disimpan ke dalam file CSV untuk analisis lanjutan. Data yang telah diekstraksi dan diolah kemudian dipisahkan menjadi data latih dan data uji menggunakan train_test_split, dan dinormalisasi menggunakan StandardScaler. Tiga jenis modeling yang digunakan yaitu K-Nearest Neighbors (KNN), Support Vector Machine (SVM), dan Random Forest, diterapkan untuk melakukan klasifikasi. Evaluasi performa dari ketiga model dilakukan dengan menghitung metrik seperti akurasi, presisi, recall, dan F1-score menggunakan fungsi evaluasi yang telah disediakan.

Hasil dari evaluasi menunjukkan bahwa model Random Forest memberikan performa yang sedikit lebih baik dibandingkan KNN dan SVM dalam kasus yang disajikan. Dengan menggunakan program ini, dapat diharapkan  dapat melakukan analisis klasifikasi penyakit daun pada jagung berbasis fitur tekstur dengan lebih efektif dan dapat mengimplementasikannya untuk tugas klasifikasi dengan memanfaatkan data yang telah diolah secara ekstensif.

## Hasil
Hasil dari evaluasi menunjukkan bahwa model Random Forest memberikan performa yang sedikit lebih baik dibandingkan KNN dan SVM dalam kasus yang disajikan. Dengan menggunakan program ini, diharapkan  dapat melakukan analisis klasifikasi penyakit daun pada jagung berbasis fitur tekstur dengan lebih efektif.





