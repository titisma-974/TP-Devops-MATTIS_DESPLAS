EXERCICE 4 :

4.1 - Commande utilisé  docker network ls. 
Les 3 réseaux par défaut sont bridge, host et none.

4.2 - Commande utilisé : docker network create --driver bridge mon-reseau

4.3 - Commande utilisé : docker run -d --name serveur-web --network mon-reseau nginx:alpine

4.4 - Grâce à la commande : wget -qO- http://serveur-web on récupère la page d'accueil de Nginx, on peut voir qu'il y a une résolution DNS car Docker embarque un serveur DNS pour les réseaux personnalisés.

4.5 - L'accès échoue car ils ne sont pas sur le même réseau personalisé, la résolution DNS ne fonctionne pas le wget -qO- http://serveur-web retourne l'erreur wget: bad address 'serveur-web'

4.6 - Commande utilisé : docker network connect mon-reseau client-externe
