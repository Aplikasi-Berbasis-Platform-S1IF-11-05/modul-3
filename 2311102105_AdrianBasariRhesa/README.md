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
    <strong>Adrian Basari Rhesa</strong>
    <br>
    <strong>2311102105</strong>
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
<!-- 2311102105-Adrian Basari Rhesa -->
<!DOCTYPE html>
<html lang="id">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Gong Xi Fa Cai - Untuk Bubub</title>
    <link
        href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@700&family=Noto+Sans+SC:wght@400;700&family=Poppins:wght@300;400;600&display=swap"
        rel="stylesheet">
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <div class="container">
        <div class="corner top-left"></div>
        <div class="corner bottom-right"></div>

        <header>
            <h1>恭喜发财</h1>
            <p class="subtitle">Gong Xi Fa Cai</p>
        </header>

        <main>
            <div class="card">
                <p>Untuk yang tersayang,</p>
                <h2>Bubub ❤️</h2>

                <p class="message">
                    Semoga di tahun baru ini, kebahagiaan menyertaimu, rezeki mengalir deras untukmu,
                    dan semua impianmu menjadi nyata.
                </p>

                <p class="closing">
                    Dan yang paling penting... <br>
                    tetaplah menjadi alasan tersenyumku ya! 😆✨
                </p>
            </div>
        </main>

        <footer>
            <p>Dibuat dengan penuh cinta ❤️</p>
        </footer>
    </div>

    <script>
        function createLantern() {
            const symbols = ['🧧', '🏮', '✨', '🌸'];
            const lantern = document.createElement('div');
            lantern.classList.add('lantern');
            lantern.innerText = symbols[Math.floor(Math.random() * symbols.length)];
            lantern.style.left = Math.random() * 100 + "vw";
            lantern.style.animationDuration = Math.random() * 3 + 2 + "s";
            document.body.appendChild(lantern);

            setTimeout(() => {
                lantern.remove();
            }, 5000);
        }
        setInterval(createLantern, 500);
    </script>

</body>

</html>
```

**style.css**
```css
/*2311102105-Adrian Basari Rhesa*/
:root {
    --primary-red: #d32f2f;
    --gold: #ffd700;
    --dark-red: #8b0000;
}

body {
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background: linear-gradient(135deg, var(--dark-red), var(--primary-red));
    font-family: 'Poppins', sans-serif;
    color: white;
    overflow: hidden;
    /* Supaya efek animasi tidak membuat scrollbar muncul */
}

/* Animasi Elemen Jatuh */
.lantern {
    position: absolute;
    top: -20px;
    font-size: 2rem;
    opacity: 0.6;
    animation: fall linear infinite;
    z-index: 1;
    /* Agar jatuh di belakang kotak ucapan */
}

@keyframes fall {
    to {
        transform: translateY(110vh);
    }
}

/* Kotak Utama (Glassmorphism Effect) */
.container {
    width: 90%;
    max-width: 450px;
    text-align: center;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    /* Efek kaca buram */
    -webkit-backdrop-filter: blur(10px);
    /* Dukungan untuk Safari */
    padding: 40px 20px;
    border-radius: 20px;
    border: 2px solid var(--gold);
    box-shadow: 0 15px 35px rgba(0, 0, 0, 0.3);
    animation: fadeIn 1.5s ease-out;
    position: relative;
    z-index: 10;
    /* Agar kotak ucapan berada di depan animasi */
}

@keyframes fadeIn {
    from {
        opacity: 0;
        transform: translateY(20px);
    }

    to {
        opacity: 1;
        transform: translateY(0);
    }
}

/* Bagian Header */
h1 {
    font-family: 'Noto Sans SC', sans-serif;
    font-size: 2.5rem;
    margin-bottom: 5px;
    color: var(--gold);
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
}

.subtitle {
    font-size: 1.1rem;
    letter-spacing: 2px;
    margin-bottom: 30px;
    text-transform: uppercase;
    font-weight: 300;
}

/* Kartu Ucapan Putih */
.card {
    background: white;
    color: #333;
    padding: 30px;
    border-radius: 15px;
    position: relative;
    box-shadow: inset 0 0 10px rgba(0, 0, 0, 0.05);
}

.card h2 {
    font-family: 'Dancing Script', cursive;
    font-size: 2.5rem;
    color: var(--primary-red);
    margin: 10px 0;
}

.message {
    line-height: 1.6;
    font-size: 1rem;
    margin-bottom: 20px;
}

.closing {
    font-style: italic;
    font-weight: 600;
    color: var(--dark-red);
}

/* Bagian Footer */
footer {
    margin-top: 25px;
    font-size: 0.9rem;
    color: var(--gold);
}

/* Hiasan Sudut (Corner Ornament) */
.corner {
    position: absolute;
    width: 50px;
    height: 50px;
    border: 3px solid var(--gold);
}

.top-left {
    top: 10px;
    left: 10px;
    border-right: none;
    border-bottom: none;
    border-top-left-radius: 10px;
}

.bottom-right {
    bottom: 10px;
    right: 10px;
    border-left: none;
    border-top: none;
    border-bottom-right-radius: 10px;
}
```
## Output

<img width="1920" height="1080" alt="Screenshot (1065)" src="https://github.com/user-attachments/assets/3bfd0a8d-e241-4103-9c50-643769ec1a67" />
