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
    <strong>Brian Farrel Evandhika</strong>
    <br>
    <strong>2311102037</strong>
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

<p align="justify">

Cascading Style Sheets (CSS) merupakan bahasa pemformatan yang difungsikan untuk mendandani dan mengontrol presentasi visual halaman web, mulai dari kombinasi warna, jenis huruf, hingga pendistribusian tata letak. Kehadirannya secara murni memisahkan antara elemen struktural (HTML) dengan estetika visual desain. CSS dieksekusi menggunakan sintaks yang terbangun atas <i>selector</i>, <i>property</i>, dan <i>value</i>; di mana <i>selector</i> bertugas mengarahkan instruksi ke elemen spesifik (seperti tag, <i>class</i>, maupun <i>id</i>). Secara arsitektural, CSS berpegang pada konsep-konsep fundamental seperti <i>box model</i> (zona konten, <i>padding</i>, <i>border</i>, dan <i>margin</i>), sistem pengaturan ruang (<i>flexbox</i>, <i>grid</i>, <i>positioning</i>), hingga hierarki aturan (<i>cascading</i> & <i>specificity</i>). Lebih jauh, CSS dibekali kemampuan canggih untuk menyajikan tata bahasa visual yang <i>responsive</i> lewat fitur <i>media queries</i> sehingga elemen web mampu beradaptasi pada berbagai dimensi layar, serta memperkaya interaksi melalui modifikasi tingkat lanjut seperti <i>pseudo-class</i>, <i>pseudo-element</i>, maupun efek-efek animasi bergerak.
</p>

## Cara Menggunakan CSS

<p align="justify">

Penerapan CSS pada pengembangan antarmuka web dilakukan dengan menautkannya ke dokumen HTML guna mengontrol rekayasa estetikanya secara komprehensif. Secara praktis, implementasi CSS bisa diwujudkan melaui tiga metode: (1) <i>Inline CSS</i>, yaitu menyematkan langsung gaya visual ke dalam atribut elemen HTML; (2) <i>Internal CSS</i>, yang dideklarasikan secara tertutup dalam blok <code>&lt;style&gt;</code> di dalam ruang <code>&lt;head&gt;</code>; dan (3) <i>External CSS</i>, yang membantun sumber definisi CSS secara mandiri ke dalam berkas terpisah (".css"). Pendekatan berbasis panel eksternal lebih direkomendasikan karena dapat memaksimalkan aksesibilitas penggunaan ulang antarhalaman serta memelihara kerapian modul direktori. Cara bekerjanya sangat terstruktur, berpatokan pada perumusan <i>selector</i> untuk menangkap target pengubahan, lalu perumusan <i>property</i> sebagai parameter ubahan, dan diakhiri pematenan nilainya dalam bentuk <i>value</i> aktual. Alhasil, antarmuka portal web bukan cuma akan menarik secara desain, namun juga lebih tersusun hierarkis, serta adaptif dan ramah perambah.

</p>

## Contoh CSS

```css
p {
  color: green;
}
```

## Task 3: Project Bucin (Edisi Imlek)
### Souce code - html
```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Perayaan Imlek untuk Kesayangan</title>
  <link rel="stylesheet" href="style.css">
  <meta name="description" content="Ucapan Selamat Tahun Baru Imlek untuk Orang Tersayang.">
</head>
<body>

  <!-- Background Animated Blobs -->
  <div class="bg-blobs">
    <div class="blob blob-1"></div>
    <div class="blob blob-2"></div>
    <div class="blob blob-3"></div>
  </div>

  <!-- Giant Background Watermark -->
  <div class="watermark-center">2311102037_Brian Farrel Evandhika</div>

  <!-- Main Content Card -->
  <main class="card">
    <div class="css-angpao-wrapper">
      <div class="css-angpao"></div>
    </div>
    <h1>Selamat Tahun Baru Imlek</h1>
    <p>Gong Xi Fa Cai, sayangku! Semoga tahun ini membawa banyak kebahagiaan, kemakmuran, dan kesehatan untuk kita. Mari melangkah bersama menyambut tahun yang penuh hoki dan cinta.</p>
    
    <div class="button-group">
      <a href="#" class="btn btn-primary">Buka Angpao 🧧</a>
      <a href="#" class="btn btn-secondary">Kirim Peluk ❤️</a>
    </div>
  </main>

  <!-- Corner Watermark -->
  <div class="watermark">2311102037_Brian Farrel Evandhika</div>

</body>
</html>
```


Output:
<img src="ss-modul3-1.png" alt="preview" style="width:100%; max-width:900px;">
<img src="ss-modul3-2.png" alt="preview" style="width:100%; max-width:900px;">

# Penjelasan
<p align="justify">
Kode ini merupakan halaman web ucapan Tahun Baru Imlek yang ditujukan untuk orang tersayang. Tampilan utama dikemas secara modern dengan latar belakang berupa animasi <i>blobs</i> (bentuk abstrak bercahaya) yang bergerak secara melayang, serta sebuah kartu bergaya kaca transparan (<i>glassmorphism</i>) di tengah layar. Di dalam kartu tersebut terdapat grafis angpao yang dibentuk murni dari CSS, pesan ucapan yang dibalut dengan efek gradasi warna, serta beberapa tombol. Terdapat pula teks memudar berukuran raksasa di latar belakang yang memuat nama dan NIM pembuat karya sebagai tanda air (<i>watermark</i>).
</p>
<p align="justify">
Seluruh visualisasi bentuk dan animasi digarap hanya dengan teknologi HTML dan CSS tanpa bantuan skrip JavaScript. Pergerakan objek abstrak latar belakang dan perlambatan layar kemunculan kartu (<i>slide-up</i>) direalisasikan menggunakan kerangka perintah <code>@keyframes</code>. Pada bagian grafis angpao merah, pembangunannya memanfaatkan modifikasi perbatasan kotak sudut dan elemen bayangan (<i>pseudo-element</i>) <code>::before</code> dan <code>::after</code> untuk memunculkan tutup depan serta koin emas simbol kemakmuran, dan dikombinasikan dengan efek skala membesar mulus ketik disorot kursor (<i>hovering</i>). Di samping itu, ukuran halaman web telah dibekali penyesuaian khusus (<i>media queries</i>) yang menjamin tampilan tetap merespons dengan elok ketika diakses melalui perangkat berlayar sempit seperti gawai pintar.
</p>
