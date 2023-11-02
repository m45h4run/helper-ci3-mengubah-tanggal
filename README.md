# helper-ci3-mengubah-tanggal
Berikut adalah langkah-langkah untuk membuat helper CodeIgniter yang dapat membantu Anda mengubah tanggal ke dalam bahasa Indonesia:

1. Buat file baru dengan nama `tanggal_helper.php` di direktori `application/helpers`.
2. Salin kode berikut ke dalam file tersebut:

```php
<?php
defined('BASEPATH') OR exit('No direct script access allowed');

if (!function_exists('tanggal_indonesia'))
{
    function tanggal_indonesia($tanggal)
    {
        $bulan = array (
            1 =>   'Januari',
            'Februari',
            'Maret',
            'April',
            'Mei',
            'Juni',
            'Juli',
            'Agustus',
            'September',
            'Oktober',
            'November',
            'Desember'
        );
        $split = explode('-', $tanggal);
        return $split[2] . ' ' . $bulan[(int)$split[1]] . ' ' . $split[0];
    }
}
```

3. Simpan file tersebut.
4. Sekarang, Anda dapat memanggil fungsi `tanggal_indonesia()` di mana saja dalam aplikasi Anda untuk mengubah tanggal ke dalam format bahasa Indonesia.

Semoga membantu! 😊
