# UAP MACHINE LEARNING CNN and FLASK Deployment

Penelitian ini telah dilakukan di bidang pemrosesan gambar, yang merupakan salah satu bidang dari kecerdasan buatan. Dalam tugas ini, saya menggunakan dataset yang cukup umum dan menggunakan arsitektur CNN, yang telah terbukti berhasil dalam pemrosesan gambar dari pembelajaran mendalam digunakan.

1. [ DATASET ](#DATASET)
2. [ Deep Learning - CNN ](#DeepLearning-CNN)
3. [ FLASK ](#FLASK)
4. [ How to Run ](#HowtoRun)
5. [ Whats Inside ](#WhatsInside)

<a name="DATASET"></a>

## 1. DATASET

Dataset UAP terdiri dari 20 gambar berwarna 32x32 dalam 10 kelas, ada 50000 gambar pelatihan dan 10.000 gambar uji. Dataset ini dikumpulkan secara pribadi.

<p align="center">
<img src="https://user-images.githubusercontent.com/81585804/176235421-94e66358-a64d-4de9-b30f-67057755cf70.png" width="350" height="250">
</p>

<a name="DeepLearning-CNN"></a>

## 2. Deep Learning - CNN

Pertama, kami menormalkan data dan kemudian membuatnya menjadi kategorikal. Setelah itu untuk augmentasi data, kami menggunakan ImageDataGenerator. Arsitektur CNN dijelaskan di bawah ini. Ada beberapa penyesuaian di dalam model. Diantaranya:

- Model ini telah diperkuat dengan meningkatkan kompleksitasnya.
- Pengoptimal model dan penerapan parameter default.
- Callback ReduceLROnPlateau dan EarlyStopping ditambahkan untuk mencegah overfitting dan overtraining.
  
<p align="center">
<img src="https://user-images.githubusercontent.com/81585804/176241200-1da85e69-edef-4029-9253-a7d45e21f99d.png" width="800" height="250">
</p>

Setelah pelatihan model selesai, grafik accuracy dan loss dari pelatihan ditunjukkan pada dua gambar berikut. Akurasi model adalah **%91,74**.

<p align="center">
<img src="https://user-images.githubusercontent.com/81585804/176241918-49af7597-30bb-4e0c-83b9-ded38d1c9f45.png" width="350" height="250">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/81585804/176242139-eac5db1e-cce6-4c0f-9fff-3537bc6cc704.png" width="350" height="250">
</p>

<a name="FLASK"></a>

## 3. FLASK

Flask adalah kerangka kerja web mikro yang ditulis dalam bahasa Python. Ini diklasifikasikan sebagai kerangka kerja mikro karena tidak memerlukan alat atau pustaka tertentu.

- Anda dapat memuat gambar lokal atau url.
- Tiga prediksi teratas dari gambar yang dimuat dan persentasenya akan ditampilkan di halaman yang dialihkan.
- Dua gambar berikut ini adalah output dari pemrograman web, FLASK.

<p align="center">
<img src="https://user-images.githubusercontent.com/81585804/176243667-85bc3c1c-9428-4729-93d9-d26167256ddc.png" width="700" height="400">
</p>

<p align="center">
<img src="https://user-images.githubusercontent.com/81585804/176243750-8bf26887-b475-4af9-a631-fc29575535ed.png" width="700" height="400">
</p>

<a name="HowtoRun"></a>

## 4. How to Run

1. Fork repo.

```console
$ git clone https://github.com/dignifonauval/UAP-Deployment.git

```

2. Memuat dependensi proyek

**NOTE:** Dependensi ini tidak termasuk bagian Deep Learning. Colab memenuhi semua dependensi (seperti tensorflow).

```console
pip install -r requirements.txt
```

3. Anda dapat menjalankan app.py. Jika Anda mau, Anda dapat menjalankan .ipynb dan Anda dapat membangun model Anda sendiri. 


<a name="WhatsInside"></a>

## 5. Whats Inside

Beberapa yang telah dicantumkan di dalam repository ini termasuk model .h5, file web (.html dan .css), serta dataset uji dan beberapa gambar yang digunakan untuk mencoba model pada tampilan web yang kami gunakan di dalamnya
