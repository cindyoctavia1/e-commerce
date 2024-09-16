link pws: https://cindy-octavia-ecommerce.pbp.cs.ui.ac.id/

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


