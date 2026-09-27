# Tugas 2 - Praproses Data

Dataset *House Prices - Advanced Regression Techniques* dari Kaggle
(https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data),
file `train.csv`, 1460 baris dan 81 kolom.

Tahapan yang dikerjakan: pembersihan nilai hilang, pemeriksaan konsistensi, penanganan
outlier, transformasi (log, standarisasi, one-hot encoding), lalu reduksi dimensi lewat
analisis korelasi dan PCA.

## Isi folder

| File | Keterangan |
|---|---|
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Praproses_Data.ipynb` | notebook praproses + laporan |
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Praproses_Data.pdf` | versi PDF dari notebook |
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Praproses_Data.csv` | dataset akhir hasil praproses (1458 baris, 255 kolom) |
| `train.csv` | data mentah dari Kaggle (1460 baris, 81 kolom) |

## Ringkasan hasil

| | Sebelum | Sesudah |
|---|---|---|
| Baris | 1460 | 1458 |
| Kolom | 81 | 255 |
| Sel kosong | 6965 | 0 |
| Kolom kategorikal | 43 | 0 (jadi 222 kolom dummy) |

## Library yang dipakai

```
pandas numpy scikit-learn matplotlib seaborn
```
