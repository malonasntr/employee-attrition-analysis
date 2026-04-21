# Proyek Akhir: Analisis dan Prediksi Attrition Karyawan pada Perusahaan Jaya Jaya Maju

## Business Understanding
Jaya Jaya Maju merupakan perusahaan multinasional yang telah berdiri sejak tahun 2000 dengan jumlah karyawan lebih dari 1000 orang. Dalam beberapa tahun terakhir, perusahaan menghadapi tantangan serius berupa tingginya tingkat attrition (karyawan keluar) yang telah melampaui angka 10%. Tingginya attrition rate ini berpotensi menimbulkan berbagai dampak negatif seperti:
1. Meningkatnya biaya rekrutmen dan training
2. Terganggunya stabilitas operasional
3. Menurunnya produktivitas tim.
   
Oleh karena itu, perusahaan membutuhkan pendekatan berbasis data untuk memahami penyebab utama attrition dan merancang strategi retensi yang lebih efektif.
### Permasalahan Bisnis
1. Apa saja faktor utama yang paling berpengaruh terhadap keputusan karyawan untuk resign dari perusahaan?
2. Bagaimana cara memantau profil karyawan serta metrik yang memengaruhi tingkat attrition secara real-time dan interaktif?
   
### Cakupan Proyek
Proyek ini mencakup beberapa tahapan utama:
1. Data Preparation & Cleaning :
    > Menangani missing values, dan melakukan encoding pada variabel kategorikal menggunakan one-hot encoding agar siap digunakan untuk analisis dan pemodelan.
3. Exploratory Data Analysis (EDA) :
    > - Menganalisis distribusi data
    > - Identifikasi pola attrition berdasarkan: usia, pengalaman kerja, overtime, jarak rumah, kepuasan kerja
3. Business Dashboard : Membangun dashboard interaktif menggunakan Looker Studio
    > - Menampilkan metrik utama: Total Employee, Total Attrition, dan Attrition Rate (%)
    > - Visualisasi faktor-faktor utama penyebab attrition
4. Machine Learning Modeling :
    > Membangun model prediktif menggunakan algoritma Random Forest untuk memprediksi kemungkinan karyawan resign dan mengidentifikasi faktor paling berpengaruh (feature importance)
6. Evaluasi Model :
    > Accuracy, Confusion Matrix, Classification Report (Precision, Recall, F1-score)

### Persiapan
Sumber data: https://github.com/dicodingacademy/dicoding_dataset/tree/main/employee

Setup environment:
```
pandas==2.2.2
scikit-learn==1.6.1
```
## Business Dashboard
Business Dashboard telah dirancang menggunakan Looker Studio untuk memberikan gambaran secara menyeluruh kepada tim HR mengenai demografi karyawan dan faktor risiko attrition.

Dashboard ini terdiri dari dua tampilan utama (dapat disaring berdasarkan status Attrition 1/0):
- Overview Metrik Utama:
    > Menampilkan Total Karyawan, Total Resign, dan persentase Attrition Rate.
- Analisis Demografi:
    > Menyoroti kelompok usia karyawan yang paling rentan resign (Karier Awal 26-35 tahun menjadi kelompok rentan) dan tingkat pengalaman (Entry Level dan Early Career).
- Analisis Faktor Kerja:
    >  Visualisasi pie chart menunjukkan dampak signifikan dari rutinitas lembur (OverTime) terhadap attrition
    > Grafik batang mengilustrasikan distribusi attrition berdasarkan Jarak dari Rumah, tingkat Kepuasan Lingkungan Kerja, dan Departemen (R&D memimpin angka resign tertinggi).

Link untuk mengakses dashboard: https://datastudio.google.com/reporting/7ebea1d0-9ee8-4452-b2a1-585fa8dcb85a

## Conclusion
Berdasarkan hasil pemodelan Random Forest (akurasi 87,74%) dan analisis dashboard, terdapat lima faktor utama yang memengaruhi tingginya attrition rate di Jaya Jaya Maju:
1. Faktor Finansial (Paling Dominan)
    > Variabel seperti MonthlyIncome dan DailyRate menjadi faktor utama. Karyawan dengan kompensasi yang kurang kompetitif cenderung lebih mudah keluar.
2. Usia dan Pengalaman Kerja
    > Karyawan usia 26–35 tahun (karier awal) dengan pengalaman kerja yang masih rendah (TotalWorkingYears kecil) memiliki tingkat attrition lebih tinggi dibandingkan karyawan senior.
3. Beban Kerja (OverTime)
    > Karyawan yang sering lembur (OverTime) lebih rentan resign, yang menunjukkan adanya masalah pada keseimbangan kerja dan kehidupan (work-life balance).
4. Jarak Tempat Tinggal
    > Semakin jauh jarak rumah ke kantor (DistanceFromHome), semakin besar kemungkinan karyawan untuk mencari pekerjaan lain.
5. Kepuasan Lingkungan Kerja
    > Tingkat kepuasan kerja (EnvironmentSatisfaction) yang rendah berkaitan dengan meningkatnya risiko karyawan keluar.

### Rekomendasi Action Items (Optional)
Untuk menurunkan attrition rate, tim HR Jaya Jaya Maju dapat melakukan langkah-langkah berikut:
- Evaluasi dan Penyesuaian Gaji :
    >  Lakukan salary benchmarking, terutama untuk karyawan level entry hingga early career di departemen dengan attrition tinggi. Pastikan kompensasi kompetitif agar karyawan tidak mudah berpindah.
- Pengelolaan Lembur dan Beban Kerja :
    >   Kurangi frekuensi lembur berlebih. Jika tidak bisa dihindari, berikan kompensasi yang adil atau tambahan cuti untuk menjaga work-life balance.
- Program Retensi Karyawan Muda :
    >  Sediakan program mentorship dan jalur karier yang jelas bagi karyawan usia 26–35 tahun agar mereka merasa memiliki peluang berkembang di perusahaan.
- Fleksibilitas Kerja dan Transportasi :
    >  Terapkan kebijakan hybrid/WFH atau berikan subsidi transportasi bagi karyawan dengan jarak tempat tinggal yang jauh.
- Peningkatan Lingkungan Kerja :
    >  Lakukan survei kepuasan karyawan secara rutin dan tindak lanjuti hasilnya untuk meningkatkan kenyamanan dan engagement kerja.
