# JavaScript 101 - Fundamental

## Brief History

JavaScript adalah bahasa pemrograman yang dibuat untuk Web. HTML, CSS dan JavaScript adalah tiga inti utama dalam World Wide Web.

Di tahun 1995, Brendan Eich yang bekerja di Netscape Communication Corporations mendapat project untuk menambah Scheme pada Netscape Navigator untuk membuat Web lebih dinamis. FYI, Netscape Navigator adalah salah satu dari web browser internet. Brendan Eich menyelesaikannya dalam 10 hari. Nama awal yang digunakan adalah LiveScript, yang kemudian diubah menjadi JavaScript, dengan tujuan untuk menunggangi ketenaran bahasa pemrograman Java pada saat itu. Ingat, JavaScript dan Java adalah dua bahasa pemrograman yang berbeda.

**JavaScript Engine pada browser:**

* Chrome: V-8 Engine
* Edge: Chakra
* Safari: Nitro Engine
* Firefox: SpiderMonkey


## Variable Declaration

Variable declaration adalah cara untuk membuat "kotak" atau *container* dalam komputer yang nantinya dapat digunakan untuk menampung data. 

**_Static typing/type enforcement_**: Kita harus mendeklarasikan variable beserta tipe data variablenya. Contoh: C, C++, Java
**_Weak typing/dynamic typing_**: Memungkinkan kita mendeklarasikan variable dengan tipe apapun. Contoh: JavaScript

Ada 3 cara untuk mendeklarasikan variable, yaitu dengan **_var, let dan const._**

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
Let adalah cara deklarasi variable dengan **block scope**. Block scope adalah semua yang berada di dalam {} (kurung kurawal).

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
Const adalah cara deklarasi variable dengan **block scope**, sama dengan let. Akan tetapi const bersifat _immutable_, artinya tidak boleh diisi dengan value yang lain

Syntax deklarasi variable:
```JavaScript
const pi = 3.14; 
const x; // error, deklarasi variable harus dengan beserta nilainya
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