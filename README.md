# java-Rmi-devoir1
Mise en oeuvre du service Calculator en utilisant Java RMI

![image](https://user-images.githubusercontent.com/64024996/152640435-eea9b4f6-f4f2-4e0f-a71b-b76c9a992d76.png)

L’interface Calculator définit toutes les caractéristiques
distantes offertes par le service:
  -Cette interface extends Remote, et chaque signature
  de méthode déclare qu’elle pourrait faire un throws
  d’un objet RemoteException.

Maintenant pour CalculatorrImpl:
  -La classe d’implémentation utilise
   java.rmi.server.UnicastRemoteObject pour s’attacher au système
  RMI
  
 Côté Serveur:
Les services distants RMI doivent être attachés à (hosted) un
processus serveur. La classe CalculatorServer est un très
simple serveur qui fournit l’essentiel pour le hosting de notre
service.

Une fois le service lancé, le serveur peut associer les objets qu'il
exporte à un nom public, reconnaissable par les éventuels clients.
  -L'application serveur est ensuite placée en attente de clients.
  -Le client accède le gestionnaire de registres (côté serveur) en utilisant la
   méthode static lookup() de la classe Naming pour localiser l'objet
   cherché.

Nous avons besoin de démarrer trois consoles, une pour le serveur,
la deuxième pour le client, et la dernière pour le RMIRegistry.

Générer les fichiers .class du Stub et du Skeleton à
partir des classes d’implémentation.
