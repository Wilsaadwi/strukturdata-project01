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
for i in range(10):
    nilai = int(input(" Masukkan Nilai Mahasiswa ke-{} : ".format(i+1)))
    nilai_mhs.append(nilai)
