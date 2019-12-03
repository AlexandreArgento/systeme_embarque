# RPI3 : Partie 1

## Question 1 :

- Décrivez de manière plus précise l'utilité ainsi que la syntaxe de chacun des 3 fichiers mentionnés ci-dessus.

  <p>Le fichier de configuration sert à <p>
  <p>Le fichier de configuration pour busybox sert à <p>
  <p>Le fichier décrivant les utilisateurs cibles sert à <p>
<p> Les commentaires sont des lignes qui commencent par un "#" et les variables de configurations sont déclarées de 3 trois manières différentes : 
 - "NOM_DE_LA_VARIABLE = y" pour intégrer la fonctionnalité dans le noyau,
 - "NOM_DE_LA_VARIABLE = m" pour rendre la fonctionnalité disponible en tant que module, 
 - "NOM_DE_LA_VARIABLE is not set" pour ignorer sa configuration.

## Question 2 :
<p>En réalisant un ls dans le config on voit le fichier raspberrypi3_defconfig? C'est donc le fichier de configuration buildroot qui permet de configurer la raspberrypi 3 avec un os 32 bits.<p>

## Question 3 :
<p>Packages contient l'ensemble des packages que l'on peut compiler lors de la phae de compilation<p>

## Question  4 : 
<p>La commande make embsys_defconfig permet de configurer le kernel avec avec seulement les packages utiles pour l'embarqué. On diminue ainsi l'espace mémoire nécessaire pour stocker tous ces packages. <p>

## Question  5 : 
<p> L'archietcture matértielle cible est ARM(little endian) <p>
<p> Le CPU ciblé est <p>
<p> L'ABI ciblé est EABIhf <p>
<p> La librairie C utilisée est uClibc-ng  <p>
<p> La version du cross compilateur utilisée est gcc 6.x  <p>
<p> La version du kernel utilisée est Custom Git repository <p>

## Question  6 :
<p> Via l'interface Buildroot, on peut voir que le protocole ssh fait partie des commandes disponibles. En allant voir dans le fichier de configuration embsys_defconfig, la ligne "BR2_ACKAGE_OPENSSH=y" apparaît, ce qui nous permet de penser que le paquet openssh sera compilé et disponible dans l'OS cible. <p> 
