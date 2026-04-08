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
    <strong>Arya Bima</strong>
    <br>
    <strong>2311102257</strong>
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

### 1. Pengertian CSS

CSS (Cascading Style Sheets) adalah bahasa untuk mengatur tampilan, warna, ukuran, dan layout halaman web. CSS bekerja bersama HTML untuk memisahkan konten (HTML) dari desain (CSS).

### 2. Cara Menghubungkan CSS ke HTML

- Inline : `style=""` di dalam tag HTML (tidak direkomendasikan)
- Internal : `<style>` di dalam `<head>`
- External : Paling baik => `<link rel="stylesheet" href="style.css">`

### 3. Sintaks Dasar CSS

```css
selector {
  property: value;
  property: value;
}
```

**Contoh:**

```css
h1 {
  color: blue;
  font-size: 32px;
  text-align: center;
}
```

### 4. Jenis Selector Utama

| Selector  | Contoh       | Keterangan                |
| --------- | ------------ | ------------------------- |
| Element   | `p {}`       | Semua tag `<p>`           |
| Class     | `.btn {}`    | Elemen dengan class="btn" |
| ID        | `#header {}` | Elemen dengan id="header" |
| Universal | `* {}`       | Semua elemen              |

### 5. Properti CSS yang Sering Digunakan

- Teks : `color`, `font-size`, `text-align`
- Box Model : `margin`, `padding`, `border`, `width`, `height`
- Layout : `display`, `position`, `flex`, `grid`

### 6. Konsep Penting

- Box Model : Setiap elemen adalah kotak (content + padding + border + margin)
- Cascading : Aturan CSS mengikuti prioritas (specificity)
- Responsive : Menggunakan Media Queries untuk menyesuaikan tampilan di berbagai ukuran layar

### 7. Prinsip Dasar

- Gunakan external CSS sebanyak mungkin.
- Pisahkan konten (HTML) dan tampilan (CSS).
- Gunakan class daripada ID untuk styling.
- Buat kode yang bersih dan mudah dibaca.

---

# Tugas 3: Project Bucin (Edisi Imlek)

`index.html:`

```html
<!-- 2311102257 - Arya Bima -->
<!doctype html>
<html lang="id">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Selamat Imlek</title>
    <link rel="stylesheet" href="style.css" />
  </head>
  <body>
    <header>
      <h1>🧧 Selamat Tahun Baru Imlek 🧧</h1>
      <div class="subtitle">Semoga keberuntungan selalu menyertaimu</div>
    </header>

    <div class="lantern"></div>

    <div class="container">
      <div class="card">
        <h2>Untuk Bubub 💖</h2>
        <p>
          Di tahun baru ini, semoga semua harapan dan impianmu tercapai. Semoga
          selalu diberi kesehatan, kebahagiaan, dan rezeki yang melimpah.
        </p>
        <div class="gold-line"></div>
        <p>
          Terima kasih sudah hadir dan membuat hari-hariku lebih berwarna. Gong
          Xi Fa Cai! ❤️
        </p>
      </div>
    </div>

    <div class="lantern"></div>

    <div class="footer">Made with ❤️ khusus untuk bubub</div>
  </body>
</html>
```

`style.css:`

```css
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Segoe UI", sans-serif;
}

body {
  background: radial-gradient(circle at top, #8b0000, #2b0000);
  color: #fff;
  text-align: center;
  overflow-x: hidden;
}

header {
  padding: 40px 20px;
}

h1 {
  font-size: 3rem;
  color: gold;
  text-shadow: 0 0 15px rgba(255, 215, 0, 0.8);
}

.subtitle {
  margin-top: 10px;
  font-size: 1.2rem;
  color: #ffd700;
}

.container {
  padding: 40px 20px;
}

.card {
  background: rgba(255, 0, 0, 0.2);
  border: 2px solid gold;
  border-radius: 20px;
  padding: 30px;
  max-width: 500px;
  margin: 0 auto;
  box-shadow: 0 0 20px rgba(255, 215, 0, 0.4);
}

.card h2 {
  color: gold;
  margin-bottom: 15px;
}

.card p {
  line-height: 1.6;
}

.lantern {
  width: 60px;
  height: 80px;
  background: red;
  border-radius: 30px;
  margin: 30px auto;
  position: relative;
  animation: float 3s ease-in-out infinite;
}

.lantern::before {
  content: "";
  width: 70px;
  height: 10px;
  background: gold;
  position: absolute;
  top: -10px;
  left: -5px;
  border-radius: 5px;
}

.lantern::after {
  content: "";
  width: 6px;
  height: 30px;
  background: gold;
  position: absolute;
  bottom: -30px;
  left: 50%;
  transform: translateX(-50%);
}

@keyframes float {
  0%,
  100% {
    transform: translateY(0);
  }
  50% {
    transform: translateY(-15px);
  }
}

.footer {
  margin-top: 50px;
  padding: 20px;
  font-size: 0.9rem;
  color: #ffcccb;
}

.gold-line {
  width: 80%;
  height: 2px;
  background: gold;
  margin: 20px auto;
}
```

Output:
<img width="1280" height="720" alt="Output Tugas 3" src="tugas-3.png" />
