# Pemograman Web
~~~
Nama  : Andry Prasetia Perdana
NIM   : 311910284
Kelas : TI 19 C1
~~~
# 1. Membuat dokumen HTML
Buatlah dokumen HTML seperti berikut
~~~
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
      <h1>CSS Internal dan <i>Inline CSS</i></h1>
    </header>
    <nav>
      <a href="lab2_css_dasar.html">CSS Dasar</a>
      <a href="lab2_css_eksternal.html">CSS Eksternal</a>
      <a href="lab1_tag_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID Selector -->
    <div id="intro">
      <h1>Hello World</h1>
      <p>Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML dan CSS.</p>
      <!-- CSS Class Selector -->
      <a class="button btn-primary" href="#intro">Informasi selengkapnya.</a>
    </div>
</body>
</html>
~~~
![Screenshot (35)](https://user-images.githubusercontent.com/81818989/114185585-173a0f80-9970-11eb-8c2b-54fd525519b4.png)
# 2. Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
~~~
<head>
    <title>CSS Dasar</title>
    <style>
        body {
            font-family:'Open Sans', sans-serif;
        }
        header {
            min-height: 80px;
            border-bottom:1px solid #77CCEF;
        }
        h1 {
            font-size: 24px;
            color: #0F189F;
            text-align: center;
            padding: 20px 10px;
        }
        h1 i {
            color:#6d6a6b;
        }
    </style>
</head>
~~~
![Screenshot (36)](https://user-images.githubusercontent.com/81818989/114197500-9df4e980-997c-11eb-9742-601ff795fd2e.png)
# 3. Menambahkan Inline CSS
Kemudian tambahkan deklarasi inline CSS pada tag
~~~
<p style="text-align: center; color: #ccd8e4;">
~~~
![Screenshot (37)](https://user-images.githubusercontent.com/81818989/114197694-c8df3d80-997c-11eb-8450-20fa0d2b9e19.png)
# 4. Membuat CSS Eksternal
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
~~~
nav {
    background: #20A759;
    color:#fff;
    padding: 10px;
}
nav a {
    color: #fff;
    text-decoration: none;
    padding:10px 20px;
}
nav .active,
nav a:hover {
    background: #0B6B3A;
}
~~~
![Screenshot (38)](https://user-images.githubusercontent.com/81818989/114197894-017f1700-997d-11eb-9a62-dfd78620c4e8.png)
Kemudian tambahkan tag untuk merujuk file css yang sudah dibuat pada bagian
~~~
<head>
    <!-- menyisipkan css eksternal -->
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
~~~
![Screenshot (39)](https://user-images.githubusercontent.com/81818989/114198074-1c518b80-997d-11eb-89d2-7e57e4030279.png)
# 5. Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut.
~~~
/* ID Selector */
#intro {
    background: #418fb1;
    border: 1px solid #099249;
    min-height: 100px;
    padding: 10px;
}
#intro h1 {
    text-align: left;
    border: 0;
    color: #fff;
}
/* Class Selector */
.button {
    padding: 15px 20px;
    background: #bebcbd;
    color: #fff;
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}
.btn-primary {
    background: #E42A42;
}
~~~
![Screenshot (40)](https://user-images.githubusercontent.com/81818989/114198227-4905a300-997d-11eb-8236-52bbdc0412f0.png)

# Pertanyaan
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
~~~
ini adalah ekperimen saya dengan mengubah warna dan menambah kolom properti dan nilai padding pada kode css
~~~
![Screenshot (42)](https://user-images.githubusercontent.com/81818989/114206689-c9c89d00-9985-11eb-8a9f-3e0943fb3920.png)

2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
~~~
Pendeklarasian CSS elemen h1 mengubah tampilan seluruh elemen yang memiliki tag h1, sedangkan #intro h1 hanya mengubah tampilan elemen h1 yang memiliki id #intro.
~~~
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
~~~
Kedua deklarasi tersebut akan tampil, namun selector ID yang akan tampil jika deklarasinya ada yang sama antara ID dan Class.
~~~
contoh
![Screenshot (43)](https://user-images.githubusercontent.com/81818989/114209124-7ad03700-9988-11eb-8c46-5ff5734b11b6.png)
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! `<p id="paragraf-1" class="text-paragraf">`
~~~
Perbedaan dari class dan id adalah class di panggil menggunakan tanda titk dan id dengan tanda pagar, jadi kedua deklarasi tetap akan tampil pada browser.
hanya saya class dapat di berikan pada banyak element html dan dapat di panggil sekaligus, sedangkan id hanya dapat bekerja pada satu penandaan saja
~~~
contoh
![Screenshot (44)](https://user-images.githubusercontent.com/81818989/114212508-1dd68000-998c-11eb-98cb-1316be33cca6.png)
![Screenshot (45)](https://user-images.githubusercontent.com/81818989/114212536-275fe800-998c-11eb-8ab9-aef90c5cf857.png)
