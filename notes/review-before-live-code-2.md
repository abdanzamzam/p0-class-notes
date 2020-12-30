[**Back to Home**](./../README.md)

# Review Before Live Code 2

## Soal 1
```javascript
/**
 * Terdapat sebuah function yang akan menghasilkan sebuah multidimensional array dengan jumlah baris dan kolom yang diminta oleh user.
 * Setiap elemennya akan diisi dengan huruf alphabet berurutan dari 'a' hingga 'z'.
 * Pengisian huruf dimulai dari baris pertama dari kiri ke kanan. Ketika baris pertama sudah terisi dengan huruf huruf alfabet,
 * maka pengisian dilanjutkan pada baris berikutnya dari kiri ke kanan, dan seterusnya.
 * Ketika pengisian huruf sudah sampai 'z', maka elemen selanjutnya akan diisi oleh huruf 'a' lagi dan seterusnya.
 *
 * RULES:
 *   - Dilarang menggunakan built-in function kecuali .push()
 */

function boxOfAlphabet(row, col) {
  // Your code here
}

console.log(boxOfAlphabet(2, 2));
// [
//   ['a', 'b'],
//   ['c', 'd']
// ]


console.log(boxOfAlphabet(3, 4));
// [
//   ['a', 'b', 'c', 'd'],
//   ['e', 'f', 'g', 'h'],
//   ['i', 'j', 'k', 'l']
// ]


console.log(boxOfAlphabet(6, 5));
// [
//   ['a', 'b', 'c', 'd', 'e'],
//   ['f', 'g', 'h', 'i', 'j'],
//   ['k', 'l', 'm', 'n', 'o'],
//   ['p', 'q', 'r', 's', 't'],
//   ['u', 'v', 'w', 'x', 'y'],
//   ['z', 'a', 'b', 'c', 'd']
// ]
```

## Soal 2
```javascript
/**
 * Terdapat function groupCharacterCoordinate yang memiliki 2 parameter.
 *   - Parameter 1 merupakan array multidimensi yang berisi karakter-karakter.
 *   - Parameter 2 merupakan karakter yang akan dicari dari parameter pertama.
 * 
 * Function ini akan menghasilkan sebuah multidimensional array seperti contoh di bawah.
 * 
 * Contoh:
 *   - Parameter 1: 
 *       [
 *         ["F","$","#","*"],
 *         ["$","A","@","O"],
 *         ["%","&","#","@"],
 *         ["A","*","&","%"]
 *       ]
 *   - Parameter 2: '$'
 *   - Output: [ '$', [ 0, 1 ], [ 1, 0 ] ]
 * 
 * RULES:
 *   - Dilarang menggunakan built-in function kecuali .push()
 */
function groupCharacterCoordinate(arr, character) {
  // Your code here
}
console.log(groupCharacterCoordinate([
  ["F", "$", "#", "*"],
  ["$", "A", "@", "O"],
  ["%", "&", "#", "@"],
  ["A", "*", "&", "%"]
], '$'));
// [ '$', [ 0, 1 ], [ 1, 0 ] ]

console.log(groupCharacterCoordinate([
  ["F", "$", "#", "*", "B", "^", "P", "%"],
  ["$", "A", "@", "O", "O", "G", "$", "?"],
  ["%", "&", "#", "@", "A", "*", "#", "F"],
  ["A", "*", "&", "%", "B", "O", "?", "N"],
  ["F", "$", "#", "*", "$", "%", "&", "B"],
  ["$", "A", "@", "O", "N", "F", "O", "P"],
  ["%", "&", "#", "@", "!", "%", "*", "#"],
  ["A", "*", "&", "%", "^", "M", "@", "P"]
], '@'));
// [ '@', [ 1, 2 ], [ 2, 3 ], [ 5, 2 ], [ 6, 3 ], [ 7, 6 ] ]
```

## Soal 3
```javascript
/**
 * Kalian ditugaskan untuk membuat sebuah program yang akan dipakai Bandara Internasional Soekarno-Hatta
 * untuk memeriksa apakah seseorang merupakan suspect dari suatu penyakit berbahaya yang baru saja mewabah akhir-akhir ini.
 * Program akan menerima input berupa object yang merepresentasikan penumpang dengan format seperti berikut:
 * 
 *   {
 *     name: (string),
 *     id: (number),
 *     temperature: (number),
 *     travelHistory: [] (array of strings)
 *   }
 * 
 * Program ini akan mengevaluasi apakah seseorang merupakan suspect dari penyakit ini atau tidak, dan menghasilkan output berupa string.
 * Berikut ini adalah kondisi-kondisi yang akan ditangani:
 *   - Jika suhu tubuhnya diatas 35 derajat celcius dan dia pernah mengunjungi salah satu dari 4 negara berikut: 'China', 'Japan', 'Korea', dan 'Singapore', maka dia dinyatakan sebagai "Suspect".
 *   - Jika suhu tubunya tidak diatas 35 derajat celcius, maka dia tidak apa-apa dan dinyatakan "Healthy".
 *       - Namun, jika suhunya tidak diatas 35 derajat celcius tetapi dia pernah berkunjung ke 4 negara diatas, maka dia dinyatakan sebagai seorang "Potential Carrier".
 *   - Jika suhu tubuhnya tinggi tetapi dia tidak pernah berkunjung ke 4 negara tersebut maka dia hanya sakit, dan dinyatakan "Sick".
 *
 * Output yang dikeluarkan program ini memiliki format sebagai berikut:
 *   "Passenger [id] [name] [status]"
 *
 * Status bisa berupa:
 * [status] : Suspect, Healthy, Potential Carrier, Sick
 *
 * RULES:
 *   - Dilarang menggunakan built-in function kecuali .push()
 */

function evaluatePassenger(passenger) {
  // Your code here
}

console.log(evaluatePassenger({ name: 'Budi', id: 50, temperature: 40, travelHistory: ['Russia', 'Japan'] })); //Passenger 50 Budi Suspect
console.log(evaluatePassenger({ name: 'Tono', id: 10, temperature: 40, travelHistory: ['Morocco', 'France', 'Burma'] })); //Passenger 10 Tono Sick
console.log(evaluatePassenger({ name: 'Tsubasa', id: 15, temperature: 30, travelHistory: ['Brazil'] })); //Passenger 15 Tsubasa Healthy
```

## Soal 4

```javascript
/**
 * Buatlah sebuah fungsi yang akan mencocokan requirement dari sebuah perusahaan dengan skill yang dimiliki oleh seseorang.
 * Fungsi ini akan menerima dua parameter yang berupa object.
 *
 * Parameter pertama adalah sebuah object perusahaan dengan beberapa data berikut: nama perusahaan, job yang ditawarkan dan requirement yang dibutuhkan untuk mendapatkan pekerjaan.
 * Parameter kedua adalah sebuah object pelamar dengan beberapa data berikut: nama pelamar, skill pelamar dan job yang dinginkan oleh pelamar tersebut.
 *
 * Fungsi ini akan menghitung persentase kecocokan perusahaan dan pelamar yang dikirimkan dengan beberapa syarat:
 *   1. Jika job yang ditawarkan oleh perusahaan tidak sesuai dengan job yang diinginkan maka persentase mereka adalah 0%.
 *   2. Jika seluruh requirement yang diminta oleh perusahaan dipenuhi oleh pelamar maka persentase mereka adalah 100%.
 *   3. Jika ada beberapa requirement yang tidak dipenuhi pelamar maka persentase akan dihitung dengan rumus:
 *        (jumlah requirement yang dipenuhi) / (requirement yang diminta)
 *      Contoh: Terdapat 3 requirement pada perusahan tetapi pelamar hanya memenuhi 2 requirement.
 *              Maka dari itu persentase pelamar tersebut adalah 66% (pembulatan ke bawah).
 *
 * Jika seseorang mendapatkan persentase diatas 60% maka fungsi akan menghasilkan pesan:
 *   Selamat [nama pelamar], Anda cocok dengan perusahaan [nama perusahaan] dengan persentase kecocokan [persentase]%.
 * Jika tidak, maka fungsi akan menghasilkan pesan:
 *   Mohon maaf [nama pelamar], Anda belum cocok dengan perusaahan [nama perusahaan]. Anda hanya mendapatkan persentase kecocokan [persentase]%.
 */

function companyMatch(company, user) {
  // Your code here
}

const company1 = {
  name: 'Pesbok',
  job: 'Frontend Developer',
  requirement: ['HTML', 'CSS', 'JS']
};

const john = {
  name: 'John',
  applyAs: 'Frontend Developer',
  skills: ['HTML', 'CSS', 'JS']
};

const kosasih = {
  name: 'Kosasih',
  applyAs: 'Backend Developer',
  skills: ['Express', 'Node', 'PHP']
};

const marry = {
  name: 'Marry',
  applyAs: 'Frontend Developer',
  skills: ['HTML', 'CSS']
};

console.log(companyMatch(company1, john)); // Selamat John, Anda cocok dengan perusahaan Pesbok dengan persentase kecocokan 100%.
console.log(companyMatch(company1, kosasih)); // Mohon maaf Kosasih, Anda belum cocok dengan perusaahan Pesbok. Anda hanya mendapatkan persentase kecocokan 0%.
console.log(companyMatch(company1, marry)); // Selamat Marry Anda cocok dengan perusahaan Pesbok dengan persentase kecocokan 66%.
```

[Answers](./review-before-live-code-2-answered.md)

[**Back to Home**](./../README.md)
