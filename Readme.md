# Currency Apps
Aplikasi ini mencakup fungsi perhitungan nilai tukar mata uang dari dollar ke rupiah.
Satu dollar dianggap senialai Rp 15.000

## Scope & Functionalities
- User dapat memasukkan angka
- User dapat menyentuh tombol hitung
- User mendapat info "INVALID" jika yang dimasukkan berupa text

## How Does it works?

Diawali dari method `MainWindows` pada class MainWindow.xaml.cs, kita mendeklarasikan 

```csharp
public MainWindow()
        {
            InitializeComponent();
            currencyController = new CurrencyController();
        }
```

logika perhitungan terdapat pada class `CurrencyController.cs` sebagai berikut : 

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```

