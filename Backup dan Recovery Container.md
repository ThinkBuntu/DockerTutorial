## Backup dan Recovery Container

Config ini akan menggambarkan prosedur cara membackup container Docker serta juga akan menunjukkan bagaimana merecover Docker dari data backup. Untuk memahami backup container dan recover Docker, pertama kita perlu memahami perbedaan antara *Docker Image* dan *Docker Container*. Pada docker image berisi sistem operasi dengan aplikasi mungkin satu atau lebih. Sedangkan Docker Container merupakan instance yang dibuat dari image.

### Docker Container Backup
Saat kita memerlukan backup container maka ikuti langkah - langkah berikut :
1. Tampilkan semua kontainer yang ada di docker  dengan perintah  
	`# docker ps ` 

2. Sebelum kita snapshot maka kita pause dan kita buat image dari container yang ada dari list diatas dengan perintah :  
	`# docker commit -p  id-container  nama-file-image`

3. Sekarang kita mempunyai image dari container yang kita snapshot, untuk melihat semua image tersebut bisa ditampilkan dengan perintah :  
	` # docker images`

4. Untuk menyimpan image tersebut dalam bentuk tar file, maka dengan perintah :  
	` docker save -o ~/nama-file-simpan.tar nama-file-image`


### Docker container recovery

Jika anda mempunyai tar file backup docker, maka untuk recover dengan perintah :
` # docker load -i /root/container1.tar`

cek apakah image dari tar file tersebut berhasil di recover dengan perintah :
` # docker images`

