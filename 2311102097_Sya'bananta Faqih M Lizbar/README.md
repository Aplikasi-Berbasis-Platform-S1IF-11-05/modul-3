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
    <strong>Sya'bananta Faqih M Lizbar</strong>
    <br>
    <strong>2311102097</strong>
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

# Dasar Teori CSS (Cascading Style Sheets)

CSS (Cascading Style Sheets) adalah bahasa desain yang digunakan untuk mengontrol tampilan dan format visual dari dokumen yang ditulis dalam bahasa markup (seperti HTML). CSS memungkinkan pemisahan antara konten (HTML) dan presentasi (desain), sehingga kode menjadi lebih rapi, mudah dikelola, dan dapat digunakan kembali.

## Metode Penempatan CSS

Terdapat tiga cara utama untuk menerapkan CSS ke dalam dokumen HTML:

Inline CSS: Ditulis langsung di dalam atribut style pada tag HTML.

Internal CSS: Ditulis di dalam tag ```<style>``` pada bagian ```<head>```.

External CSS: Ditulis di file terpisah dengan ekstensi .css dan dihubungkan menggunakan tag ``<link>``. (Metode yang direkomendasikan untuk proyek skala menengah-besar).

## Contoh CSS

```css
p {
  color: blue;
  font-size: 14px;
}
```

## Task 3: Project Bucin (Edisi Imlek)
### Souce code - html
```html
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <title>Happy Chinese New Year ❤️</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <div class="container">
        <h1>Gong Xi Fa Cai 🧧</h1>
        <h2>Untuk Bubub Tersayang ❤️</h2>

        <p class="message">
            Semoga di tahun ini kita makin langgeng, makin bucin,
            dan makin banyak rezeki biar bisa jalan bareng terus 😳✨
        </p>

        <div class="lantern"></div>
        <div class="lantern lantern2"></div>

        <p class="footer">Dari: Yang Selalu Sayang Kamu 🥰</p>
    </div>

</body>
</html>
```

### Source code - css

```css
body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: linear-gradient(#8B0000, #FF0000);
    color: gold;
    text-align: center;
}

.container {
    padding-top: 100px;
}

h1 {
    font-size: 50px;
}

h2 {
    margin-top: -10px;
    font-weight: normal;
}

.message {
    margin: 30px auto;
    width: 60%;
    font-size: 18px;
    line-height: 1.6;
}

.footer {
    margin-top: 50px;
    font-style: italic;
}

/* LAMPION */
.lantern {
    width: 80px;
    height: 100px;
    background: gold;
    border-radius: 50% 50% 40% 40%;
    margin: 30px auto;
    position: relative;
}

.lantern::before {
    content: '';
    width: 10px;
    height: 30px;
    background: gold;
    position: absolute;
    top: -30px;
    left: 35px;
}

.lantern::after {
    content: '';
    width: 5px;
    height: 20px;
    background: gold;
    position: absolute;
    bottom: -20px;
    left: 37px;
}

.lantern2 {
    margin-top: 10px;
    transform: scale(0.8);
}
```

# Penjelasan
Penerapan Pure CSS pada proyek website perayaan Imlek ini merupakan sebuah eksperimen desain yang memadukan estetika tradisional oriental dengan kecanggihan logika styling modern, di mana setiap elemen visual seperti lampion yang bergoyang, kartu ucapan bernuansa emas, hingga mekanisme "buka angpao" digerakkan sepenuhnya oleh fitur bawaan CSS tanpa bantuan JavaScript.
