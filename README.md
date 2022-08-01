### Nama : Ach Ilham M.A
### Kelas : XII RPL 1
### Absen : 03



>1. Buatlah Route yang menuju kehalaman Kategori
>2. Buatlah halaman tambah data di setiap route

# Jawaban NO.1

# 1.1
buatlah satu controller dengan menggunakan perintah artisan sebagai 
berikut:
```
php artisan make:controller KategoriController
```

# 1.2
Perintah artisan diatas akan menghasilkan satu file baru bernama KategoriController.php yang terletak di folder 
app\Http\Controller. Bukalah file controller tersebut dan tambahkan fungsi bernama 
index dan add seperti pada controh skrip dibawah:
```
<?php

namespace App\Http\Controllers;

use Illuminate\Http\Request;

class KategoriController extends Controller
{
    public function index()
    {
        return '<a href="/kategori/add">Menuju kategori add</a>';
    }
    public function add()
    {
        return 'Membuat halaman tambah data di setiap route kategori<p>
        <a href="/kategori">menuju halaman kategori</a></p>';
    }
}
```

# 1.3
Kemudian pada web.php yang ada pada folder routes/web.php tambahkan route baru 
dengen bentuk seperti berikut:
```
Route::get('/kategori', [KategoriController::class, 'index']);
Route::get('/kategori/add', [KategoriController::class, 'add']);
```
# 1.4
Untuk hasilnya seperti ini

![image](https://user-images.githubusercontent.com/109930502/182103803-2c5968b8-5e82-44ce-a78d-42ce6fb17744.png)
