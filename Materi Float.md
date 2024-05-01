# penjelasan float
`Float` CSS adalah properti yang digunakan dalam web development untuk mengubah cara elemen HTML disusun di dalam _container_ _web_. Properti ini memungkinkan elemen (seperti _images_ atau div) "mengambang" ke sisi kiri atau kanan _container_, sementara elemen lain mengalir di sekitarnya.
Secara teknis, saat elemen diberi properti `float`, elemen tersebut “diangkat” dari _normal flow_ dan ditempatkan sepanjang sisi _container_. Elemen lain kemudian mengalir di sekitar elemen yang mengambang tersebut.
Namun, `float` tidak datang tanpa tantangan. Untuk menggunakannya, kamu perlu memahami secara mendalam bagaimana elemen-elemen berinteraksi dalam ruang dua dimensi. Melalui artikel ini, kita akan menjelajahi lebih detail tentang `float`, mulai dari _syntax, values, sampai_ cara dan contoh penggunaanya..
# Syntax Float CSS
Untuk menggunakan properti `float`, terlebih dahulu kamu harus mengetahui sintaksnya. Berikut cara penulisan `float` dalam CSS:
```
selector {
  float: values;
}
```
Dalam sintaks di atas, "_values_" bisa berupa:
- `left`: elemen akan mengambang ke sisi kiri _container-_nya. Bisa juga menggunakan _value_ `inline-start.`
- `right`: elemen akan mengambang ke sisi kanan _container-_nya. Bisa juga menggunakan _value_ `inline-end.`
- `none`: elemen tidak akan mengambang. Ini adalah nilai _default_.
Dalam praktiknya, penting untuk diingat bahwa elemen yang diatur untuk mengambang dapat keluar dari _normal flow_ dan berpotensi menyebabkan masalah _layout_. Untuk mengatasi ini, kamu perlu menggunakan teknik yang disebut "**clearfix**" agar konten tidak _'runaway'_ atau berantakan.

# Values dalam Properti Float CSS
Setiap _values_ dalam properti `float` memberikan kontrol kepada web developer untuk mengatur layout elemen-elemen dalam sebuah halaman _web_. Dengan menggunakan nilai-nilai ini secara tepat, kamu dapat memastikan setiap elemen ditempatkan presisi sesuai keinginan.
Penjelasan masing-masing _values_ yang tersedia untuk properti **float**.
## none
`Value float: none` ; menetapkan bahwa elemen tidak akan mengambang. Artinya, elemen akan ditampilkan di tempatnya dalam _normal flow._ _Value_ none adalah nilai _default_ yang digunakan jika kamu tidak ingin elemen tertentu mengambang ke sisi mana pun dari _container-_nya.
contohnya : 
```css
```html
box {
    width: 100px;
    height: 100px;
    background-color: blue;
    float: none;
```

## Left
`Value float: left` ; membuat elemen akan mengambang ke sisi kiri _container_. Elemen lain di sekitar elemen yang mengambang akan mengisi ruang di sisi kanannya.
Nilai ini berguna ketika kamu ingin teks mengalir di sebelah kanan gambar atau elemen lain.
contohnya : 
```css
.box {
	width: 100px;
    height: 100px;
    background-color: #f0f0f0;
    margin: 10px;
    float: left; 
```

## Right
Berbanding terbalik dengan left, `value float: right` ; menjadikan elemen mengambang ke sisi kanan _container_, dengan elemen lain mengisi ruang di sisi kirinya. _Value_ ini sering dipakai untuk menempatkan elemen seperti menu navigasi atau panel informasi di sisi kanan halaman _web_.
contohnya : 
```css
 .box {
    width: 100px;
    height: 100px;
    background-color: lightblue;
    float: right;
```

## Cara dan Contoh Penggunaan Float CSS**
Berikut cara menggunakan `float` dan contoh penggunaannya untuk menyusun elemen HTML berdampingan:
- Tentukan elemen yang ingin diatur
Pertama, tentukan elemen HTML yang ingin kamu atur dengan `float`. Elemen ini bisa berupa gambar, div, atau elemen lain dalam kode HTML milikmu.

- Tambahkan properti float dalam CSS
Setelah itu, buka _file_ CSS yang berkaitan dengan halaman _web_-mu. Di sini, kamu akan menambahkan aturan CSS untuk elemen yang telah ditentukan.
Tambahkan properti `float` dan tentukan apakah kamu ingin elemen mengambang ke kiri (**left**) atau ke kanan (**right**).
Contoh:
```
.element-kiri {
  float: left;
}
.element-kanan {
  float: right;
}
```

- Atur lebar elemen (opsional)
Agar lebih terkontrol, kamu mungkin ingin menentukan lebar elemen yang menggunakan **float**. Hal ini membantu memastikan elemen tersebut tidak mengambil terlalu banyak ruang.
Contoh:
```
.element-kiri {
  float: left;
  width: 50%;
}
.element-kanan {
  float: right;
  width: 50%;
}
```

 - Uji tampilan web
Setelah menambahkan dan menyesuaikan _setting_ untuk **float**, simpan perubahan lalu _refresh_ halaman _web_ untuk melihat hasilnya. Sesuaikan jika diperlukan.
Misalkan kamu memiliki dua div yang ingin ditempatkan berdampingan. Berikut cara mengaturnya menggunakan **float**:

**Kode HTML:**
```html
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Contoh Tampilan Website Pembelian Menggunakan Float</title>
</head>
<body>
<div class="container">
    <div class="product">
        <img src="img5..jpg" alt="Product 1">
        <div class="product-title">Product 1</div>
        <div class="product-price">$19.99</div>
        <div class="product-description">Lorem ipsum dolor sit amet, consectetur adipiscing elit.</div>
    </div>
    <div class="product">
        <img src="img3.jpg" alt="Product 2">
        <div class="product-title">Product 2</div>
        <div class="product-price">$24.99</div>
        <div class="product-description">Sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.</div>
    </div>
    <div class="product">
        <img src="img4.jpg" alt="Product 3">
        <div class="product-title">Product 3</div>
        <div class="product-price">$29.99</div>
        <div class="product-description">Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</div>
    </div>
    <div class="clear"></div>
</div>
</body>
</html>
```

**Kode CSS:**
```css
<style>
    body {
        font-family: Arial, sans-serif;
        margin: 0;
        padding: 0;
    }
    .container {
        max-width: 1200px;
        margin: 0 auto;
        padding: 20px;
    }
    .product {
        float: left;
        width: 200px;
        margin-right: 20px;
        margin-bottom: 20px;
        background-color: #f9f9f9;
        border: 1px solid #ddd;
        padding: 10px;
    }
   .product img {
        max-width: 100%;
        height: auto;
    }
    .product-title {
        font-weight: bold;
        margin-top: 5px;
    }
    .product-price {
        color: green;
        margin-top: 5px;
    }
    .product-description {
        margin-top: 5px;
    }
    .clear {
        clear: both;
    }
</style>
```

**Hasilnya :**
![[Pasted image 20240502010000.png]]