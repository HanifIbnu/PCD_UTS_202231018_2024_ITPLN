
## Laporan Pengolahan Citra Digital C


DETEKSI WARNA PADA CITRA

Model warna RGB adalah model warna
berdasarkan konsep penambahan kuat cahaya
primer yaitu red, green dan blue. Dalam suatu
ruang yang sama sekali tidak ada cahaya, maka
ruangan tersebut adalah gelap total. Tidak ada
signal gelombang cahaya yang diserap oleh mata
kita atau RGB (0, 0, 0). Apabila kita
menambahkan cahaya merah pada ruangan
tersebut, maka ruangan akan berubah warna
menjadi merah misalnya RGB (255, 0, 0), semua
benda dalam ruangan tersebut hanya dapat terlihat
berwarna merah. Demikian apabila cahaya kita
ganti dengan hijau atau biru.


## Screenshots

![App Screenshot]![Screenshot 2024-05-11 061507](https://github.com/HanifIbnu/PCD_UTS_202231018_2024_ITPLN/assets/147982399/64ce4c18-8da3-4870-b87f-b97755c31136)


## Penjelasan Program

    cv2: Baris ini mengimpor pustaka OpenCV, yang biasa digunakan untuk tugas-tugas computer vision seperti pemrosesan dan analisis gambar.
    numpy as np: Baris ini mengimpor pustaka NumPy, yang menyediakan array efisien dan fungsi matematika yang digunakan untuk manipulasi gambar dan analisis data.
    from matplotlib import pyplot as plt: Baris ini mengimpor modul pyplot dari pustaka Matplotlib, yang digunakan untuk membuat visualisasi seperti histogram dan plot.

    color_image = cv2.imread('myname.jpeg'): Baris ini membaca file gambar bernama 'myname.jpeg' menggunakan fungsi cv2.imread dari OpenCV. Fungsi ini memuat data gambar ke dalam array NumPy, di mana setiap piksel diwakili oleh saluran warnanya (Merah, Hijau, Biru). Pastikan file gambar 'myname.jpeg' berada di direktori yang sama dengan skrip Python.

    r = color_image[:, :, 0]
    g = color_image[:, :, 1]
    b = color_image[:, :, 2]
    Baris-baris ini mengekstrak masing-masing saluran warna   (Merah, Hijau, Biru) dari gambar berwarna yang dimuat. [:, :, 0] memilih saluran pertama (indeks 0) dari array NumPy 3D, yang sesuai dengan saluran Merah. Demikian pula, [:, :, 1] memilih saluran Hijau (indeks 1) dan [:, :, 2] memilih saluran Biru (indeks 2)

    plt.subplots(1, 4, figsize = (20,10)): Baris ini membuat figure Matplotlib dengan 1 baris dan 4 kolom (grid 1x4) untuk subplot. Ini juga mengatur ukuran gambar menjadi lebar 20 inci dan tinggi 10 inci.
    c1, c2, c3, c4: Baris ini membongkar nilai yang dikembalikan dari plt.subplots menjadi empat variabel. Variabel-variabel ini mewakili sumbu dari keempat subplot di dalam grid.

    Baris-baris berikut mengatur judul, menampilkan gambar, dan mematikan sumbu untuk setiap subplot:

    c1.set_title(...): Menetapkan judul untuk subplot pertama (kiri atas) sebagai 'Gambar Asli' (Original Image).
    c1.imshow(color_image): Menampilkan gambar berwarna asli di subplot pertama.
    c1.axis('off'): Mematikan sumbu (x dan y) untuk subplot pertama, menghasilkan tampilan gambar yang lebih bersih tanpa garis yang tidak perlu.
    Operasi serupa dilakukan untuk subplot 2, 3, dan 4, menyetel judul ke 'Merah' (Red), 'Hijau' (Green), dan 'Biru' (Blue), dan menampilkan gambar saluran Merah, Hijau, dan Biru yang diekstrak dalam skala abu-abu menggunakan argumen cmap="gray".




## Penjelasan Materi

Dalam deteksi warna citra yang dilakukan dalam program ini, kita menggunakan citra warna sebagai data masukan. Citra warna umumnya terdiri dari tiga saluran warna utama: merah (R), hijau (G), dan biru (B). Setiap piksel dalam citra direpresentasikan oleh kombinasi intensitas ketiga saluran warna ini, yang membentuk warna yang kita lihat.

Dalam proses analisis yang dilakukan dalam program, langkah-langkahnya adalah sebagai berikut:

   Memuat Citra: Pertama, citra warna dimuat ke dalam program menggunakan fungsi cv2.imread() dari OpenCV. Citra ini direpresentasikan dalam bentuk array NumPy, di mana setiap elemen array mewakili nilai piksel dalam citra, termasuk saluran warna merah, hijau, dan biru.

   Pemisahan Saluran Warna: Setelah citra dimuat, langkah selanjutnya adalah memisahkan citra menjadi tiga saluran warna utama: merah, hijau, dan biru. Hal ini dilakukan dengan menggunakan indexing pada array NumPy. Misalnya, color_image[:, :, 0] mengambil saluran warna merah, color_image[:, :, 1] mengambil saluran warna hijau, dan color_image[:, :, 2] mengambil saluran warna biru.

   Tampilan Pemisahan Saluran Warna: Setelah pemisahan, setiap saluran warna ditampilkan secara terpisah menggunakan matplotlib.pyplot.imshow(). Pengaturan colormap 'gray' digunakan untuk menampilkan setiap saluran warna dalam skala keabuan. Ini memungkinkan kita untuk melihat kontribusi masing-masing saluran warna terhadap citra asli secara terpisah.

   Analisis Visual: Dengan menampilkan masing-masing saluran warna secara terpisah, kita dapat melihat kontribusi relatif dari masing-masing warna terhadap citra asli. Misalnya, jika terdapat objek dengan warna dominan merah, saluran merah akan menunjukkan intensitas yang tinggi di daerah tersebut. Hal ini memungkinkan kita untuk menganalisis distribusi warna dalam citra dan memahami bagaimana warna-warna tersebut berkontribusi terhadap keseluruhan gambar.
## Screenshots

![App Screenshot]![Screenshot 2024-05-11 070314](https://github.com/HanifIbnu/PCD_UTS_202231018_2024_ITPLN/assets/147982399/d83ddcfa-e9ca-418a-9689-4d6788f3cfd1)

## Penjelasan Program

    cv2: Baris ini mengimpor pustaka OpenCV, yang biasa digunakan untuk tugas-tugas computer vision seperti pemrosesan dan analisis gambar.
    numpy as np: Baris ini mengimpor pustaka NumPy, yang menyediakan array efisien dan fungsi matematika yang digunakan untuk manipulasi gambar dan analisis data.
    from matplotlib import pyplot as plt: Baris ini mengimpor modul pyplot dari pustaka Matplotlib, yang digunakan untuk membuat visualisasi seperti histogram dan plot.

    color_image = cv2.imread('myname.jpeg'): Baris ini membaca file gambar bernama 'myname.jpeg' menggunakan fungsi cv2.imread dari OpenCV. Fungsi ini memuat data gambar ke dalam array NumPy, di mana setiap piksel diwakili oleh saluran warnanya (Merah, Hijau, Biru). Pastikan file gambar 'myname.jpeg' berada di direktori yang sama dengan skrip Python.

    r = color_image[:, :, 0]
    g = color_image[:, :, 1]
    b = color_image[:, :, 2]
    Baris-baris ini mengekstrak masing-masing saluran warna   (Merah, Hijau, Biru) dari gambar berwarna yang dimuat. [:, :, 0] memilih saluran pertama (indeks 0) dari array NumPy 3D, yang sesuai dengan saluran Merah. Demikian pula, [:, :, 1] memilih saluran Hijau (indeks 1) dan [:, :, 2] memilih saluran Biru (indeks 2)

    plt.subplots(1, 4, figsize = (20,10)): Baris ini membuat figure Matplotlib dengan 1 baris dan 4 kolom (grid 1x4) untuk subplot. Ini juga mengatur ukuran gambar menjadi lebar 20 inci dan tinggi 10 inci.
    c1, c2, c3, c4: Baris ini membongkar nilai yang dikembalikan dari plt.subplots menjadi empat variabel. Variabel-variabel ini mewakili sumbu dari keempat subplot di dalam grid.

    Baris-baris berikut mengatur judul, menampilkan gambar, dan mematikan sumbu untuk setiap subplot:

    c1.set_title(...): Menetapkan judul untuk subplot pertama (kiri atas) sebagai 'Gambar Asli' (Original Image).
    c1.imshow(color_image): Menampilkan gambar berwarna asli di subplot pertama.
    c1.axis('off'): Mematikan sumbu (x dan y) untuk subplot pertama, menghasilkan tampilan gambar yang lebih bersih tanpa garis yang tidak perlu.
    Operasi serupa dilakukan untuk subplot 2, 3, dan 4, menyetel judul ke 'Merah' (Red), 'Hijau' (Green), dan 'Biru' (Blue), dan menampilkan gambar saluran Merah, Hijau, dan Biru yang diekstrak dalam skala abu-abu menggunakan argumen cmap="gray".




## Penjelasan Materi

Dalam deteksi warna citra yang dilakukan dalam program ini, kita menggunakan citra warna sebagai data masukan. Citra warna umumnya terdiri dari tiga saluran warna utama: merah (R), hijau (G), dan biru (B). Setiap piksel dalam citra direpresentasikan oleh kombinasi intensitas ketiga saluran warna ini, yang membentuk warna yang kita lihat.

Dalam proses analisis yang dilakukan dalam program, langkah-langkahnya adalah sebagai berikut:

   Memuat Citra: Pertama, citra warna dimuat ke dalam program menggunakan fungsi cv2.imread() dari OpenCV. Citra ini direpresentasikan dalam bentuk array NumPy, di mana setiap elemen array mewakili nilai piksel dalam citra, termasuk saluran warna merah, hijau, dan biru.

   Pemisahan Saluran Warna: Setelah citra dimuat, langkah selanjutnya adalah memisahkan citra menjadi tiga saluran warna utama: merah, hijau, dan biru. Hal ini dilakukan dengan menggunakan indexing pada array NumPy. Misalnya, color_image[:, :, 0] mengambil saluran warna merah, color_image[:, :, 1] mengambil saluran warna hijau, dan color_image[:, :, 2] mengambil saluran warna biru.

   Tampilan Pemisahan Saluran Warna: Setelah pemisahan, setiap saluran warna ditampilkan secara terpisah menggunakan matplotlib.pyplot.imshow(). Pengaturan colormap 'gray' digunakan untuk menampilkan setiap saluran warna dalam skala keabuan. Ini memungkinkan kita untuk melihat kontribusi masing-masing saluran warna terhadap citra asli secara terpisah.

   Analisis Visual: Dengan menampilkan masing-masing saluran warna secara terpisah, kita dapat melihat kontribusi relatif dari masing-masing warna terhadap citra asli. Misalnya, jika terdapat objek dengan warna dominan merah, saluran merah akan menunjukkan intensitas yang tinggi di daerah tersebut. Hal ini memungkinkan kita untuk menganalisis distribusi warna dalam citra dan memahami bagaimana warna-warna tersebut berkontribusi terhadap keseluruhan gambar.
## Penjelasan Program

    cv2: Baris ini mengimpor pustaka OpenCV, yang biasa digunakan untuk tugas-tugas computer vision seperti pemrosesan dan analisis gambar.
    numpy as np: Baris ini mengimpor pustaka NumPy, yang menyediakan array efisien dan fungsi matematika yang digunakan untuk manipulasi gambar dan analisis data.
    from matplotlib import pyplot as plt: Baris ini mengimpor modul pyplot dari pustaka Matplotlib, yang digunakan untuk membuat visualisasi seperti histogram dan plot.

    color_image = cv2.imread('myname.jpeg'): Baris ini membaca file gambar bernama 'myname.jpeg' menggunakan fungsi cv2.imread dari OpenCV. Fungsi ini memuat data gambar ke dalam array NumPy, di mana setiap piksel diwakili oleh saluran warnanya (Merah, Hijau, Biru). Pastikan file gambar 'myname.jpeg' berada di direktori yang sama dengan skrip Python.

    r = color_image[:, :, 0]
    g = color_image[:, :, 1]
    b = color_image[:, :, 2]
    Baris-baris ini mengekstrak masing-masing saluran warna   (Merah, Hijau, Biru) dari gambar berwarna yang dimuat. [:, :, 0] memilih saluran pertama (indeks 0) dari array NumPy 3D, yang sesuai dengan saluran Merah. Demikian pula, [:, :, 1] memilih saluran Hijau (indeks 1) dan [:, :, 2] memilih saluran Biru (indeks 2)

    plt.subplots(1, 4, figsize = (20,10)): Baris ini membuat figure Matplotlib dengan 1 baris dan 4 kolom (grid 1x4) untuk subplot. Ini juga mengatur ukuran gambar menjadi lebar 20 inci dan tinggi 10 inci.
    c1, c2, c3, c4: Baris ini membongkar nilai yang dikembalikan dari plt.subplots menjadi empat variabel. Variabel-variabel ini mewakili sumbu dari keempat subplot di dalam grid.

    Baris-baris berikut mengatur judul, menampilkan gambar, dan mematikan sumbu untuk setiap subplot:

    c1.set_title(...): Menetapkan judul untuk subplot pertama (kiri atas) sebagai 'Gambar Asli' (Original Image).
    c1.imshow(color_image): Menampilkan gambar berwarna asli di subplot pertama.
    c1.axis('off'): Mematikan sumbu (x dan y) untuk subplot pertama, menghasilkan tampilan gambar yang lebih bersih tanpa garis yang tidak perlu.
    Operasi serupa dilakukan untuk subplot 2, 3, dan 4, menyetel judul ke 'Merah' (Red), 'Hijau' (Green), dan 'Biru' (Blue), dan menampilkan gambar saluran Merah, Hijau, dan Biru yang diekstrak dalam skala abu-abu menggunakan argumen cmap="gray".




## Penjelasan Materi

Dalam deteksi warna citra yang dilakukan dalam program ini, kita menggunakan citra warna sebagai data masukan. Citra warna umumnya terdiri dari tiga saluran warna utama: merah (R), hijau (G), dan biru (B). Setiap piksel dalam citra direpresentasikan oleh kombinasi intensitas ketiga saluran warna ini, yang membentuk warna yang kita lihat.

Dalam proses analisis yang dilakukan dalam program, langkah-langkahnya adalah sebagai berikut:

   Memuat Citra: Pertama, citra warna dimuat ke dalam program menggunakan fungsi cv2.imread() dari OpenCV. Citra ini direpresentasikan dalam bentuk array NumPy, di mana setiap elemen array mewakili nilai piksel dalam citra, termasuk saluran warna merah, hijau, dan biru.

   Pemisahan Saluran Warna: Setelah citra dimuat, langkah selanjutnya adalah memisahkan citra menjadi tiga saluran warna utama: merah, hijau, dan biru. Hal ini dilakukan dengan menggunakan indexing pada array NumPy. Misalnya, color_image[:, :, 0] mengambil saluran warna merah, color_image[:, :, 1] mengambil saluran warna hijau, dan color_image[:, :, 2] mengambil saluran warna biru.

   Tampilan Pemisahan Saluran Warna: Setelah pemisahan, setiap saluran warna ditampilkan secara terpisah menggunakan matplotlib.pyplot.imshow(). Pengaturan colormap 'gray' digunakan untuk menampilkan setiap saluran warna dalam skala keabuan. Ini memungkinkan kita untuk melihat kontribusi masing-masing saluran warna terhadap citra asli secara terpisah.

   Analisis Visual: Dengan menampilkan masing-masing saluran warna secara terpisah, kita dapat melihat kontribusi relatif dari masing-masing warna terhadap citra asli. Misalnya, jika terdapat objek dengan warna dominan merah, saluran merah akan menunjukkan intensitas yang tinggi di daerah tersebut. Hal ini memungkinkan kita untuk menganalisis distribusi warna dalam citra dan memahami bagaimana warna-warna tersebut berkontribusi terhadap keseluruhan gambar.
## Penjelasan program

    plt.figure(figsize=(20, 5)): Baris ini membuat figure Matplotlib baru dengan ukuran lebar 20 inci dan tinggi 5 inci.
    plt.subplot(141): Baris ini membuat subplot pertama pada grid 1x4 di figure yang baru dibuat.
    plt.title('Histogram Asli'): Menetapkan judul untuk subplot pertama sebagai 'Histogram Asli'.

    plt.hist(color_image.flatten()): Fungsi hist dari Matplotlib digunakan untuk membuat histogram. Argumen pertama color_image.flatten() mengubah array 3D gambar berwarna menjadi array 1D. Hal ini dikarenakan histogram menghitung distribusi intensitas untuk semua piksel (tanpa peduli warnanya).
    bins=256: Argumen bins menentukan jumlah bin yang digunakan untuk menghitung distribusi intensitas. Semakin banyak bin, histogram akan semakin detail, namun juga bisa semakin sulit dibaca. Nilai 256 dipilih karena sesuai dengan skala intensitas warna (0-255).
    range=[0,256]: Argumen range menentukan rentang nilai intensitas yang akan dihitung pada histogram. Disini program menggunakan range [0, 256] untuk mencakup seluruh skala warna yang mungkin ada pada gambar.
    color='gray': Argumen color menentukan warna untuk menampilkan histogram. Dalam kasus ini, warna abu-abu dipilih.

    Baris selanjutnya plt.subplot(142), plt.subplot(143), dan plt.subplot(144) membuat subplot pada posisi ke-2, ke-3, dan ke-4 pada grid 1x4.
    plt.hist(r.flatten(), bins=256, range=[0,256], color='r'): Histogram dibuat khusus untuk deteksi warna merah (saluran R pada array r), ditandai dengan warna merah (color='r').
    plt.hist(g.flatten(), bins=256, range=[0,256], color='g'): Histogram dibuat khusus untuk deteksi warna hijau (saluran G pada array g), ditandai dengan warna hijau (color='g').
    plt.hist(b.flatten(), bins=256, range=[0,256], color='b'): Histogram dibuat khusus untuk deteksi warna biru (saluran B pada array b), ditandai dengan warna biru (color='b').


    plt.show(): Baris terakhir ini penting untuk menampilkan figure yang telah dibuat, yang berisi keempat subplot dan histogramnya.


## Penjelasan Materi

Histogram citra adalah grafik yang menggambarkan penyebaran nilai-nilai intensitas 
piksel dari suatu citra atau bagian tertentu di dalam citra. Dari histogram akan didapatkan
frekuensi kemunculan nisbi (relative) dari intensitas pada citra tersebut. Selain itu, histogram 
juga menunjukkan kecerahan (brightness) dan kontras (contrast) dari sebuah citra. Oleh karena 
itu, histogram dapat digunakan sebagai salah satu metode pengolahan citra yang bekerja secara 
kualitatif dan kuantitatif (Putra, 2010)

Histogram yang dihasilkan dari program tersebut memberikan representasi visual dari distribusi intensitas piksel dalam citra dan setiap saluran warna secara terpisah. Berikut adalah analisis dari setiap histogram:

   Histogram Asli: Ini adalah histogram dari citra asli setelah dikonversi ke dalam mode warna RGB yang sebelumnya dalam mode warna BGR. Histogram ini memberikan gambaran umum tentang bagaimana intensitas piksel tersebar di seluruh rentang nilai dari 0 hingga 255. Semakin tinggi puncak histogram pada suatu nilai intensitas, semakin banyak piksel dalam citra yang memiliki intensitas tersebut.

   Histogram Merah: Histogram merah mewakili distribusi intensitas piksel dalam saluran warna merah (R) dari citra. Puncak-puncak dalam histogram merah menunjukkan daerah-daerah di mana komponen merah dalam citra memiliki intensitas yang signifikan. Misalnya, jika terdapat banyak objek dengan warna dominan merah dalam citra, maka histogram merah akan memiliki puncak yang tinggi di sekitar nilai intensitas merah yang sesuai.
    Histogram merah menunjukkan distribusi data yang telah difilter berdasarkan warna merah. Sumbu x dibagi menjadi lima interval dengan lebar 50 unit, mulai dari 0 hingga 255. Sumbu y menunjukkan frekuensi data dalam setiap interval.

    Interval 0-50: Terdapat 10.000 data pada interval ini.
    Interval 50-100: Terdapat 20.000 data pada interval ini.
    Interval 100-150: Terdapat 30.000 data pada interval ini.
    Interval 150-200: Terdapat 20.000 data pada interval ini.
    Interval 200-250: Terdapat 10.000 data pada interval ini.

Dari histogram ini, dapat disimpulkan bahwa data merah terkonsentrasi di sekitar interval 150-200. Ini berarti bahwa sebagian besar data merah memiliki nilai antara 150 dan 200 dan jumlah data pada interval sekitar 20.000 data.

   Histogram Hijau: Histogram hijau mewakili distribusi intensitas piksel dalam saluran warna hijau (G) dari citra. Puncak-puncak dalam histogram hijau menunjukkan daerah-daerah di mana komponen hijau dalam citra memiliki intensitas yang signifikan. Misalnya, jika terdapat banyak objek dengan warna dominan hijau dalam citra, maka histogram hijau akan memiliki puncak yang tinggi di sekitar nilai intensitas hijau yang sesuai.
   Histogram hijau menunjukkan distribusi data yang telah difilter berdasarkan warna hijau. Sumbu x dibagi menjadi lima interval dengan lebar 50 unit, mulai dari 0 hingga 255. Sumbu y menunjukkan frekuensi data dalam setiap interval.

    Interval 0-50: Terdapat 5.000 data pada interval ini.
    Interval 50-100: Terdapat 10.000 data pada interval ini.
    Interval 100-150: Terdapat 20.000 data pada interval ini.
    Interval 150-200: Terdapat 10.000 data pada interval ini.
    Interval 200-250: Terdapat 5.000 data pada interval ini.

Dari histogram ini, dapat disimpulkan bahwa data hijau terkonsentrasi di sekitar interval interval 150-200. Ini berarti bahwa sebagian besar data merah memiliki nilai antara 150 dan 200 dan jumlah data pada interval sekitar 20.000 data.

   Histogram Biru: Histogram biru mewakili distribusi intensitas piksel dalam saluran warna biru (B) dari citra. Puncak-puncak dalam histogram biru menunjukkan daerah-daerah di mana komponen biru dalam citra memiliki intensitas yang signifikan. Misalnya, jika terdapat banyak objek dengan warna dominan biru dalam citra, maka histogram biru akan memiliki puncak yang tinggi di sekitar nilai intensitas biru yang sesuai.
   Histogram biru menunjukkan distribusi data yang telah difilter berdasarkan warna biru. Sumbu x dibagi menjadi lima interval dengan lebar 50 unit, mulai dari 0 hingga 255. Sumbu y menunjukkan frekuensi data dalam setiap interval.

    Interval 0-50: Terdapat 5.000 data pada interval ini.
    Interval 50-100: Terdapat 10.000 data pada interval ini.
    Interval 100-150: Terdapat 20.000 data pada interval ini.
    Interval 150-200: Terdapat 10.000 data pada interval ini.
    Interval 200-250: Terdapat 5.000 data pada interval ini.

Dari histogram ini, dapat disimpulkan bahwa data biru terkonsentrasi di sekitar interval 150-200. Ini berarti bahwa sebagian besar data merah memiliki nilai antara 150 dan 200 dan jumlah data pada interval sekitar 20.000 data.


NILAI AMBANG BATAS CITRA

   Segmentasi warna merupakan proses segmentasi dengan pendekatan daerah yang bekerja dengan menganalisis nilai warna dari tiap piksel pada citra dan membagi citra tersebut sesuai dengan fitur yang diinginkan. Segmentasi citra dengan deteksi warna HSV menurut
Gunanto (2009) menggunakan dasar seleksi warna pada model warna HSV dengan nilai toleransi tertentu. Pada metode segmentasi dengan deteksi warna HSV menurut Giannakupoulos (2008), dilakukan pemilihan sampel piksel sebagai acuan warna untuk membentuk segmen yang diinginkan. Citra digital menggunakan model warna RGB sebagai standar acuan warna, oleh karena itu proses awal pada metode ini memerlukan konversi model warna RGB ke HSV. Untuk membentuk segmen sesuai dengan warna yang diinginkan maka ditentukan nilai toleransi pada setiap dimensi warna HSV, kemudian nilai toleransi tersebut digunakan dalam perhitungan proses adaptive threshold. Hasil dari proses threshold tersebut akan membentuk segmen area
dengan warna sesuai toleransi yang diinginkan. 

## Screenshots

![App Screenshot]![Screenshot 2024-05-11 084649](https://github.com/HanifIbnu/PCD_UTS_202231018_2024_ITPLN/assets/147982399/af55917a-64ee-4152-8731-d7d031487f8d)
## Penjelasan Program

    Baris hsv_img = cv2.cvtColor(img, cv2.COLOR_BGR2HSV) mengonversi gambar dari format BGR (Blue-Green-Red) ke format HSV (Hue-Saturation-Value). Format HSV lebih cocok untuk deteksi warna karena memisahkan komponen warna (hue), intensitas (saturation), dan kecerahan (value) gambar.
    Variabel lower_red1, upper_red1, lower_red2, upper_red2, lower_blue, upper_blue, lower_green, dan upper_green mendefinisikan rentang nilai HSV untuk masing-masing warna yang ingin dideteksi.
    Contoh: lower_red1 = np.array([0, 100, 100]) berarti warna merah yang ingin dideteksi memiliki hue antara 0 dan 10, saturation minimal 100, dan value minimal 100.
    Dua rentang merah didefinisikan (lower_red1 dan upper_red1, lower_red2 dan upper_red2) untuk mendeteksi warna merah yang lebih luas agar citra lebih mudah untuk terbaca.
    Fungsi cv2.inRange(hsv_img, lower_range, upper_range) digunakan untuk membuat mask untuk setiap warna. Mask ini adalah gambar biner (hitam-putih) di mana piksel yang termasuk dalam rentang warna yang ditentukan diubah menjadi putih, dan sisanya menjadi hitam.

    mask1 = cv2.inRange(hsv_img, lower_red1, upper_red1) membuat mask untuk warna merah yang pertama didefinisikan.
    mask2 = cv2.inRange(hsv_img, lower_red2, upper_red2) membuat mask untuk warna merah yang kedua didefinisikan.
    Mask untuk biru dan hijau dibuat dengan cara yang sama menggunakan lower_blue, upper_blue, lower_green, dan upper_green.

    red_mask = cv2.bitwise_or(mask1, mask2) menggabungkan mask untuk warna merah pertama dan kedua dengan menggunakan operasi OR bitwise. Ini menghasilkan mask baru di mana piksel merah apa pun dari kedua rentang warna akan ditandai sebagai putih.
    result = cv2.bitwise_or(red_mask, cv2.bitwise_or(blue_mask, green_mask)) menggabungkan mask untuk merah, biru, dan hijau dengan menggunakan operasi OR bitwise.Yang mana hasilnya adalah mask baru di mana piksel merah, biru, atau hijau apa pun akan ditandai sebagai putih.

    fig, axs = plt.subplots(2, 2, figsize=(12, 12)) membuat figure Matplotlib dengan 2 baris dan 2 kolom untuk menampilkan gambar.
    axs[0, 0].imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB)) menampilkan gambar asli dalam format RGB.
    axs[0, 1].imshow(result, cmap='gray') menampilkan mask hasil deteksi (merah, biru, dan hijau) dalam skala abu-abu.
    axs[1, 0].imshow(red_blue_mask, cmap='gray') menampilkan mask untuk warna merah dan biru yang digabungkan dalam skala abu-abu.
    axs[1, 1].imshow(blue_mask, cmap='gray') menampilkan mask untuk warna biru dalam skala abu-abu.

    for ax in axs.flat: mematikan sumbu (x dan y) untuk semua subplot.
    plt.tight_layout() menata subplot agar pas di figure.
    plt.show() menampilkan figure yang berisi semua gambar dan mask.

Analisis Nilai Ambang Batas
    
    Merah:
    Bagian 1:
    lower_red1 = [0, 100, 100]:
    H (Hue): 0 mewakili warna merah murni.
    S (Saturation): 100 mewakili warna yang sepenuhnya jenuh (tidak pudar).
    V (Value): 100 mewakili warna yang cerah (tidak gelap).
    upper_red1 = [10, 255, 255]:
    H (Hue): 10 mewakili warna merah muda.
    S (Saturation): 255 mewakili semua tingkat saturasi.
    V (Value): 255 mewakili semua tingkat kecerahan.
    Bagian 2:
    lower_red2 = [160, 100, 100]:
    H (Hue): 160 mewakili warna merah marun.
    S (Saturation): 100 mewakili warna yang sepenuhnya jenuh (tidak pudar).
    V (Value): 100 mewakili warna yang cerah (tidak gelap).
    upper_red2 = [179, 255, 255]:
    H (Hue): 179 mewakili batas warna merah (sebelum beralih ke ungu).
    S (Saturation): 255 mewakili semua tingkat saturasi.
    V (Value): 255 mewakili semua tingkat kecerahan.
   
    Biru:
    lower_blue = [90, 50, 50]:
    H (Hue): 90 mewakili warna biru muda.
    S (Saturation): 50 mewakili warna yang agak jenuh (sedikit pudar).
    V (Value): 50 mewakili warna yang agak cerah (sedikit gelap)
    upper_blue = [130, 255, 255]:
    H (Hue): 130 mewakili batas warna biru (sebelum beralih ke hijau).
    S (Saturation): 255 mewakili semua tingkat saturasi.
    V (Value): 255 mewakili semua tingkat kecerahan.

    Hijau:
    lower_green = [35, 100, 100]:
    H (Hue): 35 mewakili warna hijau muda.
    S (Saturation): 100 mewakili warna yang sepenuhnya jenuh (tidak pudar).
    V (Value): 100 mewakili warna yang cerah (tidak gelap).
    upper_green = [90, 255, 255]:
    H (Hue): 90 mewakili batas warna hijau (sebelum beralih ke kuning).
    S (Saturation): 255 mewakili semua tingkat saturasi.
    V (Value): 255 mewakili semua tingkat kecerahan.
Nilai ambang batas yang dipilih dalam program ini didasarkan pada pemahaman tentang ruang warna HSV dan warna-warna yang ingin dideteksi.

    Merah:
        Bagian 1: Mencakup warna merah murni dan merah muda.
        Bagian 2: Mencakup warna merah marun dan batas atas warna merah.
    Biru:
        Mencakup warna biru muda hingga biru tua.
    Hijau:
        Mencakup warna hijau muda hingga hijau tua.

Pemilihan nilai ambang batas ini dapat diubah untuk menyesuaikan dengan gambar dan target deteksi warna yang berbeda


## Penjelasan Materi

Salah satu teknik dalam segmentasi citra digital adalah thresholding, yang bertujuan untuk mengubah citra dalam skala keabuan menjadi citra biner. Metode ini bekerja dengan menetapkan nilai ambang tertentu sehingga citra dapat dibagi menjadi dua bagian: bagian yang melebihi ambang tersebut dianggap sebagai objek, sedangkan bagian yang kurang dari ambang dianggap sebagai latar belakang. Dengan kata lain, thresholding melibatkan manipulasi nilai piksel untuk mencapai segmentasi yang diinginkan.

Prosesnya terdiri dari pemilihan nilai ambang yang sesuai dan meninjau hasil thresholding untuk memastikan bahwa segmentasi yang dihasilkan memenuhi kebutuhan. Pemilihan nilai ambang yang tepat adalah kunci keberhasilan dalam teknik ini. Berbagai metode telah dikembangkan untuk membantu dalam menentukan nilai ambang, seperti metode k-means, metode Otsu yang berdasarkan pada varians maksimum, atau metode berdasarkan pada entropi maksimum.

Salah satu tantangan dalam thresholding adalah ketika objek yang ingin disegmentasi memiliki intensitas yang mirip dengan latar belakang atau ada variasi intensitas yang besar dalam citra. Namun, penggunaan metode thresholding yang tepat dapat membantu mengatasi tantangan ini.

Secara khusus, dalam bidang tomografi terkomputasi, pengembangan telah dilakukan untuk menggunakan nilai ambang yang dapat mengambil informasi ambang dari radiografi, bukan hanya dari citra hasil rekonstruksi. Ini memungkinkan penggunaan thresholding yang lebih akurat untuk segmentasi citra tomografi, sehingga meningkatkan kualitas hasil segmentasi.
## Referensi Jurnal

http://eprints.itn.ac.id/8564/
https://www.academia.edu/download/35970079/04_Edit_Layout_RDKusmanto_JEE-Sept2011_Klasifikasi_Warna_2.pdf
https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=http://repository.unusa.ac.id/6416/1/Perancangan%2520Program%2520Penentuan%2520Histogram%2520Citra%2520dengan%2520Graphical%2520User%2520Interface%2520%2528GUI%2529.pdf&ved=2ahUKEwjqy7P5qISGAxUWb2wGHV1IAiMQFnoECA4QAw&usg=AOvVaw0cYt_9Ku51avJWu-0b4Pw7
https://ti.ukdw.ac.id/ojs/index.php/informatika/article/view/81
https://www.google.com/url?sa=t&source=web&rct=j&opi=89978449&url=https://ejournal.unib.ac.id/pseudocode/article/download/5857/2948/11576&ved=2ahUKEwjjv9rex4SGAxXGzzgGHVBBDFUQFnoECCIQAQ&usg=AOvVaw1IPmhyZnXQAuKumGYoTLmm
