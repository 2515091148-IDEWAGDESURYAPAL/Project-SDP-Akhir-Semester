# Tugas Analisis Statistik: Deskriptif, Korelasi, dan Regresi

## 1. Informasi Penyusun

- **Nama:** `[I DEWA GDE SURYA PALGUNA]`
- **NIM:** `[2515091148]`
- **Program Studi:** `[SISTEM INFORMASI]`
- **Mata Kuliah:** Statistika dan Probabilitas

---

## 2. Deskripsi Proyek

Pada bagian ini, jelaskan secara singkat dataset yang Anda gunakan. Apa saja variabel di dalamnya? Apa tujuan dari analisis yang Anda lakukan?

*Contoh:*
> Dataset yang digunakan adalah data `...` yang berisi informasi tentang `...`. Variabel kunci dalam dataset ini meliputi `variabel_A`, `variabel_B`, dan `variabel_C`. Tujuan dari proyek ini adalah untuk memahami karakteristik data melalui statistik deskriptif, menguji hubungan antara `variabel_A` dan `variabel_B` melalui analisis korelasi, serta memprediksi `variabel_C` menggunakan `variabel_A` sebagai prediktor melalui analisis regresi.

---

## 3. Struktur Proyek

Proyek ini diorganisir ke dalam beberapa folder:
- `/data`: Berisi dataset mentah yang digunakan untuk analisis.
- `/scripts`: Berisi semua skrip R yang digunakan dalam analisis, diurutkan berdasarkan alur kerja.
- `/results`: Berisi output dari analisis, seperti plot, gambar, atau tabel ringkasan.

---

## 4. Cara Menjalankan Analisis

Untuk mereproduksi hasil analisis ini, ikuti langkah-langkah berikut:
1. Pastikan Anda memiliki R dan RStudio terinstal.
2. Buka proyek R ini di RStudio.
3. Instal paket yang diperlukan dengan menjalankan perintah berikut di konsol R:
   ```R
   # install.packages(c("tidyverse", "corrplot", "knitr"))
   ```
4. Jalankan skrip di dalam folder `/scripts` secara berurutan, mulai dari `01_data_preparation.R` hingga `05_analisis_regresi.R`.

---

## 5. Hasil dan Interpretasi

Di bagian ini, mahasiswa diharapkan untuk menyajikan dan menginterpretasikan hasil dari setiap tahap analisis.

### 5.1. Statistik Deskriptif
- **Ukuran Pemusatan (Mean, Median, Modus):**
  - *Tabel atau ringkasan...*
  - Berdasarkan analisis data pendapatan tahunan startup, diperoleh nilai mean sebesar 31,88 miliar IDR, median 31,31 miliar IDR, dan modus 1,87 miliar IDR. Nilai mean dan median yang hampir sama menunjukkan bahwa distribusi data relatif seimbang, sedangkan nilai modus yang rendah mengindikasikan banyak startup dengan pendapatan kecil. Tingkat penyebaran data tergolong tinggi, ditandai dengan standar deviasi dan range yang cukup besar, yang menunjukkan adanya perbedaan pendapatan yang signifikan antar startup. Histogram memperlihatkan distribusi data yang cukup merata dengan garis mean berada di tengah, sehingga dapat disimpulkan bahwa pendapatan tahunan startup memiliki variasi luas namun tidak menunjukkan kemencengan ekstrem
  - *Interpretasi:*
  - Nilai mean sebesar 31,88 dan median sebesar 31,31 menunjukkan bahwa data pada kolom numerik memiliki pusat distribusi yang relatif seimbang, karena rata-rata dan nilai tengah hampir sama. Hal ini menandakan bahwa sebaran data tidak condong secara ekstrem ke salah satu sisi. Nilai modus sebesar 1,87 mengindikasikan bahwa nilai tersebut paling sering muncul dalam data, sehingga dapat disimpulkan bahwa cukup banyak observasi dengan nilai rendah.
Nilai intercept sebesar 3,57 menunjukkan nilai awal atau konstanta pada model yang digunakan, yang merepresentasikan nilai variabel dependen saat variabel independen bernilai nol. Arah hubungan yang bernilai positif menandakan bahwa peningkatan variabel independen cenderung diikuti oleh peningkatan variabel dependen.
Selain itu, p-value sebesar 0 menunjukkan bahwa hasil pengujian statistik sangat signifikan (p < 0,05), sehingga hubungan atau pengaruh yang diuji dalam analisis dapat dinyatakan signifikan secara statistik. Secara keseluruhan, data menunjukkan variasi nilai yang cukup besar dengan kecenderungan hubungan positif dan hasil analisis yang signifikan.

- Interpretasi Ukuran Sebaran Data
Pendapatan Tahunan (Miliar IDR)
Ringkasan Ukuran Sebaran:
Range (Rentang): 1.00 - 66.89 Miliar IDR
Standar Deviasi: 19.79 Miliar IDR
Ringkasan 5 Angka:
Minimum: 1.00 Miliar IDR
Kuartil 1 (Q1): 14.31 Miliar IDR
Median (Q2): 31.30 Miliar IDR
Kuartil 3 (Q3): 49.04 Miliar IDR
Maksimum: 66.89 Miliar IDR
Rata-rata (Mean): 31.88 Miliar IDR
Interpretasi:

Rentang Data (Range): Data pendapatan tahunan memiliki rentang yang sangat lebar, mulai dari 1.00 Miliar IDR hingga 66.89 Miliar IDR. Rentang sebesar 65.89 Miliar IDR menunjukkan variasi yang ekstrem dalam pendapatan perusahaan-perusahaan dalam dataset.

Standar Deviasi: Standar deviasi sebesar 19.79 Miliar IDR mengindikasikan tingkat penyebaran data yang tinggi. Nilai ini menunjukkan bahwa pendapatan tahunan perusahaan-perusahaan dalam sampel cenderung menyebar cukup jauh dari nilai rata-rata (31.88 Miliar IDR).

Analisis Berdasarkan Kuartil:

50% data terkonsentrasi di tengah: Data antara Q1 (14.31) dan Q3 (49.04) mencakup 50% observasi tengah, dengan rentang 34.73 Miliar IDR.
Distribusi tidak simetris: Jarak antara Q1-Median (17.0) lebih kecil dari jarak Median-Q3 (17.74), menunjukkan distribusi yang sedikit miring ke kanan (right-skewed).
25% data dengan pendapatan rendah: Seperempat perusahaan memiliki pendapatan di bawah 14.31 Miliar IDR.
25% data dengan pendapatan tinggi: Seperempat perusahaan memiliki pendapatan di atas 49.04 Miliar IDR.
Implikasi Bisnis:
Heterogenitas tinggi: Industri menunjukkan tingkat ketidaksetaraan pendapatan yang signifikan antar perusahaan.
Segmentasi jelas: Terdapat perbedaan mencolok antara perusahaan dengan pendapatan rendah (di bawah 14.31 Miliar IDR) dan perusahaan dengan pendapatan tinggi (di atas 49.04 Miliar IDR).
Risiko dalam estimasi: Standar deviasi yang besar menunjukkan bahwa menggunakan rata-rata sebagai estimasi untuk perusahaan individual bisa sangat tidak akurat.
Kesimpulan: Data pendapatan tahunan menunjukkan variasi yang sangat tinggi dengan distribusi yang cenderung miring ke kanan. Sebagian besar perusahaan memiliki pendapatan relatif rendah, namun terdapat beberapa perusahaan dengan pendapatan sangat tinggi yang menarik rata-rata keseluruhan ke atas.
- **Visualisasi (Histogram/Boxplot):**
[Histogram Pendapatan Tahunan](results/histogram_nama_kolom_numerik.png)
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* 
  .Histogram menunjukkan distribusi Pendapatan_Tahunan_Miliar_IDR dengan sumbu horizontal sebagai nilai pendapatan dan sumbu vertikal sebagai frekuensi kemunculan data. Batang-batang histogram memperlihatkan bahwa data pendapatan tersebar cukup luas, mulai dari nilai rendah hingga nilai tinggi. Garis merah putus-putus pada grafik menandai nilai mean sebesar 31,88 miliar IDR, yang berada di sekitar bagian tengah distribusi.

Bentuk histogram memperlihatkan bahwa data tidak terkonsentrasi pada satu rentang nilai tertentu, melainkan tersebar relatif merata di berbagai tingkat pendapatan. Tidak tampak kemencengan (skewness) yang ekstrem ke kiri maupun ke kanan, sehingga distribusi dapat dikatakan cukup seimbang. Meskipun demikian, terlihat adanya sejumlah data pada pendapatan rendah maupun tinggi, yang menunjukkan variasi pendapatan yang besar antar startup.

Secara keseluruhan, histogram ini memberikan gambaran bahwa pendapatan tahunan startup memiliki sebaran yang luas, dengan rata-rata pendapatan berada di tengah distribusi dan tanpa dominasi nilai ekstrem yang berlebihan.

### 5.2. Uji Normalitas
- **Hasil Uji Shapiro-Wilk:**
  - *Nilai p-value...*
  - *Interpretasi:* Apakah data Anda terdistribusi normal berdasarkan hasil uji? Apa implikasinya?
- **Plot Q-Q:**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Apakah titik-titik data mengikuti garis lurus? Apa artinya?

### 5.3. Analisis Korelasi
- **Nilai Koefisien Korelasi:**
  - *Nilai r...*
  - *Interpretasi:* Seberapa kuat dan apa arah hubungan antara dua variabel yang Anda uji? (misalnya, korelasi positif kuat, negatif lemah, atau tidak ada korelasi).
- **Visualisasi (Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Apakah pola pada scatter plot mendukung hasil koefisien korelasi?

### 5.4. Analisis Regresi
- **Model Regresi:**
  - *Persamaan regresi: Y = b0 + b1*X*
  - *Interpretasi:* Jelaskan arti dari koefisien intercept (b0) dan slope (b1) dalam konteks data Anda.
- **Evaluasi Model (R-squared):**
  - *Nilai R-squared...*
  - *Interpretasi:* Berapa persen variasi dari variabel dependen yang dapat dijelaskan oleh model regresi Anda?
- **Visualisasi (Garis Regresi pada Scatter Plot):**
  - *Sematkan gambar plot dari folder /results...*
  - *Interpretasi:* Jelaskan bagaimana garis regresi merepresentasikan hubungan antara variabel.

---

## 6. Kesimpulan

Rangkum temuan utama dari analisis Anda dalam beberapa kalimat. Apa wawasan paling penting yang Anda peroleh?
