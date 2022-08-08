###### Nama : Abdi Bakar Djallu
###### Absen : 01
###### Kelas : XII RPL 1

# Modul 4

### View Blade Template
1. Membuat folder dan file yang akan di isi
Lalu buat folder :

- Barang

- Kategori

- Layout

Folder diatas dibuat didalam folder view

Lalu didalam folder diatas terdapat sebuah file yang terdiri dari :

- home.blade.php

- index.blade.php

- app.blade.php

File dan folder diatas akan terlihat seperti berikut :

![image](https://user-images.githubusercontent.com/109929708/183359903-f50ae242-db83-475a-bae7-8d763485a5db.png)

Tugas 2 mengisi file app.blade.php didalam folder layout

Pada Folder layout file app.blade.php kita akan mengambil css dan js dari bootstrap
![image](https://user-images.githubusercontent.com/109929708/183361282-9482591f-23ba-4c8d-9c42-4d8b6a80f484.png)

Gambar diatas adalah bagian bootstrap yang akan kita pakai sebagai css dengan menambahkan syntax seperti berikut :

```
<link rel="stylesheet"href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
```

Selanjutnya bagian JS menambahkan syntax seperti berikut :

```
<script> src = "https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"</script>
```

Selanjutnya isi file app.blade.php dengan all codenya seperti berikut 

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet"href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/css/bootstrap.min.css">
    <title>
        @yield('title')
    </title>
</head>
<body>

    <!-- UNTUK NAVBAR -->
    <div class="container">
    <nav class="navbar navbar-expand-lg bg-dark">
  <div class="container-fluid">
    <a class="navbar-brand text-white" href="#">PENJUALAN</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active text-white" aria-current="page" href="/home">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/barang">Barang</a>
        </li>
        <li class="nav-item">
          <a class="nav-link text-white" href="/kategori">Kategori</a>
        </li>
    </div>
  </div>
</nav>
    </div>
    

    <!-- CONTENT -->

    <div class="container">
        @yield('content')
    </div>

<script> src = "https://cdn.jsdelivr.net/npm/bootstrap@5.2.0/dist/js/bootstrap.bundle.min.js"</script>
</body>
</html>
```

Selanjutnya folder barang yang berisi file home.blade.php akan seperti berikut :

```
@extends('layout.app')

@section('title')
    Barang
@endsection

@section('content')
    <div class="mt-3">
        <table class="table table-striped> class=">
            <thead>
                <tr>
                    <th width="5%">NO.</th>
                    <th>Nama</th>
                    <th>Kategori</th>
                    <th>qty</th>
                    <th>Harga Beli</th>
                    <th>Harga Jual</th>
                    <th width="15%">Aksi</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>Topi</td>
                    <td>Accessories</td>
                    <td>30</td>
                    <td>5000</td>
                    <td>10000</td>
                    <td>Hapus | Edit</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>Dasi</td>
                    <td>Accessories</td>
                    <td>35</td>
                    <td>10000</td>
                    <td>20000</td>
                    <td>Hapus | Edit</td>
                </tr>
            </tbody>
        </table>
    </div>
@endsection
```

Selanjutnya pada folder barang file index.blade.php all codenya akan terlihat seperti berikut :

```
@extends('layout.app')

@section('title')
    Barang
@endsection

@section('content')
    <div class="mt-3">
        <table class="table table-striped> class=">
            <thead>
                <tr>
                    <th width="5%">NO.</th>
                    <th>Nama</th>
                    <th>Kategori</th>
                    <th>qty</th>
                    <th>Harga Beli</th>
                    <th>Harga Jual</th>
                    <th width="15%">Aksi</th>
                </tr>
            </thead>
            <tbody>
                <tr>
                    <td>1</td>
                    <td>Meja</td>
                    <td>Barang</td>
                    <td>12</td>
                    <td>50000</td>
                    <td>55000</td>
                    <td>Hapus | Edit</td>
                </tr>
                <tr>
                    <td>2</td>
                    <td>Kursi</td>
                    <td>Barang</td>
                    <td>11</td>
                    <td>45000</td>
                    <td>50000</td>
                    <td>Hapus | Edit</td>
                </tr>
            </tbody>
        </table>
    </div>
@endsection
```

hasil dari code yang kita kerjakan akan terlihat seperti berikut :

code yang ditampilkan ini dari folder barang file home.blade.php
![image](https://user-images.githubusercontent.com/109929708/183363067-1881d8c5-5e0d-4abe-8a87-ca0b42055013.png)


lalu hasil folder kategori file index.blade.php akan terlihat seperti berikut :

![image](https://user-images.githubusercontent.com/109929708/183363266-3eb8462c-7a1a-4e1e-803d-26328c3d18d1.png)
