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
    <strong>Amelia Azmi</strong>
    <br>
    <strong>2311102135</strong>
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

Dalam pembuatan website, tampilan dan struktur merupakan dua aspek yang sangat penting. HTML digunakan untuk membangun kerangka dasar halaman, sedangkan CSS digunakan untuk mengatur tampilan visual agar lebih menarik.

HTML berfungsi sebagai fondasi utama yang menyusun berbagai elemen seperti teks, gambar, dan bagian halaman. Dengan HTML, konten dapat diorganisasi dengan rapi sehingga mudah dipahami oleh browser.

CSS digunakan untuk mempercantik tampilan tersebut. Dengan CSS, pengembang dapat mengatur warna, ukuran, efek visual, hingga animasi. Hal ini membuat tampilan website menjadi lebih hidup dan tidak monoton.

Selain itu, CSS modern mendukung efek seperti blur, transparansi, dan bayangan yang dapat menghasilkan desain bergaya modern seperti glassmorphism. Teknik ini memberikan kesan elegan dan futuristik pada tampilan halaman.

Penggunaan kombinasi HTML dan CSS memungkinkan pembuatan tampilan kreatif sesuai kebutuhan, termasuk desain bertema tertentu seperti perayaan Imlek dengan dominasi warna merah dan emas.

# Tugas 3
## 1. Source Kode html
```
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Imlek Card Modern</title>

    <!-- Google Font -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">

    <!-- CSS -->
    <link rel="stylesheet" href="imlek.css">
</head>
<body>

    <div class="container">
        <div class="card">

            <!-- dekorasi lingkaran -->
            <div class="glow-circle"></div>

            <!-- teks -->
            <h1>新年快乐</h1>
            <h2>Happy Lunar New Year</h2>

            <p>
                Semoga tahun ini membawa <br>
                kebahagiaan, kesehatan, <br>
                dan keberuntungan ✨
            </p>

            <!-- button -->
            <button>Best Wishes</button>

        </div>
    </div>

</body>
</html>
```
## 2. Source Kode css

```
/* RESET */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* BODY */
body {
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;

    font-family: 'Poppins', sans-serif;

    background: linear-gradient(135deg, #8b0000, #ff0000);
}

/* CONTAINER */
.container {
    perspective: 1000px;
}

/* CARD */
.card {
    width: 320px;
    height: 420px;
    padding: 30px;

    text-align: center;
    color: white;

    border-radius: 20px;

    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(12px);

    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.5);

    transition: 0.4s ease;
}

/* HOVER EFFECT */
.card:hover {
    transform: scale(1.05) rotateY(8deg);
}

/* GLOW CIRCLE */
.glow-circle {
    width: 80px;
    height: 80px;

    margin: 0 auto 20px auto;

    background: gold;
    border-radius: 50%;

    box-shadow: 
        0 0 20px gold,
        0 0 40px gold,
        0 0 60px rgba(255, 215, 0, 0.6);
}

/* TEXT */
h1 {
    font-size: 36px;
    color: gold;
}

h2 {
    font-size: 16px;
    margin: 10px 0 15px;
    font-weight: 400;
}

p {
    font-size: 14px;
    line-height: 1.6;
    margin-bottom: 25px;
}

/* BUTTON */
button {
    padding: 10px 20px;
    border: none;
    border-radius: 20px;

    background: gold;
    color: black;
    font-weight: 600;

    cursor: pointer;

    transition: 0.3s;
}

/* BUTTON HOVER */
button:hover {
    background: white;
    transform: scale(1.05);
}
```
Output:
<img src="lunar.png" alt="preview" style="width:100%; max-width:900px;">

# Penjelasan
Program ini menampilkan desain kartu ucapan digital dengan gaya modern menggunakan HTML dan CSS. Struktur halaman terdiri dari satu elemen utama berupa kartu yang berada di tengah layar.

Tampilan dibuat menggunakan konsep glassmorphism dengan efek transparansi dan blur sehingga memberikan kesan modern. Elemen lingkaran di bagian atas berfungsi sebagai dekorasi dengan efek cahaya.

CSS digunakan untuk mengatur posisi, warna, dan efek visual seperti bayangan serta animasi hover. Saat kursor diarahkan ke kartu, elemen akan sedikit berputar dan membesar sehingga terlihat interaktif.

Warna merah dan emas digunakan untuk memperkuat nuansa Imlek. Kombinasi warna ini memberikan kesan elegan sekaligus sesuai dengan tema perayaan.

Secara keseluruhan, program ini menunjukkan bagaimana CSS modern dapat digunakan untuk menciptakan desain yang menarik tanpa memerlukan JavaScript.