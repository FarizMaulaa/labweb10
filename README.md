# PRAKTIKUM 10 | PHP OOP
## Apa itu OOP (Object Oriented Progamming)
### OOP adalah singkatan dari Object Oriented Programming, yaitu suatu metode pemrograman yang fokus atau berorientasi pada objek. Tujuan dari dirancangnya OOP adalah membantu para developer dalam mengembangkan model yang sudah ada di kehidupan sehari-hari

## Langkah - langkah praktikum

### 1. buatlah file baru dengan nama mobil.php
Lalu masukkan kode di bawah ini :
```
<?php
/**
* Program sederhana pendefinisian class dan pemanggilan class.
**/
class Mobil
{
    private $warna;
    private $merk;
    private $harga;

    public function __construct()
    {
        $this->warna = "Biru";
        $this->merk = "BMW";
        $this->harga = "10000000";
    }

    public function gantiWarna ($warnaBaru)
    {
        $this->warna = $warnaBaru;
    }

    public function tampilWarna ()
    {
        echo "Warna mobilnya : " . $this->warna;
    }
}

// membuat objek mobil
$a = new Mobil();
$b = new Mobil();

// memanggil objek
echo "<b>Mobil pertama</b><br>";
$a->tampilWarna();

echo "<br>Mobil pertama ganti warna<br>";
$a->gantiWarna("Merah");
$a->tampilWarna();

// memanggil objek
echo "<br><b>Mobil kedua</b><br>";
$b->gantiWarna("Hijau");
$b->tampilWarna();
?>
```
Output :
![Screenshot (126)](https://user-images.githubusercontent.com/98897250/206978987-5dd064c3-951c-428a-bfe8-884d5c1a6d65.png)

### 2. buatlah file baru dengan nama form.php
Lalu masukkan kode di bawah ini :
```
<?php
/**
* Program memanfaatkan Program 10.2 untuk membuat form inputan sederhana.
**/

include "form.php";

echo "<html><head><title>Mahasiswa</title></head><body>";
$form = new Form("","Input Form");
$form->addField("txtnim", "Nim");
$form->addField("txtnama", "Nama");
$form->addField("txtalamat", "Alamat");
echo "<h3>Silahkan isi form berikut ini :</h3>";
$form->displayForm();
echo "</body></html>";
?>
```
### 3. buatlah file baru dengan nama form_input.php
Lalu masukkan kode di bawah ini :
```
<?php
/**
* Program memanfaatkan Program 10.2 untuk membuat form inputan sederhana.
**/

include "form.php";

echo "<html><head><title>Mahasiswa</title></head><body>";
$form = new Form("","Input Form");
$form->addField("txtnim", "Nim");
$form->addField("txtnama", "Nama");
$form->addField("txtalamat", "Alamat");
echo "<h3>Silahkan isi form berikut ini :</h3>";
$form->displayForm();
echo "</body></html>";
?>
```
Outputnya :
![Screenshot (128)](https://user-images.githubusercontent.com/98897250/206980512-2a123632-8676-4cea-aa5c-a092a39afe76.png)
