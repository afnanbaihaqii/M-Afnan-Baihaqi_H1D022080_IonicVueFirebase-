Nama : M Afnan Baihaqi 
Nim : H1D022080
Shift : B 

### ScreenShot

![Screenshot 2024-11-14 212913](https://github.com/user-attachments/assets/91863c90-17d2-4b99-8d4f-b285cf143689)
![Screenshot 2024-11-14 213015](https://github.com/user-attachments/assets/c4e92799-30af-4cb4-8717-746b6e2c6bc4)
![Screenshot 2024-11-14 213058](https://github.com/user-attachments/assets/1b78d9e5-f9ce-4b87-9e30-6218580ab24c)
![Screenshot 2024-11-14 215248](https://github.com/user-attachments/assets/9c0a1f52-3b59-4ef8-91ce-070272dd6e4f)
![Screenshot 2024-11-19 113114](https://github.com/user-attachments/assets/2244bece-0ac1-4838-b809-4b4f4b01f090)

### Penjelasan 

State utama yang digunakan adalah user, yang menyimpan data pengguna yang sedang login, serta isAuth, sebuah computed property yang mengembalikan nilai true jika user tidak null, menandakan pengguna sudah login. Fungsi loginWithGoogle bertugas menangani proses login menggunakan Google. Fungsi ini memulai dengan menginisialisasi GoogleAuth, meminta pengguna untuk login, lalu mengambil idToken yang digunakan untuk mendapatkan kredensial Firebase melalui GoogleAuthProvider. Setelah berhasil, data pengguna yang berhasil login disimpan dalam state user, dan aplikasi diarahkan ke halaman /home. Jika terjadi kesalahan selama proses login, sebuah alert akan ditampilkan menggunakan alertController dari Ionic Vue.
Selain itu, terdapat fungsi logout yang digunakan untuk keluar dari aplikasi. Fungsi ini memanggil metode signOut dari Firebase Authentication dan signOut dari GoogleAuth, kemudian mengosongkan state user dan mengarahkan pengguna ke halaman login. Store ini juga menggunakan event listener Firebase onAuthStateChanged untuk memantau perubahan status autentikasi pengguna, sehingga jika pengguna sudah login atau logout, state user diperbarui secara otomatis.

Konfigurasi ini menggunakan Firebase SDK untuk menghubungkan aplikasi dengan layanan Firebase melalui fungsi initializeApp, yang menerima objek konfigurasi (firebaseConfig). Objek konfigurasi ini berisi informasi proyek seperti apiKey, authDomain, projectId, storageBucket, dan lainnya, yang digunakan untuk mengidentifikasi dan menghubungkan aplikasi dengan proyek Firebase tertentu. Setelah inisialisasi, modul auth digunakan untuk operasi autentikasi seperti login dan logout, sementara googleProvider digunakan untuk autentikasi menggunakan akun Google. Kedua modul ini diekspor agar dapat digunakan di seluruh aplikasi. Proyek Firebase yang dikonfigurasi ini bernama vue-firebase-f4f73, dan mendukung layanan seperti Firebase Authentication dan Firebase Storage untuk mengelola data pengguna dan file.
