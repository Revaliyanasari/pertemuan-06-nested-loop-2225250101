# Tugas Pertemuan 06 - Nested Loop Python

## Identitas Mahasiswa

* **Nama:** Reva Liyanasari
* **NIM:** 2225250101
* **Kelas:** 3A
* **Mata Kuliah:** Algoritma dan Pemrograman
* **Dosen Pengampu:** Dr. Aan Hendrayana, S.Si., M.Pd.

---

## 1. Tujuan

Repositori ini dibuat untuk menyimpan hasil latihan dan Tugas 3 pada Pertemuan 06 Mata Kuliah Algoritma dan Pemrograman.

Materi yang dipelajari pada pertemuan ini meliputi:

* **Nested loop** menggunakan perulangan `for` di dalam perulangan lainnya.
* Pembentukan **pola baris-kolom dan pola simbol**.
* **Akumulasi bertingkat** untuk menghitung jumlah per baris dan jumlah keseluruhan.
* **Pencacahan (counter)** untuk menghitung banyak pasangan yang memenuhi kondisi tertentu.
* **Tracing** dua variabel kontrol, yaitu `i` dan `j`.
* Validasi input menggunakan `while`.
* Pengujian dan debugging program menggunakan VS Code.
* Pengelolaan program dan dokumentasi menggunakan Git dan GitHub.

Tujuan utama dari pertemuan ini adalah memahami hubungan antara loop luar dan loop dalam serta menerapkan nested loop untuk mengolah pasangan data, membentuk pola, melakukan akumulasi, dan pencacahan.

---

## 2. Daftar Berkas

Struktur repositori Pertemuan 06 terdiri dari `README.md`, `.gitignore`, folder `latihan`, dan folder `tugas`.

### Latihan

1. **`latihan/01_pasangan_indeks.py`**

   * Program untuk menampilkan seluruh pasangan `(i, j)` dengan `i = 1..3` dan `j = 1..4`.
   * Program juga menghitung banyak pasangan menggunakan variabel `count`.
   * Hasil yang diharapkan adalah **12 pasangan**.

2. **`latihan/02_pola_segitiga.py`**

   * Program menerima nilai `n` positif.
   * Program menghasilkan pola bintang dengan 1 simbol pada baris pertama hingga `n` simbol pada baris ke-`n`.
   * Program menggunakan nested loop untuk membentuk pola segitiga.

3. **`latihan/03_jumlah_per_baris.py`**

   * Program menggunakan `i = 1..4` dan `j = 1..3`.
   * Setiap nilai dihitung menggunakan `i * j`.
   * Program menghitung dan menampilkan jumlah pada setiap baris menggunakan akumulator `total_baris`.

4. **`latihan/04_hitung_pasangan.py`**

   * Program menerima nilai `n`.
   * Program memeriksa seluruh pasangan `i` dan `j` dari 1 sampai `n`.
   * Counter bertambah jika memenuhi kondisi `i + j <= n`.

### Tugas 3

**`tugas/tabel_perkalian_dan_statistik.py`**

Program menerima bilangan bulat positif `n` dan melakukan beberapa proses menggunakan nested loop, yaitu:

* Membentuk tabel perkalian `1 sampai n`.
* Menghitung jumlah seluruh hasil perkalian.
* Menghitung banyak hasil perkalian yang genap.
* Menghitung dan menampilkan jumlah setiap baris.
* Melakukan validasi agar nilai `n` merupakan bilangan positif.

---

## 3. Cara Menjalankan

Buka terminal pada folder utama project, kemudian jalankan program menggunakan perintah berikut.

### Latihan 1

```bash
python latihan/01_pasangan_indeks.py
```

### Latihan 2

```bash
python latihan/02_pola_segitiga.py
```

### Latihan 3

```bash
python latihan/03_jumlah_per_baris.py
```

### Latihan 4

```bash
python latihan/04_hitung_pasangan.py
```

### Tugas 3

```bash
python tugas/tabel_perkalian_dan_statistik.py
```

Pada sistem yang menggunakan `python3`, perintah dapat disesuaikan menjadi:

```bash
python3 tugas/tabel_perkalian_dan_statistik.py
```

PDF juga menjelaskan bahwa pada Windows perintah Python dapat menggunakan `python`, sedangkan pada macOS/Linux sering menggunakan `python3`.

---

## 4. Algoritma Tugas 3

Algoritma program **Tabel Perkalian dan Statistik** adalah sebagai berikut:

1. Membaca nilai `n` sebagai bilangan bulat.
2. Memeriksa apakah `n` merupakan bilangan positif.
3. Jika `n <= 0`, pengguna diminta memasukkan kembali nilai `n`.
4. Menginisialisasi `total_semua = 0`.
5. Menginisialisasi `count_genap = 0`.
6. Menggunakan loop luar `for` untuk nilai `i` dari 1 sampai `n`.
7. Menginisialisasi `total_baris = 0` pada setiap awal baris.
8. Menggunakan loop dalam `for` untuk nilai `j` dari 1 sampai `n`.
9. Menghitung nilai perkalian dengan rumus:

```python
hasil = i * j
```

10. Menampilkan hasil perkalian secara teratur pada setiap baris.
11. Menambahkan `hasil` ke `total_baris`.
12. Menambahkan `hasil` ke `total_semua`.
13. Memeriksa apakah `hasil` merupakan bilangan genap menggunakan kondisi:

```python
hasil % 2 == 0
```

14. Jika hasil merupakan bilangan genap, menambahkan `1` pada `count_genap`.
15. Setelah loop dalam selesai, menampilkan jumlah pada baris tersebut.
16. Setelah kedua loop selesai, menampilkan total seluruh hasil perkalian.
17. Menampilkan banyak hasil perkalian yang genap.

Algoritma tersebut mengikuti spesifikasi Tugas 3 pada modul, termasuk penggunaan validasi `while`, nested `for`, akumulasi per baris dan keseluruhan, serta counter untuk hasil genap.

---

## 5. Hasil Pengujian

Pengujian dilakukan menggunakan test case wajib yang terdapat pada modul.

| **Test Case**   | **n** | **Jumlah Pasangan** | **Total Semua** | **Banyak Hasil Genap** | **Status** |
| --------------- | ----: | ------------------: | --------------: | ---------------------: | ---------- |
| **Test Case 1** |     1 |                   1 |               1 |                      0 | Berhasil   |
| **Test Case 2** |     2 |                   4 |               9 |                      3 | Berhasil   |
| **Test Case 3** |     3 |                   9 |              36 |                      5 | Berhasil   |

### Test Case 1

Input:

```text
n = 1
```

Hasil:

```text
1
Total seluruh hasil = 1
Banyak hasil genap = 0
```

Status: **Berhasil**

### Test Case 2

Input:

```text
n = 2
```

Tabel perkalian:

```text
1  2
2  4
```

Jumlah seluruh hasil:

```text
9
```

Banyak hasil genap:

```text
3
```

Status: **Berhasil**

### Test Case 3

Input:

```text
n = 3
```

Tabel perkalian:

```text
1  2  3
2  4  6
3  6  9
```

Jumlah seluruh hasil:

```text
36
```

Banyak hasil genap:

```text
5
```

Status: **Berhasil**

Ketiga test case tersebut sesuai dengan nilai yang ditentukan dalam modul Pertemuan 06.

---

## 6. Analisis Efisiensi

Pada program Tugas 3, nested loop digunakan untuk membentuk tabel perkalian berukuran `n × n`.

Loop luar berjalan sebanyak `n` kali dan loop dalam juga berjalan sebanyak `n` kali untuk setiap iterasi loop luar.

Dengan demikian, badan loop dalam dijalankan sebanyak:

```text
n × n = n²
```

kali.

Contohnya:

| **n** | **Jumlah Iterasi** |
| ----: | -----------------: |
|     1 |                  1 |
|     2 |                  4 |
|     3 |                  9 |
|    10 |                100 |
|   100 |             10.000 |

Pada setiap iterasi, program melakukan perhitungan:

```python
hasil = i * j
```

serta proses akumulasi dan pengecekan apakah hasil tersebut genap.

Oleh karena itu, semakin besar nilai `n`, semakin banyak operasi yang dilakukan oleh nested loop. Efisiensi dapat diperhatikan dengan memastikan batas `range` tepat dan tidak melakukan proses yang tidak diperlukan. Modul menjelaskan bahwa perubahan kecil pada batas dua loop dapat meningkatkan jumlah operasi secara signifikan.

---

## 7. Refleksi

Pada Pertemuan 06, saya memahami bahwa **nested loop** merupakan perulangan yang berada di dalam perulangan lainnya. Loop luar digunakan untuk mengatur kelompok atau baris, sedangkan loop dalam digunakan untuk memproses elemen pada setiap kelompok tersebut.

Saya juga memahami bahwa loop dalam akan menjalankan seluruh iterasinya kembali setiap kali loop luar berpindah ke iterasi berikutnya. Oleh karena itu, tracing nilai `i` dan `j` diperlukan untuk memahami urutan eksekusi program.

Kesalahan yang saya pahami dari materi adalah kesalahan dalam menentukan lokasi inisialisasi akumulator. Jika `total_baris` digunakan untuk menghitung jumlah setiap baris, maka variabel tersebut harus direset pada setiap iterasi loop luar. Sebaliknya, `total_semua` harus diinisialisasi sebelum kedua loop agar dapat menyimpan jumlah seluruh hasil perkalian.

Selain akumulasi, saya memahami penggunaan **counter** untuk pencacahan. Counter hanya bertambah ketika kondisi yang ditentukan terpenuhi, misalnya ketika hasil perkalian merupakan bilangan genap.

Melalui latihan dan Tugas 3, saya menjadi lebih memahami hubungan antara nested loop, pola, akumulasi, pencacahan, kondisi `if`, dan tracing dua variabel kontrol.

---

## 8. Sumber

* Materi Pertemuan 06 Algoritma dan Pemrograman: **Nested Loop, Pola, Akumulasi, dan Pencacahan dalam Python di VS Code dan Pengumpulan melalui GitHub**.
* Visual Studio Code Documentation, **Python in Visual Studio Code**.