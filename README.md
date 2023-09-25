# learn-javascript-es6

# Variable

1. Variable (var) -> Tidak digunakan lagi.
2. Variable (let) -> Gunakan variabel ini untuk deklarasi, jangan gunakan var.
3. Variable (const) -> Gunakan variable ini untuk sebuah nilai yang tidak bisa diubah.

# Artimatika

## Operator Aritmatik

1. (+) Penjumlahan.
2. (-) Pengurangan.
3. (\*) Perkalian.
4. (/) Pembagian.
5. (\*\*) Ekponensial/Pangkat.
6. (%) Sisa bagi/Modulus.

# Operator Augmented Assigments

Operator ini digunakan untuk mempersingkat, jika ada sebuah variable yang melakukan operasi terhadap dirinya sendiri
Contoh :

1. result = result + 1 -> result += 1;

# Operator Perbandingan

1. (>) = lebih dari.
2. (<) = kurang dari.
3. (>=) = lebih dari sama dengan.
4. (<=) = kurang dari sama dengan.
5. (==) = sama dengan.
6. (===) = sama dengan dan sama tipe.
7. (!=) = tidak sama dengan.
8. (!==) = tidak sama dengan atau tidak sama tipe.

# Operator Logika

1. (&&) = dan -> operator ini digunakan untuk menghasilkan nilai true dengan syarat kedua atau lebih variabel bernilai true.
2. (||) = atau -> operator ini digunakan untuk menghasilkan nilai true dengan syarat salah satu variable berniali true.
3. (!) = unary -> operator ini digunakan untuk membalikan sebuah nilai.

# Console

Merupakan fitur logging milik javascript, digunakan untuk proses debugging oleh programmer tanpa mengganggu alur kerja sistem yang sedang berjalan.

0. console.debug(...) = menampilkan pesan juga dalam skala kecil (jarang digunakan).
1. console.info/log(...) = digunakan untuk menampilkan informasi.
2. console.warn(...) = menampilkan informasi peringatan.
3. console.error(...) = menampilkan pesan error.
4. console.table(...) = menampilkan informasi bentuk table.

# String Template

Digunakan untuk memanggil nilai dari sebuah variabel dengan cara yang lebih ringkas dan efisien. dengan menambahkan backtick (``) dalam penulisannya.

## Penulisan String Template

Perbandingan typing :

    //   String Template
    const nama = `Nama : ${firstName} ${middleName} ${lastName}`;
    //   Cara Lama Javascript
    const nama2 = "Nama : " + firstName + " " + middleName + " " + lastName;

## Expression didalam String Template

Selain itu, string template juga bisa digunakan untuk sebuah expression, misal untuk status lulus berikut :

      // Expressions dialam String Template
      const nilai = 100;
      const template = `Nama : ${namaAsli}, Lulus : ${nilai > 75}`;

# Konversi Number dan String

Di javascript, kita bisa mengkonversikan nilai dari sebuah variabel. nilai bisa berasal dari inputan user misalnya.

1.  parseInt(string) = mengkonversikan dari string ke number bilangan bulat
2.  parseFloat(string) = mengkonversikan dari string ke number bilangan float
3.  Number(string) = mengkonversikan dari string ke number sesuai data (bisa bulat ataupun float)
4.  .toString() = mengkonversikan dari number ke string

        //   Konversi string to number
        document.writeln(`<p> ${parseInt("1.2")} </p>`);
        document.writeln(`<p> ${parseFloat("1.2")} </p>`);
        document.writeln(`<p> ${Number("1.2")} </p>`);

        //   Konversi number to string
        const string1 = "1";
        const string2 = "1";
        const sum = string1 + string2;
        document.writeln(`<p> ${sum.toString()} </p>`);

## NaN

Not a Number adalah case ketika sebuah data yang akan dikonversikan dari number ke string, adalah bukan number. contoh "a" berbeda dengan "1" walaupun keduanya string.

        document.writeln(`<p> ${parseFloat("1")} </p>`); // 1
        document.writeln(`<p> ${parseFloat("a")} </p>`); // NaN

Javascript akan mentoleransi suatu string yang akan dikonversi, jika numbernya ada didepan. jika tidak, maka output adalah NaN. hal tadi tidak berlaku untuk konversi "Number();"

        document.writeln(`<p> ${parseFloat("1saja")} </p>`); // 1
        document.writeln(`<p> ${parseFloat("s1aja")} </p>`); // NaN
        document.writeln(`<p> ${Number("s1aja")} </p>`); // NaN

NaN tidak bisa dioperasikan dengan bilangan apapun. Semua yang dioperasikan dengan NaN akan menghasilkan output NaN

## isNaN()

Adalah function untuk cek suatu nilai, apakah NaN atau bukan. Outputnya ada boolean (true/false).

        const isNaN1 = "1";
        const isNaN2 = "salah";
        document.writeln(`<p> ${isNaN(isNaN1)} </p>`); // False
        document.writeln(`<p> ${isNaN(isNaN2)} </p>`); // True

# Array

Array digunakan untuk menampung sebuah atau banyak nilai di sebuah variabel. Jadi, kita tidak perlu membuat banyak variable untuk menampung suatu nilai.
Array di dalam javascript tidak memiliki batasan, kita bisa memasukan tipe data apapun didalam satu array, bahkan kita bisa memasukan array didalam array jika diperlukan.

## Operasi di dalam Array

1.  ( array.push(value) ) = menambah data ke dalam array.
2.  ( array.length ) = melihat panjang array
3.  ( array[index] ) = mendapat dara di posisi index
4.  ( array[index] = value ) = mengubah data di posisi index
5.  ( delete array[index] ) = hapus array berdasarkan index

        // Contoh pembuatan array
        const names = ["Fazril", "Fatma", 6];
        console.table(names);

        //   Contoh pembuatan array kosong
        const arrayKosong = [];
        arrayKosong.push("Ini");
        arrayKosong.push("Isian Baru");
        console.table(arrayKosong);

        //   array.length
        console.table(names.length);

        //   array[index]
        console.log(names[0]);

        //   array[index] = value
        names[0] = "dirubah";
        console.table(names);

        //   delete array[index]
        delete names[1];
        console.table(names);

# Object

Mirip dengan array, bedanya kalau di tipe data object, penamaan indexnya bukan lagi angka tapi langsung nama.

        // Array
        index : 0,1,2,3,4,....

        // Object
        index : nama, alamat, umur, ....

\*besar kecil huruf dinggap berbeda untuk tiap nama indexnya : "Besar" berbeda dengan "besar"

Penulisan object menggunakan kurung kurawa ( {} )

        // Contoh Penulisan Object
        const orang = {};

        // ubah property / attribute
        orang["Nama"] = "Fazril Arief Nugraha";
        orang["Alamat"] = "Indonesia";
        orang["Umur"] = 21;

        // hapus index object
        delete orang["Umur"];

object bisa juga ditulis secara langsung seperti array

        // penulisan object secara langsung
        const orang2 = {
                nama: "Fazril Arief Nugraha",
                alamat: "Indonesia",
                umur: 21,
        };

ada 2 cara akses object

        // akses properties object
        console.log(`Nama : ${orang2.nama}`); //cara cepat (sering digunakan)
        console.log(`Nama : ${orang2["nama"]}`); //cara lambat (jarang digunakan)

# if expression

pengkondisian if digunakan untuk melakukan sebuah perbadingan antara nilai 1 dengan nilai lainnya.

        // deklarasi nilai
        const examValue = 100;

        // deklarasi nilai
        const examValue = 59;

        // penulisan if
        if (examValue >= 90) {
                document.writeln("Grade A");
        } else if (examValue >= 80) {
                document.writeln("Grade B");
        } else if (examValue >= 70) {
                documnent.writeln("Grade C");
        } else if (examValue >= 60) {
                document.writeln("Grade D");
        } else {
                document.writeln("Grade E");
        }

"else if" digunakan apabila ada lebih dari 1 kondisi yang harus digunakan.
