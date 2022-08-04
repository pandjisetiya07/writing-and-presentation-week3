# TUGAS WRITING-AND_PRESENTATION-WEEK3

__PANDJI SETIYA BUDHI ARTHA__ -- _Tugas writing minggu ketiga_

| __No__ | __Materi untuk minggu ketiga__ | 
|----|-----------------------------|
|  1 | JavaScript - Array  |
|  2 | JavaScript - Object        |
|  3 | JavaScript - Rekursif      |
|  4 | JavaScript - Modules       |
|  5 | JavaScript - Regex & OOP   |
|  6 | JavaScript - Asynchronous, API and HTTP  |

--------------------------------------------------------------------------------------------

## 1. JavaScript - Array <br>

### __A. JavaScript - Array__ <br>
List order yang dapat menyimpan __tipe data apapun__ di dalamnya, seperti __String, Number, Boolean, dan lainnya.__ Contoh penulisan array :
```
//contoh penulisan array pertama
let products = ["Flashdisk", "SDD", "Monitor"];
console.log(products);

//contoh penulisan array kedua
let arrayList = [
    'array list pertama',
    'ini contoh penulisan array',
    'dapat menyimpan banyak tipe data'
    ];
console.log(arrayList);

//contoh array menyimpan banyak tipe data
// string, number, boolean
let dataRandom = ['ini string', 07, true];
console.log(dataRandom);
```
Penghitungan array di mulai dari __index ke-0__. Data pertama yang ada pada array adalah __index ke-0__ 

### __B. Update Array__ <br>
Untuk tipe data array juga dapat diupdate sama seperti jenis tipe data dan variabel lainnya.
contoh penulisan code untuk update array 
```
let updateArray = ['materi update pertama', 'writing week 2'];

updateArray[1] = 'writing week 3';
console.log(updateArray)
//hasilnya ['materi update pertama', 'writing week 3'];
```

### __C. Const in array__ <br>
Jika array menggunakan _let_ kita dapat merubah array dengan nilai array baru. pada _CONST_ kita tidak bisa melakukan update data, namun dapat mengupdate konten nilai didalam array. __Yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const__
```
let cars3 = ['tesla','honda','yamaha']
cars3[2] = ['nissan']
console.log(cars3)

// hasilnya
// ["tesla", "honda", Array(1)]
// 0: "tesla"
// 1: "honda"
// 2: Array(1) --> hasil conts array
// 0: "nissan" --> hasil conts array

// ['tesla','honda','nissan']
```
### __D. Array Properties__ <br>
Properties adalah fitur yang sudah disediakan oleh Javascript untuk memudahkan developer.Arrray memiliki 5 Properties yang sering digunakan yaitu : 
1. Constructor
2. Length
3. Index
4. Input
5. prototype. 

### __E. Array Method__ <br>
Array memiliki __built-in methods__ tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia. Contoh Array Built-in Methods
1. __push()__ -> menambahkan item array baru pada urutan yang __paling akhir__.
2. __pop()__  -> menghapus array pada index __terakhir / paling bawah__.
3. __shift()__ ->menghapus array pada index __pertama / paling atas__.
4. __unshift()__ -> menambahkan array pada index __petama / paling atas__.
5. __sort()__ -> mengurutkan array secara __Ascending atau Descending Alphanumeric__.

### __F. Looping Array__ <br>
Array memiliki __built-in methods__ untuk melakukan looping yaitu __.map() dan .forEach()__ untuk mengetahui kapan menggunakan looping kedua methods ini ? 
1. __forEach()__ -> melakukan perulangan pada setiap element array yang sudah di sediakan
```
const cars = ['tesla','honda','yamaha']
cars.forEach(element => {
    console.log(element);
});
```
2. __map()__ -> melakukan perulangan dengan membuat array baru
```
let nomor = [2,4,6,8,10]
let doubel = nomor.map(num => {
    return num + 2
})
console.log(doubel)

//hasil [4, 6, 8, 10, 12]
```
Perbedaannya adalah <br>
- .forEach tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping Jadi, gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database. <br>
- .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

------------------------------------------------------------------------------------------
## 2. JavaScript - Object <br>
sebuah kumpulan nilai yang disebut properti dapat berupa string. Dan nilai properti dapat berupa nilai apa pun, misalnya string, angka, array, dan bahkan fungsi.
```
let address = {
    'building no': 3960,
    street: 'North 1st street',
    state: 'CA',
    country: 'USA'
};
```
object kita dapat menyimpan properti dengan tipe data apapun. kita juga dapat menggunakan __Bracket Natation__ bisa digunakan untuk memanggil properti dari sebuah object seperti
```
let address = {
    'building no': 3960,
    street: 'North 1st street',
    state: 'CA',
    country: 'USA'
};
console.log(address['state'])//maka akan muncul "CA"
```

- __Update Object__ <br>
Kita juga dapat melakukan __update object__ pada variabel dengan tipe data object. <br> Object dapat mengupdate value dari key yang sudah tersedia, Object dapat menambahkan key dan value baru 
```
let address = {
    building-no: 3960,
    street: 'North 1st street',
    state: 'CA',
    country: 'USA'
};
//update value yang sudah ada di object
address.building-no = 30

//update new key and value
address.name = 'Pandji, KSB'

console.log(address); 

//maka hasilnya akan muncul

building: 30
country: "USA"
name: "Pandji, KSB"
state: "CA"
street: "North 1st street"

```
Jadi jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel. Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru.

