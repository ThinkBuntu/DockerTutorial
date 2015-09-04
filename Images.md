## Images
1. Delete dulu container yang jalan  
	`$ docker ps -q -a | xargs docker rm
	`
2. Untuk men-Delete image yang gak kepakai   
	`$ docker rmi $(docker images | grep “^<none>” | awk ‘{print $3}’)`