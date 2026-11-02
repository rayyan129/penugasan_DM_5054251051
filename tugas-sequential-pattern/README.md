# Tugas 5 - Sequential Pattern Analysis

Dataset *Online Retail* dari UCI Machine Learning Repository
(https://archive.ics.uci.edu/dataset/352/online+retail), file `Online Retail.xlsx`,
541.909 baris dan 8 kolom. Isinya transaksi toko ritel online di Inggris dari
Desember 2010 sampai Desember 2011.

Dataset tidak diunggah ke repo. Untuk menjalankan notebook, taruh `Online Retail.xlsx`
di folder `archive/` pada root repo (notebook membaca `../archive/Online Retail.xlsx`).

Tahapan yang dikerjakan: membersihkan data (Description kosong, invoice batal,
Quantity <= 0, CustomerID kosong, kode non-produk), menyusun satu sequence per pelanggan
berisi itemset per invoice yang urut waktu, lalu menjalankan PrefixSpan (diimplementasikan
sendiri agar mendukung itemset) dan mengevaluasi pola dengan support, confidence, dan lift.

## Isi folder

| File | Keterangan |
|---|---|
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Sequential_Pattern.ipynb` | notebook analisis + laporan |
| `5054251051_Rayyan_Muhtar_Ali_Tugas_Sequential_Pattern.pdf` | versi PDF dari notebook |

## Ringkasan hasil

Data bersih: 396.337 baris, 18.402 invoice, 4.334 pelanggan (sequence).

| min_support | Jumlah pola |
|---|---|
| 0,05 | 305 |
| 0,03 | 1.256 |
| **0,02 (dipakai)** | **5.170** |
| 0,015 | 16.675 |
| 0,01 | 142.218 |

Tiga pola berurutan dengan support tertinggi (min_support = 0,02):

| Pola | Support | Confidence | Lift |
|---|---|---|---|
| WHITE HANGING HEART T-LIGHT HOLDER -> WHITE HANGING HEART T-LIGHT HOLDER | 0,093 | 0,473 | 2,40 |
| REGENCY CAKESTAND 3 TIER -> REGENCY CAKESTAND 3 TIER | 0,076 | 0,375 | 1,84 |
| JUMBO BAG RED RETROSPOT -> JUMBO BAG RED RETROSPOT | 0,072 | 0,491 | 3,35 |

## Library yang dipakai

```
pandas numpy matplotlib openpyxl
```
