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
    <strong>Rasyid Nafsyarie</strong>
    <br>
    <strong>2311102011</strong>
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
    <title>Gong Xi Fa Cai, Bubub!</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <div class="lantern-wrapper">
            <div class="lantern">🏮</div>
            <div class="lantern">🏮</div>
        </div>

        <div class="card">
            <h1>Gong Xi Fa Cai</h1>
            <h2>Happy Chinese New Year</h2>
            <p>Untuk kesayanganku...</p>
            
            <input type="checkbox" id="open-message">
            <label for="open-message" class="btn-angpao">Buka Angpao 🧧</label>
            
            <div class="hidden-message">
                <p>Semoga di tahun Naga/Ular ini, kita makin langgeng dan bahagia terus ya! I love you! ❤️</p>
            </div>
        </div>
    </div>
</body>
</html>
```

### Source code - css

```css
body {
    background-color: #800000; 
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: #FFD700; 
    overflow: hidden;
}

.container {
    text-align: center;
    position: relative;
}

.lantern-wrapper {
    display: flex;
    justify-content: space-around;
    width: 100%;
    position: absolute;
    top: -150px;
}

.lantern {
    font-size: 3rem;
    animation: sway 3s ease-in-out infinite;
}

@keyframes sway {
    0%, 100% { transform: rotate(-10deg); }
    50% { transform: rotate(10deg); }
}

.card {
    background: rgba(255, 255, 255, 0.1);
    padding: 2rem;
    border: 3px solid #FFD700;
    border-radius: 15px;
    backdrop-filter: blur(5px);
    box-shadow: 0 10px 30px rgba(0,0,0,0.5);
}

#open-message {
    display: none; 
}

.hidden-message {
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.8s ease-in-out, opacity 0.5s;
    opacity: 0;
    margin-top: 20px;
    font-style: italic;
}

#open-message:checked ~ .hidden-message {
    max-height: 200px;
    opacity: 1;
}

.btn-angpao {
    display: inline-block;
    background: #FFD700;
    color: #800000;
    padding: 10px 20px;
    border-radius: 50px;
    cursor: pointer;
    font-weight: bold;
    transition: transform 0.3s;
}

.btn-angpao:hover {
    transform: scale(1.1);
}
```


Output:
<img src="Modul3.png" alt="preview" style="width:100%; max-width:900px;">

# Penjelasan
Penerapan Pure CSS pada proyek website perayaan Imlek ini merupakan sebuah eksperimen desain yang memadukan estetika tradisional oriental dengan kecanggihan logika styling modern, di mana setiap elemen visual seperti lampion yang bergoyang, kartu ucapan bernuansa emas, hingga mekanisme "buka angpao" digerakkan sepenuhnya oleh fitur bawaan CSS tanpa bantuan JavaScript.
