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
**Tabel atau ringkasan**
Berdasarkan analisis data pendapatan tahunan startup, diperoleh nilai mean sebesar 31,88 miliar IDR, median 31,31 miliar IDR, dan modus 1,87 miliar IDR. Nilai mean dan median yang hampir sama menunjukkan bahwa distribusi data relatif seimbang, sedangkan nilai modus yang rendah mengindikasikan banyak startup dengan pendapatan kecil. Tingkat penyebaran data tergolong tinggi, ditandai dengan standar deviasi dan range yang cukup besar, yang menunjukkan adanya perbedaan pendapatan yang signifikan antar startup. Histogram memperlihatkan distribusi data yang cukup merata dengan garis mean berada di tengah, sehingga dapat disimpulkan bahwa pendapatan tahunan startup memiliki variasi luas namun tidak menunjukkan kemencengan ekstrem

**Interpretasi:**

Nilai mean sebesar 31,88 dan median sebesar 31,31 menunjukkan bahwa data pada kolom numerik memiliki pusat distribusi yang relatif seimbang, karena rata-rata dan nilai tengah hampir sama. Hal ini menandakan bahwa sebaran data tidak condong secara ekstrem ke salah satu sisi. Nilai modus sebesar 1,87 mengindikasikan bahwa nilai tersebut paling sering muncul dalam data, sehingga dapat disimpulkan bahwa cukup banyak observasi dengan nilai rendah. Nilai intercept sebesar 3,57 menunjukkan nilai awal atau konstanta pada model yang digunakan, yang merepresentasikan nilai variabel dependen saat variabel independen bernilai nol. Arah hubungan yang bernilai positif menandakan bahwa peningkatan variabel independen cenderung diikuti oleh peningkatan variabel dependen. Selain itu, p-value sebesar 0 menunjukkan bahwa hasil pengujian statistik sangat signifikan (p < 0,05), sehingga hubungan atau pengaruh yang diuji dalam analisis dapat dinyatakan signifikan secara statistik. Secara keseluruhan, data menunjukkan variasi nilai yang cukup besar dengan kecenderungan hubungan positif dan hasil analisis yang signifikan.

**- Ukuran Sebaran (Standar Deviasi, Range, Kuartil):**
-Tabel atau ringkasan Ukuran Sebaran Data Pendapatan Tahunan (Miliar IDR) Hasil Ukuran Sebaran Berdasarkan analisis pada kolom Pendapatan_Tahunan_Miliar_IDR, diperoleh hasil sebagai berikut: Minimum (Min) = 1,00 Miliar IDR Kuartil 1 (Q1) = 14,31 Miliar IDR Median (Q2) = 31,30 Miliar IDR Mean (Rata-rata) = 31,88 Miliar IDR Kuartil 3 (Q3) = 49,04 Miliar IDR

Maksimum (Max) = 66,89 Miliar IDR Selain itu: Standar Deviasi = 19,79 Miliar IDR Range (Rentang) = 1,00 – 66,89 atau sebesar 65,89 Miliar IDR Interpretasi: Interpretasi Ukuran Sebaran Data Berdasarkan hasil analisis pada kolom Pendapatan_Tahunan_Miliar_IDR, diperoleh nilai standar deviasi sebesar 19,79 miliar IDR, range antara 1,00 hingga 66,89 miliar IDR, serta ringkasan lima angka yang terdiri dari minimum 1,00, Q1 14,31, median 31,30, mean 31,88, Q3 49,04, dan maksimum 66,89.

Nilai range sebesar 65,89 miliar IDR diperoleh dari selisih antara nilai maksimum (66,89 miliar IDR) dan nilai minimum (1,00 miliar IDR). Nilai maksimum 66,89 miliar IDR menunjukkan pendapatan tertinggi yang tercatat dalam data, sedangkan nilai minimum 1,00 miliar IDR merupakan pendapatan terendah. Rentang yang sangat lebar ini menunjukkan bahwa perbedaan pendapatan antar perusahaan dalam dataset sangat besar.

Nilai standar deviasi yang cukup tinggi (19,79 miliar IDR) menandakan bahwa data pendapatan menyebar cukup jauh dari nilai rata-rata (31,88 miliar IDR). Hal ini menunjukkan bahwa pendapatan perusahaan tidak terkonsentrasi di sekitar nilai mean, melainkan tersebar luas baik di bawah maupun di atas rata-rata.

Berdasarkan kuartil, sebanyak 25% data berada di bawah 14,31 miliar IDR, yang menunjukkan kelompok perusahaan dengan pendapatan relatif rendah. Sementara itu, 25% data lainnya berada di atas 49,04 miliar IDR, yang menunjukkan adanya kelompok perusahaan dengan pendapatan tinggi. Nilai median sebesar 31,30 miliar IDR yang hampir sama dengan nilai mean menunjukkan bahwa secara umum pusat data berada di sekitar nilai tersebut, meskipun tetap terdapat penyebaran yang besar.

Kesimpulan Secara keseluruhan, data Pendapatan_Tahunan_Miliar_IDR memiliki tingkat penyebaran yang tinggi. Hal ini ditunjukkan oleh standar deviasi yang besar, range yang sangat lebar, serta perbedaan yang jelas antara kelompok pendapatan rendah dan tinggi berdasarkan kuartil. Data tidak terpusat pada satu rentang nilai tertentu, melainkan tersebar luas dari pendapatan sangat rendah hingga sangat tinggi. Kondisi ini menunjukkan adanya variasi pendapatan yang signifikan antar perusahaan dalam dataset yang dianalisis.
- **Visualisasi (Histogram/Boxplot):**
![alt text](results/histogram_nama_kolom_numerik.png)
  
  - *Interpretasi:* 
  Interpretasi Diagram / Histogram Pendapatan Tahunan
Histogram Pendapatan_Tahunan_Miliar_IDR menggambarkan sebaran pendapatan tahunan perusahaan dalam dataset, dengan nilai pendapatan berkisar antara 1,00 hingga 66,89 miliar IDR. Sumbu horizontal menunjukkan besarnya pendapatan tahunan, sedangkan sumbu vertikal menunjukkan jumlah perusahaan pada setiap rentang pendapatan.

Berdasarkan diagram, terlihat bahwa data pendapatan tersebar luas dan tidak terpusat pada satu nilai tertentu. Hal ini sejalan dengan nilai range sebesar 65,89 miliar IDR, yang menunjukkan perbedaan pendapatan yang sangat besar antara perusahaan dengan pendapatan terendah (1,00 miliar IDR) dan tertinggi (66,89 miliar IDR). Nilai maksimum 66,89 miliar IDR muncul karena terdapat perusahaan dalam dataset yang memiliki pendapatan paling tinggi dibandingkan perusahaan lainnya, sehingga menjadi batas atas distribusi data.

Garis vertikal putus-putus pada histogram menunjukkan nilai mean sebesar 31,88 miliar IDR, yang berada dekat dengan median sebesar 31,30 miliar IDR. Kedekatan antara mean dan median ini mengindikasikan bahwa pusat distribusi data berada di sekitar nilai tersebut. Namun, penyebaran batang histogram yang lebih panjang ke arah kanan menunjukkan bahwa distribusi data cenderung sedikit miring ke kanan (right-skewed), yang berarti terdapat beberapa perusahaan dengan pendapatan sangat tinggi yang menarik nilai rata-rata ke atas.

Selain itu, jika dikaitkan dengan nilai kuartil, terlihat bahwa:
25% perusahaan memiliki pendapatan di bawah 14,31 miliar IDR (Q1),
50% perusahaan berada di rentang 14,31 hingga 49,04 miliar IDR (Q1–Q3),
dan 25% perusahaan lainnya memiliki pendapatan di atas 49,04 miliar IDR (Q3).

Pola ini memperlihatkan bahwa sebagian besar data berada pada rentang pendapatan menengah, namun tetap terdapat perusahaan dengan pendapatan sangat rendah dan sangat tinggi. Hal ini juga didukung oleh standar deviasi sebesar 19,79 miliar IDR, yang menunjukkan bahwa data pendapatan menyimpang cukup jauh dari nilai rata-ratanya.

Kesimpulan
Berdasarkan histogram dan nilai statistik yang ada, dapat disimpulkan bahwa pendapatan tahunan perusahaan dalam dataset memiliki tingkat variasi yang tinggi, dengan distribusi yang cenderung sedikit miring ke kanan. Meskipun rata-rata dan median berada pada kisaran yang sama, keberadaan perusahaan dengan pendapatan sangat tinggi menyebabkan penyebaran data menjadi luas. Histogram ini memberikan wawasan bahwa kondisi pendapatan perusahaan sangat beragam, sehingga rata-rata saja belum cukup untuk merepresentasikan kondisi setiap perusahaan secara individual.
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
