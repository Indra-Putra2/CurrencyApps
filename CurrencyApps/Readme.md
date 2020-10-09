# Currency App

aplikasi ini mencakup fungsi perhitungan tukar mata uang dari dollar 
ke rupiah, saru dollar dianggap senilai Rp.15000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info invalid jika yang di masukkan berupa text

## How Does it Works?

Diawali dari method `MainWindow` pada class MainWindow.xaml.cs kita
mendeklarasikan ....

```c#
    public MainWindow()
    {
        InitializeComponent();
        currency = new CurrencyController();
    }
```

logika perhitungan terdapat pada class `CurrencyController.cs` 
sebagai berikut

cara kerjanya ....
```c#
public string usdToIdr(string nominal)
    {
        var nominalDouble = Convert.ToDouble(nominal);
        var result = nominalDouble * 15000;
        return Convert.ToString(result);
    }
```