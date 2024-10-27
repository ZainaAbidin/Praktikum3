(PENJELASAN CODE 1)
Pertama, program meminta pengguna untuk memasukkan tiga bilangan. Ketiga bilangan ini disimpan dalam variabel A, B, dan C.
A = float(input("Masukkan bilangan A: "))
B = float(input("Masukkan bilangan B: "))
C = float(input("Masukkan bilangan C: "))
float(input(...)) digunakan agar input yang dimasukkan oleh pengguna dikonversi menjadi angka desimal. Misalnya, jika pengguna memasukkan "3", maka akan diubah menjadi 3.0 untuk memastikan bahwa semua jenis angka (baik desimal maupun bulat) dapat diproses.

2. Membandingkan Bilangan
Langkah berikutnya adalah mencari bilangan terbesar di antara A, B, dan C dengan menggunakan pernyataan if-else.
if A > B:
    if A > C:
        terbesar = A
    else:
        terbesar = C
else:
    if B > C:
        terbesar = B
    else:
        terbesar = C
Logika dari perbandingan ini adalah sebagai berikut:

Langkah Pertama: Cek apakah A lebih besar dari B.
Jika A lebih besar dari B (kondisi if A > B bernilai benar):
Kemudian, program memeriksa apakah A juga lebih besar dari C.
Jika A lebih besar dari C: Maka A adalah bilangan terbesar, dan terbesar diset menjadi A.
Jika A tidak lebih besar dari C: Maka C adalah bilangan terbesar, dan terbesar diset menjadi C.
Jika A tidak lebih besar dari B (kondisi if A > B bernilai salah):
Ini berarti B lebih besar atau sama dengan A. Program kemudian memeriksa apakah B lebih besar dari C.
Jika B lebih besar dari C: Maka B adalah bilangan terbesar, dan terbesar diset menjadi B.
Jika B tidak lebih besar dari C: Maka C adalah bilangan terbesar, dan terbesar diset menjadi C.

3. Menampilkan Hasil
Setelah proses perbandingan selesai, variabel terbesar akan berisi bilangan terbesar di antara A, B, dan C. Program kemudian mencetak hasilnya.
print("Bilangan terbesar adalah:", terbesar)
Contoh Eksekusi
Misalkan kita memasukkan:
A = 10
B = 25
C = 15
Maka langkah-langkahnya akan berjalan seperti berikut:

Program mengecek apakah A > B, yaitu 10 > 25. Ini salah, jadi program melanjutkan ke else.
Dalam else, program mengecek apakah B > C, yaitu 25 > 15. Ini benar, jadi terbesar diset ke B, yang bernilai 25.
Program kemudian menampilkan hasil: Bilangan terbesar adalah: 25.0.
Ringkasan
Kode ini menggunakan struktur if-else bertingkat untuk membandingkan tiga bilangan dan menentukan yang terbesar.


(PENJELASAN CODE 2)

Meminta Input Jumlah Bilangan
N = int(input("Masukkan jumlah bilangan (N): "))
Program meminta pengguna untuk memasukkan berapa banyak bilangan yang akan dimasukkan. Nilai ini disimpan dalam variabel N.
int(input(...)) digunakan untuk mengonversi input dari pengguna menjadi bilangan bulat (integer). Hal ini memastikan bahwa N adalah sebuah angka bulat yang menunjukkan jumlah iterasi atau pengulangan yang akan dilakukan.

2. Inisialisasi Variabel max_value untuk Nilai Maksimum
max_value = 0
Variabel max_value diinisialisasi dengan nilai 0. Variabel ini akan digunakan untuk menyimpan bilangan terbesar yang ditemukan selama proses pengulangan.
Pada awalnya, max_value diberi nilai 0, tetapi nantinya akan diperbarui jika bilangan yang dimasukkan pengguna lebih besar dari 0 atau dari nilai terbesar sebelumnya.

3. Inisialisasi Counter i
i = 1
Variabel i digunakan sebagai counter atau penghitung yang akan membantu dalam menjalankan pengulangan sebanyak N kali.
i dimulai dari 1 karena kita akan mulai memasukkan bilangan pertama sampai bilangan ke-N.

4. Memulai Pengulangan dengan while Loop
while i <= N:
Loop while akan terus berjalan selama i lebih kecil atau sama dengan N.
Karena N adalah jumlah bilangan yang ingin dimasukkan pengguna, maka loop ini akan memastikan pengguna memasukkan bilangan sebanyak N kali.

5. Meminta Input Bilangan dalam Loop
bilangan = float(input(f"Masukkan bilangan ke-{i}: "))
Di dalam loop, program meminta pengguna untuk memasukkan sebuah bilangan, dan menyimpannya dalam variabel bilangan.
float(input(...)) digunakan untuk memastikan bahwa nilai yang dimasukkan oleh pengguna dianggap sebagai bilangan desimal, sehingga dapat menangani angka-angka yang memiliki nilai desimal (misalnya 5.7).
{i} pada f"Masukkan bilangan ke-{i}: " digunakan untuk menampilkan nomor urut bilangan yang sedang dimasukkan oleh pengguna (bilangan ke-1, ke-2, dst.).

6. Mengecek Apakah Bilangan yang Dimasukkan Lebih Besar dari max_value
if bilangan > max_value:
    max_value = bilangan
Setelah bilangan dimasukkan, program mengecek apakah bilangan tersebut lebih besar dari nilai max_value yang tersimpan saat ini.

Jika benar (bilangan lebih besar dari max_value), maka max_value diperbarui dengan nilai bilangan tersebut.
Jika tidak (bilangan lebih kecil atau sama dengan max_value), maka max_value tidak diubah.
Contoh: Misalnya max_value sekarang adalah 10, dan pengguna memasukkan 15. Karena 15 lebih besar dari 10, max_value diperbarui menjadi 15.

7. Menambahkan Nilai Counter i
i += 1
Setelah memproses bilangan yang baru dimasukkan, program menambahkan nilai i sebanyak 1.
Ini berarti kita akan beralih ke bilangan berikutnya (bilangan ke-2, ke-3, dan seterusnya), sampai kita mencapai jumlah N.

8. Menampilkan Nilai Maksimum setelah Loop Berakhir
print("Nilai maksimum adalah:", max_value)
Setelah loop while selesai (artinya kita sudah memasukkan semua bilangan sebanyak N kali), program akan mencetak nilai max_value, yang merupakan bilangan terbesar di antara semua bilangan yang dimasukkan pengguna.
Contoh Eksekusi
Misalkan:

N = 3, artinya pengguna ingin memasukkan 3 bilangan.
Pengguna memasukkan bilangan 5, 10, dan 7.
Langkah-langkah yang terjadi adalah:

i = 1: Program meminta input 5. Karena 5 > 0, max_value menjadi 5.
i = 2: Program meminta input 10. Karena 10 > 5, max_value menjadi 10.
i = 3: Program meminta input 7. Karena 7 < 10, max_value tetap 10.
Setelah selesai, program akan mencetak:

Nilai maksimum adalah: 10.0
Ringkasan
Kode ini digunakan untuk mencari bilangan terbesar di antara beberapa bilangan yang dimasukkan pengguna, menggunakan loop while dan variabel max_value untuk menyimpan bilangan terbesar yang ditemukan selama pengulangan.













