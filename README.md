link pws: https://cindy-octavia-ecommerce.pbp.cs.ui.ac.id/

TUGAS 2
•Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
    1.	Membuat sebuah proyek Django baru.
    Mengarahkan terminal ke direktori proyek dan menjalankan perintah :
    django-admin startproject nama_proyek

    2.	 Membuat aplikasi dengan nama main pada proyek tersebut.
    Dilanjutkan dengan menjalankan perintah berikut di terminal:
    python manage.py startapp main

    3.	Melakukan routing pada proyek agar dapat menjalankan aplikasi main.
    Menambahkan 'main' di INSTALLED_APPS pada file settings.py di folder proyek, lalu tambakan path('', include('main.urls')) pada file urls.py di folder proyek

    4.	Membuat model pada aplikasi main dengan nama Product dan memiliki atribut wajib sebagai berikut.(name,price,description).
    Buat class model Product dengan atribut name, price, dan description di file models.py di direktori main, yang bertujuan sebagai template untuk pembuatan tabel database

    5.	Membuat sebuah fungsi pada views.py untuk dikembalikan ke dalam sebuah template HTML yang menampilkan nama aplikasi serta nama dan kelas kamu.
    Membuat fungsi di views.py di direktori main yang berisi data yang akan dirender di main.html ( nama e-commerce, nama dan kelas pembuat).

    6.	 Membuat sebuah routing pada urls.py aplikasi main untuk memetakan fungsi yang telah dibuat pada views.py.
    Menambahkan kode ```urlpatterns = [
    path('', show_main, name='show_main'),
    ]```  pada file urls.py di folder main untuk menghubungkan fungsi show_main dengan url.

    7.	 Melakukan deployment ke PWS terhadap aplikasi yang sudah dibuat sehingga nantinya dapat diakses oleh teman-temanmu melalui Internet.
    Login ke akun pws dan menjalankan perintah git push pws master

•Buatlah bagan yang berisi request client ke web aplikasi berbasis Django beserta responnya dan jelaskan pada bagan tersebut kaitan antara urls.py, views.py, models.py, dan berkas html.
link canva: https://www.canva.com/design/DAGQW0gfSIw/2mKEYCzSL_-RupFMqSdYvQ/edit?utm_content=DAGQW0gfSIw&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton

•Jelaskan fungsi git dalam pengembangan perangkat lunak!
Git adalah alat yang berfungsi di komputer lokal pengembang untuk mengelola versi kode. Git berfungsi untuk memungkinkan kita berkolaborasi dengan tim untuk mengembangkan kode secara lebih terstruktur dan efisien, juga memungkinkan pengembang untuk melacak progres kodenya.

•Menurut Anda, dari semua framework yang ada, mengapa framework Django dijadikan permulaan pembelajaran pengembangan perangkat lunak?
Karena Django mengusung konsep MVT (Model-View-Template) sehingga menyebabkan kode terorganisir secara rapi dan efisien, yang akan memudahkan pemula untuk belajar pengembangan perangkat lunak. Django juga memiliki komunitas yang besar sehingga menyediakan banyak dukungan bagi pemula.

•Mengapa model pada Django disebut sebagai ORM?
Django ORM (Object-Relational Mapping) adalah bagian dari kerangka kerja Django yang bertanggung jawab untuk memetakan objek Python ke struktur basis data relasional. model pada Django disebut sebagai ORM karena Django ORM memungkinkan kita untuk berinteraksi dengan database menggunakan objek Python, tanpa perlu menulis SQL secara langsung.
Source: 
Pengantar Django ORM: Memahami dan Menggunakan Model dalam Django - Rumah Coding
Django Models: Memahami Dasar-Dasar ORM dalam Pengembangan Web | by M Ulin Nuha Abduh | Jul, 2024 | Medium

TUGAS 3

Jelaskan mengapa kita memerlukan data delivery dalam pengimplementasian sebuah platform?
Sistem data delivery berperan dalam menjamin data yang dikirimkan aman, terenkripsi, dan mematuhi peraturan yang berlaku.Data delivery juga memastikan bahwa informasi yang dibutuhkan oleh platform, pengguna, atau sistem terkait tersedia tepat waktu yang akan berdampak pada peningkatan pengalaman pengguna.

Menurutmu, mana yang lebih baik antara XML dan JSON? Mengapa JSON lebih populer dibandingkan XML?
JSON adalah format data yang cara penulisannya menggunakan objek JavaScript. JavaScript Object Notation atau yang lebih dikenal dengan JSON adalah merupakan sebuah format yang digunakan untuk menyimpan, membaca, serta menukar informasi dari web server sehingga dapat dibaca oleh para pengguna.

XML merupakan singkatan dari Extensible Markup Language yang merupakan bahasa komputer dengan tujuan menyederhanakan proses pertukaran maupun penyimpanan berbagai data.
Menurut saya, JSON lebih baik dibandingkan XML, berikut alasanya sekaligus mengapa JSON lebih populer dibanding XML:
1.	JSON lebih ringkas dan sederhana dibandingkan XML. JSON menggunakan lebih sedikit teks dan tidak memerlukan tag pembuka dan penutup yang kompleks seperti XML.
2.	JSON lebih cepat diparsing daripada XML karena struktur JSON lebih sederhana dan mendukung akses data secara langsung dalam JavaScript.
3.	JSON secara default lebih banyak didukung dalam aplikasi web dan framework modern, yang sering kali memanfaatkan JavaScript di sisi klien (client-side).
4.	JSON pada dasarnya adalah subset dari objek JavaScript, sehingga dapat dengan mudah digunakan tanpa perlu parsing tambahan di lingkungan web (JavaScript).Sedangkan XML perlu diparsing dengan lebih hati-hati menggunakan metode seperti DOM parsing atau SAX parsing, yang seringkali lebih lambat dan lebih kompleks dibandingkan parsing JSON.

Jelaskan fungsi dari method is_valid() pada form Django dan mengapa kita membutuhkan method tersebut?
Method is_valid() pada Django forms digunakan untuk melakukan validasi pada data yang dikirimkan melalui form. Method is_valid() dibutuhkan untuk memudahkan proses validasi, Menangani pesan error secara terorganisir, memastikan integritas data. Method ini memastikan bahwa hanya data yang valid yang diproses lebih lanjut oleh aplikasi, menjaga agar data yang dimasukkan pengguna tidak mengandung kesalahan atau tidak memenuhi syarat.

Mengapa kita membutuhkan csrf_token saat membuat form di Django? Apa yang dapat terjadi jika kita tidak menambahkan csrf_token pada form Django? Bagaimana hal tersebut dapat dimanfaatkan oleh penyerang?

Token CSRF adalah fitur keamanan yang melindungi aplikasi web dari serangan Pemalsuan Permintaan Lintas Situs (CSRF), yaitu jenis serangan di mana penyerang mencoba memanfaatkan sesi pengguna yang sudah terotentikasi untuk mengirimkan permintaan berbahaya tanpa sepengetahuan pengguna.. Hal ini memungkinkan  server aplikasi untuk memeriksa apakah pengiriman formulir berasal dari browser asli atau dipalsukan oleh peretas.Token CSRF adalah input formulir yang melacak sesi pengguna. Kerangka kerja aplikasi web sisi server situs web biasanya menghasilkan token CSRF untuk setiap sesi pengguna unik.  Server memeriksa apakah token sudah benar setiap kali pengguna mengirimkan formulir. Token CSRF umumnya terdiri dari string dan angka acak, sehingga nilainya tidak dapat diprediksi.
Jika kita tidak menambahkan csrf_token pada form di Django, aplikasi akan menjadi rentan terhadap serangan CSRF. Dalam serangan CSRF, penyerang dapat melakukan hal-hal berikut:
1.	Pengiriman Permintaan Berbahaya dari Situs Eksternal: Seorang penyerang dapat membuat situs berbahaya yang mengirimkan permintaan palsu ke aplikasi Django menggunakan kredensial pengguna yang sah (misalnya, pengguna yang sudah login di aplikasi). Misalnya, penyerang dapat membuat formulir palsu di situs lain yang, ketika diklik oleh pengguna, mengirimkan permintaan untuk mengubah data atau melakukan tindakan berbahaya seperti mentransfer uang atau mengubah pengaturan akun.
2.	Eksploitasi Otentikasi Pengguna: Jika pengguna sudah login di aplikasi, sesi autentikasi mereka (cookie) dapat dimanfaatkan untuk mengirimkan permintaan tanpa sepengetahuan mereka. Penyerang tidak perlu mengetahui username atau password pengguna, cukup memanfaatkan sesi yang aktif di browser korban untuk mengirimkan permintaan yang sah secara teknis (dari perspektif server).
Penyerang dapat memanfaatkan absennya csrf_token dalam form untuk melakukan serangan CSRF dengan langkah-langkah berikut:
1.	Membuat Formulir atau Permintaan Palsu: Penyerang membuat halaman web atau skrip yang mengirimkan permintaan HTTP POST/GET ke aplikasi Django yang berisikan data berbahaya. Misalnya, formulir yang mengubah kata sandi akun atau melakukan transaksi tanpa sepengetahuan pengguna.
2.	Memancing Pengguna untuk Membuka Halaman Palsu: Pengguna diarahkan untuk mengunjungi halaman web penyerang (misalnya, melalui email phishing atau link berbahaya). Jika pengguna membuka halaman tersebut saat mereka sedang login ke aplikasi Django yang ditargetkan, formulir di halaman web penyerang akan mengirimkan permintaan menggunakan kredensial sesi yang valid.
3.	Permintaan Berbahaya Dijalankan oleh Server: Jika aplikasi Django tidak memverifikasi token CSRF, server akan memproses permintaan tersebut karena terlihat seperti berasal dari pengguna yang sah. Server akan menggunakan cookie otentikasi yang valid milik pengguna, sehingga permintaan tampak seperti berasal dari pengguna asli.
4.	Serangan Berhasil: Penyerang bisa mengubah informasi sensitif, melakukan tindakan seperti penghapusan data, mengubah preferensi akun, atau bahkan membuat transaksi keuangan tanpa sepengetahuan korban.

Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas secara step-by-step (bukan hanya sekadar mengikuti tutorial)
Membuat input form untuk menambahkan objek model pada app sebelumnya.
-Kita akan membuat berkas baru pada direktori main dengan nama forms.py untuk membuat struktur form yang dapat menerima Product Entry baru. Field dari model ProductEntry yang digunakan untuk form adalah name, price dan description. Lalu menambahkan import redirect pada views.py. Membuat fungsi baru dengan nama create_product_entry yang buat berisi form yang memasukkan memasukkan QueryDict berdasarkan input dari user pada request.POST. dan memvalidasi serta menyimpan input data dari form dan melakukan redirect ke fungsi show_main pada views aplikasi main setelah data form berhasil disimpan. Lalu ubah fungsi show_main untuk menampilkan objek Product yang sudah tersimpan di database. Lalu masukkan import dan path url dari fungsi create_product_entry. Buat berkas create_product_entry.html untuk menambahkan product baru.Lalu tambahkan kode untuk menampilkan product dalam bentuk tabel dan sebuah button yang akan dihubungkan ke form di main.html.

Tambahkan 4 fungsi views baru untuk melihat objek yang sudah ditambahkan dalam format XML, JSON, XML by ID, dan JSON by ID.
-Kita akan membuat 4 fungsi di views.py di folder main yaitu show_xml, shows_json, show_xml_by_id, dan show_json_by_id yang menerima parameter request dan mengembalikan semua object dari Product/objek tertentu dari Product berdasarkan id, yang lalu akan di translate ke format yg diinginkan melalui serializers.

Membuat routing URL untuk masing-masing views yang telah ditambahkan pada poin 2.
-Masukkan import di urls.py di foler main yang berisi nama ke 4 fungsi yang sudah dibuat tadi dan tambahkan path URL ke dalam urlpatterns untuk mengakses fungsi yang sudah diimpor tadi.

![alt text]("C:\Users\Cindy\OneDrive\Pictures\Screenshots\Screenshot 2024-09-16 204951.png"?raw=true)
Source:
https://www.localstartupfest.id/faq/perbedaan-xml-dan-json/
https://id.linux-console.net/?p=28432#gsc.tab=0
