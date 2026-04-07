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
    <strong>Megan Sulthon Aryomukti</strong>
    <br>
    <strong>2311102119</strong>
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
<!-- 2311102119-Megan Sulthon Aryomukti -->
<!DOCTYPE html>
<html lang="id">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gong Xi Fa Cai - Spesial</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="container">

        <header>
            <h1>Gong Xi Fa Cai 🧧</h1>
            <p class="subtitle">Selamat Tahun Baru Imlek</p>
        </header>

        <main>
            <div class="card">
                <p>Untuk seseorang yang spesial,</p>
                <h2>Bubub ❤️</h2>

                <p class="message">
                    Semoga tahun ini penuh dengan kebahagiaan, rezeki yang melimpah,
                    dan segala hal baik yang kamu harapkan.
                </p>

                <p class="closing">
                    Dan semoga… kamu tetap jadi milikku ya 😆✨
                </p>
            </div>
        </main>

        <footer>
            <p>Dibuat dengan ❤️</p>
        </footer>

    </div>

</body>

</html>
```

**style.css**
```css
/*2311102119-Megan Sulthon Aryomukti*/
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(135deg, #8b0000, #c62828);
    color: #fff;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

/* Container */
.container {
    text-align: center;
    background: rgba(255, 255, 255, 0.05);
    padding: 40px 25px;
    border-radius: 20px;
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 215, 0, 0.4);
    max-width: 500px;
    width: 90%;
}

/* Header */
h1 {
    font-size: 2.8rem;
    color: #ffd700;
    margin-bottom: 5px;
}

.subtitle {
    font-size: 1rem;
    color: #ffe082;
    margin-bottom: 30px;
}

/* Card */
.card {
    background: linear-gradient(145deg, #b71c1c, #e53935);
    padding: 25px;
    border-radius: 15px;
    transition: 0.3s;
}

.card:hover {
    transform: translateY(-5px);
}

/* Text */
.card p {
    margin-bottom: 10px;
    line-height: 1.6;
}

.card h2 {
    color: #ffd700;
    margin-bottom: 15px;
}

.message {
    font-size: 1.1rem;
}

.closing {
    margin-top: 15px;
    font-style: italic;
}

/* Footer */
footer {
    margin-top: 20px;
    font-size: 0.9rem;
    color: #ffcc80;
}```

## Output

<img width="1366" height="768" alt="Screenshot (1135)" src="https://github.com/user-attachments/assets/0f622d92-1853-45ee-92fc-89fd4d2a72c3" />

