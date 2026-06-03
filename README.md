💳 Bank Transaction Fraud Detection: Clustering & Classification
Proyek machine learning end-to-end untuk mendeteksi pola transaksi keuangan mencurigakan menggunakan pendekatan Unsupervised Learning (Clustering) dilanjutkan dengan Supervised Learning (Classification).

📌 Overview
Dataset ini menyajikan perilaku transaksi keuangan dari 2.512 nasabah bank di Amerika Serikat. Proyek ini dibagi menjadi dua tahap utama:

Clustering — Mengelompokkan transaksi berdasarkan kesamaan pola menggunakan K-Means
Classification — Membangun model prediktif untuk mengklasifikasikan transaksi ke dalam cluster yang telah terbentuk


📊 Dataset
AtributDetailSumberDicoding IndonesiaJumlah Sampel2.512 transaksiJumlah Fitur16 fiturTipe DataNumerik & Kategorikal
Fitur Utama:

TransactionAmount — Nilai transaksi
CustomerAge — Usia nasabah
CustomerOccupation — Profesi nasabah
AccountBalance — Saldo akun
TransactionDuration — Durasi transaksi (detik)
LoginAttempts — Jumlah percobaan login
Channel — Kanal transaksi (Online/ATM/Branch)
TransactionType — Jenis transaksi (Credit/Debit)


🛠️ Tech Stack
KategoriLibraryData Manipulationpandas, numpyVisualisasimatplotlib, seabornPreprocessingscikit-learn (LabelEncoder, StandardScaler)Clusteringscikit-learn (KMeans), yellowbrick (KElbowVisualizer)Dimensionality Reductionscikit-learn (PCA)Classificationscikit-learn (DecisionTreeClassifier, RandomForestClassifier, GridSearchCV)Model Savingjoblib

🔄 Alur Proyek
Raw Data
   │
   ▼
Data Cleaning (dropna, drop_duplicates, drop kolom ID/Date)
   │
   ▼
Preprocessing (Encoding, Outlier Handling, Scaling, Binning)
   │
   ▼
K-Means Clustering ──► Elbow Method + Silhouette Score
   │
   ▼
Interpretasi Cluster (Inverse Transform → Analisis Deskriptif)
   │
   ▼
Export Data (data_clustering_inverse.csv)
   │
   ▼
One Hot Encoding + Train-Test Split
   │
   ▼
Model Klasifikasi (Decision Tree, Random Forest, Hyperparameter Tuning)
   │
   ▼
Evaluasi & Simpan Model

📈 Hasil & Evaluasi
Clustering
MetrikNilaiAlgoritmaK-MeansJumlah Cluster Optimal2Silhouette Score0.572Metode Reduksi DimensiPCA (2 Komponen)
Classification
ModelAccuracyPrecisionRecallF1-ScoreDecision Tree100%1.001.001.00Random Forest100%1.001.001.00Random Forest (Tuned)100%1.001.001.00

🔍 Insight Cluster
Cluster 0 — Nasabah Mapan Usia Paruh Baya
FiturNilaiRata-rata Usia45.06 tahunRata-rata SaldoRp 5.142Rata-rata TransaksiRp 255.55Profesi DominanDoctorKelompok UsiaMiddleKanal DominanBranch

💡 Rekomendasi: Tawarkan produk investasi jangka panjang, asuransi jiwa, dan layanan wealth management premium.

Cluster 1 — Nasabah Muda Aktif Bertransaksi
FiturNilaiRata-rata Usia44.33 tahunRata-rata SaldoRp 5.058Rata-rata TransaksiRp 258.15Profesi DominanStudentKelompok UsiaYoungKanal DominanBranch

💡 Rekomendasi: Tawarkan produk tabungan otomatis, program cashback, edukasi keuangan, dan kredit berbunga rendah.


📁 Struktur File
fraud-detection-clustering-classification.zip
├── [Clustering]_Submission_Akhir_BMLP_Listya_Dwi_Subagya.ipynb
├── [Klasifikasi]_Submission_Akhir_BMLP_Listya_Dwi_Subagya.ipynb
├── model_clustering.h5
├── PCA_model_clustering.h5
├── decision_tree_model.h5
├── explore_RandomForest_classification.h5
├── tuning_classification.h5
├── data_clustering.csv
└── data_clustering_inverse.csv

🚀 Cara Menjalankan

Clone repository ini:

bashgit clone https://github.com/ListyaDwiSubagya/fraud-detection-clustering-classification.git

Buka notebook di Google Colab atau Jupyter Notebook
Jalankan notebook Clustering terlebih dahulu, lalu notebook Klasifikasi
Pastikan semua library sudah terinstall:

bashpip install pandas numpy matplotlib seaborn scikit-learn yellowbrick joblib

🏆 Pencapaian

✅ Lulus submission Dicoding Indonesia — Belajar Machine Learning untuk Pemula (BMLP)
✅ Menerapkan kriteria Advanced pada seluruh kriteria penilaian
✅ Silhouette Score: 0.572 (Clustering berkualitas baik)
✅ Akurasi Klasifikasi: 100%


👤 Author
Listya Dwi Subagya

📝 License
Proyek ini dibuat untuk keperluan edukasi dalam program Belajar Machine Learning untuk Pemula oleh Dicoding Indonesia.
