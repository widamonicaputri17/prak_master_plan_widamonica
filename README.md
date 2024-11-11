# Wida Monica Putri
# 362358302008

# Tugas Praktkum 1  :Dasar State dengan Model View
# 2. 
Langkah 4 adalah pembuatan data_layer.dart, yang mengekspor task.dart dan plan.dart. Langkah ini menyederhanakan impor mendatang karena menggabungkan model-model ini ke dalam satu titik akses. 
# 3.
Variabel plan pada Langkah 6 mewakili model data utama untuk menyimpan tugas. 
# 4. 
![Screenshot 2024-11-11 092710](https://github.com/user-attachments/assets/74550e5e-6264-4a5c-a767-814c59e7695d)
![Screenshot 2024-11-11 093230](https://github.com/user-attachments/assets/a31ada8b-e7d2-406a-86bb-fe9e2159feaf)
Pada Langkah 9 , _buildTaskTilewidget dibuat, yang menampilkan setiap tugas dengan kotak centang (untuk status penyelesaian) dan kolom teks (untuk mengedit deskripsi). 
Penjelasan: Bagian UI ini memungkinkan pengguna berinteraksi langsung dengan tugas individual, memungkinkan mereka menandai tugas sebagai selesai atau mengubah deskripsi.
# 5.
Langkah 11 (Scroll Listener di initState) : Menambahkan scroll listener untuk menghilangkan fokus dari keyboard saat menggulir, yang meningkatkan pengalaman pengguna dengan menyembunyikan keyboard secara otomatis selama pengguliran.
Langkah 13 ( disposemetode) : menghindari kebocoran memori dan menjaga manajemen sumber daya tetap efisien.


# Tugas Praktikum 2:  Mengelola Data Layer
# 2.
InheritedWidget adalah jenis widget Flutter yang digunakan untuk berbagi data secara efisien. Dalam praktikum ini, InheritedNotifier merupakan subkelas dari InheritedWidget yang digunakan karena menyediakan fungsionalitas tambahan dari ValueNotifier, yang secara otomatis memperbarui widget yang bergantung pada datanya.
# 3.
Metode pada Langkah 3 ( completedCountdan completenessMessage) ditambahkan untuk menghitung dan menampilkan kemajuan penyelesaian tugas.
completedCountmenghitung berapa banyak tugas yang ditandai sebagai selesai.
# 4.
![Screenshot 2024-11-11 102748](https://github.com/user-attachments/assets/2b7e372c-ac46-403a-9ad6-9b5546e7cea0)
# 1.
Judul Header (Master Plan Wida) : Judul "Master Plan Wida" di bagian atas adalah nama keseluruhan daftar tugas, diberi gaya latar belakang hijau cerah agar menonjol.
# 2. 
Daftar Tugas dengan Kotak Centang : Bagian utama menampilkan daftar tugas, masing-masing dengan kotak centang. Kotak yang dicentang menunjukkan tugas yang telah selesai, sedangkan kotak yang tidak dicentang menunjukkan tugas yang masih tertunda. Ini memberikan perbedaan visual yang jelas antara tugas yang telah selesai dan tugas yang belum selesai.
# 3.
Tampilan Kemajuan : Di bagian bawah, pesan "3 dari 22 tugas" menunjukkan kepada pengguna berapa banyak tugas yang telah diselesaikan dari total tugas. 
# 4.
Tombol Tindakan Mengambang (FAB) : Tombol "+" hijau di kanan bawah biasanya merupakan "Tombol Tindakan Mengambang" (FAB) di Flutter, yang sering digunakan untuk menambahkan item baru. Dalam kasus ini, mengkliknya kemungkinan akan memungkinkan pengguna untuk menambahkan tugas baru ke dalam daftar.



#Tugas Praktikum 3 : State di Multiple Screen
# 2. Menjelaskan gambar diagram
Gambar di atas menunjukkan diagram hierarki widget dalam aplikasi Flutter, khususnya tentang bagaimana tampilan berpindah dari satu layar ke layar lain menggunakan Navigator.push. Berikut penjelasan dari masing-masing bagian:

# 1. Hierarki di Kiri (Sebelum Navigator Push):
Pada hierarki awal, aplikasi menggunakan MaterialApp sebagai widget utama, yang membungkus PlanProvider dan PlanCreatorScreen.
Di dalam PlanCreatorScreen, terdapat struktur Column yang berisi dua widget utama: TextField dan Expanded.
Expanded kemudian membungkus ListView, yang berfungsi untuk menampilkan daftar item.
# 2. Hierarki di Kanan (Setelah Navigator Push):
Setelah pengguna melakukan navigasi ke layar baru dengan Navigator.push, tampilan berpindah ke PlanScreen.
Di dalam PlanScreen, struktur widget baru ditampilkan, diawali dengan Scaffold sebagai pembungkus utama.
Di dalam Scaffold, terdapat struktur Column yang berisi widget Expanded, SafeArea, ListView, dan Text.
## SafeArea digunakan untuk menghindari overlap dengan area tertentu pada layar (seperti status bar atau notch), sementara Expanded membungkus ListView, seperti pada hierarki awal, tetapi kali ini terdapat tambahan widget Text.
## Secara keseluruhan, diagram ini menggambarkan proses navigasi dari satu layar ke layar lainnya dalam aplikasi Flutter, di mana layar baru memiliki struktur widget yang berbeda, meskipun beberapa elemen, seperti ListView, tetap ada dalam kedua layar.
# 3. Hasil setelah langkah 14
# gambar 1 :
![Screenshot 2024-11-11 122053](https://github.com/user-attachments/assets/4e2a1fc5-c24a-4b42-841c-b3e9f65eed84)
Ketika tidak ada rencana yang ditambahkan, aplikasi menampilkan pesan dalam bahasa Indonesia: "Anda belum memiliki rencana apapun."
Terdapat ikon dokumen sebagai ilustrasi, menekankan bahwa belum ada data rencana yang tersedia.
Tampilan ini adalah halaman kosong atau empty state yang muncul ketika pengguna belum menambahkan rencana apa pun. Dengan pesan ini, pengguna diarahkan untuk menambahkan rencana baru melalui tombol.
Secara keseluruhan, aplikasi ini memungkinkan pengguna untuk menambah, melihat, dan mengelola daftar rencana serta tugas harian mereka dengan tampilan yang sederhana dan user-friendly.
# gambar 2 :
![Screenshot 2024-11-11 123154](https://github.com/user-attachments/assets/103ea770-4ef9-4dc3-a833-934c0d149a2e)
Aplikasi menampilkan daftar "Master Plans" untuk pengguna dengan nama "Monica".
Terdapat tombol atau area input "Add a plan" untuk menambahkan rencana baru.
Di bawahnya, terdapat daftar rencana dengan tanggal tertentu, seperti "09 November 2024", "10 November 2024", dan "11 November 2024".
Setiap rencana menampilkan jumlah tugas yang sudah selesai dan total tugas, misalnya, "1 out of 1 tasks" menunjukkan bahwa ada 1 tugas dan sudah selesai.
Tampilan ini menunjukkan daftar rencana yang sudah ada beserta tugas-tugasnya. Aplikasi ini mempermudah pengguna dalam melacak rencana harian dan status penyelesaian tugas mereka.

