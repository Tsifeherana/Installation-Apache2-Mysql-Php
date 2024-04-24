# Devoir Linux
 	---------------------------INSTALLATION APACHE2------------------------------------------
	1)Télécharger apache2 sur son site officiel: https://httpd.apache.org/download.cgi
	2)Décompresser et désarchiver simultanément httpd-2.4.59.tar.gz
		tar -xzf httpd-2.4.59.tar.gz
	3)Entrez dans le répertoire après la décompression : httpd-2.4.59
		:~$cd httpd-2.4.59
	4)Avant d’exécuter le fichier configuration, il faut :
		-Installer les dépendances suivants :
		:~$sudo apt-get install build-essential libssl-dev libexpat-dev libpcre3-dev libapr1-dev libaprutil1-dev
			-Executer maintenant le fichier configure:
			:~$./configure –-prefix=/usr/local/apache2
	5)Lancer la commande make :
		:~$make
	6)installer installer les fichiers binaires, les bibliothèques, les en-têtes et d'autres ressources d’apache2 dans leurs 	emplacements finaux sur le système à l’aide du commande :
		:~$sudo make install 

	-----------------------------------------INSTALLATION PHP---------------------------------------------------

	-Télécharger php dans le suite officiel de php : php-8.3.6.tar.gz (fichiers code source et archiver)
	-Décompresser et désarchiver simultanément php-8.3.6.tar.gz :
		$tar -xzf php-8.3.6.tar.gz
	-Entrez dans le répertoire après la décompression : php-8.3.6
		$cd php-8.3.6
	-Exécuter le fichier de configuration appelé configure
		$./configure
	Lors de l’installation il y a manque des dépendances tels que: pkg-config,libxml-2.0
	Installation pkg-config et libxml-2.0:
		$sudo apt install pkg-config
		$sudo apt install libxml2-dev
	Et il y a encore une erreur, lors de l’exécution de configuration :
	«error:Package requirements (sqlite ≥ 3.7.7) were not met : No package ‘sqlite3’ found»
	-Installer sqlite3 :
		$sudo apt-get install libsqlite3-dev
	-lancer la commande make afin de faire la compilation de code source
		$make
	-après, lancer la commande:

	 ----------------------------------------INSTALLATION MYSQL-----------------------------------------------

	-Télécharger mysql dans le suite officiel de mysql : mysql-8.3.0.tar.gz (fichiers code source et archives)
	-Décompresser et désarchiver simultanément mysql-8.3.0.tar.gz :
	:~$tar -xzf mysql-8.3.0.tar.gz
	-Entrez dans le répertoire après la décompression : mysql-8.3.0
		:~$cd mysql-8.3.0
	-il n’y a pas de fichier de configuration configure dans le répertoire mysql-8.3.0, pour cela, il faut :
		-créer un dossier construct et entrez dans ce dossier :
			:~$mkdir construct | cd construct
		-installer la commande cmake (une commande qui permet de simplifier le processus de compilation et d’installation sur différents plateforme):
			:~$sudo apt install cmake
		-Puis exécuter cmake dans le répertoire parent :
			:~$cmake ..
	-lancer la commande make afin de faire la compilation de code source mysql-8.3.0
		:~$make
	-après, installer mysql :
		:~$sudo make install
