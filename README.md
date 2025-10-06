**Nama   :** Wahyu Andika  
**NIM    :** 312410182  
**Kelas  :** TI.24.A2  
**Matkul :** Pemrograman Web 1  
**Dosen Pengampu :** Agung Nugroho, S.Kom., M.Kom

# Praktikum Form Dropdown & Listbox Praktikum 3 #

**1. Struktur HTML Dasar**
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/af050ca7-dede-45e2-84af-e0d595e06659" />

```<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Dropdown dan Listbox</title>
</head>
<body>
    <header>
        <h1>Membuat Form</h1>
    </header>
</body>
</html>
```

**Penjelasan:**
Membuat struktur dasar HTML5 dengan deklarasi <!DOCTYPE html>, menambahkan tag <meta> untuk charset UTF-8 dan viewport agar responsif, serta membuat judul halaman menggunakan <title> dan header `<h1>.`

**2. Membuat Form Dasar**
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/c9de4770-525b-4a21-8a91-798ae2fb98bf" />

```<form action="proses.php" method="post">
    <fieldset>
        <legend>Data Pendaftaran</legend>
    </fieldset>
</form>
```
**Penjelasan :**

- Pada langkah ini kita menambahkan struktur dasar sebuah form menggunakan tag `<form>`.
- Atribut `action` berisi file tujuan saat data dikirim (`proses.php`), dan `method="post"` digunakan untuk mengirim data secara aman.
- Tag `<fieldset>` digunakan untuk mengelompokkan isi form.
- Tag `<legend>` memberikan judul pada kelompok form tersebut.

**3. Menambahkan Input Nama dan Dropdown Fakultas**
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/587e3be8-79b5-4cc7-88a1-233ec36ee089" />

```<p>
    <label for="nama">Nama</label>
    <input type="text" id="nama" name="nama">
</p>

<p>
    <label for="fakultas">Fakultas</label>
    <select id="fakultas" name="fakultas">
        <option value="">-- Pilih Fakultas --</option>
        <option value="teknik">Fakultas Teknik</option>
        <option value="ekonomi">Fakultas Ekonomi dan Bisnis</option>
        <option value="hukum">Fakultas Hukum</option>
        <option value="kedokteran">Fakultas Kedokteran</option>
    </select>
</p>
```

**Penjelasan :**

- Pada langkah ini ditambahkan dua elemen penting dalam form, yaitu:
- **Input teks “Nama”** menggunakan tag `<input type="text">` untuk mengisi nama lengkap pendaftar.
- **Dropdown “Fakultas”** menggunakan tag `<select>` dan beberapa `<option>` untuk menampilkan daftar pilihan fakultas.  
    Dropdown memudahkan pengguna memilih salah satu pilihan tanpa perlu mengetik manual.

**4. Menambahkan Alamat dan Jenis Kelamin**
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/fbbc5a47-deaa-4f52-9607-5dbb3d0080b7" />

```<p>
    <label for="alamat">Alamat</label>
    <textarea id="alamat" name="alamat" cols="20" rows="3" placeholder="Masukkan alamat lengkap"></textarea>
</p>

<p>
    <label>Jenis Kelamin</label>
    <input id="jk_l" type="radio" name="kelamin" value="L">
    <label for="jk_l">Laki-laki</label>
    <input id="jk_p" type="radio" name="kelamin" value="P">
    <label for="jk_p">Perempuan</label>
</p>
```

**Penjelasan :**
- **Field Alamat** menggunakan `<textarea>` agar pengguna dapat menulis teks lebih panjang.
- **Jenis Kelamin** menggunakan *radio button* untuk memilih salah satu dari dua pilihan.

**5. Menambahkan tombol login beserta style nya**
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/555d9ed4-61f7-4159-9bb9-b42021e8bc2d" />

**6. Final Form HTML + CSS**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Membuat Form</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            padding: 40px;
        }

        header {
            text-align: center;
            margin-bottom: 20px;
        }

        h1 {
            color: #197a43;
        }

        form {
            max-width: 500px;
            margin: 0 auto;
            background: #fff;
            padding: 20px;
            border: 1px solid #ccc;
        }

        fieldset {
            border: 1px solid #197a43;
            padding: 15px;
        }

        legend {
            font-weight: bold;
            color: #197a43;
        }

        p {
            margin-bottom: 15px;
        }

        label {
            display: inline-block;
            width: 120px;
            font-size: 14px;
        }

        input[type="text"],
        textarea {
            width: 250px;
            padding: 5px;
            border: 1px solid #aaa;
            border-radius: 4px;
        }

        textarea {
            resize: vertical;
        }

        .btn-login {
            border: 1px solid #197a43;
            background-color: #197a43;
            color: #ffffff;
            font-weight: 600;
            padding: 8px 20px;
            border-radius: 5px;
            cursor: pointer;
            margin-left: 120px;
            transition: transform .15s ease, box-shadow .15s ease;
            box-shadow: 0 4px 12px rgba(25,122,67,0.12);
        }

        .btn-login:hover {
            background-color: #155d32;
            transform: translateY(-2px);
            box-shadow: 0 8px 18px rgba(21,93,50,0.18);
        }

        .btn-login:active {
            transform: translateY(0);
            box-shadow: 0 3px 8px rgba(0,0,0,0.08);
        }
    </style>
</head>
<body>
    <header>
        <h1>Membuat Form</h1>
    </header>

    <form action="proses.php" method="post">
        <fieldset>
            <legend>Data Pelanggan</legend>

            <p>
                <label for="nama">Nama</label>
                <input type="text" id="nama" name="nama">
            </p>

            <p>
                <label for="alamat">Alamat</label>
                <textarea id="alamat" name="alamat" cols="20" rows="3"></textarea>
            </p>

            <p>
                <label>Jenis Kelamin</label>
                <input type="radio" id="jk_l" name="kelamin" value="L">
                <label for="jk_l">Laki-laki</label>
                <input type="radio" id="jk_p" name="kelamin" value="P">
                <label for="jk_p">Perempuan</label>
            </p>

            <p>
                <input type="submit" value="Login" class="btn-login">
            </p>
        </fieldset>
    </form>
</body>
</html>
```

**Penjelasan:**
Pada langkah ini ditambahkan tombol Login ke dalam form menggunakan elemen <input type="submit"> dengan class .btn-login.
Style CSS memberikan warna hijau khas #197a43, efek hover, dan bayangan agar tombol terlihat modern dan responsif.
Tombol diletakkan di bawah bagian Jenis Kelamin

## Modifikasi ##
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/db8954af-e892-4e2e-a62b-1170376402de" />

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Dropdown dan Listbox</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #e8f5e9 0%, #c8e6c9 100%);
            padding: 40px 20px;
            min-height: 100vh;
        }
        
        header {
            text-align: center;
            margin-bottom: 30px;
        }
        
        h1 {
            color: #2e7d32;
            font-size: 32px;
            font-weight: 600;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            margin-bottom: 10px;
        }
        
        .subtitle {
            color: #558b2f;
            font-size: 16px;
            font-weight: 400;
        }
        
        form {
            max-width: 600px;
            margin: 0 auto;
        }
        
        fieldset {
            border: 2px solid #a5d6a7;
            background: #ffffff;
            padding: 35px;
            border-radius: 15px;
            box-shadow: 0 8px 32px rgba(46, 125, 50, 0.15);
            animation: fadeInUp 0.6s ease-out;
        }
        
        .legend-title {
            color: #2e7d32;
            font-weight: 600;
            font-size: 22px;
            padding-bottom: 20px;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #66bb6a 0%, #43a047 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-align: center;
            border-bottom: 2px solid #a5d6a7;
        }
        
        form p {
            margin-bottom: 20px;
        }
        
        form p > label {
            display: inline-block;
            width: 120px;
            font-weight: 600;
            color: #2e7d32;
            vertical-align: top;
            padding-top: 8px;
        }
        
        form input[type="text"],
        form select,
        form textarea {
            border: 2px solid #a5d6a7;
            padding: 10px 15px;
            font-size: 14px;
            width: calc(100% - 140px);
            border-radius: 8px;
            transition: all 0.3s ease;
            background: #f1f8e9;
            font-family: inherit;
        }
        
        form input[type="text"]:focus,
        form select:focus,
        form textarea:focus {
            outline: none;
            border-color: #66bb6a;
            background: #ffffff;
            box-shadow: 0 0 0 4px rgba(102, 187, 106, 0.1);
            transform: translateY(-2px);
        }
        
        form select {
            cursor: pointer;
        }
        
        form select[multiple] {
            padding: 8px;
            min-height: 120px;
        }
        
        form select option {
            padding: 8px;
            border-radius: 4px;
            margin: 2px 0;
        }
        
        form select option:hover {
            background: #c8e6c9;
        }
        
        .info-text {
            margin-left: 120px;
            font-size: 12px;
            color: #689f38;
            font-style: italic;
            margin-top: -10px;
            margin-bottom: 20px;
            display: flex;
            align-items: center;
        }
        
        .info-text::before {
            content: "ℹ️";
            margin-right: 5px;
        }
        
        form input[type="submit"] {
            border: none;
            background: linear-gradient(135deg, #66bb6a 0%, #43a047 100%);
            color: #ffffff;
            font-weight: 600;
            padding: 14px 40px;
            border-radius: 25px;
            cursor: pointer;
            font-size: 16px;
            margin-left: 120px;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(67, 160, 71, 0.3);
            text-transform: uppercase;
            letter-spacing: 1px;
        }
        
        form input[type="submit"]:hover {
            background: linear-gradient(135deg, #43a047 0%, #2e7d32 100%);
            box-shadow: 0 6px 20px rgba(46, 125, 50, 0.4);
            transform: translateY(-3px);
        }
        
        form input[type="submit"]:active {
            transform: translateY(-1px);
            box-shadow: 0 3px 10px rgba(46, 125, 50, 0.3);
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .form-icon {
            width: 60px;
            height: 60px;
            background: linear-gradient(135deg, #66bb6a 0%, #43a047 100%);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 20px;
            font-size: 30px;
            box-shadow: 0 4px 15px rgba(67, 160, 71, 0.3);
        }
    </style>
</head>
<body>
    <header>
        <div class="form-icon">📝</div>
        <h1>Form Pendaftaran Mahasiswa</h1>
        <p class="subtitle">Silakan lengkapi data pendaftaran Anda</p>
    </header>
    
    <form action="proses.php" method="post">
        <fieldset>
            <div class="legend-title">Data Pendaftaran</div>
            
            <p>
                <label for="nama">Nama</label>
                <input type="text" id="nama" name="nama" placeholder="Masukkan nama lengkap">
            </p>

            <p>
                <label for="alamat">Alamat</label>
                <textarea id="alamat" name="alamat" cols="20" rows="3" placeholder="Masukkan alamat lengkap"></textarea>
            </p>

            <p>
                <label>Jenis Kelamin</label>
                <input id="jk_l" type="radio" name="kelamin" value="L">
                <label for="jk_l">Laki-laki</label>
                <input id="jk_p" type="radio" name="kelamin" value="P">
                <label for="jk_p">Perempuan</label>
            </p>
            
            <p>
                <label for="fakultas">Fakultas</label>
                <select id="fakultas" name="fakultas">
                    <option value="">-- Pilih Fakultas --</option>
                    <option value="teknik">Fakultas Teknik</option>
                    <option value="ekonomi">Fakultas Ekonomi dan Bisnis</option>
                    <option value="hukum">Fakultas Hukum</option>
                    <option value="kedokteran">Fakultas Kedokteran</option>
                </select>
            </p>
            
            <p>
                <label for="prodi">Program Studi</label>
                <select id="prodi" name="prodi">
                    <option value="">-- Pilih Program Studi --</option>
                    <option value="ti">Teknik Informatika</option>
                    <option value="si">Sistem Informasi</option>
                    <option value="te">Teknik Elektro</option>
                    <option value="tm">Teknik Mesin</option>
                </select>
            </p>
            
            <p>
                <label for="matkul">Mata Kuliah</label>
                <select id="matkul" name="matkul[]" multiple>
                    <option value="pemweb">Pemrograman Web</option>
                    <option value="basdat">Basis Data</option>
                    <option value="jarkom">Jaringan Komputer</option>
                    <option value="sisop">Sistem Operasi</option>
                    <option value="alpro">Algoritma & Pemrograman</option>
                    <option value="strdat">Struktur Data</option>
                </select>
            </p>
            <p class="info-text">
                Tekan Ctrl (Windows) atau Cmd (Mac) untuk memilih lebih dari satu
            </p>
            
            <p>
                <label for="hobi">Hobi</label>
                <select id="hobi" name="hobi[]" multiple size="5">
                    <option value="olahraga">Olahraga</option>
                    <option value="membaca">Membaca</option>
                    <option value="musik">Musik</option>
                    <option value="traveling">Traveling</option>
                    <option value="gaming">Gaming</option>
                    <option value="fotografi">Fotografi</option>
                    <option value="menulis">Menulis</option>
                </select>
            </p>
            <p class="info-text">
                Pilih satu atau lebih hobi
            </p>
            
            <p>
                <input type="submit" value="Daftar">
            </p>
        </fieldset>
    </form>
</body>
</html>
```
