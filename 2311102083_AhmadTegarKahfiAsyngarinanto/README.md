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
    <strong>Ahmad Tegar Kahfi Asyngarinanto</strong>
    <br>
    <strong>2311102083</strong>
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
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Selamat Tahun Baru Imlek</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>

  <div class="confetti">
    <div class="dot"></div><div class="dot"></div><div class="dot"></div>
    <div class="dot"></div><div class="dot"></div><div class="dot"></div>
    <div class="dot"></div><div class="dot"></div><div class="dot"></div>
    <div class="dot"></div>
  </div>

  <div class="lanterns">
    <div class="lantern">
      <div class="lantern-string"></div>
      <div class="lantern-top"></div>
      <div class="lantern-body">福</div>
      <div class="lantern-bottom"></div>
      <div class="lantern-tassel"><span></span><span></span><span></span></div>
    </div>
    <div class="lantern lantern-2">
      <div class="lantern-string"></div>
      <div class="lantern-top"></div>
      <div class="lantern-body">春</div>
      <div class="lantern-bottom"></div>
      <div class="lantern-tassel"><span></span><span></span><span></span></div>
    </div>
    <div class="lantern lantern-3">
      <div class="lantern-string"></div>
      <div class="lantern-top"></div>
      <div class="lantern-body">喜</div>
      <div class="lantern-bottom"></div>
      <div class="lantern-tassel"><span></span><span></span><span></span></div>
    </div>
  </div>

  <div class="hero">
    <div class="hero-chinese">新年快乐</div>
    <div class="hero-title">Selamat Tahun Baru Imlek 2576</div>
    <div class="hero-subtitle">Gong Xi Fa Cai — Semoga Rezeki Selalu Melimpah</div>
  </div>

  <div class="divider">✦ ✦ ✦ ✦ ✦</div>

  <div class="card-container">
    <div class="card">
      <div class="card-icon">🧧</div>
      <div class="card-title">Angpao</div>
      <div class="card-desc">Simbol keberuntungan dan harapan baik untuk tahun yang baru.</div>
    </div>
    <div class="card">
      <div class="card-icon">🐉</div>
      <div class="card-title">Naga</div>
      <div class="card-desc">Lambang kekuatan, keberanian, dan keberuntungan dalam budaya Tionghoa.</div>
    </div>
    <div class="card">
      <div class="card-icon">🏮</div>
      <div class="card-title">Lampion</div>
      <div class="card-desc">Cahaya lampion menerangi jalan menuju kebahagiaan dan kemakmuran.</div>
    </div>
    <div class="card">
      <div class="card-icon">🌸</div>
      <div class="card-title">Bunga Plum</div>
      <div class="card-desc">Simbol ketahanan dan harapan baru di awal tahun yang penuh berkah.</div>
    </div>
  </div>

  <div class="greeting-box">
    <h2>🎊 Pesan Tahun Baru 🎊</h2>
    <p>
      Semoga di tahun baru ini, segala doa dan harapanmu terkabul.<br>
      Kesehatan, kebahagiaan, dan rezeki selalu menyertai setiap langkahmu.<br><br>
      <strong>新年快乐，万事如意！</strong><br>
      <em>Selamat Tahun Baru, semoga segala sesuatu berjalan sesuai harapan!</em>
    </p>
  </div>

  <div class="footer">
    Dibuat dengan ❤️ oleh Ahmad Tegar Kahfi Asyngarinanto — 2311102083
  </div>

</body>
</html>
```

**style.css**
```css
@import url('https://fonts.googleapis.com/css2?family=Noto+Serif:ital,wght@0,400;0,700;1,400&display=swap');

* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  background-color: #8B0000;
  font-family: 'Noto Serif', serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  overflow-x: hidden;
}

.lanterns { display: flex; justify-content: center; gap: 40px; padding-top: 20px; }
.lantern { display: flex; flex-direction: column; align-items: center; animation: swing 3s ease-in-out infinite; }
.lantern-2 { animation-delay: 0.5s; }
.lantern-3 { animation-delay: 1s; }

@keyframes swing {
  0%, 100% { transform: rotate(-8deg); }
  50%       { transform: rotate(8deg); }
}

.lantern-string { width: 2px; height: 30px; background: #FFD700; }
.lantern-top    { width: 20px; height: 10px; background: #FFD700; border-radius: 4px 4px 0 0; }
.lantern-bottom { width: 20px; height: 10px; background: #FFD700; border-radius: 0 0 4px 4px; }

.lantern-body {
  width: 50px; height: 70px;
  background: radial-gradient(ellipse at center, #FF6600, #CC0000);
  border-radius: 50% / 30%;
  border: 3px solid #FFD700;
  display: flex; align-items: center; justify-content: center;
  color: #FFD700; font-size: 22px; font-weight: bold;
  box-shadow: 0 0 15px rgba(255, 150, 0, 0.7);
}

.lantern-tassel { display: flex; gap: 4px; }
.lantern-tassel span { width: 2px; height: 25px; background: #FFD700; }

.hero { text-align: center; padding: 30px 20px 10px; }
.hero-chinese { font-size: 72px; color: #FFD700; letter-spacing: 10px; animation: glow 2s ease-in-out infinite alternate; }
.hero-title   { font-size: 28px; color: #FFD700; margin-top: 10px; letter-spacing: 2px; }
.hero-subtitle { font-size: 16px; color: #FFCCCB; margin-top: 8px; font-style: italic; }

@keyframes glow {
  from { text-shadow: 0 0 10px #FFD700, 3px 3px 0 #5c0000; }
  to   { text-shadow: 0 0 30px #FFD700, 0 0 50px #FF6600, 3px 3px 0 #5c0000; }
}

.divider { color: #FFD700; font-size: 22px; letter-spacing: 8px; margin: 16px 0; opacity: 0.8; }

.card-container { display: flex; gap: 20px; flex-wrap: wrap; justify-content: center; padding: 10px 30px 30px; max-width: 900px; }

.card {
  background: linear-gradient(135deg, #FFD700 0%, #FFA500 100%);
  border-radius: 16px; padding: 24px 20px; width: 200px; text-align: center;
  box-shadow: 0 8px 20px rgba(0,0,0,0.3); border: 2px solid #FF6600;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}
.card:hover { transform: translateY(-8px); box-shadow: 0 16px 30px rgba(0,0,0,0.4); }
.card-icon  { font-size: 40px; margin-bottom: 10px; }
.card-title { font-size: 15px; font-weight: bold; color: #8B0000; margin-bottom: 6px; }
.card-desc  { font-size: 12px; color: #5c0000; line-height: 1.5; }

.greeting-box {
  background: linear-gradient(135deg, #FFD700, #FFA500);
  border: 3px solid #FF6600; border-radius: 20px;
  padding: 30px 40px; max-width: 600px; text-align: center;
  margin: 0 20px 30px; box-shadow: 0 8px 25px rgba(0,0,0,0.3);
}
.greeting-box h2 { color: #8B0000; font-size: 20px; margin-bottom: 12px; }
.greeting-box p  { color: #5c0000; font-size: 14px; line-height: 1.8; }

.footer { color: #FFCCCB; font-size: 12px; padding: 20px; text-align: center; opacity: 0.7; }

.confetti { position: fixed; top: 0; left: 0; width: 100%; height: 100%; pointer-events: none; overflow: hidden; z-index: -1; }
.dot { position: absolute; width: 8px; height: 8px; border-radius: 50%; animation: fall linear infinite; opacity: 0.6; }

.dot:nth-child(1)  { left: 5%;  background: #FFD700; animation-duration: 6s;  animation-delay: 0s; }
.dot:nth-child(2)  { left: 15%; background: #FF6600; animation-duration: 8s;  animation-delay: 1s; }
.dot:nth-child(3)  { left: 25%; background: #FFD700; animation-duration: 7s;  animation-delay: 2s; }
.dot:nth-child(4)  { left: 35%; background: #FFA500; animation-duration: 9s;  animation-delay: 0.5s; }
.dot:nth-child(5)  { left: 50%; background: #FFD700; animation-duration: 6s;  animation-delay: 1.5s; }
.dot:nth-child(6)  { left: 60%; background: #FF6600; animation-duration: 8s;  animation-delay: 3s; }
.dot:nth-child(7)  { left: 70%; background: #FFD700; animation-duration: 7s;  animation-delay: 0.8s; }
.dot:nth-child(8)  { left: 80%; background: #FFA500; animation-duration: 10s; animation-delay: 2s; }
.dot:nth-child(9)  { left: 90%; background: #FFD700; animation-duration: 6s;  animation-delay: 1s; }
.dot:nth-child(10) { left: 45%; background: #FF6600; animation-duration: 9s;  animation-delay: 4s; }

@keyframes fall {
  0%   { top: -10px; transform: rotate(0deg); }
  100% { top: 110vh;  transform: rotate(360deg); }
}
```

## Output

![Bukti](Assets/Bukti.png)
