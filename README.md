-------------------------------------INSTALLATION APACHE2------------------------------------------------

-Télécharger apache2 sur son site officiel: https://httpd.apache.org/download.cgi
-Décompresser et désarchiver simultanément httpd-2.4.59.tar.gz
	:~$tar -xzf httpd-2.4.59.tar.gz
-Entrez dans le répertoire après la décompression : httpd-2.4.59
	:~$cd httpd-2.4.59
-Avant d’exécuter le fichier configuration, il faut :
	-Installer les dépendances suivants :
	:~$sudo apt-get install build-essential libssl-dev libexpat-dev libpcre3-dev libapr1-dev libaprutil1-dev
	-Executer maintenant le fichier configure:
	:~$./configure –-prefix=/usr/local/apache2
-Lancer la commande make :
	:~$make
-installer installer les fichiers binaires, les bibliothèques, les en-têtes et d'autres ressources d’apache2 dans leurs emplacements finaux sur le système à l’aide du commande :
	:~$sudo make install
