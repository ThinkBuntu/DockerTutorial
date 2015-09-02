## Install
1. Check Tipe dari Ubuntu Server
	` $ uname -r  `  
	  
	maka Anda akan mendapat data versi dari ubuntu yang Anda gunakan. Yaitu :  
	•	Ubuntu Vivid 15.04
	•	Ubuntu Trusty 14.04 (LTS)
	•	Ubuntu Precise 12.04 (LTS)
	•	Ubuntu Saucy 13.10
	 
2. Update repository server :  
	` $ sudo apt-get update `  

3. Jika Anda menggunakan server Ubuntu Trusty 14.04 maka install required dan optional packages. dengan perintah :  
	` $ sudo apt-get install linux-image-generic-lts-trusty `  

4. Reboot server Anda :  
	` sudo reboot `

5. Login dengan user root
6. Pastikan server Anda ada * curl *  
	` $ which curl `  
	  
	Jika belum ada curl install dengan perintah :  
	` $ sudo apt-get install curl `  
	 
7. Install docker terbaru   
	` $ curl -sSL https://get.docker.com/ | sh `  
	Jika di server Anda ada filter proxy, maka tambahkan key dengan perintah :  
	` $ curl -sSL https://get.docker.com/gpg | sudo apt-key add - `  

8. Verifikasi installasi docker  
	` $ sudo docker run hello-world `  

9. DONE

