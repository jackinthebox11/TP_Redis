# TP_Redis

##Quelles sont les types de données stockés dans Redis, que peut on faire comme types de requêtes ?

###Definition :
est un système de gestion de base de données clef-valeur scalable, très hautes performances, écrit avec le langage de programmation C ANSI et distribué sous licence BSD. Il fait partie de la mouvance NoSQL et vise à fournir les performances les plus élevées possibles.

###Les types de données :
Redis permet de manipuler des types de données simples : chaînes de caractères, tableaux associatifs, listes, ensembles et ensembles ordonnés.


###Les types de requetes :
Il est impossible de requêter les valeurs comme on le fait habituellement avec un WHERE en MySQL.

* C'est le type le plus simple : à une clef, on peut y associer une valeur : Les principales commandes associées sont SET, GET, INCR, DECR, et GETSET.
* Les listes de redis sont des listes liées : Les principales commandes commencent en général par L comme List et sont RPUSH et LPUSH, LRANGE, LINDEX, LLEN.
* Une hash permet de stocker dans un même enregistrement plusieurs couples de clef/valeurs : On y trouve HSET, HGET, HLEN, mais aussi HGETALL pour obtenir tous les couples clef-valeur, HINCRBY pour incrémenter un compteur dans la hash, HKEYS et HVALS pour obtenir toutes les clefs ou valeurs et HDEL pour faire le ménage.
* Les Sets sont des collections d'objets non ordonnées : Les commandes commencent toutes avec un S comme Set, parmi celles-ci on trouve SADD pour ajouter une valeur à un set, SCARD pour obtenir la taille d'un set, et surtout les commandes SINTER, SUNION, SDIFF qui permettent respectivement d'obtenir l'intersection, l'union et la différences entre 2 sets.
* 