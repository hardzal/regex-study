# regex-study

- Dot `.` digunakna untuk memilih semua jenis karakter

- Jika kita ingin mengetahui hanya karakter tertentu diantara karakter lainnya maka gunakan `[]`

misal `/b[aiueo]r/`
maka regex diatas akan menerima kata bar bir bur ber bor bur

- Jika untuk mengecualikan karakter tertentu bisa menggunakan ^
misal `/b[^eo]r/`
maka hanya bisa menerima karakter selain ber bor

- Untuk menentukan karakter / angka tertentu juga bisa menggunakan -
misal `/[0-9]/`

- `+` digunakan untuk menyatakan suatu karakter ada atau bisa lebih dari sekali kemunculannya secara beruntut
? menunjukkan bahwa suatu karakter optional (Tidak wajib ada)
- `*` digunakan untuk menyatakan Ketika suatu karakter bisa tidak diperlukan atau bisa berulang lebih dari satu kali
- `{n}` bisa digunakan untuk menunjukkan bahwa suatu huruf bisa ditentukan berapa kali perulangannya secara beruntut
- `{n,}` mirip dengan sebelumnya tetapi untuk yang ini minimal berapa karakter yang bisa digunakan
- `{n,m}` mirip dengan seblumnya perbedaanya menggunakan range dari n ke m yang artinya suatu karakter bisa dibatasi serta diminimalkan jumlah nya pada urutan tertentu

`/be+r/`
`/be*r/`
`/be{2}r/`

- `()` digunakan untuk mengelompokkan suatu rule tertentu
rule dibawah menggunakan \1 untuk menghindari pengulangan ulang. \2 digunakan untuk mengulangi sebanyak 2 kali
(ha)-\1,(haa)-\2 

- `:?` You can group an expression and ensure that it is not captured by references
(?:ha)-ha,(haa)-\1

- `|` mirip [] tetapi bekerja hanya per karakter 
(c|r)at|dog

- `\` digunakan untuk menghindari symbol karakter tertentu
(\*|\.)

- `^[0-9]` digunakan untuk hanya memilih number pada awal kalimat


- ``$`` digunakan untuk akhir kalimat
html$

- `\w` untuk karakter, number dan underscore
- `\w` untuk selain karakter, number dan underscore
- `\s` untuk symbol
- `\S` untuk selain symbol

- Pola berikut untuk memiliih hanya angka yang ada di depan PM
`\d+(?=PM)`
- Pola berikut untuk memilih selain angka yang ada di depan PM
`\d+(?!PM)`

- memilih number yang hanya ada dibelakang $
`(?<=\$)\d+`
- dibawah pola kebalikannya dari yang atas
`(?<!\$)\d+`

- `\pola\g` global
- `\pola\m` multiline
- `\pola\i` insensitive

- `.*r` greedy matchmaking
- `.*?r` lazy matching
