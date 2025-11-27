# muhammadihsansinaga-103112430219-MODUL1
# <h1 align="center">Laporan Praktikum Modul 1 <br> PENGENALAN C++ </h1>
<p align="center">MUHAMMAD IHSAN SINAGA - 103112430219</p>

## Dasar Teori

C++ dikembangkan oleh Bjarne Stroustrup di Bell Laboratories pada awal 1980-an sebagai perluasan dari bahasa C. Dengan menambahkan fitur pemrograman berorientasi objek, C++ mendukung konsep seperti enkapsulasi, pewarisan, dan polimorfisme. Kombinasi efisiensi C dan fleksibilitas OOP menjadikan C++ populer untuk pengembangan sistem, game, dan aplikasi besar.

## guided

### aritmatika
```c++
#include <iostream>
using namespace std;
int main()
{
    int W, X, Y;
    float Z;
    X = 7;
    Y = 3;
    W = 1;
    Z = (X + Y) / (Y + W);
    cout << "Nilai z = " << Z << endl;
    return 0;
}

```
> Output

Program ini menghitung nilai Z dengan rumus (X + Y) / (Y + W). Karena kedua operannya bertipe int, pembagian dilakukan secara integer division, sehingga hasil desimal dibulatkan ke bawah. Misalnya 10 / 4 menghasilkan 2, bukan 2.5. Nilai 2 tersebut kemudian disimpan ke variabel Z bertipe float, sehingga nilai akhirnya adalah 2.0.
### fungsi
```c++
#include <iostream>
using namespace std;

// Prosedur: hanya menampilkan hasil, tidak mengembalikan nilai
void tampilkanHasil(double p, double l)
{
    cout << "\n=== Hasil Perhitungan ===" << endl;
    cout << "Panjang : " << p << endl;
    cout << "Lebar   : " << l << endl;
    cout << "Luas    : " << p * l << endl;
    cout << "Keliling: " << 2 * (p + l) << endl;
}

// Fungsi: mengembalikan nilai luas
double hitungLuas(double p, double l)
{
    return p * l;
}

// Fungsi: mengembalikan nilai keliling
double hitungKeliling(double p, double l)
{
    return 2 * (p + l);
}

int main()
{
    double panjang, lebar;

    cout << "Masukkan panjang: ";
    cin >> panjang;
    cout << "Masukkan lebar  : ";
    cin >> lebar;

    // Panggil fungsi
    double luas = hitungLuas(panjang, lebar);
    double keliling = hitungKeliling(panjang, lebar);

    cout << "\nDihitung dengan fungsi:" << endl;
    cout << "Luas      = " << luas << endl;
    cout << "Keliling  = " << keliling << endl;

    // Panggil prosedur
    tampilkanHasil(panjang, lebar);

    return 0;
}
```
> Output

Program C++ ini digunakan untuk menghitung luas dan keliling persegi panjang dengan memanfaatkan fungsi dan prosedur. Pengguna terlebih dahulu memasukkan nilai panjang dan lebar sebagai input. Fungsi hitungLuas menghitung hasil dari panjang dikalikan lebar, sedangkan fungsi hitungKeliling menghitung nilai 2 × (panjang + lebar). Kedua hasil tersebut ditampilkan ke layar setelah perhitungan selesai. Selain itu, prosedur tampilkanHasil digunakan untuk menampilkan seluruh data, termasuk panjang, lebar, luas, dan keliling, tanpa mengembalikan nilai apa pun. Program ini menggambarkan perbedaan antara fungsi yang menghasilkan nilai dan prosedur yang hanya menampilkan output.
### kondisi
```c++
#include <iostream>
using namespace std;
// int main()
// {
//     double tot_pembelian, diskon;
//     cout << "total pembelian: Rp";
//     cin >> tot_pembelian;
//     diskon = 0;
//     if (tot_pembelian >= 100000)
//         diskon = 0.05 * tot_pembelian;
//     cout << "besar diskon = Rp" << diskon;
// }



// int main()
// {
//     double tot_pembelian, diskon;
//     cout << "total pembelian: Rp";
//     cin >> tot_pembelian;
//     diskon = 0;
//     if (tot_pembelian >= 100000)
//         diskon = 0.05 * tot_pembelian;
//     else
//         diskon = 0;
//     cout << "besar diskon = Rp" << diskon;
// }



int main()
{
    int kode_hari;
    cout << "Menentukan hari kerja/libur\n"<<endl;
    cout << "1=Senin 3=Rabu 5=Jumat 7=Minggu "<<endl;
    cout << "2=Selasa 4=Kamis 6=Sabtu "<<endl;
    cin >> kode_hari;
    switch (kode_hari)
    {
    case 1:
    case 2:
    case 3:
    case 4:
    case 5:
        cout<<"Hari Kerja";
        break;
    case 6:
    case 7:
        cout<<"Hari Libur";
        break;
    default:
        cout<<"Kode masukan salah!!!";
    }
    return 0;
}
```
> Output

Program C++ di atas terdiri dari beberapa bagian contoh kode, tetapi hanya bagian terakhir yang aktif dijalankan. Pada bagian aktif, program digunakan untuk menentukan apakah suatu hari termasuk hari kerja atau hari libur berdasarkan kode angka yang dimasukkan pengguna.
### perulangan
```c++
#include <iostream>
using namespace std;
// int main()
// {
//     int jum;
//     cout << "jumlah perulangan: ";
//     cin >> jum;
//     for (int i = 0; i < jum; i++)
//     {
//         cout << "saya sahroni\n";
//     }
//     return 1;
// }


// while
int main()
{
    int i = 1;
    int jum;
    cin >> jum;
    do
    {
        cout << "bahlil ke-" << (i + 1) << endl;
        i++;
    } while (i < jum);
    return 0;
}
```
> Output

Program C++ ini digunakan untuk menampilkan teks berulang menggunakan perulangan do...while. Variabel i diberi nilai awal 1, kemudian pengguna diminta memasukkan jumlah pengulangan melalui variabel jum. Di dalam blok do, program menampilkan tulisan "bahlil ke-" disertai angka urutan (i + 1), lalu menaikkan nilai i dengan i++. Perulangan akan terus berjalan selama syarat i < jum terpenuhi. Jika kondisi tidak lagi benar, proses berhenti dan program berakhir dengan return 0;. Dengan demikian, program akan menampilkan kalimat “bahlil ke-” sebanyak jumlah yang dimasukkan pengguna, minimal satu kali karena sifat dasar perulangan do...while.
### Struct   
```c++
#include <iostream>
#include <string>
using namespace std;

// Definisi struct
struct Mahasiswa {
    string nama;
    string nim;
    float ipk;
};

int main() {

    Mahasiswa mhs1;

    cout << "Masukkan Nama Mahasiswa: ";
    getline(cin, mhs1.nama);
    // cin >> mhs1.nama;
    cout << "Masukkan NIM Mahasiswa : ";
    cin >> mhs1.nim;
    cout << "Masukkan IPK Mahasiswa : ";
    cin >> mhs1.ipk;

    cout << "\n=== Data Mahasiswa ===" << endl;
    cout << "Nama : " << mhs1.nama << endl;
    cout << "NIM  : " << mhs1.nim << endl;
    cout << "IPK  : " << mhs1.ipk << endl;

    return 0;
}
```
> Output

Program C++ ini berfungsi untuk menginput dan menampilkan data seorang mahasiswa menggunakan struktur (struct). Di awal, dideklarasikan sebuah struct bernama Mahasiswa yang terdiri dari tiga atribut: nama dan nim bertipe string, serta ipk bertipe float. Struktur ini digunakan untuk menyimpan beberapa data mahasiswa dalam satu kesatuan variabel.
### Test
```c++
#include <iostream>
using namespace std;
int main()
{
    string ch;
    cout << "Masukkan sebuah karakter: ";
    // cin >> ch;
    ch = getchar();  //Menggunakan getchar() untuk membaca satu karakter
    cout << "Karakter yang Anda masukkan adalah: " << ch << endl;
    return 0;
}
```
> Output

Program C++ ini digunakan untuk membaca satu karakter dari input pengguna dan menampilkannya kembali ke layar. Pada awalnya, variabel ch bertipe string dideklarasikan untuk menampung karakter yang dimasukkan. Program kemudian menampilkan pesan "Masukkan sebuah karakter: " agar pengguna memberikan input. Fungsi getchar() digunakan untuk mengambil satu karakter dari keyboard dan menyimpannya ke dalam variabel ch. Setelah itu, karakter yang dimasukkan ditampilkan menggunakan cout. Program ditutup dengan return 0; sebagai tanda bahwa eksekusi telah selesai dengan normal. Perlu dicatat, tipe data yang lebih sesuai untuk getchar() sebenarnya adalah char, karena fungsi ini hanya membaca satu karakter saja.
## Unguided

### soal 1
```go
#include <iostream>
#include <iomanip>
using namespace std;

int main() {
    double a, b;

    cout << "Masukkan angka pertama: ";
    cin >> a;
    cout << "Masukkan angka kedua  : ";
    cin >> b;

    cout << "\n=== Hasil Operasi Aritmetika ===" << endl;

    cout << fixed << setprecision(2);

    double hasilTambah = a + b;
    double hasilKurang = a - b;
    double hasilKali   = a * b;

    cout << "Penjumlahan : " << hasilTambah << endl;
    cout << "Pengurangan : " << hasilKurang << endl;
    cout << "Perkalian   : " << hasilKali << endl;

    if (b == 0)
        cout << "Pembagian   : Error (tidak bisa dibagi nol)" << endl;
    else
        cout << "Pembagian   : " << a / b << endl;

    return 0;
}

```
> Output
> ![Screenshot bagian x](ssunguided1modul1.png)
Program C++ ini berfungsi untuk menghitung hasil penjumlahan, pengurangan, perkalian, dan pembagian dari dua angka yang dimasukkan pengguna. Variabel a dan b menyimpan input angka, lalu hasil operasi ditampilkan dengan dua angka di belakang koma menggunakan setprecision(2). Sebelum melakukan pembagian, program memeriksa apakah nilai b bernilai nol untuk menghindari kesalahan. Jika nol, akan muncul pesan error; jika tidak, hasil pembagian ditampilkan. Program diakhiri dengan return 0; sebagai tanda eksekusi berhasil.


### Soal 2

```go
#include <iostream>
#include <string>
#include <vector>

using namespace std;

const vector<string> kata_belasan = {
    "nol", "satu", "dua", "tiga", "empat", "lima", "enam", "tujuh", "delapan", "sembilan",
    "sepuluh", "sebelas", "dua belas", "tiga belas", "empat belas", "lima belas",
    "enam belas", "tujuh belas", "delapan belas", "sembilan belas"
};

const vector<string> kata_puluhan = {
    "", "", "dua puluh", "tiga puluh", "empat puluh", "lima puluh",
    "enam puluh", "tujuh puluh", "delapan puluh", "sembilan puluh"
};

string ubahAngkaKeKalimat(int angka) {
    if (angka < 0 || angka > 100) {
        return "Angka tidak tersedia (rentang 0-100).";
    }

    if (angka < 20) {
        return kata_belasan[angka];
    } 
    else if (angka < 100) {
        int puluhan = angka / 10;
        int satuan = angka % 10;

        string kalimat = kata_puluhan[puluhan];
        if (satuan != 0) {
            kalimat += " " + kata_belasan[satuan];
        }

        return kalimat;
    } 
    else {
        return "seratus";
    }
}

int main() {
    int nilai;

    cout << "Masukkan angka (0-100): ";
    if (!(cin >> nilai)) {
        cerr << "Input yang diberikan bukan angka valid." << endl;
        return 1;
    }

    string hasil = ubahAngkaKeKalimat(nilai);

    cout << "\nHasil konversi: " << nilai << " = " << hasil << endl;

    return 0;
}

```
> Output
> ![Screenshot bagian x](ssunguided2modul1.png)
Program ini mengubah angka dari 0 hingga 100 menjadi bentuk tulisan dalam bahasa Indonesia. Data kata-kata disimpan dalam dua vektor: satu untuk angka belasan (kata_belasan) dan satu untuk puluhan (kata_puluhan). Fungsi ubahAngkaKeKalimat() menentukan apakah angka termasuk belasan, puluhan, atau seratus, lalu menghasilkan teks yang sesuai. Di main(), program meminta input angka dari pengguna, memvalidasinya, lalu menampilkan hasil konversinya di layar.
### Soal 3
```go
#include <iostream>
using namespace std;

void polaCermin(int n) {
    if (n <= 0) {
        cout << "Masukkan angka positif!" << endl;
        return;
    }

    // Bagian pola angka
    for (int baris = n; baris >= 1; baris--) {

        // Spasi kiri
        for (int s = 1; s <= n - baris; s++) {
            cout << " ";
        }

        // Angka menurun di kiri
        for (int kiri = baris; kiri >= 1; kiri--) {
            cout << kiri;
            if (kiri != 1) cout << " ";
        }

        cout << " * ";

        // Angka menaik di kanan
        for (int kanan = 1; kanan <= baris; kanan++) {
            cout << kanan;
            if (kanan != baris) cout << " ";
        }

        cout << endl;
    }

    // Tanda bintang di bawah
    for (int s = 1; s <= n; s++) cout << " ";
    cout << "*" << endl;
}

int main() {
    int n;
    cout << "Masukkan bilangan bulat positif: ";
    cin >> n;

    cout << "\nHasil Pola Cermin:\n";
    polaCermin(n);

    return 0;
}

```
> Output
> ![Screenshot bagian x](ssunguided3modul1.png)
Program ini menampilkan pola cermin angka dengan simbol * di tengah berdasarkan input angka dari pengguna. Fungsi polaCermin() mencetak angka menurun di sisi kiri dan angka menaik di sisi kanan dengan spasi di antaranya, membentuk pola simetris seperti cermin. Setelah semua baris selesai, program menampilkan satu bintang di bagian bawah tengah sebagai penutup pola.

## Referensi

1. https://en.wikipedia.org/wiki/Data_structure
