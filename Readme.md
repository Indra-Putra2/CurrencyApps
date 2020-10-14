# Currency App

aplikasi ini mencakup fungsi perhitungan tukar mata uang dari dollar 
ke rupiah, saru dollar dianggap senilai Rp.15000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info invalid jika yang di masukkan berupa text

## How Does it Works?

Diawali dari method `MainWindow` pada class MainWindow.xaml.cs

```c#
    public MainWindow()
    {
        InitializeComponent();
        currency = new CurrencyController();
    }
```

logika perhitungan terdapat pada class `CurrencyController.cs` 

```c#
public string usdToIdr(string nominal)
    {
        var nominalDouble = Convert.ToDouble(nominal);
        var result = nominalDouble * 15000;
        return Convert.ToString(result);
    }
```

### Latihan
1. Percobaan - percobaan
  - Pada **percobaan 1 nomor 4**, ketika dimasukkan sembarang angka 
    atau huruf lalu klik tombol Hitung, maka akan muncul sesuai 
    dengan input yang dimasukkan.
  - Pada **percobaan 2 nomor 2**, angka yang di masukkan akan
    dikalikan dengan 10000.
  - Pada **percobaan 2 nomor 3**, ketika dimasukkan sembarang huruf 
    akan terjadi error, karena string tidak bisa di convert ke double.
  - Pada **percobaan 3 nomor 2**, angka yang dinputkan akan 
    ditampilkan setelah dikalikan 4.
  - Pada **percobaan 3 nomor 3**, ketika dinputkan sembarang huruf, 
    maka hasil yang ditampilkan adalah **"invalid"**.

2. ``CurrencyController.cs`` digunakan untuk memisahkan antara 
    program utama dan logic agar mudah dibaca.

3. Kegunaan isAllowed method adalah untuk mengecek variabel 
   ``nominalInput`` yang dimasukkan oleh user berupa integer atau
   string.

4. Fungsi RegEx adalah untuk mengetahui pola 
   tertentu yang dihasilkan oleh input pengguna. Contoh, bila pengguna 
   menginputkan integer dan string secara bersamaan (Contoh: b450),maka 
   RegEx akan mengetahui bahwa input yang dimasukkan bukanlah angka 
   sehingga hasilnya akan mengeluarkan **"invalid"**.

5. Class Diagram

   ![Class Diagram](CurrencyApps/Class%20Diagram.jpg)
    
