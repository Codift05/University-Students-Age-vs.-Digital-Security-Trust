# Analisis Korelasi Usia & Persepsi Keamanan Aplikasi Digital Mahasiswa

---

## Gambaran Umum

Repositori ini memuat implementasi Python untuk menganalisis **korelasi antara usia mahasiswa dan persepsi keamanan mereka dalam menggunakan aplikasi digital**. Penelitian ini bertujuan untuk memahami apakah ada hubungan yang signifikan antara kedua variabel ini. Kode ini secara cerdas memilih antara **Korelasi Pearson** atau **Korelasi Spearman** berdasarkan uji normalitas data, dan memvisualisasikan hasilnya dengan grafik yang informatif.

**Catatan:** Data yang digunakan dalam skrip ini adalah **data dummy** yang dihasilkan secara acak dan hanya bertujuan sebagai contoh implementasi analisis. Untuk penelitian yang sesungguhnya, Anda perlu mengganti data ini dengan data survei atau eksperimen yang sebenarnya.

---

## Fitur Utama

* **Generasi Data Dummy:** Skrip ini menghasilkan data dummy untuk usia (17-25 tahun) dan skor persepsi keamanan (10-20) untuk tujuan demonstrasi.
* **Uji Normalitas Adaptif:** Menggunakan uji Shapiro-Wilk pada data 'Persepsi_Keamanan' untuk memeriksa distribusi data.
* **Pemilihan Korelasi Cerdas:**
    * **Korelasi Pearson** digunakan jika data terdistribusi normal ($p > 0.05$).
    * **Korelasi Spearman** digunakan jika data tidak terdistribusi normal ($p \le 0.05$).
* **Visualisasi Intuitif:** Menghasilkan *scatter plot* dengan garis regresi menggunakan `seaborn` dan `matplotlib`, memudahkan interpretasi hubungan.
* **Output Hasil Komprehensif:** Menyajikan koefisien korelasi ($r$), *p-value*, jenis uji yang diterapkan, dan *p-value* dari uji normalitas.

---

## Struktur Proyek

.
├── README.md
└── correlation_analysis.py


* `README.md`: Berkas ini, berisi deskripsi proyek dan instruksi.
* `correlation_analysis.py`: Skrip Python utama yang menjalankan seluruh analisis.

---

## Cara Menjalankan

### Prasyarat

Pastikan Anda telah menginstal pustaka Python berikut:

```bash
pip install pandas numpy scipy seaborn matplotlib
Eksekusi Skrip
Klon repositori ini ke sistem lokal Anda:

Bash

git clone [https://github.com/YourUsername/your-repo-name.git](https://github.com/YourUsername/your-repo-name.git)
cd your-repo-name
(Ganti YourUsername/your-repo-name.git dengan URL repositori Anda yang sebenarnya.)

Jalankan skrip Python:

Bash

python correlation_analysis.py
Setelah eksekusi, sebuah grafik interaktif akan muncul menampilkan hasil korelasi, dan ringkasan analisis akan dicetak langsung ke konsol Anda.

Contoh Hasil
Berikut adalah contoh visualisasi yang mungkin Anda dapatkan (nilai numerik dapat bervariasi karena data dummy):

(Penting: Setelah menjalankan kode dan mendapatkan plot, simpan plot tersebut sebagai correlation_plot_example.png di direktori yang sama dengan README.md dan correlation_analysis.py, lalu ganti URL gambar di atas agar gambar muncul di README Anda.)

Output konsol akan mirip dengan ini:

JSON

{
    "Jenis_Uji": "Pearson",
    "Nilai_Korelasi": 0.12345,
    "p_value": 0.56789,
    "Normalitas_p_value": 0.12345
}
Kontribusi
Kami sangat menyambut kontribusi Anda. Baik itu laporan bug, saran fitur, atau pull request, silakan berinteraksi dengan kami.
