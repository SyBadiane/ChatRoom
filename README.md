# ChatRoom
Réaliser dans le cadre d'un tp de classe(Fonctionnel mais reste à être améliorer n'hésitez pas ;) ).

C'est un système de gestion de services dans un environnement large-échelle
Des utilisateurs se trouvant sur Internet envoient des requêtes à un serveur qui réalise des traitements en s’appuyant sur d’autres serveurs qui lui sont accessibles (ils sont dans le même réseau que lui) avant de renvoyer une réponse.

Il comprend: 
  2 types de client (L'un développé en JAVA et l'autre en PHP)
  1 SERVEUR PRINCIPAL (aiguilleur nommé messenger developpé en JAVA avec la techonologie REST)
  3 SERVEUR SECONDAIRE (machines 1, 2 et 3 developpées en JAVA avec la techonologie XMLRPC)

Les clients vont faire appel au SP via un Web Service (De type REST).
Les échanges entre le SP et les SS se feront via XML-RPC.

En gros : 
1. Les utilisateurs soumettent des requêtes à un répartiteur de charge (SP).
2. Pour chaque requête, le SP choisit de la rediriger vers une et une seule machine.
3. La machine choisie traite la requête, fournit le résultat à l'aiguilleur qui le retransmet à l'utilisateur.
4. Pendant le temps de traitement de la requête, le SP peut aiguiller une nouvelle requête vers une autre machine ou vers la même machine.

NB: 
Noubliez pas d'importer les jar qui se trouvent dans le dossier lib des projets (Messenger et SS-Salon1).
Messenger et ChatClient Java sont des projets maven. 

#END!
