## Adjust memory and swap accounting
Saat kita menjalankan Docker, sering muncul peringatan :
  
`WARNING: Your kernel does not support cgroup swap limit. WARNING: Your kernel does not support swap limit capabilities. Limitation discarded. `

Untuk memperbaiki ini, aktifkan memory dan swap accounting di systems. Untuk mengaktifkannya gunakan GNU GRUB (GNU GRand Unified Bootloader), dengan perintah :
1. Login ke user Root
2. Edit file `/etc/default/grub`
3. Ubah nilai `GRUB_CMDLINE_LINUX` menjadi :  
	` GRUB_CMDLINE_LINUX="cgroup_enable=memory swapaccount=1" `
4. Save dan Close.
5. Update GRUB dengan perintah :  
	` $ sudo update-grub `
6. Reboot Server   

	  
