# TP 1 : Partie 1

## Question 1 :

- Qu'est ce qu'un Makefile?
  <p>Makefile permet d'automatiser l'exécution de commandes terminales. Il vérifie que les cibles sont à jour avant d'éxécuter les instructions données.<p>
  
- À quoi sert make?
  <p>make permet de lancer le makefile du dossier courant. On peut voir à l'intérieur du makefile donné qu'il appelle d'autre makefile situées dans d'autres dossiers en se déplacant à l'intérieur du fichier (commande cd) et en éxécutant le nouveau makefile du dossier associé (&& make).<p>
  
## Question 2 :
  
- Quel compilateur est utilisé ici?
  <p>Comme on peut le voir dans le makefile du dossier gps/src/lib/ptmx, à la ligne 2 on définit le compilateur qui est gcc et il est appelé à la ligne 5.<p>
  
## Question 3 :

- Qu'est ce qu'une librairie partagée ?
<p>Une librairie partagée n'est chargée que lorsqu'elle est appelée par un programme. Cela permet d'économiser en mémoire et de ne pas surcharger la mémoire avec des librairies inutilisées. <p>

## Question 4 :
- Donnez un exemple de fichier C et la ligne de commande correspondante pour obtenir un binaire exécutable (un hello world par exemple).

<p>Pour obtenir un binaire exécutable du fichier hello_world.c on peut écrire la ligne de code suivante dans la ligne de commande : <p>
<p>gcc hello_world.c -o hello_world.o<p>
  
 
## question 5 :
