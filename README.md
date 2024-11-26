##**Business Understanding**##

Konteks
<br><br>
Bukalapak merupakan salah satu perusahaan perdagangan elektronik Indonesia. Perusahaan ini didirikan pada 2010 oleh Achmad Zaky, Nugroho Herucahyono, dan Muhamad Fajrin Rasyid sebagai lokapasar untuk memfasilitasi para pelaku Usaha Kecil dan Menengah (UKM). Kini, Bukalapak berkembang menjadi platform all commerce dengan ekspansi ke lini bisnis online to offline (O2O), business to business (B2B), finansial, dan logistik.  
<br><br>
Meskipun Bukalapak mengalami pertumbuhan pengguna, perusahaan menghadapi tantangan dalam mempertahankan pelanggan yang sudah ada. Tingkat churn (pelanggan yang berhenti menggunakan platform) meningkat dalam beberapa bulan terakhir, menjadi perhatian serius bagi tim manajemen. Situasi ini serupa dengan yang dialami oleh banyak platform e-commerce lainnya di pasar yang sangat kompetitif, di mana pelanggan memiliki banyak pilihan dan dapat dengan mudah beralih ke platform lain.  
<br><br>
Untuk mengatasi masalah ini, Bukalapak berencana mengembangkan model prediksi churn yang dapat mengidentifikasi pelanggan dengan risiko tinggi untuk meninggalkan platform. Pendekatan ini didasarkan pada praktik terbaik dalam industri e-commerce, di mana analitik prediktif telah terbukti efektif dalam meningkatkan retensi pelanggan.  
<br><br>
Rumusan Masalah
<br><br>
Masalah utama terletak pada ketidakmampuan Bukalapak untuk membedakan antara pelanggan yang berpotensi churn dan pelanggan yang loyal. Akibatnya, promosi diberikan secara sembarangan, baik kepada pelanggan yang kemungkinan besar akan meninggalkan platform (churn) maupun kepada pelanggan yang sudah memiliki tingkat loyalitas yang tinggi. Hal ini tidak hanya menyebabkan pemborosan sumber daya pada pelanggan yang sebenarnya tidak memerlukan insentif tambahan, tetapi juga mengurangi efektivitas upaya retensi terhadap pelanggan yang berisiko churn.
<br><br>
Tujuan
<br><br>
Untuk mengatasi masalah ini, Bukalapak perlu mengembangkan strategi yang lebih terarah dalam menawarkan promosi. Dengan mengidentifikasi pelanggan yang memiliki risiko tinggi untuk churn, perusahaan dapat mengalokasikan sumber daya pemasaran dengan lebih efektif, meningkatkan retensi pelanggan, dan pada akhirnya mengoptimalkan anggaran promosi.
<br><br>
Pendekatan Analitik
<br><br>
Pendekatan analitik penulis berfokus pada pengembangan model prediktif untuk mengidentifikasi pelanggan e-commerce yang berisiko churn. Kami akan menganalisis data historis pelanggan, melakukan rekayasa fitur, dan menguji berbagai algoritma machine learning. Model ini akan dioptimalkan untuk memaksimalkan recall, memastikan deteksi dini pelanggan yang berisiko. Hasilnya adalah sistem prediksi yang memungkinkan tim retensi pelanggan untuk mengambil tindakan proaktif, dengan tujuan utama mengurangi churn dan meningkatkan loyalitas pelanggan.
<br><br>
Metrik Evaluasi
<br><br>
![gambar](https://github.com/user-attachments/assets/3ec35df9-a23e-474b-a39a-897e1379badc)

Kondisi:  
<br><br>
1. True Positive: Churn pelanggan terjadi, artinya pelanggan berhenti menggunakan layanan Bukalapak atau tidak melakukan pembelian dalam 30-90 hari terakhir atau lebih.  
2. False Positive (Kesalahan Tipe I)**: Pelanggan diprediksi akan churn tetapi sebenarnya tidak.  
   Konsekuensi: Promosi diberikan secara tidak perlu kepada pelanggan, yang menyebabkan pemborosan anggaran bagi Bukalapak.  
3. True Negative: Pelanggan tidak churn, artinya mereka terus menggunakan layanan Bukalapak atau melakukan pembelian dalam 30-90 hari terakhir atau lebih.  
4. False Negative (Kesalahan Tipe II): Pelanggan diprediksi tidak akan churn tetapi sebenarnya churn.  
   Konsekuensi: Risiko kehilangan banyak pelanggan yang meninggalkan layanan Bukalapak, dan anggaran yang dialokasikan untuk promosi bagi pelanggan yang berpotensi churn tidak dimanfaatkan secara optimal.  
Referensi: https://www.omnisend.com/blog/ecommerce-churn/
<br><br>
Alasan Pemilihan Skor F2 Sebagai Metrik Evaluasi  
<br><br>
Skor F2 dipilih sebagai metrik evaluasi utama untuk model prediksi churn pelanggan karena menekankan *recall* dibandingkan *precision*. Dalam kasus prediksi churn, fokus utamanya adalah mengidentifikasi sebanyak mungkin pelanggan yang berpotensi churn (*true positives*), meskipun ada risiko *false positives*.  
<br><br>
Alasan utama:
<br><br>
1 Biaya kehilangan pelanggan (false negative) jauh lebih tinggi daripada biaya intervensi yang tidak perlu (*false positive*). Kehilangan pelanggan secara signifikan memengaruhi pendapatan jangka panjang perusahaan e-commerce.  
2 Dengan mengidentifikasi lebih banyak pelanggan yang berisiko churn, tim retensi dapat mengambil tindakan pencegahan lebih awal dan lebih menyeluruh, yang berpotensi menyelamatkan lebih banyak pelanggan.  
3 Meskipun terdapat risiko *false positives*, tindakan retensi seperti promosi atau perbaikan layanan umumnya tidak merugikan pelanggan yang sebenarnya loyal.  
4 Skor F2 memberikan bobot lebih besar pada *recall* (2x) dibandingkan *precision*, mencerminkan prioritas bisnis untuk secara agresif mengurangi churn.  
<br><br>
Dengan mengoptimalkan skor F2, model ini diharapkan dapat mengidentifikasi mayoritas pelanggan yang berisiko churn, memungkinkan intervensi tepat waktu dan efektif untuk mempertahankan basis pelanggan e-commerce.
<br><br>
Untuk penjelasan lebih lanjut dari model e-commerce churn dapat dilihat pada file notebook JSON yang terlampir. 
