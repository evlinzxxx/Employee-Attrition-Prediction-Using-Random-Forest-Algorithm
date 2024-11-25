# Submission Kedua: Analisis Data Karyawan

by: Evlin Sitanggang

## Business Understanding

Jaya Jaya Maju adalah perusahaan besar dengan lebih dari 1.000 karyawan di berbagai divisi. Dashboard ini dirancang untuk membantu tim HR memahami kondisi tenaga kerja di perusahaan, menganalisis area yang memerlukan perhatian khusus, serta mendukung pengambilan keputusan strategis. Tujuannya adalah untuk meningkatkan kesejahteraan karyawan sekaligus memastikan kinerja optimal organisasi.

### Permasalahan Bisnis

Perusahaan Jaya Jaya Maju menghadapi tantangan besar dengan tingkat attrition yang tinggi, yang kini melebihi 10%. Hal ini berisiko mengganggu kelancaran operasional serta meningkatkan beban biaya dalam proses rekrutmen dan pelatihan karyawan baru. Untuk mengatasi masalah tersebut, manajer HR perlu memperoleh wawasan mendalam mengenai faktor-faktor yang mempengaruhi keputusan karyawan untuk bertahan atau meninggalkan perusahaan.


### Tujuan Proyek

1. Memberikan insight mendalam terkait profil dan distribusi karyawan di perusahaan.
2. Mengidentifikasi area yang memerlukan perbaikan dalam kesejahteraan dan kinerja karyawan.
3. Menyediakan rekomendasi strategis berdasarkan data untuk mengatasi masalah yang ada.

---
## Persiapan
### Sumber data: https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee

### Setup Environment - Metabase:
1. docker pull metabase/metabase:v0.46.4
2. docker run -p 3000:3000 --name metabase metabase/metabase
3. http://localhost:3000/setup

email : evelinsitanggang@gmail.com pass : Batudewa22_


## Business Dashboard

Dashboard ini menyajikan data utama terkait karyawan perusahaan Jaya Jaya Maju:

### **KPI Utama**
- **Total Karyawan:** 1,058 orang.
- **Rata-rata Gaji Karyawan:** 6,625.95 USD.
- **Rata-rata Masa Kerja:** 11.44 tahun.
- **Rata-rata Tahun di Perusahaan:** 7.07 tahun.

### **Distribusi Karyawan**
1. **Status Karyawan:**
   - 83% aktif, sedangkan 17% sudah tidak aktif.
2. **Gender:**
   - 59% perempuan, 41% laki-laki.
3. **Status Pernikahan:**
   - 44% menikah, 33% single, dan 23% lainnya (cerai/duda/janda).
4. **Departemen:**
   - **Research & Development (R&D):** Departemen dengan jumlah karyawan tertinggi.
   - **Sales dan Human Resources:** Memiliki jumlah karyawan yang relatif lebih sedikit.
5. **Usia Karyawan:**
   - Mayoritas berada di rentang usia **30-40 tahun**, mencerminkan dominasi usia produktif.
6. **Tingkat Pendidikan:**
   - Sebagian besar karyawan berpendidikan Sarjana (Bachelor's Degree).
7. **Kepuasan Lingkungan Kerja:**
   - 314 karyawan merasa "Very High", tetapi ada 200 karyawan yang merasa kurang puas (kategori "Low").
8. **Work-Life Balance:**
   - 638 karyawan berada di kategori "Excellent", tetapi 56 karyawan melaporkan kategori "Outstanding", menunjukkan ruang peningkatan.

---

## Kesimpulan

1. **Pengaruh Level Jabatan:**
   Sebagian besar karyawan yang keluar berasal dari level jabatan rendah, seperti **Sales Executive** dan **Laboratory Technician**, yang memiliki jumlah terbanyak di perusahaan. Level jabatan rendah ini biasanya diikuti oleh gaji yang lebih rendah, yang berkontribusi pada risiko turnover. Rata-rata gaji karyawan perusahaan adalah **6,625.95 USD**, namun sebagian besar karyawan di level jabatan ini memiliki gaji di bawah rata-rata.

2. **Distribusi Usia dan Risiko Turnover:**
   Mayoritas karyawan yang keluar berada pada rentang usia **30–40 tahun**, yaitu usia produktif yang sering kali lebih terbuka terhadap peluang karier baru. Rentang usia ini memerlukan perhatian khusus untuk strategi retensi, seperti program pengembangan karier dan kenaikan gaji berbasis kinerja, guna mengurangi turnover.

3. **Departemen dengan Risiko Tinggi:**
   Departemen **Research & Development**, yang memiliki jumlah karyawan terbanyak, menunjukkan potensi risiko turnover yang tinggi. Beban kerja yang besar, dikombinasikan dengan kemungkinan gaji yang tidak sebanding dengan tanggung jawab, bisa menjadi salah satu alasan turnover di departemen ini. Peninjauan beban kerja dan pemberian insentif tambahan dapat membantu mengurangi risiko ini.

4. **Kepuasan Karyawan:**
   Tingkat kepuasan kerja menunjukkan bahwa mayoritas karyawan memiliki kepuasan yang tinggi hingga sangat tinggi. Namun, terdapat **15% karyawan** dengan penilaian kinerja yang rendah, yang berpotensi keluar jika tidak ada upaya untuk memenuhi kebutuhan mereka. Hal ini menunjukkan pentingnya survei kepuasan karyawan yang lebih mendalam untuk mengidentifikasi area yang perlu diperbaiki.

5. **Pendapatan:**
   Karyawan yang keluar cenderung memiliki gaji di bawah rata-rata perusahaan (**6,625.95 USD**). Distribusi ini menunjukkan bahwa peningkatan struktur gaji, terutama di level jabatan rendah, dapat menjadi langkah penting untuk mengurangi turnover.

---

## Rekomendasi

1. **Meningkatkan Keseimbangan Beban Kerja:**
   - Distribusi kerja antar departemen perlu dievaluasi, terutama antara R&D dan departemen lainnya.
2. **Program Retensi Karyawan Usia Produktif:**
   - Memberikan bonus berbasis kinerja, pelatihan karier, dan rencana jenjang karier untuk menjaga loyalitas karyawan.
3. **Meningkatkan Kepuasan Kerja:**
   - Fokus pada survei kebutuhan karyawan dan pengembangan program kesejahteraan (seperti rekreasi kantor dan fleksibilitas waktu kerja).
4. **Pengembangan Kompetensi Departemen Lain:**
   - Departemen Sales dan HR dapat diberikan pelatihan tambahan untuk meningkatkan kontribusinya dalam pertumbuhan perusahaan.

Dengan langkah-langkah ini, Jaya Jaya Maju dapat mengatasi permasalahan bisnis yang ada dan meningkatkan kinerja serta kesejahteraan karyawan secara menyeluruh.

--- 

## Implementasi Model

Berikut adalah langkah-langkah untuk melakukan prediksi berdasarkan model yang sudah dibuat sebelumnya:

### 1. **Membaca Model yang Sudah Dilatih**
   - **Kode**: 
     ```python
     model = joblib.load('/content/random_forest.joblib')
     ``` 
     Model machine learning yang sudah dilatih sebelumnya (dalam format `.joblib`) dimuat agar dapat digunakan untuk melakukan prediksi.

### 2. **Membaca Dataset**
   - **Kode**: 
     ```python
     data = pd.read_csv('/content/predict.csv')
     ```
     Dataset yang akan diprediksi dibaca dari file CSV menggunakan Pandas.

### 3. **Mengencode Kolom Kategorikal**
   - **Kode**:
     ```python
     for col in categorical_columns:
         if col in data.columns:
             data[col] = label_encoder.fit_transform(data[col])
     ```
     - Kolom-kolom yang berisi data kategorikal (seperti teks) dikonversi menjadi angka menggunakan **`LabelEncoder`**.
     - **Tujuan**: Agar data kategorikal dapat diproses oleh model machine learning.

### 4. **Melakukan Scaling pada Kolom Numerik**
   - **Kode**:
     ```python
     numeric_columns = data.select_dtypes(include=['float64', 'int64']).columns
     data_scaled[numeric_columns] = scaler.fit_transform(data[numeric_columns])
     ```
     - Kolom numerik diambil dari dataset.
     - Nilai pada kolom numerik diskalakan menggunakan **`MinMaxScaler`** untuk memastikan bahwa semua fitur berada dalam rentang 0 hingga 1.
     - **Tujuan**: Mengoptimalkan performa model dengan data yang terstandarisasi.

### 5. **Menghapus Kolom yang Tidak Diperlukan**
   - **Kode**:
     ```python
     if 'Attrition_Prediction' in data_scaled.columns:
         data_scaled = data_scaled.drop(columns=['Attrition_Prediction'])
     ```
     - Jika ada kolom tambahan seperti `Attrition_Prediction`, kolom tersebut dihapus karena tidak digunakan saat model dilatih.

### 6. **Melakukan Prediksi**
   - **Kode**:
     ```python
     predictions = model.predict(data_scaled)
     ```
     - Dataset yang sudah di-encode dan diskalakan digunakan untuk memprediksi hasil dengan model machine learning yang telah dilatih.
     - **Output**: Prediksi berupa angka (1 untuk "Attrition" atau 0 untuk "No Attrition").

### 7. **Menambahkan Kolom Hasil Prediksi**
   - **Kode**:
     ```python
     data['Attrition_Prediction'] = ['Yes' if pred == 1 else 'No' for pred in predictions]
     ```
     - Kolom baru ditambahkan ke dataset asli, menunjukkan hasil prediksi dalam bentuk teks **`Yes`** (Attrition) atau **`No`** (Tidak Attrition).

### 8. **Menampilkan Hasil Prediksi**
   - **Kode**:
     ```python
     result = data[['EmployeeId', 'Attrition_Prediction']]
     print(tabulate(result, headers='keys', tablefmt='fancy_grid'))
     ```
     - Menampilkan hanya **EmployeeId** dan hasil prediksi dalam tabel menggunakan library **`tabulate`**.
     - **Tujuan**: Memberikan tampilan yang mudah dipahami.

   Tabel dibawah ini menunjukkan hasil prediksinya :

   |  | EmployeeId | Attrition_Prediction|
   |--|------------|---------------------|
   |0 |          2 | No                  |
   |1 |          7 | No                  |
   |2 |          8 | No                  |
   |3 |         12 | No                  |
   |4 |        290 | No                  |
   |5 |        409 | Yes                 |
