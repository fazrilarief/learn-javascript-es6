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

## Operator Augmented Assigments

Operator ini digunakan untuk mempersingkat, jika ada sebuah variable yang melakukan operasi terhadap dirinya sendiri
Contoh :

1. result = result + 1 -> result += 1;

## Operator Perbandingan

1. (>) = lebih dari.
2. (<) = kurang dari.
3. (>=) = lebih dari sama dengan.
4. (<=) = kurang dari sama dengan.
5. (==) = sama dengan.
6. (===) = sama dengan dan sama tipe.
7. (!=) = tidak sama dengan.
8. (!==) = tidak sama dengan atau tidak sama tipe.

## Operator Logika

1. (&&) = dan -> operator ini digunakan untuk menghasilkan nilai true dengan syarat kedua atau lebih variabel bernilai true.
2. (||) = atau -> operator ini digunakan untuk menghasilkan nilai true dengan syarat salah satu variable berniali true.
3. (!) = unary -> operator ini digunakan untuk membalikan sebuah nilai.

## Console

Merupakan fitur logging milik javascript, digunakan untuk proses debugging oleh programmer tanpa mengganggu alur kerja sistem yang sedang berjalan.

0. console.debug(...) = menampilkan pesan juga dalam skala kecil (jarang digunakan).
1. console.info/log(...) = digunakan untuk menampilkan informasi.
2. console.warn(...) = menampilkan informasi peringatan.
3. console.error(...) = menampilkan pesan error.
4. console.table(...) = menampilkan informasi bentuk table.

## String Template

Digunakan untuk memanggil nilai dari sebuah variabel dengan cara yang lebih ringkas dan efisien. dengan menambahkan backtick (``) dalam penulisannya.

### Penulisan String Template

Perbandingan typing :

    //   String Template
    const nama = `Nama : ${firstName} ${middleName} ${lastName}`;
    //   Cara Lama Javascript
    const nama2 = "Nama : " + firstName + " " + middleName + " " + lastName;

### Expression didalam String Template

Selain itu, string template juga bisa digunakan untuk sebuah expression, misal untuk status lulus berikut :

      // Expressions dialam String Template
      const nilai = 100;
      const template = `Nama : ${namaAsli}, Lulus : ${nilai > 75}`;
