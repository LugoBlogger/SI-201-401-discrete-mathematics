# Assignment 03

FullName (StudentID) 

Silahkan mengerjakan semua problem berikut

## Problem 1 (15 poin)
Selesaikan konversi bilangan dari basis yang diberikan
ke basis yang ditanyakan

1. $222_{8}$ menuju basis 2
2. $\text{FAFAFA}_{16}$ menuju basis 10
3. $148_{10}$ menuju basis 8
4. $10101010111000_{2}$ menuju basis 16

Petunjuk: Sertakan cara mendapatkan hasil konversi.
Untuk pengecekan jawaban bisa dilakukan menggunakan
kalkulator yang ada di Windows/Mac/Linux.

## Problem 2 (10 poin)

Gambarkan graf untuk fungsi-fungsi berikut:

1. $f(x) = 3 \lfloor x \rfloor  - 5$ dengan $x \in \mathbb{R}$
2. $f(x) = \lfloor x \rfloor + \lceil x \rceil$ dengan $x \in \mathbb{R}$
3. $f(x) = (2-x)!$ dengan $x < 2$ dan $x \in \mathbb{Z}$
4. $f(x) = \sqrt{\lceil x \rceil }$ dengan $x \in \mathbb{R}$

Petunjuk: Bisa digambar manual, atau dengan bantuan koordinat di 
`drawio`. Apabila menggunakan `drawio`, simpan ke dalam `.png`
untuk dipanggil di dalam file markdown yang dikumpulkan.


## Problem 3 (25 poin)

Sederhanakan ekspresi Boolean berikut:
1. $\overline{x_1 x_2 \, \overline{x_1 x_2 \, \overline{x_1 x_2 \,
   \overline{x_3} \,x_2 x_1}\, x_2 x_1} \, x_2 x_1}$ 

2. $\overline{(x_1 + x_2) \, \overline{(x_1 + x_2) \, 
   \overline{(x_1 x_2) \,
   \overline{x_1 + x_3 + x_1} \, (x_2 + x_1)} \,
   (x_2 + x_1)} \, (x_2 + x_1)}$   
   
Diberikan $F(x_1, x_2, x_3) = x_3(x_1 + x_2) + x_3 + (x_1 x_2)$  dan 
$G(x_1, x_2, x_3) = (\overline{x_3} + (\overline{x_1}\,\overline{x_2}))  
\, (\overline{x_3} (\overline{x_1} + \overline{x_2}))$, tentukan  
1. $(F+G)(x_1, x_2, x_3)$  
2. $(FG)(x_1, x_2, x_3)$

## Problem 4 (50 poin)

1. Di dalam pertemuan tentang logika, kita belajar mengenai implikasi, 
   invers, konvers, dan kontrapositive. Carilah bentuk fungsi Boolean yang 
   mewakili ke-empat operator logika tersebut.

2. Tunjukkan persamaan berikut apakah berlaku atau tidak
   untuk varibel Boolean $x_1$, $x_2$, dan $x_3$
   $$
    x_1 + (x_2 \cdot x_3) \stackrel{?}{=}
        (x_1 + x_2) \cdot (x_1 + x_3)
   $$
   menggunakan tabel nilai Boolean.
