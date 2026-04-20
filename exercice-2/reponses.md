EXERCICE 1 :

1.2 : la commande est run -d --name -mon-nginx -p 8080:80 nginx:alpine
1.3 : La commande est docker ps
1.4 : On voit la page d'accueil de NGINX "Welcome to nginx!"
1.5 : docker logs [ID]
1.6 : La commande est docker ps -a, elle liste même les conteneur arrêté
1.7 : docker rm [ID]
1.8 docker run -d --name mon-nginx -p 8080:80 --rm nginx:alpine

EXERCICE 2 :
 
2.4 docker run -d --name mon-site --rm -p 9090:80 mon-site:v1
2.5 Commande pour lister les images : docker images 
2.6 Commande utilisé : docker history mon-site:v1
On peut voir que deux layers ont été ajouté mais seul de layeur de COPY index.html "pèse" quelque chose
2.7 Les étapes "CREATED" il y a 4 jours sont des étapes liées au cache, celles qui datent d'il y a 58 secondes sont des étapes réexécutées.
2.8 Commande utilisé pour supprimer mon-site:V1 --> docker rmi mon-site:v1

EXERCIE 3 :

3.1 le fichier n'existe plus car les conteneurs sont éphémères, tout ce qui est créer avec le conteneur sera supprimé en même temps que le conteneur, avec l'option --rm tout a été supprimé. Chaque nouveau conteneur sera comme "neuf".
