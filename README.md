## Fundamental Javascript

1. Untuk pengembangan aplikasi seperti apa bahasa JavaScript? <br/>
   JavaScript digunakan untuk pengembangan aplikasi web baik front-end maupun back-end, serta untuk pengembangan aplikasi mobile dan desktop menggunakan teknologi web seperti React Native dan Electron. JavaScript juga dapat digunakan untuk pengembangan game dan aplikasi IoT (Internet of Things). Karena kemampuan JavaScript yang fleksibel, dinamis, dan mudah dipelajari, bahasa ini sangat populer dan banyak digunakan oleh para developer di seluruh dunia.

   - Apa fungsi dan kegunaannya? <br/>
     JavaScript digunakan untuk pengembangan aplikasi web baik front-end maupun back-end, serta untuk pengembangan aplikasi mobile dan desktop menggunakan teknologi web seperti React Native dan Electron. JavaScript juga dapat digunakan untuk pengembangan game dan aplikasi IoT (Internet of Things). Karena kemampuan JavaScript yang fleksibel, dinamis, dan mudah dipelajari, bahasa ini sangat populer dan banyak digunakan oleh para developer di seluruh dunia.
   - Apa kelebihan daripada bahasa pemrograman yang lain? <br/>
     JavaScript memiliki beberapa kelebihan dibandingkan bahasa pemrograman lainnya, di antaranya:<br/>
     - Dapat digunakan di sisi klien dan sisi server <br/> JavaScript dapat digunakan untuk mengembangkan aplikasi di sisi klien (browser) maupun di sisi server (Node.js), sehingga memungkinkan pengembangan aplikasi end-to-end.
     - Mudah dipelajari <br/> JavaScript memiliki sintaks yang mudah dipahami dan mudah dipelajari bagi pemula. Selain itu, ada banyak sumber daya dan tutorial yang tersedia secara online untuk mempelajari JavaScript.
     - Populer dan banyak digunakan <br/> JavaScript merupakan salah satu bahasa pemrograman paling populer dan banyak digunakan di dunia. Hal ini membuat banyaknya komunitas dan dukungan dari pengembang dan perusahaan teknologi.
     - Fleksibel <br/> JavaScript dapat digunakan untuk mengembangkan berbagai jenis aplikasi, seperti web, mobile, desktop, game, dan sebagainya. Selain itu, JavaScript juga mendukung banyak paradigma pemrograman, seperti prosedural, objek, dan fungsional.
     - Interaktif <br/> JavaScript dapat memberikan interaksi yang lebih baik pada aplikasi web, seperti validasi form, efek animasi, manipulasi DOM, dan lain-lain. Hal ini membuat aplikasi menjadi lebih menarik dan interaktif bagi pengguna.

2. Tipe deklarasi variabel

   - Var <br/> Merupakan tipe deklarasi variabel pada JavaScript yang digunakan untuk mendeklarasikan sebuah variabel dengan functional scope. Artinya, variabel yang dideklarasikan dengan var hanya dapat diakses di dalam function tempat variabel tersebut dideklarasikan. Var tidak memiliki fitur block-level scope seperti halnya let dan const. Variabel yang dideklarasikan dengan var juga dapat diubah nilainya setelah dideklarasikan.

     Tipe deklarasi var ini dianggap tidak relevan lagi untuk digunakan karena terdapat beberapa kelemahan:

     - Functional Scope <br/> Variabel yang dideklarasikan menggunakan var hanya memiliki scope pada fungsi tempat ia dideklarasikan. Ini berarti variabel tersebut dapat diakses dan dimodifikasi di dalam fungsi tempat ia dideklarasikan, serta di dalam fungsi yang bersarang di dalamnya. Namun, variabel tersebut tidak dapat diakses di luar fungsi tempat ia dideklarasikan.

       ```
       function example() {
       var message = "Hello World!";
       console.log(message); // Output: Hello World!
       }

       example();
       console.log(message); // Output: Uncaught ReferenceError: message is not defined
       ```

     - Hoisting: Variabel yang dideklarasikan menggunakan var akan mengalami hoisting, yaitu proses pemindahan deklarasi variabel ke atas scope saat runtime. Ini berarti variabel tersebut dapat diakses sebelum dideklarasikan secara eksplisit, meskipun nilainya masih undefined.

       ```
       console.log(message); // Output: undefined
       var message = "Hello World!";
       ```

     - Dapat Dideklarasikan Ulang <br/> Variabel yang dideklarasikan menggunakan var dapat dideklarasikan ulang dalam scope yang sama tanpa memunculkan pesan kesalahan. Ini berarti nilai dari variabel tersebut dapat ditimpa dengan nilai yang baru.

     ```
     var message = "Hello World!";
     var message = "Hi there!";
     console.log(message); // Output: Hi there!
     ```

     - Tidak Aman untuk Pengembangan Besar <br/> Dalam pengembangan perangkat lunak yang besar dan kompleks, penggunaan variabel var dapat memunculkan banyak masalah, seperti variabel yang tidak sengaja ditimpa, atau variabel yang diakses di luar scope yang dimaksudkan. Oleh karena itu, sebaiknya digunakan tipe deklarasi variabel yang lebih aman, seperti let atau const.

   <i>Functional scope dan block scope adalah dua konsep yang berhubungan dengan ruang lingkup variabel dalam JavaScript.

Functional scope merupakan ruang lingkup dimana variabel hanya dapat diakses di dalam fungsi di mana variabel itu dideklarasikan. Variabel yang dideklarasikan di luar fungsi tidak dapat diakses di dalam fungsi tersebut. Ini berarti bahwa variabel hanya memiliki ruang lingkup di dalam fungsi tempat variabel dideklarasikan.

Sementara itu, block scope berarti bahwa variabel hanya dapat diakses di dalam blok kode tertentu, seperti di dalam blok if atau loop. Variabel yang dideklarasikan di luar blok kode tidak dapat diakses di dalam blok kode tersebut. Ini berarti bahwa variabel hanya memiliki ruang lingkup di dalam blok kode tempat variabel dideklarasikan.

Perbedaan utama antara functional scope dan block scope adalah bahwa variabel dengan functional scope hanya memiliki ruang lingkup di dalam fungsi tempat variabel dideklarasikan, sedangkan variabel dengan block scope hanya memiliki ruang lingkup di dalam blok kode tempat variabel dideklarasikan.

Block code adalah kumpulan dari satu atau beberapa statement kode yang dikelompokkan bersama dalam satu blok, biasanya diawali dengan tanda kurung kurawal { dan diakhiri dengan tanda kurung kurawal yang sama }. </i>

- Let <br/> Adalah tipe deklarasi variabel yang digunakan untuk mendeklarasikan variabel dengan block scope, sehingga variabel hanya dapat diakses di dalam blok kode tempat mereka dideklarasikan atau dalam blok kode bersarang. Variabel let bersifat mutable, artinya nilainya dapat diubah setelah dideklarasikan.

- Const <br/> Merupakan tipe deklarasi variabel yang digunakan untuk membuat variabel dengan nilai yang tetap atau konstan dan nilainya tidak dapat diubah setelah dideklarasikan. Const juga bersifat block scoped, artinya hanya dapat diakses di dalam blok kode tempat variabel itu dideklarasikan atau di dalam blok yang bersarang di dalamnya.

3.  Operator di JavaScript
    Ada beberapa jenis operator di dalam JavaScript, yaitu:

    - Operator Aritmatika <br/> Operator ini digunakan untuk melakukan operasi matematika, seperti penjumlahan (+), pengurangan (-), perkalian (\*), pembagian (/), modulus (%), dan sebagainya.
    - Operator Perbandingan <br/> Operator ini digunakan untuk membandingkan dua nilai atau variabel, seperti sama dengan (==), tidak sama dengan (!=), lebih besar (>), lebih kecil (<), lebih besar atau sama dengan (>=), dan lebih kecil atau sama dengan (<=).
    - Operator Logika <br/> Operator ini digunakan untuk mengkombinasikan nilai boolean, yaitu true atau false, seperti AND (&&), OR (||), dan NOT (!).
    - Operator Penugasan <br/> Operator ini digunakan untuk menetapkan nilai ke dalam sebuah variabel, seperti penugasan sederhana (=), penugasan tambah (+=), penugasan kurang (-=), penugasan kali (\*=), penugasan bagi (/=), dan sebagainya.
    - Operator Bitwise <br/> Operator ini digunakan untuk melakukan operasi bit pada nilai atau variabel, seperti AND (&), OR (|), XOR (^), left shift (<<), right shift (>>), dan unsigned right shift (>>>).

4.  Bahasa javascript merupakan statically-typed atau dynamic-typed language? <br>
    JavaScript merupakan dynamically-typed language. Artinya, tipe data dari suatu variabel dapat berubah-ubah selama program dijalankan tanpa harus didefinisikan sebelumnya

    - Apa perbedaan statically-typed atau dynamic-typed language? <br/>
      Statically-typed language adalah bahasa pemrograman yang membutuhkan tipe data variabel ditentukan secara eksplisit dan dideklarasikan sebelum digunakan contohnya Java, C++, dan Go. Sementara dynamic-typed language adalah bahasa pemrograman yang tidak membutuhkan tipe data variabel ditentukan secara eksplisit, variabel bisa langsung dideklarasikan dan tipe datanya akan ditentukan secara otomatis pada saat runtime, contohnya JavaScript, Python, dan Ruby. Dalam statically-typed language, kesalahan tipe data akan ditemukan pada saat kompilasi sedangkan pada dynamic-typed language kesalahan tipe data akan ditemukan saat runtime.

5.  Bahasa JavaScript merupakan compiled language atau scripting language? <br>
    Bahasa JavaScript merupakan sebuah scripting language.

    - Apa perbedaan compiled dan scripting? <br/>
      Compiled language adalah bahasa pemrograman yang memerlukan proses kompilasi terlebih dahulu sebelum bisa dijalankan. Proses kompilasi ini mengubah kode sumber menjadi kode mesin yang dapat dieksekusi oleh komputer. Contoh dari bahasa pemrograman compiled language adalah C, C++, dan Java.

      Sementara itu, scripting language adalah bahasa pemrograman yang tidak memerlukan proses kompilasi terlebih dahulu dan dapat dijalankan secara langsung oleh interpreter pada waktu runtime. Contoh dari bahasa pemrograman scripting language adalah JavaScript, Python, dan Ruby.

      Perbedaan utama antara compiled language dan scripting language terletak pada proses kompilasi. Pada compiled language, proses kompilasi memerlukan waktu untuk menghasilkan kode mesin yang dapat dieksekusi oleh komputer, sedangkan pada scripting language tidak memerlukan proses kompilasi dan langsung dieksekusi oleh interpreter pada saat runtime. Selain itu, compiled language lebih cepat dalam eksekusi kode dibandingkan dengan scripting language, karena telah dikompilasi ke dalam kode mesin yang langsung dapat dieksekusi. Namun, scripting language lebih mudah dalam penggunaannya dan lebih fleksibel karena tidak perlu proses kompilasi terlebih dahulu.

    - Apa perbedaan bahasa JavaScript dengan bahasa lain (seperti php/javascript/golang)?
      Bahasa JavaScript memiliki perbedaan dengan bahasa pemrograman lainnya, seperti PHP, Golang, dan lain-lain. Beberapa perbedaan yang dapat dilihat antara bahasa JavaScript dengan bahasa pemrograman lainnya antara lain:
      - Jenis Bahasa Pemrograman<br/> Bahasa JavaScript adalah bahasa pemrograman yang dijalankan di sisi klien (client-side) dan di sisi server (server-side), sedangkan PHP dan Golang hanya berjalan di sisi server.
      - Tipe Data<br/> Bahasa JavaScript adalah bahasa pemrograman yang memiliki tipe data dinamis, sedangkan PHP dan Golang adalah bahasa pemrograman yang memiliki tipe data statis.
      - Skema Pemrograman<br/> Bahasa JavaScript lebih mengutamakan pemrograman berorientasi objek (OOP), sedangkan PHP lebih menggunakan skema pemrograman procedural dan OOP, sedangkan Golang lebih mengutamakan pemrograman konkuransi.
      - Framework<br/> Bahasa JavaScript memiliki banyak framework seperti React, Vue, Angular dan Node.js yang populer dalam pengembangan aplikasi web, sedangkan PHP memiliki banyak framework seperti Laravel, CodeIgniter, dan Golang memiliki Beego, Gin, dan Revel.
      - Pemakaian<br/> Bahasa JavaScript digunakan untuk membangun aplikasi web, mengembangkan aplikasi mobile, dan juga dapat digunakan untuk membuat game. Sedangkan PHP digunakan untuk membangun aplikasi web dinamis, sementara Golang digunakan untuk mengembangkan aplikasi berbasis cloud dan sistem backend.

6.  Dalam bahasa pemrograman JavaScript terdapat tipe data apa saja? Jelaskan masing-masing tipe data tersebut!

    Secara garis besar tipe data terdiri dari dua jenis yaitu tipe data primitif dan non primitif atau object
    Tipe data primitif adalah adalah tipe data sederhana yang hanya memiliki sebuah value dan tidak memiliki property maupun method. Tipe data primitif terdiri dari: <br/>

    Secara garis besar tipe data terdiri dari dua jenis yaitu tipe data primitif dan non primitif atau object

    - Tipe data primitif adalah adalah tipe data sederhana yang hanya memiliki sebuah value dan tidak memiliki property maupun method.

      - Number <br/>
        Tipe data yang mewakili angka, bisa berupa bilangan positif, negatif, integer maupun angka desimal.
      - String <br/>
        Tipe data yang digunakan untuk mewakili data tekstual atau karakter.
      - Boolean <br/>
        Tipe data yang hanya memiliki dua nilai, true dan false.
      - Undefined <br/>
        Tipe data untuk menggambarkan kondisi ketika variabel dideklarasikan tanpa inisialisasi atau tidak diberi nilai
      - Null <br/>
        Tipe data untuk menunjukkan bahwa suatu variabel saat ini tidak memiliki nilai apa pun atau kosong.

    - Tipe non-primitif/object adalah adalah tipe data yang bisa berisi lebih dari satu value dengan tipe data yang berbeda - beda.
      - Array <br/>
        Tipe data yang bisa berisi lebih dari satu nilai dengan tipe data yang beragam dan setiap nilai yang tersimpan di dalam array ini memiliki ‘nomor urut’ yang dikenal dengan istilah index, dimulai dari 0.
      - object <br/>  
        Tipe data yang kompleks yang memungkinkan kita menyimpan lebih dari satu nilai dengan tipe data yang berbeda dalam bentuk pasangan key dan value.
      - function <br>
        Merupakan block code yang dapat dipanggil atau digunakan berkali - kali untuk mengeksekusi perintah tertentu
