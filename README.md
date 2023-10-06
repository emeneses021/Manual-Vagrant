# Manual-Vagrant

1. Crear un directorio (mkdir "directori") y entrar en cd "directori"
2. Crear un directori con el nombre Vagrantile (vagrant init ubuntu/jammy64)
3. Añadir al parametro (vagrant up --provider=virtualbox)
4. Ahora ponemos (vagrant ssh)
5. Miramos los archivos con (ll /vagrant)
6. Ahora actualizamos la maquina poniendo apt update y después apt upgrade
7. Instalamos el sevidor web de apache2 (apt install -y apache2)
8. Ahora instalamos el sevidor de bases de dades (apt install -y mysql-server)
9. Instalaremos librerles de php (apt install -y php libapache2-mod-php)
10. Despues ponemos esta (apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl)
11. Reiniciaremos el servidor apache (systemctl restart apache2)
12. Ahora accedemos a la consola MySQL (mysql)
13. Creamos la base de dades (CREATE DATABASE bbdd;)
14. Crearemos un usuario (CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';)
15. Dando privilegio al usuario pondremos :(GRANT ALL ON bbdd.* to 'usuario'@'localhost';)
16. Nos saldremos de la bese de dades (exit)
17. Comprobamps la conexion de las dades (mysql -u usuario -p)
18. Vamos a nextcloud y en "Communic projects" le damos a Get ZIP file para descargar el archivo comprimido
19. Ahora lo copiamos a la carpeta
20. Movemos el archivo(/var/www/html) (sudo mv /vagrant/latest.zip /var/www/html/)  
21. Vamos a /var/www/html/ (cd /var/www/html/)
22. Entramos en el archivo (sudo unzip archivo)
23. Copia el contenido de nextcloud al repositorio (sudo cp -R nextcloud/. .)
24. Le ponemos permisos (chmod -R 775 .)
25. Y todavia mas permisos (chown -R root:www-data .)
26. Editamos el fichero (vi VagrantFile)






