# 1. Penjelasan konsep array
Pada program yang saya buat, konsep **array** digunakan untuk menyimpan data nilai mahasiswa yang dimasukkan oleh pengguna. Dalam bahasa pemrograman Python, struktur data yang berfungsi seperti array disebut **list**. List memungkinkan kita untuk menyimpan banyak data dalam satu variabel yang sama, sehingga pengolahan data menjadi lebih mudah dan terorganisir.

Pada program ini, saya membuat sebuah list bernama `nilai_mhs` yang berfungsi sebagai tempat penyimpanan seluruh nilai mahasiswa yang diinput oleh pengguna. Setiap nilai yang dimasukkan akan ditambahkan ke dalam list tersebut menggunakan fungsi `append()`. Dengan cara ini, semua nilai mahasiswa dapat tersimpan dalam satu struktur data yang sama dan bisa diproses lebih lanjut oleh program.

Contoh bagian kode yang menunjukkan penggunaan array pada program adalah sebagai berikut:

```python
nilai_mhs = []

for i in range(10):
    nilai = int(input("Masukkan Nilai Mahasiswa ke-{} : ".format(i+1)))
    nilai_mhs.append(nilai)
```

Pada kode tersebut, program melakukan perulangan sebanyak 10 kali untuk menerima input nilai mahasiswa. Setiap nilai yang dimasukkan akan dimasukkan ke dalam list `nilai_mhs`. Setelah proses input selesai, list tersebut akan berisi seluruh data nilai mahasiswa yang kemudian digunakan untuk proses analisis.

Penggunaan array pada program ini sangat membantu dalam melakukan berbagai proses pengolahan data. Misalnya, untuk mencari nilai tertinggi dan nilai terendah, program cukup membaca setiap elemen yang ada di dalam list. Dengan menggunakan perulangan, program dapat membandingkan setiap nilai yang tersimpan di dalam array hingga ditemukan nilai paling besar dan paling kecil.

Selain itu, array juga digunakan untuk menghitung rata-rata nilai mahasiswa. Program menjumlahkan seluruh nilai yang ada di dalam list menggunakan fungsi `sum()`, kemudian hasilnya dibagi dengan jumlah data yang ada. Karena semua nilai tersimpan dalam satu array, proses perhitungan ini dapat dilakukan dengan lebih sederhana.

Array juga digunakan untuk menentukan jumlah mahasiswa yang lulus dan tidak lulus. Program akan memeriksa setiap nilai yang ada dalam array dan membandingkannya dengan batas kelulusan yang telah ditentukan, yaitu nilai 60. Jika nilai mahasiswa lebih besar atau sama dengan 60 maka dihitung sebagai lulus, sedangkan jika kurang dari 60 maka dihitung sebagai tidak lulus.

Dari program yang telah dibuat dapat disimpulkan bahwa penggunaan array sangat penting dalam pengolahan data. Dengan menggunakan array, data nilai mahasiswa dapat disimpan dalam satu struktur yang terorganisir sehingga proses pencarian nilai, perhitungan rata-rata, serta analisis kelulusan dapat dilakukan dengan lebih efisien dan sistematis.


# 2. Screenshot hasil eksekusi
![image](https://github.com/Wilsaadwi/strukturdata-project01/blob/b3e05e4745f984d67fec354a7f3cc667d6013c1c/eksekusi1.png)
![image](https://github.com/Wilsaadwi/strukturdata-project01/blob/631243a26d5499c074b6daec661c887ee36daf9a/eksekusi2.png)

# 3. Analisis Kompleksitas
# **Analisis Kompleksitas Sistem**
Program ini digunakan untuk mengolah nilai mahasiswa menggunakan struktur data list (array) di Phyton. Di dalam program terdapat beberapa proses utama seperti menginputkan nilai, mencari nilai tertinggi dan nilai terendah, menghitung rata-rata, serta menghitung jumlah mahasiswa yang lulus. Setiap proses memiliki kompleksitas waktu yang berbeda tergantung dari jumlah data yang diproses.

**1. Proses input nilai mahasiswa**

Pada bagian ini, program menggunakan perulangan for untuk memasukkan 10 nilai mahasiswa ke dalam list *nilai_mhs*

```python
for i in range(10):
    nilai = int(input("Masukkan Nilai Mahasiswa ke-{} : ".format(i+1)))
    nilai_mhs.append(nilai)
```
Perulangan tersebut berjalan sebanyak jumlah data yang dimasukkan. Jika jumlah mahasiswa dilambangkan dengan n, maka proses input akan dilakukan sebanyak n kali. Karena jumlah langkah bergantung pada banyaknya data, maka kompleksitas waktunya adalah O(n).

**2. Proses mencari nilai tertinggi dan terendah**

Pada program ini, nilai tertinggi dan terendah dicari menggunakan fungsi max() dan min().
```python
nilai_tertinggi = max(nilai_mhs)
nilai_terendah = min(nilai_mhs)
```
Fungsi tersebut bekerja dengan cara memeriksa seluruh elemen dalam list. Oleh karena itu, kompleksitas waktunya juga O(n) karena semua nilai harus dibandingkan untuk mendapatkan nilai maksimum dan minimum.

Setelah itu terdapat perulangan lagi:
```python
for n in nilai_mhs:
    if n > nilai_tertinggi:
        nilai_tertinggi = n
    elif n < nilai_terendah:
        nilai_terendah = n
```
Perulangan ini juga memeriksa seluruh elemen list sehingga kompleksitasnya tetap O(n).

**3. Proses menghitung rata-rata nilai**

Rata-rata dihitung dengan menjumlahkan seluruh nilai terlebih dahulu kemudian dibagi dengan jumlah data.
```python
total_nilai = sum(nilai_mhs)

for n in nilai_mhs:
    total_nilai += n
```
Fungsi *sum()* akan menjumlahkan semua elemen pada list sehingga kompleksitasnya O(n). Selain itu, terdapat perulangan yang kembali menjumlahkan seluruh nilai dalam list. Karena perulangan tersebut jugas membaca semua data satu per satu, maka kompleksitasnya juga O(n).

Dengan demikian, proses perhitungan rata-rata secara keseluruhan masih termasuk dalam kompleksitas O(n).

**4. Proses menghitung jumlah mahasiswa lulus**

Program memeriksa setiap nilai untuk menentukan apakah mahasiswa tersebut lulus atau tidak dengan syarat nilai ≥ 60.
```python
for n in nilai_mhs:
    if n >= 60:
        jumlah_lulus += 1
    else:
        jumlah_tidak_lulus += 1
```
Perulangan ini mengecek seluruh elemen pada list satu per satu. Karena seluruh data harus diperiksa, maka kompleksitas waktunya adalah O(n).

**5. Proses pembuatan grafik**

Grafik dibuat menggunakan library **matplotlib**.
```python
grafik.barh(kategori, nilai)
grafik.pie(data, labels=label, autopct='%1.0f%%')
```
Pada bagian ini data yang digunakan hanya dua kategori yaitu nilai tertinggi dan terendah serta jumlah mahasiswa lulus dan tidak lulus. Karena jumlah datanya tetap dan tidak bergantung pada banyaknya nilai mahasiswa, maka kompleksitasnya dapat dianggap O(1) atau konstan.

**Kesimpulan**

Dari beberapa proses yang dilakukan dalam program ini dapat disimpulkan bahwa sebagian besar operasi memiliki kompleksitas O(n). Hal ini disebabkan karena program harus membaca atau memproses seluruh elemen dalam list nilai mahasiswa untuk melakukan perhitungan seperti mencari nilai tertinggi, menghitung rata-rata, serta menentukan jumlah mahasiswa yang lulus.

Dengan kompleksitas O(n), program masih tergolong efisien untuk jumlah data yang cukup besar karena waktu eksekusinya bertambah secara linear mengikuti jumlah data yang diproses.

# 4. Refleksi pembelajaran

Pada proyek ini saya belajar bagaimana mengolah data nilai mahasiswa menggunakan bahasa Python dengan memanfaatkan struktur data array (list). Dari tugas ini saya jadi lebih memahami bahwa array sangat membantu ketika kita ingin menyimpan banyak data dalam satu variabel, sehingga data tersebut bisa diproses dengan mudah.

Saat mengerjakan program ini saya juga belajar menggunakan perulangan untuk membaca setiap data yang ada di dalam array. Dari situ saya bisa mencari nilai tertinggi, nilai terendah, menghitung rata-rata nilai, serta menentukan jumlah mahasiswa yang lulus dan tidak lulus. Sebelumnya saya hanya memahami konsep array secara teori, tetapi melalui tugas ini saya bisa melihat langsung bagaimana konsep tersebut digunakan dalam sebuah program.

Selama mengerjakan proyek ini saya juga sempat mengalami beberapa kesulitan, terutama saat membuat grafik menggunakan library matplotlib dan saat mencoba menghubungkan hasil program dari Google Colab ke GitHub. Pada awalnya saya cukup bingung karena belum terbiasa menggunakan kedua tools tersebut. Namun setelah mencoba beberapa kali dan mencari tahu cara penggunaannya, akhirnya saya bisa menjalankan program dengan baik dan menampilkan grafik dari data yang sudah diolah.

Dari tugas ini saya merasa pemahaman saya tentang penggunaan array dan perulangan menjadi lebih baik. Selain itu, saya juga belajar bahwa visualisasi data dengan grafik dapat membantu kita melihat hasil analisis data dengan lebih jelas. Melalui proyek ini saya jadi lebih mengerti bagaimana konsep yang dipelajari di materi struktur data bisa diterapkan langsung dalam pembuatan program sederhana.
