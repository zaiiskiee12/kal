---
title: 'Penyelesaian Sistem Persamaan '

---

# Penyelesaian Sistem Persamaan Linear

Penyelesaian Sistem Persamaan Linear (SPL) dapat dilakukan dengan beberapa metode, tergantung pada jumlah variabel dan karakteristik sistemnya.

* Metode Substitusi → Cocok untuk sistem dengan 2 variabel.
* Metode Eliminasi → Cocok untuk sistem dengan lebih dari 2 variabel.
* Metode Matriks → Efisien untuk sistem yang lebih besar.
* Metode Grafik → Hanya cocok untuk visualisasi pada sistem 2 variabel.

## Operasi Baris Elementer

Operasi Baris Elementer (OBE) adalah teknik yang digunakan dalam manipulasi matriks untuk menyelesaikan sistem persamaan linear, menemukan invers matriks, dan berbagai aplikasi lainnya.

* Operasi Baris Elementer (OBE) digunakan untuk menyelesaikan SPL, menghitung invers matriks, dan berbagai manipulasi matriks lainnya.
* Terdapat tiga operasi utama: pertukaran baris, perkalian baris dengan skalar, dan penjumlahan baris.
* OBE adalah dasar dari metode Eliminasi Gauss, Eliminasi Gauss-Jordan, dan metode matriks lainnya.

## Eleminasi Gauss

Metode Eliminasi Gauss adalah teknik penyelesaian Sistem Persamaan Linear (SPL) dengan mengubah matriks augmented ke bentuk segitiga atas menggunakan Operasi Baris Elementer (OBE).

* Eliminasi Gauss digunakan untuk mengubah matriks augmented menjadi bentuk segitiga atas
* Setelah bentuk segitiga atas diperoleh, digunakan substitusi balik untuk menyelesaikan sistem
* Metode ini lebih cepat dibanding substitusi biasa, terutama untuk sistem dengan banyak variabel

Contoh Soal 1

$$
\begin{array}{cc}
x_1+2x_2+3x_3=6\\
2x_1+4x_2+6x_3=12\\
x_3+x_2=2
\end{array}
$$

Penyelesaian:

$$
\begin{array}{cc}
x_1 + 2x_2 + 3x_3 = 6 \\
2x_1 + 4x_2 + 6x_3 = 12 \\
x_3 + x_2 = 2
\end{array}
$$

Matriks augmented:

$$
\begin{bmatrix}
1 & 2 & 3 & | & 6 \\
2 & 4 & 6 & | & 12 \\
0 & 1 & 1 & | & 2
\end{bmatrix}
$$

Baris kedua dikurangi 2 kali baris pertama:

$$
\begin{bmatrix}
1 & 2 & 3 & | & 6 \\
0 & 0 & 0 & | & 0 \\
0 & 1 & 1 & | & 2
\end{bmatrix}
$$

Maka,

$$
x_1 + 2x_2 + 3x_3 + 6 = x_1 + 2(2 - x_3) + 3x_3 = 6 \\
x_1+ 4 -2x_2 + 3x_3 = 6 \\
x_1+x_3 = 6 - 4 \\
x_1 = 2 - x_3
$$

Karna ada variabel bebas $x_3 = t $ Sehingga, solusi umum dari sistem persamaan tersebut adalah:

$$
\begin{aligned}
x_1 &= 2-t, \\
x_2 &= 2-t, \\
x_3 &= t, \quad t \in \mathbb{R}.
\end{aligned}
$$

---

Contoh Soal 2

$$
\begin{array}{cc}
x_1+x_2+x_3=3\\
2x_1+x_3=5\\
x_1+2x_2=3
\end{array}
$$

Penyelesaian : 

$$
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
2 & 0 & 1 & 5 \\
1 & 2 & 0 & 3
\end{array}
$$

Langkah 1: Eliminasi Baris Pertama
Kita akan mengeliminasi elemen di bawah elemen pertama pada kolom pertama dengan mengurangi baris kedua dengan 2 kali baris pertama dan mengurangi baris ketiga dengan baris pertama.

- Baris 2 → Baris 2 - 2 × Baris 1
- Baris 3 → Baris 3 - Baris 1

Maka hasilnya adalah:

$$
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & -2 & -1 & -1 \\
0 & 1 & -1 & 0
\end{array}
$$

Langkah 2: Eliminasi Baris Kedua
Sekarang kita akan mengeliminasi elemen di bawah elemen kedua pada kolom kedua dengan menambah baris ketiga dengan setengah baris kedua.

- Baris 3 → Baris 3 + 1/2 dikali baris 2

Hasilnya adalah:


$$
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & -2 & -1 & -1 \\
0 & 0 & -\frac{3}{2} & -\frac{1}{2}
\end{array}
$$

Langkah 3: Normalisasi Baris Ketiga
Kita akan mengalikan baris ketiga dengan $(-\frac{2}{3})$ untuk menjadikan elemen di baris ketiga, kolom ketiga menjadi 1:

- Baris 3 → -2/3 dikali baris 3

Hasilnya menjadi:

$$
\begin{array}{ccc|c}
1 & 1 & 1 & 3 \\
0 & -2 & -1 & -1 \\
0 & 0 & 1 & \frac{1}{3}
\end{array}
$$


Langkah 4: Eliminasi Kolom Ketiga
Sekarang kita akan mengeliminasi elemen-elemen di atas kolom ketiga.

- Baris 1 → Baris 1 - Baris 3
- Baris 2 → Baris 2 + Baris 3

Maka hasilnya adalah:

$$
\begin{array}{ccc|c}
1 & 1 & 0 & \frac{8}{3} \\
0 & -2 & 0 & -\frac{2}{3} \\
0 & 0 & 1 & \frac{1}{3}
\end{array}
$$


Langkah 5: Normalisasi Baris Kedua
Kita akan mengalikan baris kedua dengan -1/2 untuk menjadikan elemen di baris kedua, kolom kedua menjadi 1:

- Baris 2 → -1/2 x baris 2

Hasilnya menjadi:

$$
\begin{array}{ccc|c}
1 & 1 & 0 & \frac{8}{3} \\
0 & 1 & 0 & \frac{1}{3} \\
0 & 0 & 1 & \frac{1}{3}
\end{array}
$$

Langkah 6: Eliminasi Kolom Kedua
Sekarang kita akan mengeliminasi elemen di atas kolom kedua.

- Baris 1 → Baris 1 - Baris 2

Hasil akhirnya menjadi:

$$
\begin{array}{ccc|c}
1 & 0 & 0 & \frac{7}{3} \\
0 & 1 & 0 & \frac{1}{3} \\
0 & 0 & 1 & \frac{1}{3}
\end{array}
$$

Solusi akhir dari persamaan diatas adalah: 

$$
\begin{array}{cc}
x_1=\frac{7}{3} \\
x_2=\frac{1}{3} \\
x_3=\frac{1}{3}
\end{array}
$$

<iframe src="https://www.geogebra.org/classic/jmccwhfc?embed" width="840" height="540" allowfullscreen style="border: 1px solid #e4e4e4;border-radius: 4px;" frameborder="0"></iframe>

---

Contoh Soal 3

$$
\begin{array}{cc}
2x_1+2x_2=4\\
x_1+x_2=2
\end{array}
$$

Penyelesaian :

$$
\begin{array}{cc}
2x_1 + 2x_2 = 4 \quad (1) \\
x_1 + x_2 = 2 \quad (2)
\end{array}
$$

matriks augmented:

$$
\begin{bmatrix}
2 & 2 & | & 4 \\
1 & 1 & | & 2
\end{bmatrix}
$$

Membuat elemen di bawah pivot menjadi nol. Kita dapat melakukannya dengan mengurangi baris pertama dengan dua kali baris kedua:

$$ R_1 - 2R_2 \rightarrow R_1 $$

Maka:

$$
R_1: \quad 2 - 2 \cdot 1 = 0 \\
2 - 2 \cdot 1 = 0 \\
4 - 2 \cdot 2 = 0
$$

Sehingga:

$$
\begin{bmatrix}
0 & 0 & | & 0 \\
1 & 1 & | & 2
\end{bmatrix}
$$

Matriks ini menunjukkan bahwa kita memiliki satu persamaan yang valid dan satu persamaan yang identik (0 = 0). Dari baris kedua, kita dapat menuliskan persamaan:

$$
x_1 + x_2 = 2 \quad (2)
$$

Karena baris pertama adalah 0 = 0, ini menunjukkan bahwa sistem ini memiliki solusi tak terhingga. Kita dapat menyelesaikan untuk salah satu variabel. Misalkan kita menyelesaikan untuk $(x_1)$:

$$ x_1 = 2 - x_2 $$

Dengan demikian, solusi umum untuk sistem persamaan ini adalah:

$$
(x_1, x_2) = (2 - x_2, x_2) \quad \text{untuk setiap } x_2 \in \mathbb{R}
$$

Sebagai contoh, jika kita memilih $(x_2 = 0)$, maka:

$$
x_1 = 2 - 0 = 2 \quad \Rightarrow \quad (x_1, x_2) = (2, 0)
$$

Jika kita memilih $(x_2 = 1)$, maka:

$$
x_1 = 2 - 1 = 1 \quad \Rightarrow \quad (x_1, x_2) = (1, 1)
$$

Dan jika kita memilih $(x_2 = 2)$, maka:

$$
x_1 = 2 - 2 = 0 \quad \Rightarrow \quad (x_1, x_2) = (0, 2)
$$

Dengan demikian, solusi dari sistem persamaan ini adalah semua pasangan $(x_1, x_2)$ yang memenuhi:

$$
(x_1, x_2) = (2 - x_2, x_2) \quad \text{untuk setiap } x_2 \in \mathbb{R}
$$

---

Contoh Soal 4

Diberikan sistem persamaan:

$$
\begin{aligned}
x_1 + x_2 = 5 \\
x_1 + 2x_3 = 6
\end{aligned}
$$

Kita akan menyelesaikannya menggunakan metode eliminasi Gauss. Pertama, kita tuliskan sistem ini dalam bentuk matriks augmented:

$$
\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
1 & 0 & 2 & | & 6
\end{bmatrix}
$$

Langkah pertama adalah membuat elemen di bawah pivot (elemen pertama di kolom pertama) menjadi nol. Kita lakukan operasi berikut:

$$
R_2 - R_1 \rightarrow R_2
$$

Setelah melakukan perhitungan, kita mendapatkan:

$$
R_2: \quad 1 - 1 = 0 \\
0 - 1 = -1 \\
2 - 0 = 2 \\
6 - 5 = 1
$$

Sehingga, matriks augmented menjadi:

$$
\begin{bmatrix}
1 & 1 & 0 & | & 5 \\
0 & -1 & 2 & | & 1
\end{bmatrix}
$$

Selanjutnya, kita dapat menyelesaikan baris kedua untuk mengekspresikan $(x_2)$ dalam bentuk $(x_3)$:

$$
-1x_2 + 2x_3 = 1 \implies x_2 = 2x_3 - 1
$$

Sekarang kita substitusi $(x_2)$ ke dalam persamaan pertama:

$$
x_1 + (2x_3 - 1) = 5
$$

Maka kita dapatkan:

$$
x_1 + 2x_3 - 1 = 5 \implies x_1 = 6 - 2x_3
$$

Karena kita memiliki dua persamaan dengan tiga variabel, kita dapat menyatakan solusi dalam bentuk parameter. Misalkan $(x_3 = p)$, maka:

$$
\begin{aligned}
x_1 = 6 - 2p \\
x_2 = 2p - 1 \\
x_3 = p
\end{aligned}
$$

Jadi, solusi umum dari sistem persamaan ini adalah:

$$
\begin{cases}
x_1 = 6 - 2p \\
x_2 = 2p - 1 \\
x_3 = p
\end{cases}
$$

di mana (p) adalah parameter bebas.