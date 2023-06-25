# Credit Card Customer Segmentation [ID]

## Latar Belakang

Bank seringkali menghadapi tantangan dalam memahami perilaku penggunaan kartu kredit oleh nasabah mereka. Memahami pola dan kecenderungan penggunaan kartu kredit dapat membantu bank untuk menawarkan produk dan layanan yang lebih tepat sasaran, meningkatkan retensi nasabah, serta mengoptimalkan strategi pemasaran dan penawaran kredit.

Dalam konteks ini, permasalahan yang dihadapi adalah bagaimana melakukan segmentasi pelanggan (customer segmentation) berdasarkan data penggunaan kartu kredit selama 6 bulan terakhir. Segmentasi pelanggan akan membantu bank dalam mengidentifikasi kelompok pelanggan dengan perilaku penggunaan kartu kredit yang serupa. Dengan melakukan segmentasi, bank dapat memahami preferensi dan kebutuhan kelompok pelanggan yang berbeda secara lebih baik, sehingga dapat mengembangkan strategi yang lebih efektif dalam memenuhi kebutuhan mereka.

## Problem Statement
membuat model clustering untuk melakukan segmentasi pelanggan berdasarkan data penggunaan kartu kredit selama 6 bulan terakhir dengan tujuan meningkatkan pemahaman perilaku pelanggan dan efektivitas strategi pemasaran bank.

## Metode yang Digunakan
1. Data Visualization
2. Feature Engineering
3. Unsupervised Machine Learning
    - K-means clustering
    - PCA

## Hasil dan Kesimpulan

Dari eksplorasi data didapatkan:
- Sebaran data seluruh kolom numerik tiddak normal.
- Perbedaan antara mean dan median cukup jauh, hal ini menandakan adanya outlier dan data skewed
- Credit limit dan balance tiap individu paling banyak di kisaran 0 - 5000
- Credit limit paling dipengaruhi oleh balance dan payments berdasarkan plot korelasi

Dari analisis model didapatkan:
- Data direduksi dengan PCA menjadi 12 fitu dari yang sebelumnya 16 fitur. Restensi informasi sebesar 98%.
- Jumlah cluster yang paling baik berdasarkan metode elbow dan sillhouette score adalah 4 dan 5 cluster.
- Dengan 5 cluster didapat nilai sillhouette score yang lebih tinggi.
- dengan 5 cluster dihasilkan clustering dengan karakteristik:
    - Cluster 0: Moderate Spenders (Pengeluar Sedang)
    - Cluster 1: High Balance, Low Purchases (Saldo Tinggi, Pembelian Rendah)
    - Cluster 2: Cash Advance Users (Pengguna Penarikan Tunai)
    - Cluster 3: Active and High Spenders (Pengeluar Aktif dan Tinggi)
    - Cluster 4: Low Balance, Low Activity (Saldo Rendah, Aktivitas Rendah)

Berikut adalah beberapa strategi penawaran produk dan layanan yang dapat dijalankan untuk setiap cluster:

Cluster 0: Moderate Spenders (Pengeluar Sedang)
- Tawarkan program diskon atau penawaran khusus untuk mendorong pembelian lebih banyak.
- Fokus pada pengembangan program loyalitas yang menawarkan insentif bagi pelanggan setia.
- Berikan pilihan pembayaran yang fleksibel, seperti angsuran atau cicilan.

Cluster 1: High Balance, Low Purchases (Saldo Tinggi, Pembelian Rendah)
- Tawarkan produk atau paket premium yang dapat menarik minat pelanggan dengan saldo tinggi.
- Promosikan fitur atau manfaat khusus yang disertai dengan produk atau layanan premium.
- Berikan penghargaan eksklusif atau akses ke acara-acara khusus kepada pelanggan dalam cluster ini.

Cluster 2: Cash Advance Users (Pengguna Penarikan Tunai)
- Tingkatkan kesadaran tentang biaya dan bunga yang terkait dengan penarikan tunai.
- Tawarkan alternatif lain seperti pinjaman pribadi dengan suku bunga yang lebih rendah.
- Sediakan informasi dan sumber daya mengenai manajemen keuangan yang baik untuk membantu pelanggan mengurangi ketergantungan pada penarikan tunai.

Cluster 3: Active and High Spenders (Pengeluar Aktif dan Tinggi)
- Fokus pada pengembangan program loyalitas yang memberikan penghargaan dan keuntungan bagi pelanggan yang aktif.
- Tawarkan produk-produk eksklusif atau langka yang dapat menarik minat pelanggan ini.
- Berikan pelayanan pelanggan yang responsif dan personal untuk meningkatkan kepuasan mereka.

Cluster 4: Low Balance, Low Activity (Saldo Rendah, Aktivitas Rendah)
- Tawarkan produk atau paket yang terjangkau dan sesuai dengan kebutuhan pelanggan.
- Berikan pilihan pembayaran yang fleksibel dan mudah digunakan.
- Lakukan promosi atau diskon khusus untuk mendorong aktivitas pembelian yang lebih tinggi.