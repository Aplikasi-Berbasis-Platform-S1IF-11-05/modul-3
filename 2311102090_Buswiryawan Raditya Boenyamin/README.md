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
    <strong>Buswiryawan Raditya Boenyamin</strong>
    <br>
    <strong>2311102090</strong>
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

## Pengertian HTML

HTML (*HyperText Markup Language*) merupakan bahasa dasar yang digunakan untuk membangun sebuah web. HTML menangani elemen-elemen dasar pada pembangunan sebuah *website*. Struktur HTML paling dasar terdiri dari tag `<html>`, `<head>`, dan `<body>`.

---

## 1. Tag HTML

*Tag* dalam HTML secara normal memiliki **sepasang tag**, di mana tag pertama merupakan tag pembuka dan yang kedua merupakan tag penutup. Konten yang ingin ditampilkan pada laman web diletakkan di antara kedua tag tersebut.

```html
<nama_tag> letakkan konten di sini … </nama_tag>
```

Tag dalam HTML tidak semuanya berbentuk pasangan. Ada beberapa tag yang hanya berdiri sendiri, seperti tag `<br/>` yang berguna untuk berpindah baris.

---

## 2. Elemen HTML

Elemen HTML merupakan tag HTML yang telah memiliki konten atau isi di antara kedua tag pembuka dan penutupnya. Elemen HTML dapat berupa teks atau juga dapat menyisipkan tag HTML lain.

```html
<!DOCTYPE html>
<html>
<head>
  <!-- Contoh elemen berisi tag lain -->
  <title>Page Title</title>
</head>
<body>
  <h1>My First Heading</h1>
  <!-- Contoh elemen berisi teks -->
  <p>My first paragraph.</p>
</body>
</html>
```

---

## 3. Atribut HTML

Atribut HTML merupakan tambahan informasi dari sebuah tag HTML. Bentuk atribut untuk setiap tag HTML berbeda-beda, seperti menambahkan informasi warna elemen, ukuran lebar, ukuran panjang, dan lain-lain.

Atribut yang paling sering digunakan adalah **`id`** dan **`class`**, karena keduanya berperan besar dalam pengembangan laman web dengan CSS dan JavaScript.

Atribut HTML dideklarasikan di dalam tag pembuka dengan format `nama_atribut="value"`.

```html
<a href="www.google.co.id">Google.co.id</a>
<input type="button" id="btnSubmit" class="btnSubmit1" value="Kirim"/>
```

---

## 4. Struktur Dasar HTML

```html
<!DOCTYPE html>
<html>
<head>
  <title>Page Title</title>
</head>
<body>
  <h1>My First Heading</h1>
  <p>My first paragraph.</p>
</body>
</html>
```

| Elemen | Fungsi |
|--------|--------|
| `<!DOCTYPE html>` | Mendefinisikan dokumen menjadi HTML5 |
| `<html>` | Elemen dasar dari halaman HTML |
| `<head>` | Berisi informasi meta tentang dokumen |
| `<title>` | Menentukan judul untuk dokumen |
| `<body>` | Berisi konten halaman yang terlihat |

---

## 5. Heading

Heading pada HTML berguna untuk menampilkan judul dari konten laman web. Heading berperan penting untuk mesin pencarian karena sistem mesin pencarian menggunakan heading sebagai index pencarian.

Terdapat **enam tingkatan heading** — semakin kecil nilainya, semakin penting dan semakin besar ukurannya.

```html
<h1>Heading 1</h1>
<h2>Heading 2</h2>
<h3>Heading 3</h3>
<h4>Heading 4</h4>
<h5>Heading 5</h5>
<h6>Heading 6</h6>
```

---

## 6. Hyperlink

Hyperlink memungkinkan halaman web berpindah laman atau bernavigasi menuju laman web yang lain. Tag yang digunakan adalah `<a>…</a>`.

Atribut **`href`** wajib digunakan dan bernilai URL atau alamat dari laman web tujuan.

```html
<a href="www.google.co.id">Visit Google</a>
```

---

## 7. Tabel

Tabel pada HTML digunakan untuk menampilkan data yang membutuhkan bentuk tabel.

| Tag | Fungsi |
|-----|--------|
| `<table>` | Mendefinisikan tabel |
| `<tr>` | Mendefinisikan baris (*table row*) |
| `<th>` | Mendefinisikan heading kolom (*table header*) |
| `<td>` | Mendefinisikan sel data (*table data*) |

Untuk melakukan **Merge Cell**, gunakan atribut:
- **`colspan`** — menggabungkan beberapa kolom secara horizontal
- **`rowspan`** — menggabungkan beberapa baris secara vertikal

```html
<table width="80%" height="50%" border="1">
  <tr>
    <th rowspan="2">Nama Lengkap</th>
    <th colspan="2">Gelar Pendidikan</th>
    <th rowspan="2">Age</th>
  </tr>
  <tr>
    <th>Sarjana</th>
    <th>Magister</th>
  </tr>
</table>
```

---

## 8. Image

Tag yang digunakan untuk menampilkan gambar adalah `<img/>`. Tag ini tidak memiliki pasangan penutup sehingga ditambahkan garis miring di akhir.

Atribut **`src`** wajib diisi dengan alamat direktori gambar yang disimpan.

```html
<img src="gambar.jpg" width="50%" height="50%"/>
```

---

## 9. Audio dan Video

Sejak HTML5, audio dan video dapat disisipkan langsung tanpa plugin seperti Flash Player.

**Audio** menggunakan tag `<audio>` dan `<source>`:

```html
<audio controls>
  <source src="horse.ogg" type="audio/ogg">
  <source src="horse.mp3" type="audio/mpeg">
  Your browser does not support the audio element.
</audio>
```

**Video** menggunakan tag `<video>` dan `<source>`:

```html
<video width="400" controls>
  <source src="mov_bbb.mp4" type="video/mp4">
  <source src="mov_bbb.ogg" type="video/ogg">
  Your browser does not support HTML5 video.
</video>
```

---

## 10. Form

Form pada HTML digunakan sebagai wadah untuk menampung dan mengumpulkan data dari pengguna. Tag dasarnya adalah `<form>…</form>`.

Atribut utama tag form:
- **`action`** — menentukan tujuan data saat tombol Submit ditekan
- **`method`** — bernilai `POST` atau `GET`

### Elemen-Elemen Form

| Tag | Type | Fungsi |
|-----|------|--------|
| `<input/>` | `text` | Input data teks |
| `<input/>` | `password` | Input data password |
| `<input/>` | `email` | Input data email |
| `<input/>` | `radio` | Pilihan berbentuk radio button |
| `<input/>` | `checkbox` | Pilihan berbentuk checkbox |
| `<input/>` | `submit` | Tombol pengiriman data form |
| `<select>` + `<option>` | — | Pilihan berbentuk dropdown list |
| `<textarea>` | — | Input teks panjang/paragraf |
| `<button>` | `button` | Tombol aksi |

### Atribut Elemen Form

| Atribut | Fungsi |
|---------|--------|
| `id` | ID elemen untuk CSS/JavaScript |
| `name` | Nama elemen untuk pengolahan data |
| `class` | Kelas elemen untuk CSS/JavaScript |
| `placeholder` | Teks sementara sebelum ada input |
| `value` | Nilai default elemen |
| `disabled` | Membuat elemen tidak dapat dioperasikan |
| `readonly` | Membuat elemen tidak dapat diubah |
| `checked` | Membuat checkbox/radio terpilih secara default |
| `selected` | Membuat option pada select terpilih secara default |

---

*Sumber: Modul 3 Praktikum Pemrograman Web 2024 — Laboratorium High Performance, Fakultas Informatika, Universitas Telkom Purwokerto*

# Tugas 2 Ujian Web Purba
Bikin tampilan table dasar, tapi posisinya wajib persis di tengah layar. Nah, syarat utamanya: HARAM pakai CSS, inline style, atau styling apapun. Coba gali lagi ingatan lu soal tag-tag HTML jadul yang bisa ngakalin ini.
```
<!-- 2311102090_Buswiryawan Raditya Boenyamin_S1IF-11-05 -->

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tabel</title>
</head>
<body>
    <table align="center" border="1" cellpadding="10" cellspacing="0">
        <tr>
            <th>Nama</th>
            <th>NIM</th>
            <th>Kelas</th>
        </tr>
        <tr>
            <td>Buswiryawan Raditya Boenyamin</td>
            <td>2311102090</td>
            <td>S1IF-11-05</td>
        </tr>
        <tr>
            <td>Raditya</td>
            <td>2311102090</td>
            <td>S1IF-11-05</td>
        </tr>
        <tr>
            <td>Boenyamin</td>
            <td>2311102090</td>
            <td>S1IF-11-05</td>
        </tr>
        <tr>
            <td>Mulyono</td>
            <td>2311102666</td>
            <td>S1IF-11-02</td>
        </tr>
        <tr>
            <td>Bahlil</td>
            <td>2311102066</td>
            <td>S1IF-11-02</td>
        </tr>
    </table>
</body>
</html>
```
Output:
<img width="1901" height="961" alt="image" src="Output/Output1.png" />


