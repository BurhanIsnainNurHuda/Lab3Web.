# Lab3Web.

    Nama: Burhan Isnain Nur Huda 
    NIM: 312410266 
    Kelas: TI.24.A.2
    Mata Kuliah: Pemograman Web 1

#  Praktikum 3 - Form Dropdown & Listbox Multiple Selection

Halo semuanya! 👋  
Di praktikum kali ini aku bikin form sederhana pakai HTML.  
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
