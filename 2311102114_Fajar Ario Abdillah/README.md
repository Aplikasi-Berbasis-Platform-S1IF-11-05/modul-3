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
    <strong>Fajar Ario Abdillah</strong>
    <br>
    <strong>2311102114</strong>
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
  <strong>Apri Pandu Wicaksono</strong>
  <br>
  <strong>Hamka Zaenul Ardi</strong>
  <br />
  <h3>LABORATORIUM HIGH PERFORMANCE <br>FAKULTAS INFORMATIKA <br>UNIVERSITAS TELKOM PURWOKERTO <br>2026 </h3>
</div>

<hr>

# Dasar Teori

## 1. CSS

CSS (Cascading Style Sheets) adalah bahasa yang digunakan untuk mengatur tampilan dan desain halaman web yang dibuat dengan HTML, seperti warna, ukuran teks, tata letak, jarak antar elemen, hingga responsivitas pada berbagai ukuran layar. Dengan CSS, tampilan website dapat dibuat lebih menarik, rapi, dan profesional tanpa mengubah struktur dasar HTML. CSS bekerja dengan cara memilih elemen HTML (menggunakan selector) lalu memberikan aturan gaya (property dan value), sehingga memisahkan antara struktur (HTML) dan tampilan (CSS), yang membuat pengembangan web menjadi lebih efisien dan mudah dikelola.

---

## 2. Cara Penulisan CSS

Penulisan CSS mengikuti struktur dasar berupa selector, property, dan value. Selector digunakan untuk memilih elemen HTML yang ingin diberi gaya, sedangkan property adalah jenis gaya yang ingin diterapkan (misalnya warna atau ukuran), dan value adalah nilai dari gaya tersebut. Format penulisannya adalah selector { property: value; }, di mana setiap aturan diakhiri dengan tanda titik koma. Contohnya, p { color: red; font-size: 16px; } berarti semua elemen paragraf akan berwarna merah dengan ukuran teks 16px. Saat menuliskannya di file Markdown, kamu bisa membungkus kode CSS menggunakan tanda tiga backtick (```) dan menambahkan kata css agar formatnya rapi dan mudah dibaca.

---

## 3. Selector CSS

Selector digunakan untuk memilih elemen HTML mana yang akan diberi style.

| Selector | Contoh | Keterangan |
|----------|--------|------------|
| Tag | `p { }` | Memilih semua elemen `<p>` |
| Class | `.card { }` | Memilih elemen dengan `class="card"` |
| ID | `#hero { }` | Memilih elemen dengan `id="hero"` |
| Universal | `* { }` | Memilih semua elemen |
| Pseudo-class | `.card:hover { }` | Memilih elemen saat kondisi tertentu |
| nth-child | `.dot:nth-child(1) { }` | Memilih elemen anak ke-n |

---

## 4. Property CSS yang Digunakan

Beberapa property penting yang dipakai pada praktikum ini:

- `background-color` — Mengatur warna latar belakang elemen.
- `font-size` — Mengatur teks.
- `font-family` — Menentukan jenis font.
- `margin` — Mengatur jarak luar antar elemen.
- `padding` — Mengatur jarak dalam (antara konten dan border).
- `border` — Memberi garis tepi pada elemen.
- `text-align` — Mengatur posisi teks (kiri, tengah, kanan).
- `display` — Mengatur bagaimana elemen ditampilkan.
- `width & height` — Mengatur lebar dan tinggi elemen.

---

## 5. CSS Animation

CSS Animation memungkinkan kita membuat tampilan website menjadi lebih hidup dan interaktif tanpa bantuan JavaScript. Dengan menggunakan @keyframes dan properti animation, kita dapat mengontrol perubahan gaya elemen secara halus dan terstruktur.

```css
@keyframes warnaBerubah {
  0% {
    background-color: red;
  }
  50% {
    background-color: yellow;
  }
  100% {
    background-color: green;
  }
}

.box {
  width: 100px;
  height: 100px;
  animation: warnaBerubah 3s infinite;
}
```

---

# Tugas 3 — Project Bucin (Edisi Imlek)

## Code

**index.html**
```html
<!DOCTYPE html>
<html lang="id">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Perayaan Imlek</title>
    <link rel="stylesheet" href="style.css" />
</head>

<body>
    <!--
    Watermark:
    Nama  : Fajar Ario Abdillah
    NIM   : 2311102114
  -->

    <div class="watermark">Fajar Ario Abdillah - 2311102114</div>

    <header class="hero">
        <nav class="navbar">
            <div class="logo">Imlek Fest</div>
            <ul class="nav-links">
                <li><a href="#tentang">Tentang</a></li>
                <li><a href="#tradisi">Tradisi</a></li>
                <li><a href="#harapan">Harapan</a></li>
            </ul>
        </nav>

        <div class="hero-content">
            <p class="subtitle">Gong Xi Fa Cai</p>
            <h1>Selamat Merayakan Tahun Baru Imlek</h1>
            <p class="desc">
                Semoga tahun baru membawa kesehatan, kebahagiaan, keberuntungan,
                dan rezeki yang melimpah untuk kita semua.
            </p>
            <a href="#tentang" class="btn">Lihat Perayaan</a>
        </div>

        <div class="lantern lantern-left"></div>
        <div class="lantern lantern-right"></div>
    </header>

    <main>
        <section id="tentang" class="section card-section">
            <h2>Tentang Perayaan Imlek</h2>
            <p>
                Tahun Baru Imlek adalah momen yang penuh makna bagi banyak orang.
                Perayaan ini identik dengan nuansa merah dan emas, lampion, kebersamaan
                keluarga, serta harapan baik untuk tahun yang baru.
            </p>
        </section>

        <section id="tradisi" class="section grid-section">
            <h2>Tradisi Khas Imlek</h2>
            <div class="grid-cards">
                <article class="card">
                    <h3>🏮 Lampion Merah</h3>
                    <p>
                        Lampion melambangkan harapan, kebahagiaan, dan suasana meriah
                        dalam perayaan Tahun Baru Imlek.
                    </p>
                </article>

                <article class="card">
                    <h3>🧧 Angpao</h3>
                    <p>
                        Angpao menjadi simbol doa, berkah, dan rezeki yang dibagikan
                        kepada keluarga atau orang terdekat.
                    </p>
                </article>

                <article class="card">
                    <h3>🍊 Jeruk Keberuntungan</h3>
                    <p>
                        Buah jeruk sering hadir saat Imlek sebagai simbol keberuntungan
                        dan kemakmuran.
                    </p>
                </article>

                <article class="card">
                    <h3>🥟 Makan Bersama</h3>
                    <p>
                        Hidangan keluarga menjadi lambang kebersamaan dan rasa syukur
                        menyambut tahun yang baru.
                    </p>
                </article>
            </div>
        </section>

        <section id="harapan" class="section blessing-section">
            <h2>Harapan di Tahun Baru</h2>
            <blockquote>
                “Semoga tahun ini dipenuhi kebahagiaan, kesehatan, cinta, dan banyak
                keberuntungan.”
            </blockquote>
            <p>
                Mari sambut tahun baru dengan semangat baru, hati yang hangat,
                dan harapan terbaik untuk masa depan.
            </p>
        </section>
    </main>

    <footer class="footer">
        <p>© 2025 Perayaan Imlek | Dibuat oleh Ario</p>
    </footer>
</body>

</html>
```

**style.css**
```css
/*
  Watermark:
  Nama  : Fajar Ario
  NIM   : 2311102114
*/

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

html {
  scroll-behavior: smooth;
}

body {
  font-family: Arial, Helvetica, sans-serif;
  background: linear-gradient(180deg, #5c0000, #2b0000);
  color: #fff7e6;
  line-height: 1.6;
  min-height: 100vh;
}

.watermark {
  position: fixed;
  bottom: 14px;
  right: 14px;
  font-size: 12px;
  color: rgba(255, 240, 210, 0.3);
  pointer-events: none;
  z-index: 999;
  letter-spacing: 1px;
}

.hero {
  min-height: 100vh;
  padding: 24px 8%;
  position: relative;
  overflow: hidden;
  background:
    radial-gradient(circle at top, rgba(255, 215, 0, 0.18), transparent 30%),
    linear-gradient(180deg, #7a0000 0%, #420000 60%, #2b0000 100%);
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 100px;
}

.logo {
  font-size: 28px;
  font-weight: bold;
  color: #ffd54f;
  letter-spacing: 1px;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 24px;
}

.nav-links a {
  text-decoration: none;
  color: #fff7e6;
  font-weight: bold;
  transition: 0.3s;
}

.nav-links a:hover {
  color: #ffd54f;
}

.hero-content {
  max-width: 720px;
  margin: 100px auto 0;
  text-align: center;
}

.subtitle {
  color: #ffd54f;
  font-size: 20px;
  margin-bottom: 16px;
  text-transform: uppercase;
  letter-spacing: 3px;
}

.hero-content h1 {
  font-size: 56px;
  margin-bottom: 20px;
  line-height: 1.2;
  color: #fff4d6;
}

.desc {
  font-size: 18px;
  margin-bottom: 32px;
  color: #ffe9b0;
}

.btn {
  display: inline-block;
  text-decoration: none;
  background: #d4a017;
  color: #4a0000;
  padding: 14px 28px;
  border-radius: 999px;
  font-weight: bold;
  transition: 0.3s;
}

.btn:hover {
  background: #ffd54f;
  transform: translateY(-2px);
}

.lantern {
  position: absolute;
  top: 110px;
  width: 80px;
  height: 110px;
  background: linear-gradient(180deg, #ff3b3b, #b30000);
  border: 4px solid #ffd54f;
  border-radius: 40px;
  box-shadow: 0 0 20px rgba(255, 213, 79, 0.35);
}

.lantern::before {
  content: "";
  position: absolute;
  top: -80px;
  left: 50%;
  width: 4px;
  height: 80px;
  background: #ffd54f;
  transform: translateX(-50%);
}

.lantern::after {
  content: "";
  position: absolute;
  bottom: -18px;
  left: 50%;
  width: 18px;
  height: 18px;
  background: #ffd54f;
  transform: translateX(-50%);
  border-radius: 0 0 10px 10px;
}

.lantern-left {
  left: 8%;
}

.lantern-right {
  right: 8%;
}

.section {
  padding: 80px 8%;
}

.section h2 {
  text-align: center;
  margin-bottom: 28px;
  font-size: 36px;
  color: #ffd54f;
}

.card-section,
.blessing-section {
  max-width: 1000px;
  margin: 0 auto;
  text-align: center;
}

.card-section p,
.blessing-section p {
  font-size: 18px;
  color: #ffe9b0;
}

.grid-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 24px;
  margin-top: 24px;
}

.card {
  background: rgba(255, 245, 220, 0.08);
  border: 1px solid rgba(255, 213, 79, 0.35);
  padding: 24px;
  border-radius: 18px;
  box-shadow: 0 10px 24px rgba(0, 0, 0, 0.2);
  transition: 0.3s;
}

.card:hover {
  transform: translateY(-6px);
  background: rgba(255, 245, 220, 0.12);
}

.card h3 {
  margin-bottom: 12px;
  color: #ffd54f;
}

.card p {
  color: #fff0c7;
}

blockquote {
  margin: 0 auto 24px;
  max-width: 800px;
  font-size: 24px;
  font-style: italic;
  color: #fff4d6;
  border-left: 4px solid #ffd54f;
  padding-left: 20px;
  text-align: left;
}

.footer {
  text-align: center;
  padding: 24px;
  background: rgba(0, 0, 0, 0.2);
  color: #ffe9b0;
  font-size: 14px;
}

@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    gap: 16px;
    margin-bottom: 60px;
  }

  .nav-links {
    flex-wrap: wrap;
    justify-content: center;
  }

  .hero-content {
    margin-top: 60px;
  }

  .hero-content h1 {
    font-size: 38px;
  }

  .desc {
    font-size: 16px;
  }

  .lantern {
    width: 60px;
    height: 90px;
    top: 140px;
  }

  .section h2 {
    font-size: 28px;
  }

  blockquote {
    font-size: 20px;
  }
}
```

## Output

![Bukti](assets/Screenshot%202026-04-07%20084844.png)