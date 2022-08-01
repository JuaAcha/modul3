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
        return 'Mengakses Fungsi di Controller menggunakan route';
    }
    public function add()
    {
        return 'Mengakses halaman tambah data di setiap route Kategori controller';
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
