## Create a Docker group
Daemon docker mengikat ke soket Unix bukannya port TCP. Secara default yang socket Unix dimiliki oleh *user root* dan user lain dapat mengaksesnya dengan sudo. Untuk alasan ini, Daemon Docker selalu berjalan sebagai *root*.
Untuk menghindari harus menggunakan *sudo* ketika Anda menggunakan perintah docker, maka kita membuat grup Unix dengan nama *docker*. Ketika docker daemon berjalan, itu membuat soket Unix dapat dibaca / ditulis oleh seluruh user dalam group docker.

Untuk membuat Group Docker yaitu dengan perintah 
1. Login dengan akses root / sudo. Misalkan nama user anda saat ini adalah *thinkbuntu*
2. Buat docker group dan tambahkan user Anda  
	` $ sudo usermod -aG docker thinkbuntu `
3. Logout dan login kembali, lalu check apakah sudah bisa berjalan. 
4. Test dengan perintah  
	` $ docker run hello-world `  
	Jika muncul pesan seperti ini, maka check kembali DOCKER\_HOST environment  
	` Cannot connect to the Docker daemon. Is 'docker daemon' running on this host? `
5. 
