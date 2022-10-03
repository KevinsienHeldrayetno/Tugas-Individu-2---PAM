# Tugas Individu 2
## Rangkuman Materi JavaScript

Nama  : Kevinsien Heldrayetno\
NIM   : 120140174\
Kelas : RB

## Closure
Closure merupakan suatu fungsi sebagai fungsi outer yang memiliki fungsi inner yang dapat mengakses baik fungsi dari outer, maupun variabel yang terdapat secara lokal maupun global. Closure dibuat ketika fungsi child menyimpan lingkup fungsi induk bahkan setelah fungsi induk telah dijalankan.
Contoh:
```
function OuterNIM() {
    var outerNIM = 174;
    function InnerNIM() {
        alert(outerNIM);
    }
    return InnerNIM;
}
var innim = OuterNIM();

innim(); 
```

## Immediately Invoked Function Expression
Immediately Invoked Function Expression (IIFE) merupakan fungsi yang akan mengeksekusi fungsi secara langsung setelah fungsi dideklarasi. IIFE biasanya digunakan untuk memastikan variabel hanya dapat diakses dalam lingkup fungsi yang ditentukan.
Contoh:
```
(function (){
    console.log('Contoh');
})();
```

## First-class function
First-class function merupakan fungsi yang disimpan dalam bentuk variabel, objek dan array. Frist class Function dapat direturn oleh fungsi lain.

## Higher-order function
Higher-order function adalah fungsi yang memiliki fungsi lain yang menerima fungsi sebagai parameter dan atau mengembalikan fungsi.
```
let AK = [
    {nama: 'Skadi', DP: 19},
    {nama: 'Rosmontis', DP: 25},
    {nama: 'Mudrock', DP: 36},
    {nama: 'Fiammetta', DP: 29},
    {nama: 'GoldenGlow', DP: 22},
]
AK = AK.filter(AK => AK.DP >=21)
alert(AK.map(AK => AK.nama))
```

## Execution Context
Execution Context merupakan fungsi yang digunakan untuk menjalankan fungsi.
contoh:
```
b();
console.log(a);

var a = "Testing";
function b(){
    console.log("Testing 2");
}
```


## Execution Stack
Execution Stack digunakan untuk menyimpan semua konteks eksekusi yang dibuat.
contoh:
```
function b(){

}

function a(){
    b();
}

a();
```

## Event Loop
Event Loop merupakan proses perulangan yang hanya mempunyai satu thread.
```
console.log("sebelum delay");
  
function delayperdetik(sec) {
   let start = now = Date.now()
   while(now-start < (sec*1000)) {
     now = Date.now();
   }
}
  
delayperdetik(5);
  
console.log("setelah delay");//keluar setelah delay 5 detik
```
## Callbacks
Callbacks merupakan fungsi yang akan dikembalikan ke dalam fungsi lain sebagai argumen.
```
// function
function fun(var1, callback) {
    console.log('Hi' + ' ' + var1);
    callback();
}

// callback function
function calfun() {
    console.log('Test berhasil');
}

greet('Peter', calfun);
```

