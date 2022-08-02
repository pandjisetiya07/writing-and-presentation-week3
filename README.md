# TUGAS WRITING-AND_PRESENTATION-WEEK3

__PANDJI SETIYA BUDHI ARTHA__ -- _Tugas writing minggu ketiga_

| __No__ | __Materi untuk minggu ketiga__ | 
|----|-----------------------------|
|  1 | JavaScript - Array & Multidimensional Array |
|  2 | JavaScript - Object        |
|  3 | JavaScript - Rekursif      |
|  4 | JavaScript - Modules       |
|  5 | JavaScript - Regex & OOP   |
|  6 | JavaScript - Asynchronous, API and HTTP  |

--------------------------------------------------------------------------------------------

## 1. JavaScript - Array & Multidimensional Array <br>

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