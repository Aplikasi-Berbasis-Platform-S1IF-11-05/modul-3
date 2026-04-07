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
    <strong>Verdi Pangestu</strong>
    <br>
    <strong>2311102100</strong>
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

CSS (*Cascading Style Sheets*) adalah bahasa yang dipakai untuk mengatur tampilan elemen-elemen HTML. Kalau HTML bertugas menyusun struktur konten, CSS bertugas membuat tampilan tersebut menjadi menarik — mulai dari warna, ukuran font, tata letak, hingga animasi.

CSS disebut *cascading* karena aturan-aturannya diterapkan secara bertingkat — style yang lebih spesifik akan menimpa style yang lebih umum.

---

## 2. Cara Penulisan CSS

Ada tiga cara menulis CSS:

- **Inline** — ditulis langsung di dalam tag HTML menggunakan atribut `style`.
- **Internal** — ditulis di dalam tag `<style>` di bagian `<head>`.
- **External** — ditulis di file `.css` terpisah lalu dihubungkan dengan `<link>`.

Pada praktikum ini digunakan metode **external** dengan file `style.css` yang dihubungkan ke `index.html`.

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

- `background-color` / `background` — Mengatur warna atau gradien latar belakang.
- `color` — Mengatur warna teks.
- `font-size`, `font-family` — Mengatur ukuran dan jenis huruf.
- `display: flex` — Mengatur tata letak elemen secara fleksibel.
- `border-radius` — Membuat sudut elemen menjadi melengkung.
- `box-shadow` — Menambahkan bayangan pada elemen.
- `animation` — Menggerakkan elemen dengan keyframe.
- `transform` — Mengubah posisi atau rotasi elemen.
- `transition` — Membuat perubahan style menjadi lebih halus.

---

## 5. CSS Animation

CSS Animation memungkinkan kita membuat gerakan pada elemen tanpa JavaScript. Caranya dengan mendefinisikan `@keyframes` lalu menghubungkannya ke elemen menggunakan property `animation`.

```css
@keyframes swing {
  0%, 100% { transform: rotate(-8deg); }
  50%       { transform: rotate(8deg); }
}

.lantern {
  animation: swing 3s ease-in-out infinite;
}
```

Property `animation` yang sering dipakai:
- `animation-duration` — Durasi satu siklus animasi.
- `animation-timing-function` — Pola kecepatan (ease, linear, dll).
- `animation-delay` — Jeda sebelum animasi mulai.
- `animation-iteration-count` — Berapa kali animasi diulang (`infinite` = terus-menerus).

---

# Tugas 3 — Project Bucin (Edisi Imlek)

## Code

**index.html**
```html
<!-- 2311102100-Verdi Pangestu -->
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gong Xi Fa Cai - Spesial Untuk Ayang</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <div class="lantern left">🏮</div>
        <div class="lantern right">🏮</div>

        <header>
            <h1>Gong Xi Fa Cai</h1>
            <h2>Selamat Tahun Baru Imlek</h2>
        </header>

        <main>
            <div class="message-card">
                <p>Spesial untuk kesayangan, <strong>Ayang Bebeb</strong> ❤️</p>
                <p>Semoga tahun ini bawa banyak hoki, cuan yang melimpah, kebahagiaan, dan pastinya makin cinta sama aku.</p>
            </div>
        </main>

        <footer>
            <p>✨ Dibuat dengan 100% Cinta✨</p>
        </footer>
    </div>

</body>
</html>
```

**style.css**
```css
/*2311102100-Verdi Pangestu*/
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    /* Latar belakang merah gelap dengan efek gradient ke merah terang */
    background-color: #8b0000; 
    background-image: radial-gradient(circle at center, #d32f2f 0%, #5a0000 100%);
    color: #ffd700; /* Warna teks dominan Emas */
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    overflow: hidden; /* Mencegah scroll jika lampion keluar layar */
}

/* === CONTAINER UTAMA === */
.container {
    position: relative;
    max-width: 650px;
    width: 90%;
    padding: 50px 30px;
    border: 3px solid #daa520; /* Border emas gelap */
    border-radius: 20px;
    background: rgba(139, 0, 0, 0.4); /* Efek tembus pandang merah */
    box-shadow: 0 0 40px rgba(255, 215, 0, 0.2), inset 0 0 20px rgba(255, 215, 0, 0.1);
    backdrop-filter: blur(8px); /* Efek glassmorphism murni CSS */
}

/* === TIPOGRAFI === */
h1 {
    font-size: 4rem;
    margin-bottom: 10px;
    /* Efek teks bercahaya emas */
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.6), 0 0 20px #ffd700;
    letter-spacing: 3px;
}

h2 {
    font-size: 1.5rem;
    margin-bottom: 40px;
    color: #ffdf00;
    font-weight: 400;
    letter-spacing: 1px;
}

/* === KARTU PESAN UNTUK BUBUB === */
.message-card {
    background: linear-gradient(135deg, #b71c1c 0%, #e53935 100%);
    padding: 30px;
    border-radius: 15px;
    border: 1px dashed #ffd700; /* Border putus-putus emas */
    margin-bottom: 25px;
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4);
    transition: transform 0.4s ease, box-shadow 0.4s ease; /* Hover effect CSS */
}

/* Interaksi CSS Murni tanpa JS */
.message-card:hover {
    transform: translateY(-8px);
    box-shadow: 0 15px 35px rgba(255, 215, 0, 0.3);
}

.message-card p {
    font-size: 1.25rem;
    line-height: 1.8;
    margin-bottom: 15px;
    color: #ffffff; /* Teks putih agar kontras dengan merah */
    text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}

.message-card strong {
    color: #ffd700;
    font-size: 1.5rem;
    font-weight: bold;
}

footer p {
    font-size: 0.9rem;
    color: #daa520;
    margin-top: 30px;
    font-style: italic;
}

/* === ANIMASI LAMPION (PURE CSS) === */
.lantern {
    font-size: 5rem;
    position: absolute;
    top: -40px;
    /* Memanggil animasi ayunan */
    animation: swing 3s ease-in-out infinite alternate;
    transform-origin: top center; /* Sumbu ayunan di bagian atas */
    filter: drop-shadow(0px 10px 10px rgba(0,0,0,0.5));
}

.lantern.left {
    left: -20px;
}

.lantern.right {
    right: -20px;
    animation-delay: 1.5s; /* Dibuat tidak sinkron agar lebih natural */
}

/* Keyframes untuk ayunan lampion */
@keyframes swing {
    0% { transform: rotate(-12deg); }
    100% { transform: rotate(12deg); }
}

/* Responsif untuk HP (Pure CSS Media Query) */
@media (max-width: 600px) {
    h1 { font-size: 2.8rem; }
    .lantern { font-size: 3.5rem; top: -30px; }
    .message-card p { font-size: 1.1rem; }
}
```

## Output
<img width="1919" height="972" alt="Cuplikan layar 2026-04-07 111154" src="https://github.com/user-attachments/assets/d173d552-f79d-43bc-bc55-bc393d7b52a5" />
