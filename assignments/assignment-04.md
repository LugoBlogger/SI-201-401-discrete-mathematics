# Assignment 04

**Group members**
- FullName1 (StudentID) (Problem #)
- FullName2 (StudentID) (Problem #)
- FullName3 (StudentID) (Problem #)
- etc.

## Problem 1 (Combinatorial)
Dalam suatu acara makan bersama, terdapat 3 meja bundar yang dapat diisi
oleh 4 orang. Total tamu yang data sebanyak 15 orang. 
Ada berapa banyak cara menyusun lokasi tempat duduk tamu-tamu tersebut?

### Answer

## Problem 2 (Graph 1a)
Suatu graf dikatakan graf _bipartite_ jika kita dapat memisahkan 
himpunan simpul-simpulnya (_vertices_), $V$ menjadi dua himpunan simpul $V_1$ 
dan $V_2$ yang mana tidak ada busur (_edge_) sama sekali yang menghubungkan
dua simpul di dalam satu himpunan yang sama.

Sebagai contoh:
<table>
  <tr>
    <td><b>Graf</b></td>
    <td><b>Penjelasan</b></td>
  </tr>
  <tr>
    <td><img src="../figures/bipartite-ex-01.png" width=800></td>
    <td> <b>Bipartite</b> karena kita dapat memisahkan simpul-simpulnya menjadi dua himpunan 
    <i>V</i><sub>1</sub> = {
      <i>v</i><sub>1</sub>, 
      <i>v</i><sub>3</sub>, 
      <i>v</i><sub>5</sub> } dan 
    <i>V</i><sub>2</sub> = {
      <i>v</i><sub>2</sub>, 
      <i>v</i><sub>4</sub>, 
      <i>v</i><sub>6</sub> } yang mana dimasing-masing himpunan 
    <i>V</i></sub>1</sub>  dan <i>V</i><sub>2</sub> tidak ada busur penghubung dan setiap anggota <i>V</i><sub>1</sub> dan <i>V</i><sub>2</sub> memiliki setidaknya satu busur penghubung.</td>
  </tr>
  <tr>
    <td><img src="../figures/bipartite-ex-02.png" width=800></td> 
    <td>Bukan bipartite, karena bagaimanapun kita memisahkan simpul-simpulnya, selalu ada penghubung antara simpul dalam satu himpunan yang sama. Misal kita buat <i>V</i><sub>1</sub> = { <i>v</i><sub>1</sub> } dan 
    <i>V</i><sub>2</sub> = { <i>v</i><sub>2</sub>, <i>v</i><sub>3</sub> }. 
    Maka sangatlah jelas <i>v</i><sub>2</sub> dan <i>v</i><sub>3</sub> masih terhubung oleh busur dan tidak sesuai dengan definisi bipartite.</td>
  </tr>
</table>
Dari penjelasan di atas tentukan dan jelaskan apakah graf dibawah ini bipartite atau bukan:

1. <img src="../figures/bipartite-Q1.png" width=200 style="vertical-align:top">

2. <img src="../figures/bipartite-Q2.png" width=250 style="vertical-align:top">

3. <img src="../figures/bipartite-Q3.png" width=300 style="vertical-align:top">


### Answer

## Problem 3 (Graph 1b)
Tentukan dan jelaskan apakah mungkin melalui semua busur hanya sekali
di graf di bawah ini

<img src="../figures/euler-path-Q1.png" width=100>

### Answer

## Problem 4 (Graph coloring)

Lakukan pewarnaan pada setiap simpul graf di bawah ini sedemikian rupa
sehingga tidak ada dua simpul yang terhubung oleh suatu busur memiliki
warna yang sama. Himpunan warna yang dapat dipakai:
(Merah, Jingga, Kuning, Hijau, Biru, Ungu, dst.)

<img src="../figures/graph-coloring-Q1.png" width=300>

Ada berapa jumlah warna paling sedikit yang digunakan untuk mewarnai
graf diatas?

### Answer

## Problem 5 (Tree)

Berikut adalah papan dari _ultimate Tic-Tac-Toe_ berukuran 2x2.

<img src="../figures/ultimate-tix-tac-toe-2x2-Q1.drawio.png" width=300>

Jika pemain pertama memulai dengan simbol X. Tentukan dan gambarkan 
diagram tree untuk 
kemungkinan dua langkah pertama dimulai dari papan kosong.
_Petunjuk_: Gunakan drawio untuk menggambar langkah papan lebih cepat.

### Answer

