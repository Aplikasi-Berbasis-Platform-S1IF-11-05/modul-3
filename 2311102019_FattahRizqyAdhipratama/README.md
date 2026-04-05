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
    <strong>Fattah Rizqy Adhipratama</strong>
    <br>
    <strong>2311102019</strong>
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

<p align="justify">
CSS (Cascading Style Sheets) merupakan bahasa yang digunakan untuk mengatur tampilan dan tata letak halaman web. CSS bekerja dengan cara memisahkan bagian struktur halaman yang dibuat menggunakan HTML dengan bagian desain atau tampilannya, seperti warna, ukuran teks, jarak antar elemen, dan posisi objek pada halaman.
</p>

<p align="justify">
Dengan menggunakan CSS, tampilan website menjadi lebih rapi, menarik, dan mudah dikelola. Selain itu, penggunaan CSS juga memudahkan pengembang ketika ingin melakukan perubahan desain karena cukup mengubah file stylesheet tanpa harus mengedit struktur HTML secara langsung.
</p>

<p align="justify">
CSS memiliki tiga cara penerapan, yaitu inline CSS, internal CSS, dan external CSS. Inline CSS ditulis langsung pada tag HTML, internal CSS ditulis di dalam tag <style> pada file HTML, sedangkan external CSS ditulis pada file terpisah dengan ekstensi .css. Dari ketiga cara tersebut, external CSS paling sering digunakan karena lebih efisien dan mudah digunakan kembali pada banyak halaman. Dalam penerapannya, CSS menggunakan selector untuk memilih elemen HTML yang akan diberikan gaya, lalu diikuti dengan properti dan nilai. Contohnya seperti mengatur warna teks menggunakan color, ukuran huruf dengan font-size, dan warna latar belakang menggunakan background-color.
</p>

# Tugas 3 - Project Bucin (Edisi Imlek)
## 1. Source code index.html
```<!-- 2311102019
Fattah Rizqy Adhipratama
S1IF-11-05 -->
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gong Xi Fa Cai 🏮</title>
  <link href="https://fonts.googleapis.com/css2?family=Ma+Shan+Zheng&family=Cormorant+Garamond:ital,wght@0,300;0,600;1,300;1,500&family=EB+Garamond:ital,wght@0,400;1,400&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <div class="bg" aria-hidden="true">
    <div class="bg__glow"></div>
    <span class="spark s1">✦</span>
    <span class="spark s2">✦</span>
    <span class="spark s3">✦</span>
    <span class="spark s4">✦</span>
    <span class="spark s5">✦</span>
    <span class="spark s6">✦</span>
  </div>

  <div class="page">

    <!-- Kiri: dekorasi vertikal -->
    <aside class="side side--left" aria-hidden="true">
      <span class="side__char">春</span>
      <div class="side__line"></div>
      <span class="side__char">節</span>
      <div class="side__line"></div>
      <span class="side__char">快</span>
      <div class="side__line"></div>
      <span class="side__char">樂</span>
    </aside>

    <!-- Card utama -->
    <main class="card">

      <!-- Header card -->
      <header class="card__header">
        <span class="header__ornament">— 🏮 —</span>
        <h1 class="card__title">
          <span class="title__cn">新年快樂</span>
          <span class="title__id">Selamat Tahun Baru Imlek</span>
        </h1>
      </header>

      <div class="card__rule"></div>

      <!-- Pesan utama -->
      <section class="card__message">
        <p class="msg__greeting">Buat kamu yang selalu bikin hari-hariku<br />terasa seperti tahun baru tiap saat —</p>

        <blockquote class="msg__quote">
          "Di antara ribuan lampion yang menyala malam ini,<br />
          yang paling terang tetap senyummu."
        </blockquote>

        <p class="msg__body">
          Semoga tahun kuda ini membawa kamu keberuntungan yang kamu pantas dapatkan,
          ketenangan yang selama ini kamu cari, dan kebahagiaan yang tidak perlu
          kamu perjuangkan sendirian.
        </p>
      </section>

      <div class="card__rule card__rule--short"></div>

      <!-- Footer card -->
      <footer class="card__footer">
        <span class="footer__fu">福</span>
        <p class="footer__sign">dengan sayang yang tidak bisa disembunyikan</p>
        <span class="footer__year">龍年 · 2025</span>
      </footer>

    </main>

    <!-- Kanan: dekorasi vertikal -->
    <aside class="side side--right" aria-hidden="true">
      <span class="side__char">恭</span>
      <div class="side__line"></div>
      <span class="side__char">喜</span>
      <div class="side__line"></div>
      <span class="side__char">發</span>
      <div class="side__line"></div>
      <span class="side__char">財</span>
    </aside>

  </div>

</body>
</html>
```

## 2. Source Code style.css
```*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --red-bg:   #1A0000;
  --red-dark: #6B0000;
  --red-mid:  #A00010;
  --gold:     #C9A84C;
  --goldb:    #060502;
  --cream:    #FFF5E0;
  --muted:    rgba(255,245,224,.6);
}

body {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  background:
    radial-gradient(ellipse at 60% 10%, rgba(160,0,20,.6) 0%, transparent 55%),
    radial-gradient(ellipse at 20% 80%, rgba(120,30,0,.5) 0%, transparent 50%),
    var(--red-bg);
  font-family: 'EB Garamond', Georgia, serif;
  padding: 2rem 1rem;
}

/* BACKGROUND */
.bg { position: fixed; inset: 0; pointer-events: none; overflow: hidden; }

.bg__glow {
  position: absolute;
  width: 600px; height: 600px;
  top: 50%; left: 50%;
  transform: translate(-50%, -50%);
  background: radial-gradient(circle, rgba(180,60,0,.18) 0%, transparent 70%);
  animation: breathe 5s ease-in-out infinite;
}

@keyframes breathe {
  0%,100% { transform: translate(-50%,-50%) scale(1); }
  50%      { transform: translate(-50%,-50%) scale(1.2); }
}

.spark {
  position: absolute;
  color: var(--goldb);
  font-size: .6rem;
  opacity: 0;
  animation: twinkle ease-in-out infinite;
}
.s1{top:12%;left:18%;animation-duration:4s;animation-delay:0s;}
.s2{top:25%;right:15%;animation-duration:6s;animation-delay:1s;}
.s3{top:60%;left:10%;animation-duration:5s;animation-delay:2s;}
.s4{top:75%;right:12%;animation-duration:4.5s;animation-delay:.5s;}
.s5{top:40%;left:5%;animation-duration:7s;animation-delay:3s;}
.s6{top:85%;left:55%;animation-duration:5.5s;animation-delay:1.5s;}

@keyframes twinkle {
  0%,100%{ opacity:0; transform:scale(.5); }
  50%    { opacity:.8; transform:scale(1.2); }
}
```
**Source Codenya:** [style.css](./style.css)

# Output
![alt text](Task3-1.png)

# Penjelasan
<p align="justify">
Program ini merupakan halaman web yang dibuat menggunakan HTML dan CSS murni (pure CSS) tanpa bantuan JavaScript maupun framework styling seperti Bootstrap dan Tailwind CSS. Tujuan dari project ini adalah menampilkan ucapan bertema Tahun Baru Imlek dengan nuansa visual yang elegan, romantis, dan khas budaya Tionghoa.

Pada file index.html, struktur halaman disusun menggunakan elemen semantik HTML seperti header, main, section, footer, dan aside. Penggunaan elemen tersebut membuat struktur halaman menjadi lebih rapi dan mudah dipahami. Bagian awal halaman berisi elemen dekoratif latar belakang berupa efek cahaya dan bintang kecil yang ditempatkan di dalam class bg. Setelah itu terdapat container utama dengan class page yang membagi tampilan menjadi tiga bagian, yaitu panel kiri, kartu utama, dan panel kanan.

Panel kiri dan kanan menggunakan elemen aside yang berisi karakter Mandarin vertikal sebagai dekorasi khas Imlek, seperti 春節快樂 dan 恭喜發財. Di bagian tengah terdapat elemen main dengan class card yang menjadi fokus utama tampilan. Card ini berisi judul ucapan Tahun Baru Imlek, pesan romantis, kutipan, serta footer yang menampilkan simbol keberuntungan 福.

Pada file style.css, tampilan halaman diatur menggunakan CSS custom dengan memanfaatkan CSS variables pada selector :root untuk mendefinisikan warna utama seperti merah gelap, emas, dan krem. Warna-warna tersebut dipilih untuk memperkuat identitas visual Imlek. Layout halaman menggunakan Flexbox sehingga elemen dapat tersusun rapi dan responsif.

Secara keseluruhan, tugas ini menunjukkan penggunaan HTML semantik, Flexbox, CSS variables, pseudo-element, keyframes animation, dan responsive design untuk menghasilkan halaman web bertema Imlek yang menarik secara visual dan tetap sesuai ketentuan.
</p>