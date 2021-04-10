# Pemrograman Web
```
Nama  : Arif Samsudin
NIM   : 311910255
Kelas : TI.19.C1

```
## 1. Membuat dokumen HTML
Buatlah dokumen HTML seperti berikut
```
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
```
![1](https://user-images.githubusercontent.com/81839328/114265902-91749d80-9a1d-11eb-87be-d69f5030ac33.JPG)

## 2. Mendeklarasikan CSS Internal
Kemudian tambahkan deklarasi CSS internal seperti berikut pada bagian head dokumen.
```
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
```
![2](https://user-images.githubusercontent.com/81839328/114265978-f29c7100-9a1d-11eb-9383-705fbbfc8c18.JPG)

## 3. Menambahkan Inline CSS
Kemudian tambahkan deklarasi inline CSS pada tag <p> seperti berikut.
```
<p style="text-align: center; color: #ccd8e4;">
```
![3](https://user-images.githubusercontent.com/81839328/114266068-60e13380-9a1e-11eb-8e1d-7e534a03b8a3.JPG)
  
## 4. Membuat CSS Eksternal
Buatlah file baru dengan nama style_eksternal.css kemudian buatlah deklarasi CSS seperti berikut.
```
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
```
![4](https://user-images.githubusercontent.com/81839328/114266146-db11b800-9a1e-11eb-854b-bd3755dd5cd2.JPG)

Kemudian tambahkan tag <link> untuk merujuk file css yang sudah dibuat pada bagian <head>
```  
<head>
    <!-- menyisipkan css eksternal -->
    <link rel="stylesheet" href="style_eksternal.css" type="text/css">
</head>
```
![5](https://user-images.githubusercontent.com/81839328/114266186-26c46180-9a1f-11eb-960a-2fd98a8d4d08.JPG)

## 5. Menambahkan CSS Selector
Selanjutnya menambahkan CSS Selector menggunakan ID dan Class Selector. Pada file style_eksternal.css, tambahkan kode berikut.
```
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
```
![6](https://user-images.githubusercontent.com/81839328/114266285-ace0a800-9a1f-11eb-834b-762a0412a4f5.JPG)

## Jawab Pertanyaan
```
1. Lakukan eksperimen dengan mengubah dan menambah properti dan nilai pada kode CSS dengan mengacu pada CSS Cheat Sheet yang diberikan pada file terpisah dari modul ini.
```   
Saya melakukan perubahan pada warna font, border width, menambahkan properti font size pada body.   
![7](https://user-images.githubusercontent.com/81839328/114267128-4447fa00-9a24-11eb-8843-b79ceb9f17ba.JPG)
``` 
2. Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!
``` 
Pendeklarasian CSS elemen h1 mengubah tampilan seluruh elemen yang memiliki tag h1, sedangkan #intro h1 hanya mengubah tampilan elemen h1 yang memiliki id #intro.
```
3. Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!
```
Deklarasi yang akan ditampilkan adalah inline CSS karena Inline CSS memiliki perrmintaan HTTP yang lebih kecil sehingga sistem membaca lebih cepat.
![8](https://user-images.githubusercontent.com/81839328/114267914-b6224280-9a28-11eb-8350-a6ca694ed616.JPG)
![9](https://user-images.githubusercontent.com/81839328/114267918-b8849c80-9a28-11eb-8437-07b79d5ace11.JPG)
```
4. Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ( <p id="paragraf-1" class="text-paragraf"> )
```
Perbedaan dari class dan id adalah class di panggil menggunakan tanda titk dan id dengan tanda pagar, jadi kedua deklarasi tetap akan tampil pada browser.
hanya saja class dapat di berikan pada banyak element html dan dapat di panggil sekaligus, sedangkan id hanya dapat bekerja pada satu penandaan saja

