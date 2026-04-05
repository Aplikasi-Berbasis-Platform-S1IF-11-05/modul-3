<div align="center">
  <br />
  <h1>LAPORAN PRAKTIKUM <br> APLIKASI BERBASIS PLATFORM </h1>
  <br />
  <h3>MODUL 3 <br> CSS </h3>
  <br />
  <img width="512" height="512" alt="telyu" src="https://github.com/user-attachments/assets/724a3291-bcf9-448d-a395-3886a8659d79" />
  <br />
  <br />
  <br />
  <h3>Disusun Oleh :</h3>
  <p>
    <strong>Arsya Fathiha Rahman</strong>
    <br>
    <strong>2311102152</strong>
    <br>
    <strong>S1 IF-11-REG05</strong>
  </p>
  <br />
  <h3>Dosen Pengampu :</h3>
  <p>
    <strong>Dedi Agung Prabowo, S.Kom., M.Kom</strong>
  </p>
  <br />
  <br />
  <h4>Asisten Praktikum :</h4>
  <strong>Apri Pandu Wicaksono </strong>
  <br>
  <strong>Hamka Zaenul Ardi</strong>
  <br />
  <h3>LABORATORIUM HIGH PERFORMANCE <br>FAKULTAS INFORMATIKA <br>UNIVERSITAS TELKOM PURWOKERTO <br>2026 </h3>
</div>

<hr>

# Dasar Teori

HTML (HyperText Markup Language) merupakan bahasa markup yang digunakan untuk menyusun struktur dasar sebuah halaman web. HTML berfungsi untuk menentukan elemen-elemen seperti judul, paragraf, gambar, serta pembagian bagian halaman menggunakan tag tertentu. Dengan HTML, konten dapat disusun secara terstruktur sehingga mudah dipahami baik oleh browser maupun pengguna.

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mengatur tampilan visual dari elemen HTML. CSS memungkinkan pengembang untuk mengatur warna, ukuran, posisi, jarak, hingga efek visual seperti bayangan dan animasi. Dengan adanya CSS, tampilan halaman web dapat dibuat lebih menarik, konsisten, dan sesuai dengan kebutuhan desain tanpa mengubah struktur HTML.

Dalam pengembangan web modern, HTML dan CSS memiliki peran yang saling melengkapi. HTML berfokus pada struktur dan isi, sedangkan CSS berfokus pada presentasi. Pemisahan ini membuat kode menjadi lebih rapi, mudah dikelola, dan memudahkan dalam pengembangan lebih lanjut.

Selain itu, CSS juga mendukung berbagai teknik layout seperti Flexbox dan Grid yang digunakan untuk mengatur posisi elemen secara fleksibel dan responsif. Penggunaan properti seperti box-shadow, border-radius, dan gradient memungkinkan pembuatan desain yang lebih estetis dan interaktif.

Pada implementasi desain halaman bertema Imlek, CSS dimanfaatkan untuk menciptakan identitas visual melalui penggunaan warna merah dan emas yang melambangkan keberuntungan dan kemakmuran. Efek bayangan, gradasi warna, serta pengaturan tata letak digunakan untuk menghasilkan tampilan yang tidak hanya menarik, tetapi juga memberikan pengalaman visual yang lebih hidup bagi pengguna.
# Tugas 3
## 1. Source Kode html
```
//2311102152
//Arsya Fathiha Rahman
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Imlek Book Ornamental</title>
    <link rel="stylesheet" href="lunar.css">
</head>
<body>

    <div class="book">

        <!-- halaman kiri -->
        <div class="page left">
            <h2>新年快乐</h2>

            <p class="small">
                Ga harus sempurna,<br>
                yang penting tetap jalan.
            </p>

            <!-- bunga -->
            <div class="flower"></div>
        </div>

        <!-- halaman kanan -->
        <div class="page right">

            <!-- lampion -->
            <div class="lantern l1"></div>
            <div class="lantern l2"></div>

            <h1>LUNAR FESTIVAL</h1>

            <p class="text">
                Semoga tahun ini lebih ringan,<br>
                tanpa harus buru-buru.<br><br>

                Yang penting tetap ada arah,<br>
                dan tetap punya tujuan.
            </p>

            <div class="line"></div>

            <span class="sign">— Amanda</span>

        </div>

    </div>

</body>
</html>
```
## 2. Source Kode css

```
body {
    margin: 0;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    font-family: 'Poppins', sans-serif;

    background: linear-gradient(135deg, #ffd6e0, #ff99cc, #ff66b2);
}

/* BOOK */
.book {
    display: flex;
    width: 650px;
    height: 380px;
    box-shadow: 0 20px 60px rgba(255, 0, 0, 0.4);
    transition: 0.3s;
}

/* PAGE */
.page {
    width: 50%;
    padding: 30px;
    position: relative;
}

/* KIRI */
.left {
    background: linear-gradient(145deg, #ff4d6d, #b30000);
    color: white;

    border-top-left-radius: 15px;
    border-bottom-left-radius: 15px;

    box-shadow: inset -8px 0 20px rgba(0,0,0,0.6);
}

/* KANAN */
.right {
    background: linear-gradient(145deg, #ff0033, #990000);
    color: white;

    border-top-right-radius: 15px;
    border-bottom-right-radius: 15px;

    box-shadow: inset 8px 0 20px rgba(0,0,0,0.6);
}

/* judul kiri */
.left h2 {
    text-align: center;
    font-size: 42px;
    color: gold;
}

/* teks kecil */
.small {
    text-align: center;
    margin-top: 20px;
    font-size: 14px;
}

/* bunga */
.flower {
    position: absolute;
    bottom: 20px;
    left: 20px;
    width: 80px;
    height: 80px;
    border: 2px solid gold;
    border-radius: 50%;
    opacity: 0.5;
}

/* judul kanan */
.right h1 {
    color: gold;
    text-align: center;
    margin-top: 40px;
}

/* isi */
.text {
    font-size: 14px;
    line-height: 1.8;
    margin-top: 20px;
}

/* garis */
.line {
    width: 50px;
    height: 2px;
    background: gold;
    margin: 20px auto;
}

/* sign */
.sign {
    display: block;
    text-align: center;
    font-size: 12px;
}

/* LANTERN */
.lantern {
    position: absolute;
    width: 35px;
    height: 45px;
    background: red;
    border-radius: 50%;
    border: 2px solid gold;
}

.lantern::after {
    content: "";
    position: absolute;
    bottom: -10px;
    left: 50%;
    width: 3px;
    height: 10px;
    background: gold;
    transform: translateX(-50%);
}

/* posisi lampion */
.l1 {
    top: 20px;
    left: 20px;
}

.l2 {
    top: 20px;
    right: 20px;
}

/* hover */
.book:hover {
    transform: scale(1.04);
}
```
Output:
<img src="lunar.png" alt="preview" style="width:100%; max-width:900px;">
<img width="1445" height="854" alt="lunar png" src="https://github.com/user-attachments/assets/c6958108-f2cd-409d-8273-80036df3affb" />

# Penjelasan
Program ini dibuat menggunakan HTML dan CSS untuk menghasilkan tampilan halaman web yang menyerupai sebuah buku terbuka dengan tema Imlek. Struktur utama pada HTML terdiri dari elemen div dengan class book yang berfungsi sebagai wadah utama. Di dalamnya terdapat dua elemen div dengan class page left dan page right yang merepresentasikan halaman kiri dan halaman kanan dari sebuah buku.

Pada bagian halaman kiri (left), ditampilkan teks sederhana berupa karakter Tiongkok “新年快乐” yang berarti Selamat Tahun Baru, serta kalimat singkat sebagai pengantar. Sedangkan pada halaman kanan (right), ditampilkan judul utama “Gong Xi Fa Cai”, isi ucapan, garis pemisah, dan tanda tangan sebagai penutup. Pembagian ini bertujuan untuk memberikan kesan seperti membaca isi buku yang terbagi menjadi dua halaman.

Dari sisi CSS, tampilan buku dibuat menggunakan properti display: flex pada class .book untuk menyusun kedua halaman secara berdampingan. Masing-masing halaman diberi lebar 50% agar terlihat seimbang seperti buku asli. Warna yang digunakan didominasi oleh gradasi merah untuk menyesuaikan dengan tema Imlek, serta ditambahkan warna emas sebagai aksen agar terlihat lebih elegan.

Efek visual seperti box-shadow digunakan untuk menciptakan kesan kedalaman, khususnya pada bagian dalam halaman (inset shadow) yang memberikan ilusi lipatan di tengah buku. Selain itu, border-radius diterapkan pada sisi luar halaman untuk memberikan bentuk yang lebih halus dan menyerupai buku nyata.

Interaksi sederhana juga ditambahkan melalui efek hover pada elemen .book, yaitu perubahan skala (scale) saat kursor diarahkan ke objek. Efek ini memberikan kesan interaktif dan membuat tampilan lebih dinamis meskipun tidak menggunakan JavaScript.

Secara keseluruhan, kombinasi antara HTML dan CSS pada program ini berhasil menghasilkan desain yang unik dan berbeda, yaitu tampilan berbentuk buku terbuka dengan nuansa Imlek yang kuat melalui penggunaan warna, tata letak, dan elemen visual yang mendukung konsep tersebut.
