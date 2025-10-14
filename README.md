- Nama : Muhamad Nikmal Wahid
- kelas : TI 24 a3
- Pemrograman Web


# Pratikum 4: HTML Layout 

## Intruksi Praktikum 
- Siapkan Text editor seperti VScode
- Buat file baru
- Buat struktur dasar dari dokumen HTML
- Mengikuti langkah-langkah yang tertera
- Lakukan validasi dokumen CSS

# Membuat List
## Langkah-langkah pratikum 
Membuat dokumen HTML seperti berikut: 
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
</body>
</html>
```
## Membuat Box Element
```
<section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
</section>
```
![Step1](ss1.png)

## CSS Float Property
```
<style>
        div {
            float: left;
            padding: 10px;
        }
        .div1 {
            background: red;
        }
        .div2 {
            background: yellow;
        }
        .div3 {
            background: green;
        }
</style>
```
![Step2](ss2.png)

## Mengatur Clearfix Element
```
<section>
        <div class="div1">Div 1</div>
        <div class="div2">Div 2</div>
        <div class="div3">Div 3</div>
        <div class="div4">Div 4</div>
</section>
```
```
.div4 {
            background: blue;
            clear: left;
            float: none;
        }
```
![Step3](ss3.png)

# Membuat Layout Sederhana
## Membuat pratikum
Buat folder baru dengan nama lab4_layout, kemudian membuat file baru dengan nama home.html dan file css dengan nama style.css
```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
    </div>
</body>
</html>
```
Kemudian Tambahkan 
```
<header>
    <h1>Layout Sederhana</h1>
</header>

<nav>
    <a href="home.html" class="active">Home</a>
    <a href="artikel.html">Artikel</a>
    <a href="about.html">About</a>
    <a href="kontak.html">Kontak</a>
</nav>

<section id="hero"></section>

<section id="wrapper">
    <section id="main"></section>
    <aside id="sidebar"></aside>
</section>

<footer>
    <p>&copy; 2021 - Universitas Pelita Bangsa</p>
</footer>
```
Tambahkan CSS
```
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:ital,wght@0,300;0,400;0,600;0,700;0,800;1,300;1,400;1,600;1,700;1,800&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans+Condensed:ital,wght@0,300;0,700;1,300&display=swap');

/* CSS */

* {
    margin: 0;
    padding: 0;
}

body {
    line-height: 1;
    font-size: 100%;
    font-family: 'Open Sans', sans-serif;
    color: #5a5a5a;
}

#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #cccccc;
}

/* Header */
header {
    padding: 20px;
}
header h1 {
    margin: 20px 10px;
    color: #b5b5b5;
}
```

## Membuat Navigasi
```
nav {
    display: block;
    background-color: #1f5faa;
}

nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #ffffff;
    font-size: 14px;
    text-decoration: none;
    font-weight: bold;
}

nav a.active, 
nav a:hover {
    background-color: #2b83ea;
}

```
![Step4](ss4.png)

## Membuat Hero Panel
```
<section id="hero">
    <h1>Hello World!</h1>
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
        elit, iaculis innisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
        pretium ac.
    </p>
    <a href="home.html" class="btn btn-large">Learn more &raquo;</a>
</section>
```
Tambahkan CSS
```
#hero {
    background-color: #e4e4e5;
    padding: 50px 20px;
    margin-bottom: 20px;
}

#hero h1 {
    margin-bottom: 20px;
    font-size: 35px;
}

#hero p {
    margin-bottom: 20px;
    font-size: 18px;
    line-height: 25px;
}
```
## Mengatur sel data 
```
#wrapper {
    margin: 0;
}

#main {
    float: left;
    width: 640px;
    padding: 20px;
}

/* Sidebar */

#sidebar {
    float: left;
    width: 260px;
    padding: 20px;
}
```
![Step5](ss5.png)

## Membuat sidebar Widget
```
<aside id="sidebar">
    <div class="widget-box">
        <h3 class="title">Widget Header</h3>
        <ul>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
            <li><a href="#">Widget Link</a></li>
        </ul>
    </div>

    <div class="widget-box">
        <h3 class="title">Widget Text</h3>
        <p>
            Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt
            arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer
            pharetra est nunc, nec pretium nunc pretium ac.
        </p>
    </div>
</aside>
```
Tambah CSS
```
.widget-box {
    border: 1px solid #eee;
    margin-bottom: 20px;
}

.widget-box .title {
    padding: 10px 16px;
    background-color: #428bca;
    color: #fff;
}

.widget-box ul {
    list-style-type: none;
}

.widget-box li {
    border-bottom: 1px solid #eee;
}

.widget-box li a {
    padding: 10px 16px;
    color: #333;
    display: block;
    text-decoration: none;
}
.widget-box li:hover a {
    background-color: #eee;
}

.widget-box p {
    padding: 15px;
    line-height: 25px;
}
```

## Mengatur Footer
```
footer {
    clear: both;
    background-color: #1d1d1d;
    padding: 20px;
    color: #eee;
}
```
![Step6](ss6.png)

## Menambahkan Elemen Lainnya pada main Content
```
<section id="main">
    <div class="row">
        <div class="box">
            <img src="https://dummyimage.com/120/db7d25/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>
                Donec sed odio dui. Etiam porta sem malesuada magna mollis
                euismod.
            </p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>

        <div class="box">
            <img src="https://dummyimage.com/120/3e73e6/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>
                Donec sed odio dui. Etiam porta sem malesuada magna mollis
                euismod.
            </p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>

        <div class="box">
            <img src="https://dummyimage.com/120/71e6d4/fff.png" alt="" class="image-circle">
            <h3>Heading</h3>
            <p>
                Donec sed odio dui. Etiam porta sem malesuada magna mollis
                euismod.
            </p>
            <a href="#" class="btn btn-default">View detail</a>
        </div>
    </div>
</section>
```
Tambah CSS
```
.box {
    display: block;
    float: left;
    width: 33.333333%;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
    padding: 0 10px;
    text-align: center;
}

.box h3 {
    margin: 15px 0;
}

.box p {
    line-height: 20px;
    font-size: 14px;
    margin-bottom: 15px;
}

box img {
    border: 0;
    vertical-align: middle;
}

.image-circle {
    border-radius: 50%;
}

.row {
    margin: 0 -10px;
    box-sizing: border-box;
    -moz-box-sizing: border-box;
    -webkit-box-sizing: border-box;
}

.row:after, row:before,
.entry:after, .entry:before {
    content: '';
    display: table;
}

.row:after,
.entry:after {
    clear: both;
}
```
![Step7](ss7.png)

## Menambahkan Content Artikel
```
<hr class="divider" />

<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="">
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
        pretium ac.
    </p>
</article>

<hr class="divider" />

<article class="entry">
    <h2>First featurette heading.</h2>
    <img src="https://dummyimage.com/150/7b8a70/fff.png" alt="" class="right-img">
    <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem
        elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla,
        vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc
        pretium ac.
    </p>
</article>
```
Tambah CSS
```
.divider {
    border: 0;
    border-top: 1px solid #eeeeee;
    margin: 40px 0;
}

.entry {
    margin: 15px 0;
}

.entry h2 {
    margin-bottom: 20px;
}

.entry p {
    line-height: 25px;
}

.entry img {
    float: left;
    border-radius: 5px;
    margin-right: 15px;
}

.entry .right-img {
    float: right;
}

```
# Pertanyaan dan Tugas
1. Buatlah form yang menampilkan dropdown menu dan listbox dengan multiple selection.

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Form Data Mahasiswa</title>
</head>
<body>
    <header>
        <h1>Form Data Mahasiswa</h1>
    </header>

    <form action="proses.php" method="Post">
        <fieldset>
            <legend>Data Mahasiswa</legend>

            <p>
                <label for="nama">Nama</label>
                <input type="text" id="nama" name="nama" placeholder="Masukkan nama lengkap">
            </p>

            <p>
                <label for="nim">NIM</label>
                <input type="text" id="nim" name="nim" placeholder="Masukkan NIM">
            </p>

            <p>
                <label>Jenis Kelamin</label>
                <input id="jk_l" type="radio" name="kelamin" value="L">
                <label for="jk_l">Laki-laki</label>
                <input id="jk_p" type="radio" name="kelamin" value="P">
                <label for="jk_p">Perempuan</label>
            </p>

            <p>
                <label for="prodi">Program Studi</label>
                <select id="prodi" name="prodi">
                    <option value="ti">Teknik Informatika</option>
                    <option value="si">Sistem Informasi</option>
                    <option value="mi">Manajemen Informatika</option>
                    <option value="tl">Teknik Lingkungan</option>
                </select>
            </p>

            <p>
                <label for="minat">Bidang Minat</label>
                <select id="minat" name="minat[]" size="3" multiple>
                    <option value="web">Web Development</option>
                    <option value="mobile">Mobile Development</option>
                    <option value="ai">Artificial Intelligence</option>
                    <option value="data">Data Science</option>
                    <option value="network">Computer Network</option>
                </select>
            </p>


            <p>
                <input type="submit" value="Kirim Data">
            </p>
        </fieldset>
    </form>

    <style>
        form p > label {
            display: inline-block;
            width: 120px;
        }

        form input[type="text"],
        form textarea,
        form select {
            border: 1px solid #197a43;
            padding: 4px;
            border-radius: 3px;
        }

        form input[type="submit"] {
            border: 1px solid #197a43;
            background: #197a43;
            color: #fff;
            font-weight: bold;
            padding: 5px 15px;
            cursor: pointer;
        }

        form input[type="submit"]:hover {
            background: #145a32;
        }
    </style>
</body>
</html>
```
![Step8](ss8.png)


   


