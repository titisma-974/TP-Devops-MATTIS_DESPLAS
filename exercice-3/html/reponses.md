EXERCICE 3 :
3.2 : On remarque que le texte change en direct 
3.4 : commandes utilisé : 
	- docker run -it --rm -v mes-donnees:/data alpine sh
	- echo "je survis" > /data/persistant.txt
	- exit 
3.5 : commandes utilisé : 
	- docker run -it --rm -v mes-donnees:/data alpine sh
	- ls /data 
	- cat /data/persistant.txt
Le fichier /data/persistant existe toujours, cela démontre qu'il est possible de stocker des données via docker sans que cela soit volatile.

3.6 : commande utilisé : 
	- docker volume inspect mes-donnees
Grâce a cette commande on peut voir que le "Mountpoint" est : /var/lib/docker/volumes/

3.7 : Commandes utilisés : 
	- docker ps -a 
	- docker volume rm mes-donnes 
La précaution a avoir avant de supprimer un volume est de vérifier qu'il n'est pas encore monté/utilisé par un conteneur et il faut aussi vérfier qu'il ne faut pas faire de backup.
