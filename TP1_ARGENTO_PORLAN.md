# TP 1 : Partie 1

## Question 1 :

- Qu'est ce qu'un Makefile?
  <p>Makefile permet d'automatiser l'exécution de commandes terminales. Il vérifie que les cibles soient à jour avant d'éxécuter les instructions données.<p>
  
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


# Partie 2 :

## Question 1 :

<p>$ sh run.sh<p>
<p>PTTY: /dev/pts/X<p>
  
- Cette commande permet
<p> Au bout de quelques secondes nous avons un message d'erreur : "segmentation fault" qui veut dire que le programme pointe vers une case mémoire non attribuée.<p>
  
## Question 2 : Quel signal a reçu le processus pour se terminer ainsi? Comment vérifiez vous le numéro du signal reçu?

<p> En activant la génération d'un fichier core et à l'aide de gdb on obtient le nom du signal responsable de l'erreur. Ici c'est SIGSEGV <p>
  
## Question 3 : Grâce à GDB et au fichier core généré, analysez la source du problème du binaire gps. Quelle partie du code est fausse? Pourquoi?

<p>La commande run essaye d'appeler une librairie partagée "libptmx.so" qui n'existe pas dans le dossier gps. "No such file or directory".<p>
  
