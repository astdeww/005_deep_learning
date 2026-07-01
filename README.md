# DEEP LEARNING
Secara sederhana, Deep Learning adalah salah satu cabang dari Machine Learning (yang merupakan bagian dari Artificial Intelligence) yang meniru cara kerja jaringan saraf di otak manusia untuk mempelajari pola dari data dalam jumlah besar.

Kata "Deep" (Mendalam) merujuk pada banyaknya lapisan (hidden layers) yang menyusun jaringan saraf tiruan (Artificial Neural Network) tersebut. Jika Machine Learning tradisional biasanya hanya memiliki sedikit lapisan, Deep Learning bisa memiliki puluhan, ratusan, bahkan ribuan lapisan untuk memproses informasi yang sangat kompleks.

---

<b>Bagaimana Cara Kerjanya? (Analogi Sederhana)</b>
Bayangkan bagaimana proses otak kita ketika belajar mengenali objek, misalnya sebuah Mobil:
1. Lapisan Input: Mata menerima data mentah berupa piksel visual dari gambar mobil.
2. Lapisan Tersembunyi Awal (Hidden Layers): Jaringan mulai mendeteksi pola paling dasar, seperti garis horizontal, vertikal, dan sudut-sudut tajam.
3. Lapisan Tersembunyi Lebih Dalam: Pola dasar tadi digabungkan untuk mengenali bentuk yang lebih kompleks, seperti bentuk lingkaran (roda), persegi panjang (pintu), atau kaca depan.
4. Lapisan Output: Semua informasi digabungkan untuk menghasilkan keputusan akhir: "Ini adalah mobil."

Hebatnya, dalam Deep Learning, proses pencarian dan pengenalan ciri-ciri (fitur) ini terjadi secara otomatis. Kita tidak perlu mendefinisikan satu per satu kepada komputer bentuk roda atau pintu itu seperti apa.

---

<b>Perbedaan Utama: Machine Learning vs. Deep Learning</b>
- <b>Machine Learning</b> Tradisional: Membutuhkan intervensi manusia untuk memilih ciri data secara manual (feature engineering). Jika ingin mendeteksi penipuan transaksi, manusia harus menentukan indikatornya dulu (misal: lokasi transaksi, jam transaksi).

- <b>Deep Learning</b>: Data mentah langsung dimasukkan ke dalam model, dan biarkan algoritma yang bekerja sendiri untuk menemukan hubungan atau pola tersembunyi yang bahkan mungkin terlewat oleh logika manusia.

--- 

<b>Mengapa Deep Learning Sangat Powerful Saat Ini?</b>
- <b>Skalabilitas Data</b>: Model Machine Learning tradisional punya batas optimal; setelah mencapai titik tertentu, performanya tidak akan meningkat walau diberi tambahan data. Sebaliknya, performa Deep Learning justru terus meroket seiring semakin banyaknya data (Big Data) yang diberikan.

- <b>Dukungan Komputasi Modern</b>: Proses Deep Learning melibatkan miliaran operasi matematika (perkalian matriks). Perkembangan hardware seperti GPU dan TPU membuat pelatihan model raksasa ini bisa diselesaikan dalam hitungan hari atau jam, bukan lagi tahun.

Teknologi inilah yang menjadi otak di balik deteksi wajah di HP, sistem mobil otonom (self-driving cars), pengenalan suara (seperti Siri atau Google Assistant), hingga model bahasa besar (LLM) yang kita gunakan saat ini.

---

Berdasarkan tinjauan komprehensif dalam jurnal ilmiah oleh [A Comprehensive Overview and Comparative Analysis on Deep Learning Models](https://arxiv.org/pdf/2305.17473), metode atau arsitektur di dalam Deep Learning (DL) dikelompokkan menjadi beberapa kategori utama berdasarkan fungsi dan paradigma pembelajarannya.

Berikut adalah rincian metode-metode DL yang dibahas di dalam jurnal tersebut:

## 1. Model Terawasi (Supervised Deep Learning Models)
Model dalam kategori ini digunakan untuk fungsi <b> diskriminatif atau klasifikasi </b> pola dengan memanfaatkan data yang memiliki label.

- <b>Multi-Layer Perceptron (MLP)</b>: Arsitektur feedforward dasar yang sepenuhnya terhubung (fully connected), menjadi fondasi dari jaringan saraf tiruan yang lebih dalam.

- <b>Convolutional Neural Network (CNN)</b>: Sangat unggul dalam mengekstrak fitur spasial secara otomatis. Metode ini sangat populer untuk pengolahan <b>gambar dan video</b>. Beberapa varian terkenalnya meliputi VGG, Inception, ResNet, Xception, MobileNet, DenseNet, dan NASNet.

- <b>Recurrent Neural Network (RNN)</b>: Dirancang untuk menangani <b>data sekuensial atau deret waktu (time-series)</b> karena memiliki memori internal untuk mengingat urutan data. Varian lanjutannya meliputi:
    - Long Short-Term Memory (LSTM) & Bidirectional LSTM.
    - Gated Recurrent Unit (GRU) & Bidirectional GRU.

- <b>Temporal Convolutional Network (TCN)</b>: Modifikasi dari CNN 1-Dimensi yang menggunakan konvolusi kausal (causal) dan terdilasi (dilated) sehingga mampu menangani dependensi data jangka panjang pada time-series secara lebih efisien daripada RNN tradisional.

- <b>Kolmogorov-Arnold Network (KAN)</b>: Arsitektur mutakhir (rilis tahun 2024) yang menempatkan fungsi aktivasi non-linear yang dapat dipelajari (spline) langsung pada edge (bobot), bukan pada node (neuron). Variannya meliputi CKAN (untuk konvolusi) dan TKAN (untuk temporal/sekuensial). 


## 2. Model Generatif / Tidak Terawasi (Generative / Unsupervised Models)
Model ini dilatih menggunakan data tanpa label untuk menemukan pola tersembunyi atau menghasilkan sampel data baru yang mirip dengan distribusi data asli.

- Autoencoder (AE): Jaringan yang melatih fungsi encoder (untuk kompresi data ke ruang laten) dan decoder (untuk rekonstruksi data kembali ke bentuk asli). Variannya meliputi Sparse AE, Denoising AE, dan Variational Autoencoder (VAE).

- Generative Adversarial Network (GAN): Sistem dua jaringan (Generator dan Discriminator) yang saling bertarung secara adversarial untuk menghasilkan data sintetis yang sangat realistis (misalnya gambar wajah manusia buatan). Variannya meliputi WGAN, CycleGAN, dan StyleGAN.

- Deep Belief Network (DBN): Model generatif yang tersusun dari tumpukan Restricted Boltzmann Machines (RBM) yang dilatih lapis demi lapis (layer-by-layer).

## 3. Arsitektur Transformer
Model yang menggantikan mekanisme sekuensial RNN dengan mekanisme fokus penuh bernama self-attention. Transformer memungkinkan pelatihan data dilakukan secara paralel sehingga jauh lebih cepat dan efisien.
    - Varian NLP: BERT, GPT, Transformer-XL, dan XLNet.
    - Varian Computer Vision: Vision Transformer (ViT), Swin Transformer, dan Transformer in Transformer (TNT).

## 4. Deep Reinforcement Learning (DRL)
Metode yang menggabungkan kemampuan persepsi Deep Learning dengan prinsip Reinforcement Learning (pengambilan keputusan berbasis agen). Agen belajar secara mandiri melalui trial and error untuk memaksimalkan reward dari lingkungan. Contoh modelnya adalah Deep Q-learning Network (DQN), Double DQN, dan Dueling DQN.

## 5. Deep Transfer Learning (DTL)
Metode memindahkan pengetahuan atau bobot (weights) yang sudah dipelajari oleh suatu model dari satu tugas besar (seperti model yang dilatih menggunakan jutaan gambar di ImageNet) ke tugas baru yang kekurangan data latih. Pendekatan ini bisa berbasis instans, pemetaan (mapping), jaringan (network-based seperti teknik freezing dan fine-tuning), atau adversarial.

## 6. Model Hibrida (Hybrid Deep Learning Models)
Metode yang menggabungkan beberapa arsitektur dasar untuk saling melengkapi kelemahan masing-masing. Kombinasi yang paling sering digunakan di industri meliputi:
    - CNN + LSTM / CNN + GRU: Menggabungkan CNN untuk ekstraksi fitur spasial dan RNN untuk fitur temporal (sangat umum digunakan pada video atau sensor pintar).
    - Autoencoder + GAN / AE + CNN: Menggabungkan kekuatan model generatif dan supervised untuk augmentasi data atau meningkatkan ketahanan model.


