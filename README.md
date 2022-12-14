# TUGAS WRITING-AND_PRESENTATION-WEEK3

__PANDJI SETIYA BUDHI ARTHA__ -- _Tugas writing minggu ketiga_

| __No__ | __Materi untuk minggu ketiga__ | 
|----|-----------------------------|
|  1 | JavaScript - Array  |
|  2 | JavaScript - Object        |
|  3 | JavaScript - Rekursif      |
|  4 | JavaScript - Regex & OOP   |

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
Jadi jika membutuhkan untuk update seluruh data object gunakan ???let??? pada saat deklarasi variabel. Jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru.

- __Delete Object Property__ <br>
Kita dapat menghapus properti dari object menggunakan delete operator, seperti contoh sebagai berikut : 
```
let address = {
    building-no: 3960,
    street: 'North 1st street',
    state: 'CA',
    country: 'USA'
};
delete address.state 

console.log(address)

//hasilnya 

building: 3960
country: "USA"
street: "North 1st street"
```
--------------------------------------------------------------------------------------------
## __3. JavaScript - Rekursif__ <br>
Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu. Ciri dari rekursif:

1. Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.

2. Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.

--------------------------------------------------------------------------------------------
## __4. JavaScript - Regex & OOP__ <br>
Regex adalah susunan karakter/deretan karakter spesial yang menggambarkan pattern/pola untuk pencarian text pada sebuah string atau document. Regex = Text matching. <br>
Contoh kasus Regex :
1. Validasi input dari sebuah FORM
2. Mencari keyword tertentu pada email atau halaman web
3. Mencari IP address dalam kisaran tertentu, dan masih banyak lagi

__A. Literals__
adalah konsep regex yang paling sederhana dimana kita membuat regex sesuai dengan text yang ingin kita cari/match atau mengandung text yang kita cari.

__B. test()__ yaitu mengembalikan nilai BOOLEAN (TRUE/FALSE) untuk kecocokan sebuat text yang dicari.
```
let regex = new RegExp('pandjiartha')
console.log(regex.test(pandjiartha'))
// maka akan muncul nilai "TRUE"

let regex2 = new RegExp('pandjiartha')
console.log(regex.test(pandji'))
// maka akan muncul nilai "FALSE"

//menggunakan karakter set
//Kita bisa menggunakan karakter set untuk mencari
//minimal 1 karakter yang sesuai.
//Karakter set menggunakan bracket square []

let regexExp = new RegExp('a-z')
console.log(regexExp.test('chi'))
//maka akan bernilai "TRUE"

let regexExp = new RegExp('1-5')
console.log(regexExp.test('243'))
//maka akan bernilai "TRUE"

let regexExp = new RegExp('a-c')
console.log(regexExp.test('abd'))
//maka akan bernilai "FALSE"
```
__B. match()__ match() sama seperti test() yaitu sebuah method bawaan dari javascript. Namun match() mengembalikan nilai array dari karakter yang match.


## __JavaScript - OOP__ <br>
Object Oriented Programming (OOP) adalah suatu paradigma dalam pemrograman. Ada 4 hal pilar dalam OOP:
1. Encapsulation -> adalah cara untuk membatasi akses langsung ke properti atau method dari sebuah objek.
2. Abstraction -> adalah sebuah teknik untuk menyembunyikan detail tertentu dari sebuah objek/method dan hanya menampilkan fungsionalitas atau fitur penting dari objek tersebut.
3. Inheritance -> adalah sebuah proses dimana sebuah class mewariskan property dan methodnya ke class lain atau childnya.
4. Polymorpishm -> berasal dari dua kata, yaitu poly yang berarti banyak dan morphism yang berarti bentuk. kemampuan dari suatu objek untuk memiliki banyak bentuk
-----------------------------------------------------
