# JavaScript 101 - Fundamental

## Brief History

JavaScript adalah bahasa pemrograman yang dibuat untuk Web. HTML, CSS dan JavaScript adalah tiga inti utama dalam World Wide Web.

Di tahun 1995, Brendan Eich yang bekerja di Netscape Communication Corporations mendapat project untuk menambah Scheme pada Netscape Navigator untuk membuat Web lebih dinamis. FYI, Netscape Navigator adalah salah satu dari web browser internet. Brendan Eich menyelesaikannya dalam 10 hari. Nama awal yang digunakan adalah LiveScript, yang kemudian diubah menjadi JavaScript, dengan tujuan untuk menunggangi ketenaran bahasa pemrograman Java pada saat itu. Ingat, **JavaScript dan Java adalah dua bahasa pemrograman yang berbeda.**

**JavaScript Engine pada browser:**

* Chrome: V-8 Engine
* Edge: Chakra
* Safari: Nitro Engine
* Firefox: SpiderMonkey


## Variable Declaration

Variable declaration adalah cara untuk membuat "kotak" atau *container* dalam komputer yang nantinya dapat digunakan untuk menampung data. 

**_Static typing/type enforcement_**: Kita harus mendeklarasikan variable beserta tipe data variablenya. Contoh: C, C++, Java
**_Weak typing/dynamic typing_**: Memungkinkan kita mendeklarasikan variable dengan tipe apapun. Contoh: JavaScript

Ada 3 cara untuk mendeklarasikan variable, yaitu dengan **_var, let (ES6) dan const (ES6)._**

### Var
Var adalah cara deklarasi variable dengan **function scope**. Yang dimaksud dengan **scope** adalah area dimana variable itu hidup/dapat diakses. Function scope artinya **variable tersebut hanya dapat diakses nilainya di dalam fungsi itu saja**.

Jika deklarasi variable dengan var tidak berada di dalam function, variable itu hidup di dalam **global scope**/dapat diakses dimana saja di dalam program.

Syntax deklarasi variable:
```JavaScript
var a; // return undefined
var b = 0; // inisialisasi nilai variable
var c = 1, d = 2; // deklarasi beberapa variable
```

### Let
Let adalah cara deklarasi variable dengan **block scope**. Block scope adalah **semua yang berada di dalam {} (kurung kurawal).**

Syntax deklarasi variable:
```JavaScript
let a = 25; 
let a = 10; // error, tidak boleh deklarasi ulang variable

for(let i = 0; i < 10; i++){
    console.log(i) // variable i ada di dalam scope looping for
}

console.log(i); // error, karena i hanya hidup di dalam looping
```

### Const
Const adalah cara deklarasi variable dengan **block scope**, sama dengan let. Akan tetapi const bersifat _immutable_, artinya tidak boleh dideklarasi ulang dengan value yang lain.

Syntax deklarasi variable:
```JavaScript
const pi = 3.14; 
const x; // error, deklarasi variable harus dengan beserta nilainya
pi = 123; // error karena pi tidak boleh dideklarasi ulang
```


## Data Type
JavaScript memiliki _built-in_ data type yang disebut juga **primitive** data type, yaitu:
1. Number
2. String
3. Boolean
4. null
5. undefined
6. NaN
7. Array

Setiap tipe data memiliki sifat dan fungsinya masing-masing. 

### 1. Number
Number adalah tipe data yang kita gunakan untuk berhitung (penjumlahan, pengurangan, pembagian, perkalian).

```JavaScript
var a = 42;
var age = 26;
```

### 2. String
String adalah tipe data yang kita gunakan saat akan mencetak sebuah nilai ke layar, mengolah karakter (string, kata atau kalimat).

Untuk mendeklarasikan sebuah data adalah tipe data string, data harus dikelilingi oleh tanda petik satu ('...') atau petik dua ("...").

```JavaScript
var a = 'a'; // deklarasi dengan value sebuah karakter
var foo = 'I love javascript'; // deklarasi value dengan kalimat
```

### 3. Boolean
Boolean adalah tipe data yang kita gunakan jika dibutuhkan suatu keputusan (ya atau tidak). Boolean hanya memiliki dua nilai, *true* atau *false*.

```JavaScript
//deklarasi variable dengan tipe data boolean
var boo = true;
var foo = false;
```

### 4. Null

### 5. undefined

### 6. NaN

### 7. Object

### Convert Between Types
Akan ada saatnya dimana kita ingin mengolah tipe data number dengan tipe data string, atau juga sebaliknya. Untuk bisa mengubahnya, konversi dari satu tipe data ke tipe data yang lain dalam javascript disebut ***coercion***.

Coercion dalam JavaScript dapat dibagi dua, yaitu *explicit* dan *implicit*.

* Explicit Coercion : dengan secara jelas mengkonversi tipe data dari satu ke tipe data yang lain
```JavaScript
var a = '45';
var b = Number(a); // var b sekarang berisi angka 45
var c = String(b); // var c sekarang berisi karakter '45'
```

* Implicit Coercion : javascript machine dengan secara otomatis akan melakukan konversi tipe data
```JavaScript
// melakukan perbandingan. Javascript konversi '99.99' menjadi number 99.99 sehingga hasil perbandingannya bernilai true
'99.99' === 99.99; 

var age = 26;
var str = 'I am ' + age + ' years old'; // konversi variable age dengan nilai 26 menjadi string '26'
```

## Blocks
Jika kita memiliki beberapa statement yang saling berhubungan secara logika satu sama lain, kita bisa mengelompokkannya dalam kurung kurawal {} atau block.

```JavaScript
//contoh stand-alone block statement
{
    var a = 42;
    foo(a / 2);
}
```

Akan tetapi, kebanyakan block tidak stand-alone seperti di atas. Seringkali block dikaitkan dengan statement lain, seperti **if statement, for dan while statement (loop), function statement**, dan lain-lain.