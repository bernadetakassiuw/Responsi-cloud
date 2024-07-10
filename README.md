# Responsi-cloud

Bangun website data diri sederhana yang terdiri dari dua halaman di Killercoda Ubuntu Playground (Tidak usah terlalu memikirkan soal desain websitenya, yang terpenting dapat menampilkan konten dengan jelas). Gunakan Docker untuk mengelola container, image, network, dan (opsional) volume. Website data diri Anda akan terdiri dari dua halaman sederhana yang di-hosting di container terpisah:
1. Membuat direktori website-profil
   '''mkdir website-profil'''
2. Di dalam direktori website-profil buatkan file index.html
3. Upload file foto.jpeg ke dalam direktori website-profil
4. Membuat Docker network
   '''docker network create my-bernadeta-anselina-kassiuw-network'''
5. Membuat Dockerfile untuk website-profil
6. Ubah direktori kerja ke dalam file website-profil
   '''cd website-profil'''
7. Build dan jalankan container website-profil
   '''docker build -t website-profil .'''
8. Setelah selesai dibuild jalankan perintah
   '''docker run -d --name website-profil --network my-bernadeta-anselina 
    kassiuw-network -p 8081:80 website-profil'''
9. Hasilnya, foto profil dapat diakses melalui traffic port 8081
10. Membuat direktori file website-utama
    '''mkdir website-utama'''
11. Buat file index.html dalam direktori website-utama, pada file ini   
    tambahkan link untuk mengakses foto.jpeg
12. Buatkan Dockerfile di direktori website-utama
13. Pindahkan direktori kerja ke dalam website-utama
    '''cd website-utama'''
14. Build dan jalankan container website-utama
    '''docker build -t website-utama .'''
15. Setelah container dibuat, jalankan perintah
    '''docker run -d --name website-utama --network my-bernadeta-anselina- 
    kassiuw-network -p 8080:80 website-utama'''
16. Hasilnya, tampilan website-utama diakses melalui port 8080
17. Berikut tampilan halaman utama, terdapat data diri dan untuk mengakses foto dapat mengklik pada profil saya
    
 
