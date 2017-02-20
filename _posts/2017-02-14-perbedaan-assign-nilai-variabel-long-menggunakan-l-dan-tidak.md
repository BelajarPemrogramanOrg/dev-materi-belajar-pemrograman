---
ID: 317
post_title: >
  Apa Perbedaan Antara Assign Nilai ke
  Variabel long di Java Menggunakan L dan
  Tidak Menggunakannya?
author: Muhammad Ikhsan
post_date: 2017-02-14 09:19:17
post_excerpt: ""
layout: post
permalink: >
  http://belajarpemrograman.app/perbedaan-assign-nilai-variabel-long-menggunakan-l-dan-tidak/
published: true
---
<h2 class="no-mar-top">Pertanyaan</h2>
Di materi yang berjudul <a href="http://belajarpemrograman.app/catatan-belajar-bahasa-pemrograman-java/">Catatan Belajar Bahasa Pemrograman Java</a>, dijelaskan bahwa untuk mengekspresikan nilai dari sebuah variabel bertipe <code>long</code> dapat digunakan literal <code>int</code> (misal 1000) atau literal <code>long</code>, yaitu dengan menambahkan <code>L</code> atau <code>l</code> di akhir penulisan nilai bilangan (misal 1000L). Jika keduanya bisa digunakan, lalu apa bedanya?
<pre>long longNumber  = 1000;
long longNumberL = 1000L;</pre>
<h2>Jawaban</h2>
<ul>
 	<li>Rentang nilai dalam tipe data <code>int</code>:
Minimal -2.147.483.648
Maksimal 2.147.483.647</li>
 	<li>Rentang nilai dalam tipe data <code>long</code>:
Minimal -9.223.372.036.854.775.808
Maksimal 9.223.372.036.854.775.807</li>
</ul>
Untuk meng-<em>assign</em> sebuah nilai bilangan bulat dalam rentang nilai dari -2.147.483.648 sampai 2.147.483.647 ke sebuah variabel bertipe <code>long</code>, kita dapat menggunakan literal <code>int</code>.

Namun untuk meng-assign sebuh nilai bilangan bulat yang tidak berada dalam rentang nilai tipe data <code>int</code>, namun masih dalam rentang nilai tipe data <code>long</code>, kita harus menggunakan literal <code>long</code>. Yaitu dengan menambahkan <code>L</code> atau <code>l</code> di akhir penulisan bilangan.

Baik <code>L</code> maupun <code>l</code> dapat digunakan dalam literal <code>long</code>, keduanya sama saja. Namun, untuk <em>readibility</em> alias supaya mudah dibaca, sebaiknya gunakan kapital <code>L</code>. Bilangan 313 ditulis dengan literal <code>long</code> menggunakan <code>313L</code> lebih mudah dikenali sebagai 313 daripada jika dituliskan <code>313l</code>. Gampang terbaca salah, dikira angka 3131.
<pre>// Memasukkan nilai ke dalam variabel bertipe long menggunakan literal int.
// Selama nilai tersebut masih dalam rentang nilai tipe data int, 
// maka tidak terjadi error.
long longNumber  = 1000;

// Memasukkan nilai ke dalam variabel bertipe long menggunakan literal int.
// Karena rentang nilai tipe data int maksimal 2147483647, 
// maka akan terjadi error saat kompilasi.
long longNumber  = 2147483648;

// Memasukkan nilai ke dalam variabel bertipe long menggunakan literal long.
// Karena 2147483648 masih berada di dalam rentang nilai tipe data long, 
// maka tidak terjadi error.
long longNumberL = 2147483648L;</pre>