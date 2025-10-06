# Lab3Web.

    Nama: Burhan Isnain Nur Huda 
    NIM: 312410266 
    Kelas: TI.24.A.2
    Mata Kuliah: Pemograman Web 1

#  Praktikum 3 - Form Dropdown & Listbox Multiple Selection

Halo! 
Di praktikum kali ini saya bikin form sederhana pakai HTML.  
Tujuannya buat latihan bikin **dropdown** dan **listbox** yang bisa milih lebih dari satu item.

---

##  Apa yang saya Bikin

Jadi saya bikin form data mahasiswa.  
Isinya:
- Dropdown buat milih **Fakultas**
- Listbox buat milih **bidang minat**
- Tombol kirim buat submit data  

Tampilannya juga saya kasih sedikit CSS seperti tugas sebelum nya biar gak polos banget.

---

##  Langkah-langkahnya

### 1. Bikin File dan Struktur Dasar
Pertama aku buat folder baru namanya `Lab3Web` dan file `formulir.html`.  
Terus aku tulis struktur HTML dasarnya kayak gini:

    html
    <!DOCTYPE html>
    <html lang="id">
    <head>
    <meta charset="UTF-8">
    <title>Formulir Data Mahasiswa</title>
    </head>
    <body>
    <h2>Formulir Data Mahasiswa</h2>
    </body>
    </html>

Penjelasan:

`<!DOCTYPE html>` → ngasih tahu browser kalau dokumen ini pakai versi HTML5.
`<html lang="id">` → kode halaman web, dan lang="id" artinya bahasa Indonesia.
`<head>` → tempat taruh info penting kayak judul halaman, encoding, dan style CSS.
`<meta charset="UTF-8">` → biar huruf-huruf (termasuk huruf Indonesia) bisa tampil dengan benar.
`<meta name="viewport" ...>` → bikin tampilan halaman tetap proporsional kalau dibuka di HP.
`<title>` → teks yang muncul di tab browser (judulnya “Formulir Data Mahasiswa”).
`<body>` → semua isi halaman yang bakal muncul di browser, kayak form, teks, tombol, dll.

2. Nambahin Dropdown

Bagian ini buat milih fakultas.
Saya pake tag `<select>` sama `<option>` biar bisa milih satu aja.

    <label for="fakultas">Pilih Fakultas:</label>
    <select name="fakultas" id="fakultas" required>
    <option value="">-- Pilih Fakultas --</option>
    <option value="ft">Fakultas Teknik</option>
    <option value="fisip">Fakultas Ilmu Sosial & Politik</option>
    <option value="fekon">Fakultas Ekonomi</option>
    <option value="fkip">Fakultas Keguruan & Ilmu Pendidikan</option>
    </select>

Penjelasan:

`<label>` → teks penjelas untuk form input. Atribut for="fakultas" nyambung ke id="fakultas".
`<select>` → membuat menu dropdown.
`name="fakultas"` → nama variabel yang dikirim saat form disubmit.
`id="fakultas"` → penghubung dengan label.
`required` → pengguna wajib pilih salah satu sebelum bisa klik submit.
`<option>` → isi pilihan yang muncul di dropdown.
`value` → nilai yang dikirim ke server.
`Teks di dalam <option>` adalah yang dilihat pengguna di layar.
`Baris pertama (-- Pilih Fakultas --)` cuma placeholder agar pengguna tahu harus memilih dulu.

3. Nambahin Listbox Multiple Selection

Di sini saya bikin biar user bisa milih lebih dari satu bidang minat.

    <label for="minat">Bidang Minat (boleh pilih lebih dari satu):</label>
    <select name="minat[]" id="minat" multiple size="5">
    <option value="programming">Pemrograman</option>
    <option value="design">Desain Grafis</option>
    <option value="jaringan">Jaringan Komputer</option>
    <option value="ai">Kecerdasan Buatan</option>
    <option value="data">Analisis Data</option>
    </select>

Penjelasan:

Sama kayak dropdown, tapi di sini kita tambahin dua atribut penting:
`multiple` → artinya user bisa pilih lebih dari satu item.
`size="5"` → jumlah item yang langsung kelihatan di layar tanpa scroll.
`name="minat[]"` → tanda [] artinya datanya bisa dikirim dalam bentuk array (karena bisa lebih dari satu pilihan).
`<option>` → masing-masing adalah bidang minat yang bisa dipilih (programming, desain, jaringan, dll).
Kalau kamu tekan `Ctrl (di Windows)` atau `Cmd (di Mac)` sambil klik beberapa opsi, kamu bisa pilih lebih dari satu minat.
4. Kasih Tombol Kirim

Terakhir saya tambahin tombol submit biar form-nya bisa dikirim.

    <input type="submit" value="Simpan Data">

5. Biar Gak Monoton, Saya Tambahin CSS Dikit

Supaya tampilannya lebih enak dilihat dan gak kayak tugas seadanya

    <style>
    body {
    font-family: Arial, sans-serif;
    background-color: #f3f6fa;
    padding: 20px;
    }

     form {
    background-color: #fff;
    border-radius: 10px;
    padding: 25px;
    width: 400px;
    margin: 0 auto;
    box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }

    label {
    font-weight: bold;
    display: block;
    margin-top: 15px;
    }

    select, input[type="submit"] {
    margin-top: 8px;
    width: 100%;
    padding: 8px;
    border-radius: 6px;
    border: 1px solid #ccc;
    }

    input[type="submit"] {
    background-color: #3498db;
    color: white;
    font-weight: bold;
    border: none;
    cursor: pointer;
    transition: 0.3s;
    }

    input[type="submit"]:hover {
    background-color: #2980b9;
    }
    </style>

Penjelasan:

`<style>` → tempat nulis CSS langsung di dalam file HTML (internal CSS).
`body` → ngatur font, warna background, dan padding seluruh halaman.
`h2` → bikin judul di tengah dan warnanya lebih gelap.
`form` → ngasih warna putih, sudut melengkung (border-radius), bayangan (box-shadow), dan posisi di tengah.
`label` → supaya teks label terlihat tebal dan agak terpisah dari elemen sebelumnya.
`select, input[type="submit"]` → biar dropdown, listbox, dan tombol punya ukuran lebar yang sama (100%) dan bentuk seragam.
`input[type="submit"]:hover` → bikin efek warna berubah saat kursor diarahkan ke tombol (efek interaktif).

### Hasil Screenshoot
![Gambar WhatsApp 2025-10-06 pukul 13 36 15_e572a735](https://github.com/user-attachments/assets/7fbf2a16-6987-417a-a51a-0df1e048efd1)

