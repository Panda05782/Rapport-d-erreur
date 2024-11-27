# Rapport-d-erreur

Identification de l'erreur:
Dans la situation, l'utilisation des commandes ping et dig montre que le pc direction ne reçoit pas de réponse. 

Collecte de symptômes:
La commande dig sur le pc direction  montre que il y a un problème sur le serveur SOA au niveau de allow-recursion. L'utilisation de la commande ps -A, netstat -nltpu, checkzone et checkconf montre que il n'y a pas de problème au niveau de la configuration pour se connecter au autres machines

Description du problème:
Dans le fichier... de la machine SOA, le allow-recursion n'est pas bien syntaxer ceux qui fait que la machine se comporte comme un résolveur alors qui ne doit pas l'être.

Proposition de solution:
Pour résoudre ce problème, il faudra changer le paramètre de allow-recursion pour que la machine SOA ne se comporte plus comme un résolveur. Par après nous pouvons utiliser les commandes... pour vérifier si la machine fonctionne bien. Pour une double vérification, l'utilisation des machines du côté du client est éfficace pour bien observer si le problème est résolu ou non
