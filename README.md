# Analisis Segmentasi Pasar & Prediksi Rating Video Game

Repository ini berisi Tugas Besar Mata Kuliah Data Mining (Kelompok 8). Proyek ini menganalisis data ulasan video game untuk melakukan segmentasi pasar dan memprediksi rating pengguna menggunakan Machine Learning.

## Anggota Kelompok
* **Adinar Tri Panuntun** - 102022300174
* **Ahmad Akmal Amran** - 102022300010
* **Muhammad Alvaro Shidqi Faozan** - 102022300096
* **Raffi Akbar Firdaus** - 102022300186

## Tentang Dataset
Data yang digunakan berasal dari Kaggle: [Video Game Reviews and Ratings](https://www.kaggle.com/datasets/jahnavipaliwal/video-game-reviews-and-ratings/data).

Dataset ini memiliki **47.774 baris** data dengan fitur utama:
* **Informasi Game:** Judul, Genre, Platform, Tahun Rilis, Developer, Publisher.
* **Metrik Teknis:** Mode Game (Online/Offline), Multiplayer, Perangkat Khusus, Durasi Main (Jam), Jumlah Pemain Minimal.
* **Kualitas:** Grafis, Soundtrack, Cerita (Story).
* **Target & Harga:** Target Usia, Harga (USD).
* **Target Prediksi:** User Rating (dikonversi menjadi kelas: Poor, Average, Good).

## Fitur & Metodologi Aplikasi

Aplikasi ini dibangun menggunakan **Streamlit** dan memiliki dua fitur utama:

### 1. Segmentasi Pasar (Unsupervised Learning)
Kami menggunakan algoritma **K-Means Clustering** untuk memetakan karakteristik pasar game. Fitur input yang digunakan meliputi:
* **Harga (Price)**
* **Target Usia (Age Group)**
* **Genre**
* **Fitur Multiplayer**
* **Mode Game (Online/Offline)**

Hasil analisis dikelompokkan menjadi 3 kluster utama:
* **Kluster 1:** Game premium offline, gameplay kompleks (Strategy/RPG), untuk remaja/dewasa.
* **Kluster 2:** Game naratif single-player (Puzzle/Adventure), kasual, harga menengah-tinggi.
* **Kluster 3:** Game santai offline untuk keluarga/semua umur.

### 2. Prediksi Rating (Supervised Learning)
Kami menggunakan algoritma **Naive Bayes Classifier** untuk memprediksi kategori rating game baru. Pengguna dapat memasukkan parameter berikut untuk melihat prediksi rating:
* **Demografis:** Target Usia.
* **Ekonomi:** Harga.
* **Teknis:** Platform, Dukungan Perangkat Khusus, Mode Game, Jumlah Pemain.
* **Konten:** Genre, Durasi Game (Jam), Multiplayer.
* **Kualitas:** Kualitas Grafis, Soundtrack, dan Cerita.

Output prediksi berupa kelas: **Poor**, **Average**, atau **Good**, beserta probabilitasnya.

## Cara Menjalankan Project

1.  **Clone repository ini.**
2.  **Install library yang diperlukan:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Jalankan aplikasi Streamlit:**
    ```bash
    streamlit run app.py
    ```

## Tautan
* **Dashboard Aplikasi:** [Buka di Streamlit](https://tb-damin-si4708-k8.streamlit.app/)
* **Notebook Analisis:** `TB_DAMIN_K8.ipynb`
