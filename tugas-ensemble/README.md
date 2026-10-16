# Tugas 3 - Ensemble Method & Class Imbalance

Dataset *Credit Card Fraud Detection* dari Kaggle
(https://www.kaggle.com/mlg-ulb/creditcardfraud), file `creditcard.csv`, 284.807 baris
dan 31 kolom. Fraud hanya 492 transaksi (0,173%).

Dataset tidak diunggah ke repo karena ukurannya sekitar 150 MB. Untuk menjalankan
notebook, taruh `creditcard.csv` di folder `archive/` pada root repo
(notebook membaca `../archive/creditcard.csv`).

Tahapan yang dikerjakan: cek distribusi kelas, hapus duplikat, split 80:20 stratified,
standarisasi `Time` dan `Amount`, lalu membandingkan Random Forest tanpa penanganan
imbalance dengan SMOTE, random undersampling, dan class weight. Gradient Boosting
dipakai sebagai pembanding.

## Isi folder

| File | Keterangan |
|---|---|
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Ensemble.ipynb` | notebook model + laporan |
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Ensemble.pdf` | versi PDF dari notebook |

## Ringkasan hasil (kelas fraud, data uji)

| Model | Precision | Recall | F1 | AUC-ROC | AUPRC |
|---|---|---|---|---|---|
| RF Baseline | 0,972 | 0,726 | 0,831 | 0,924 | 0,788 |
| RF + SMOTE | 0,911 | 0,758 | 0,828 | 0,966 | 0,804 |
| RF + Undersampling | 0,085 | 0,874 | 0,155 | 0,977 | 0,698 |
| RF + Class weight | 0,971 | 0,705 | 0,817 | 0,925 | 0,796 |
| GB Baseline | 0,504 | 0,695 | 0,584 | 0,765 | 0,528 |
| GB + SMOTE | 0,538 | 0,821 | 0,650 | 0,965 | 0,795 |

## Library yang dipakai

```
pandas numpy scikit-learn imbalanced-learn matplotlib seaborn
```
