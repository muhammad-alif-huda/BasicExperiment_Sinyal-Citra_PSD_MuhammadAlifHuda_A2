# Eksperimen Operasi Dasar pada Sinyal dan Citra
> [cite_start]**Mata Kuliah:** Pengolahan Sinyal Digital [cite: 2]

## Identitas Mahasiswa
* [cite_start]**Nama:** Muhammad Alif Huda Zamzami [cite: 276]
* **NIM:** 452024611045
* **Kelas:** Ti 5/ A2

---

## Deskripsi Singkat Project
[cite_start]Project ini merupakan implementasi eksperimen berbasis Python untuk menerapkan dan menganalisis berbagai operasi dasar pada sinyal 1D (diskrit) dan citra 2D[cite: 12, 277]. 
[cite_start]Fokus utama dari project ini adalah memahami bagaimana operasi sederhana seperti penjumlahan, penggeseran (shifting), dan amplifikasi (scaling) menjadi fondasi dari konsep yang lebih besar dalam Pengolahan Sinyal Digital, 
seperti superposisi, sistem linier, filtering, hingga augmentasi data[cite: 2, 15].

---

## Library yang Digunakan
[cite_start]Project ini dibangun menggunakan bahasa pemrograman Python dengan beberapa library utama berikut[cite: 27, 278]:
* [cite_start]**NumPy** - Untuk komputasi matriks dan pemrosesan array sinyal/citra[cite: 28].
* [cite_start]**Matplotlib** - Untuk visualisasi plot sinyal 1D dan penampilan citra[cite: 29].
* [cite_start]**OpenCV (cv2) / PIL** - Untuk membaca, melakukan resize, dan memanipulasi citra 2D[cite: 30].
* [cite_start]**SciPy** - *(Jika diperlukan)* Untuk pendukung pemrosesan sinyal[cite: 31].

---




Cara Menjalankan Notebook
Buka notebook menggunakan Jupyter, Google Colab, atau environment Python lokal dengan mengikuti langkah-langkah berikut
git clone [https://github.com/](https://github.com/TugasEksperiment_PSD1_MuhammadAlifHudaZamzami_A2.git
cd operasi-dasar-sinyal-citra

instalasi Library (Dependencies)
pip install -r requirements.txt

Menjalankan Jupyter Notebook
  Buka notebook menggunakan Jupyter atau Google Colab:
ika lokal: Jalankan perintah jupyter notebook lalu buka file notebook/operasi_sinyal_citra.ipynb
Jika Google Colab: Upload file .ipynb ke Google Drive dan buka via Google Colab.

Ringkasan Hasil Eksperimen
1. Bagian A:
  Operasi pada Sinyal 1D
1. Membuat Sinyal Diskrit: Berhasil membuat sinyal sinus $x_1[n] = \sin(0.5\pi n)$ dan sinyal kedua $x_2[n]$ berupa unit step menggunakan rentang $n = 0$ sampai $30$.
2. Menjumlahan Sinyal: Menggabungkan kedua sinyal menjadi $y[n] = x_1[n] + x_2[n]$. Hasilnya menunjukkan adanya perubahaan amplitudo dan bentuk sinyal akibat pengaruh nilai unit step
3. Penggeseran Sinyal: Menguji nilai $k = -3, 0, 4$. Nilai $k$ positif menggeser sinyal ke kanan (delay), sedangkan $k$ negatif menggeser ke kiri
4. Amplifikasi Sinyal: Menguji nilai $\alpha = 0.5, 1, 2, -1$. Nilai $\alpha > 1$ memperbesar amplitudo (gain), $0 < \alpha < 1$ memperkecilnya, dan nilai negatif membalik fase sinyal.

Bagian B:
Operasi pada Citra 2D
  Penjumlahan Citra: Melakukan perpaduan dua citra berukuran sama. Penjumlahan meningkatkan tingkat kecerahan (brightness) citra secara keseluruhan.
Melakukan translasi citra dengan variasi nilai $\Delta i$ dan $\Delta j$. Terdapat area kosong yang muncul akibat pergeseran posisi objek.
Amplifikasi Citra: Mengubah tingkat kecerahan dan kontras citra melalui perkalian skalar $\alpha$ dengan variasi $0.5, 1, 1.5,$ dan $2$.

Bagian C:
Uji Sistem Linier   
   Uji Homogenitas: Menguji apakah sistem memenuhi sifat $T(\alpha x) = \alpha T(x)$.  
   Uji Additivitas: Menguji apakah sistem memenuhi sifat $T(x_1 + x_2) = T(x_1) + T(x_2)$.  
   Kesimpulan Linieritas: Berdasarkan pengujian, sistem $T_1(x) = 2x$ terbukti merupakan Sistem Linier, sedangkan sistem $T_2(x) = x^2$ merupakan Sistem Non-Linier.
Kesimpulan Singkat
  Eksperimen ini membuktikan bahwa operasi matematika dasar pada ranah diskrit (1D) dan spasial (2D) memiliki dampak langsung terhadap karakteristik fisik sinyal maupun citra. 
Pemahaman mengenai sistem linier sangat krusial dalam Pengolahan Sinyal Digital karena sifat homogenitas dan additivitasnya memungkinkan analisis sistem yang kompleks melalui prinsip superposisi.

