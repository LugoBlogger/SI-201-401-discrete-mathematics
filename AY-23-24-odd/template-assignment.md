> Berikut adalah tempate soal menggunakan contoh soal
> dan jawaban dari teki-teko logika di pertemuan minggu
> ke 2. Silahkan format (bukan jawaban) mengikuti contoh 
> pengerjaaan soal berikut.
> Pada bagian akhir disertakan juga panduan pengetikan
> dan beberapa *links* yang sekiranya berguna
> untuk mengetik beberapa persamaan.

# Template Assignment 01

**Anggota kelompok**
- Nama Mahasiswa 1 (NIM) (no soal yang dikerjakana)
- Nama Mahasiswa 2 (NIM) (1)
- Nama Mahasiswa 3 (NIM) (2)
- dst.


## Soal 1

Disebuah pulau fiksi terdapat dua macam penghuni yaitu,
pemuka agama dan pencuri. Pemuka agama selalu berkata jujur
sedangkan pencuri selalu berkata bohong. Kita dihadapkan
dengan dua orang $A$ dan $B$ di pulau tersebut dan kita
tidak tahu apakah $A$ pemuka agama atau pencuri demikian
dengan $B$. Kita hanya memperoleh informasi dari dua 
pernyataan berikut:
- $A$ berkata, \"$`B`$ adalah pemuka agama\".
- $B$ berkata, \"Kami berdua memiliki dua peran berbeda\".

Tentukan peran (pemuka agama atau pencuri) dari 
kedua orang $A$ dan $B$.

### Jawaban

Misalkan dua proposisi $p$ dan $q$ sebagai berikut:
- $p = $ \"$`A`$ adalah pemuka agama\"
- $q = $ \"$`B`$ adalah pemuka agama\"

Dan perkataan $A$ dan $B$ dapat dinyatakan dalam bentuk 
proposisi 
- perkataan A: "$B$ adalah pemuka agama" = $q$
- perkataan B: "Kami berdua memiliki dua peran berbeda"    
  = $(p \wedge \neg q) \vee (\neg p \wedge q)$

Bentuk proposisi perkataan B merupakan dua pasangan 
kemungkinan dari perkataan B:    
$$
\begin{gather*}
\text{($A$ adalah pemuka agama 
      \textbf{dan} $B$ adalah pencuri) 
\textbf{atau} 
  ($A$ adalah pencuri \textbf{dan} $B$ adalah pemuka agama)}
\end{gather*}
$$

Kita memiliki dua kemungkinan bahwa $p$ bernilai benar 
($A$ adalah pemuka agama) atau salah ($A$ adalah pencuri). 
Kita akan uji masing-masing kemungkinan tersebut apakah
terjadi kontradiksi atau konsisten dengan pernyataan 
yang diberikan dan perkataan yang dikatakan oleh $A$ dan $B$.

Tanda $\Rightarrow$ menunjukkan konsekuensi ekuivalen   

**Kemungkinan pertama**: $\boxed{p \text{ benar}}$  
$\Rightarrow$ $A$ adalah pemuka agama    
$\Rightarrow$ perkataan $A$ benar 
  $\Rightarrow$ $\boxed{q \text{ benar}}$    
$\Rightarrow$ perkataan $B$ benar 
  $\Rightarrow$ $((p \wedge \neg q) \vee (\neg p \wedge q))$ benar

Di lain sisi, karena kita memiliki $p$ benar ($\textbf{T}$) dan 
$q$ benar ($\textbf{F}$) (lihat proposisi yang diberi kotak), 
dapat dihitung bahwa 

$$
\begin{align*}
  (p \wedge \neg q) \vee (\neg p \wedge q) 
    &= (\textbf{T} \,\wedge \textbf{F}) 
        \vee (\textbf{F} \wedge \textbf{T}) \\
    &= \textbf{F} \vee \textbf{F} \\
    &= \textbf{F} 
\end{align*} 
$$

Disini kita memiliki kontradiksi dua nilai yang berlawanan
untuk proposisi $(p \wedge \neg q) \vee (\neg p \wedge q)$. 
Sehingga kemungkinan pertama bahwa $p$ adalah benar tidak tepat.

**Kemungkinan kedua**: $\boxed{p \text{ salah}}$   
$\Rightarrow$ $A$ adalah pencuri    
$\Rightarrow$ perkataan $A$ salah
  $\Rightarrow$ $\boxed{q \text{ salah}}$     
$\Rightarrow$ $B$ adalah pencuri    
$\Rightarrow$ perkataan $B$ salah
  $\Rightarrow$ $(p \wedge \neg q) \vee (\neg p \wedge q)$ salah

Di lain sisi, karena kita memiliki $p$ salah ($\textbf{F}$) dan
$q$ salah ($\textbf{F}$) (lihat proposisi yang diberi kotak),
dapat dihitung bahwa

$$\
\begin{align*}
  (p \wedge \neg q) \vee (\neg p \wedge q) 
    &= (\textbf{F} \,\wedge \textbf{T}) 
        \vee (\textbf{T} \wedge \textbf{F}) \\
    &= \textbf{F} \vee \textbf{F} \\
    &= \textbf{F} 
\end{align*} 
$$

Disini kita memiliki konsistensi, sehingga kemungkinan kedua ini
merupakan kemungkinan yang benar.

Kesimpulannya, kita memiliki $p$ salah dan $q$ salah yaitu
$A$ adalah pencuri dan $B$ adalah pencuri.


## Beberapa contoh _styling_ dan format di Markdown
Berikut hanyalah sebagian kecil contoh. Untuk lebih lengkap
silahkan mengakses [Markdown Guide](https://www.markdownguide.org/)

Contoh **huruf tebal**

Contoh _huruf miring_


Contoh daftar dengan nomor 
1. item 1
   1. item 1.1
   2. item 1.2
      1. item 1.2.1
2. item 2
3. item 3

Contoh daftar tanpa nomor 
- item 1 
  - item 1.1
  - item 1.2
    - item 1.2.3
- item 2 (setelah kalimat ini terdapat beberapa spasi
  agar Paragraf item 2 berada di baris baru dan sejajar 
  item 2)    
  Paragraf item 2
- item 3
  - item 3.1


Contoh penyisipan gambar menggunakan perintah bawaan 
Markdown
![nama_image](pexels-photo-41126.jpeg)

Contoh penyisipan gamabr menggunakan perintah HTML `<img>`
<img src="./pexels-photo-41126.jpeg" width=300>


Contoh tabel
|$p$ | $q$ | $p \wedge r$  |
|--|---|----|
|T | T | T  | 
|T | F | F  | 
|F | T | F  | 
|F | F | F  | 

Persamaan dan simbol matematika diketika menggunakan
perintah TeX, lebih lengkap dapat dilihat di 
[MathJax basic tutorial and quick reference](https://math.meta.stackexchange.com/questions/5020/mathjax-basic-tutorial-and-quick-reference).    

Gunakan [detexify](https://detexify.kirelabs.org/classify.html) untuk mencari secara cepat perintah TeX yang sesuai
seperti yang telah didemonstrasikan di pertemuan minggu 2.

Contoh persamaan dalam paragraf $p \wedge q$, 
$p \vee r$, 
$p \rightarrow q$,
$p \leftrightarrow q$

**Contoh persamaan rata tengah**
$$(\neg p \rightarrow q) \vee (p \leftrightarrow q)$$

