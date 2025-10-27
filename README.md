# Lab6Web


**Tahap 1. Struktur Dasar HTML**

File: index.html

Kode :
```
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Layout Sederhana - Praktikum 6</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
```

**Tahap 2. Header & Navbar**

Tambahkan ke <body> setelah tag <body>

Kode :
```
<header>
  <h1>Layout Sederhana</h1>
</header>

<nav>
  <a href="#" class="active">Home</a>
  <a href="#">Artikel</a>
  <a href="#">About</a>
  <a href="#">Kontak</a>
</nav>
  
</body>
</html>
```

**Tambahkan ke style.css**

Kode :
```
header {
  background: #f3e9ff;
  border-bottom: 2px solid #d1c4e9;
  padding: 20px;
  text-align: left;
  color: #341f97;
  font-weight: bold;
}

nav {
  background: #6c5ce7;
}

nav a {
  color: white;
  text-decoration: none;
  display: inline-block;
  padding: 12px 18px;
}

nav a:hover,
nav a.active {
  background: #341f97;
}
```

Output :



<img width="1918" height="345" alt="Screenshot 2025-10-27 145511" src="https://github.com/user-attachments/assets/e60bea08-ebca-4658-ad21-ea3d19c50fd3" />




**Tahap 3. Hero Section (“Hello World!”)**

Tambahkan setelah </nav>

Kode :
```
<section id="hero">
  <h1>Hello World!</h1>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
  <a href="#" class="btn">Learn more &raquo;</a>
</section>

</body>
</html>
```

**Tambahkan ke style.css**

Kode :
```
#hero {
  background: #eceaff;
  text-align: center;
  padding: 50px 20px;
}

#hero h1 {
  color: #2d3436;
}

#hero p {
  max-width: 700px;
  margin: 15px auto;
  color: #333;
  line-height: 1.6;
}

.btn {
  display: inline-block;
  padding: 10px 20px;
  background: #00cec9;
  color: white;
  text-decoration: none;
  border-radius: 5px;
  font-weight: bold;
}

.btn:hover {
  background: #009b95;
}
```

Output :



<img width="1919" height="580" alt="Screenshot 2025-10-27 145614" src="https://github.com/user-attachments/assets/91d68c2d-c068-4c2f-b16c-2cf13f4d3e3b" />




**Tahap 4. Wrapper (Main Content + Sidebar)**

Tambahkan setelah Hero Section

Kode :
```
<section id="wrapper">
  <section id="main">
    <!-- Isi konten utama akan ditaruh di sini -->
  </section>

  <aside id="sidebar">
    <!-- Sidebar akan diisi nanti -->
  </aside>
</section>
```

**Tambahkan ke style.css**

Kode :
```
#wrapper {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  gap: 20px;
}

#main {
  width: 70%;
}

#sidebar {
  width: 28%;
}
```

Output :



<img width="1919" height="583" alt="Screenshot 2025-10-27 150037" src="https://github.com/user-attachments/assets/3b0dbe52-0024-49e1-b782-2dcda55764c7" />




**Tahap 5. Tiga Box Lingkaran (Row)**

Tambahkan ke dalam <section id="main">

Kode :
```
<div class="row">
  <div class="box">
    <img src="https://dummyimage.com/120/ff7675/fff.png" class="image-circle" alt="">
    <h3>Heading</h3>
    <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
    <a href="#" class="btn small">View detail</a>
  </div>

  <div class="box">
    <img src="https://dummyimage.com/120/74b9ff/fff.png" class="image-circle" alt="">
    <h3>Heading</h3>
    <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
    <a href="#" class="btn small">View detail</a>
  </div>

  <div class="box">
    <img src="https://dummyimage.com/120/55efc4/fff.png" class="image-circle" alt="">
    <h3>Heading</h3>
    <p>Donec sed odio dui. Etiam porta sem malesuada magna mollis euismod.</p>
    <a href="#" class="btn small">View detail</a>
  </div>
</div>
```

**Tambahkan ke style.css**

Kode :
```
.row {
  display: flex;
  justify-content: space-between;
  text-align: center;
  gap: 10px;
}

.box {
  width: 32%;
  background: #fff;
  padding: 20px;
  border: 1px solid #ddd;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}

.image-circle {
  border-radius: 50%;
  margin-bottom: 10px;
}
```

Output :



<img width="1919" height="762" alt="Screenshot 2025-10-27 150152" src="https://github.com/user-attachments/assets/be5bb199-d1c8-41fa-af76-5ac09ba76725" />




**Tahap 6. Sidebar (Widget Header & Text)**

Tambahkan ke dalam <aside id="sidebar">Kode 

Kode :
```
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
  <p>Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu. Proin in leo fringilla, vestibulum mi porta, faucibus felis. Integer pharetra est nunc, nec pretium nunc pretium ac.</p>
</div>
```

**Tambahkan ke style.css**

kode :
```
/* ===== SIDEBAR ===== */
.widget-box {
  background: #fff;
  border: 1px solid #ccc;
  margin-bottom: 20px;
  padding: 10px;
  border-radius: 6px;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.widget-box .title {
  background: #6c5ce7;
  color: white;
  padding: 10px;
  margin: -10px -10px 10px -10px;
  border-radius: 6px 6px 0 0;
}
```

Output :



<img width="1919" height="1079" alt="Screenshot 2025-10-27 150250" src="https://github.com/user-attachments/assets/3634b800-841e-434f-b309-e89415e1fe35" />




**Tahap 7. Featurette Articles**

Tambahkan setelah </div> (tiga box) di #main

Kode :
```
<hr class="divider">

<article class="entry">
  <h2>First featurette heading.</h2>
  <img src="https://dummyimage.com/150/dfe6e9/2d3436.png" alt="">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
</article>

<hr class="divider">

<article class="entry">
  <h2>Second featurette heading.</h2>
  <img src="https://dummyimage.com/150/dfe6e9/2d3436.png" class="right-img" alt="">
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum lorem elit, iaculis in nisl volutpat, malesuada tincidunt arcu.</p>
</article>
```

**Tambahkan ke style.css**

kode :
```
.entry {
  background: #fff;
  border: 1px solid #ddd;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.08);
}

.entry img {
  float: left;
  margin-right: 15px;
  border-radius: 4px;
}

.right-img {
  float: right;
  margin-left: 15px;
}

.divider {
  border: 0;
  border-top: 1px dashed #ccc;
  margin: 25px 0;
  clear: both;
}
```

Output :



<img width="1919" height="1000" alt="Screenshot 2025-10-27 150403" src="https://github.com/user-attachments/assets/86f78182-0ad7-42fb-824f-ccdb2dcc57b0" />




**Tahap 8. Footer**

Tambahkan di paling bawah body

Kode :
```
<footer>
  <p>&copy; 2025 - Universitas Pelita Bangsa</p>
</footer>

```

**Tambahkan ke style.css**

Kode :
```
footer {
  background: #2d3436;
  color: white;
  text-align: center;
  padding: 15px 0;
  font-size: 14px;
  margin-top: 30px;
}

```

Output :



<img width="1916" height="997" alt="Screenshot 2025-10-27 150511" src="https://github.com/user-attachments/assets/6086fc8b-7432-43e0-85c8-414a4f0fbff2" />




**Tahap 9. Responsif (biar rapi di HP)**

Tambahkan di akhir style.css

Kode :
```
@media (max-width: 800px) {
  #wrapper {
    flex-direction: column;
  }

  .row {
    flex-direction: column;
  }

  #main, #sidebar {
    width: 100%;
  }

  .entry img, .right-img {
    float: none;
    display: block;
    margin: 10px auto;
  }
}
```

Output :


<img width="1919" height="980" alt="Screenshot 2025-10-27 150544" src="https://github.com/user-attachments/assets/49c3f8fa-fee1-4570-a3da-15e92f6550b5" />





**Tahap 10 — Validasi HTML (di akhir**)

Buka situs https://validator.w3.org

→ Pilih File Upload → pilih index.html → klik Check

```

