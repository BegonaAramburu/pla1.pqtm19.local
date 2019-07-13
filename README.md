# Configuración de un entorno Web de desarrollo
## Introducción
Este documento es una guía práctica para crearnos un entorno Web......
## Índice
1. Instalación Xampp
1. Configuración Virtual Host de Apache
1. Instalación de Eclipse
1. Definición de WorkSpace
1. Definición de proyecto
1. Definición de repositorio local
1. Creación de un Repositorio de GitHub
1. Exportación de la rama "master" local sobre el repositorio GitHub

## 1. Instalación de Xampp

XAMPP es un servidor independiente de plataforma de código libre. Nos permite instalar de forma sencilla Apache en nuestro propio ordenador, obteniendo de este modo un servidor Web.
XAMPP incluye además servidores de bases de datos como MySQL con su gestor phpMyAdmin e incorpora también el intérprete de PHP, el intérprete de Perl, entre muchas cosas más.
XAMPP es una herramienta de desarrollo que te permite probar tu trabajo (páginas web o programación por ejemplo) en tu propio ordenador sin necesidad de tener que acceder a internet.

### Proceso de instalación
Antes de instalar el paquete Xampp, deberemos comprobar que no existe ningún servidor Web instalado previamente en nuestro ordenador( esto lo podemos hacer escribiendo http://localhost en nuestro navegador y viendo si nos da un mensaje de error).

A continuación nos dirigimos al siguiente enlace https://www.apachefriends.org/es/index.html desde donde podremos descargar la aplicación de manera gratuita. Escogeremos la última versión (que a día de 12/07/2019 es la 7.3.7(PHP 7.3.7)) correspondiente al sistema operativo de nuestro ordenador y clicaremos en el botón de descargar.
Una vez tengamos el archivo descargado, haremos un doble clic en él y nos aparecerá un aviso de permisos restringidos. Pulsamos Ok y empezamos con la instalación. Vamos siguiendo las instrucciones *next* y en la pantalla de *Select components* escogeremos los siguientes:

![select components](./media/Install_Xampp/5_Install_Xampp.PNG)

Ahora nos muestra la carpeta en la que se va a instalar Xampp, que por defecto será C:\xampp, le decimos *next*, aquí y en las pantallas siguientes hasta que sale *Ready to install* y entonces empezará la instalación. Parará un momento para preguntarnos si queremos iniciar el panel de control y marcaremos el checkbox, *next*, escogemos el idioma (inglés o alemán) y *save*.
Se nos abre el panel de control y tenemos que clicar los *start* de *Apache* y *MySQL*, siendo ésta la imagen final:

![panel de control](./media/virtualhost.png)

Instalación finalizada!!

## 2. Configuración Virtual Host de Apache

Configurar un Host Virtual es la mejor solución para obtener proyectos 100% independientes y mantener la raíz del sitio Web autónoma y poder, de esta manera, crear rutas absolutas de archivos y carpetas.
Para crear un Host Virtual tendremos que seguir los siguientes pasos:
### 2.1. Editamos el archivo httpd_vhosts.conf
que está ubicado en C:\xampp\apache\conf\extra\httpd_vhosts.conf
### 2.2. Le añadimos las siguientes líneas de código al archivo httpd_vhosts.conf:

```
<VirtualHost *:80>
	ServerAdmin webmaster@pla1.pqtm19.local
	DocumentRoot "C:/PQTM19/Projectes/pla1.pqtm19.local"
	ServerName pla1.pqtm19.local
	ErrorLog "logs/pla1.pqtm19.local-error.log"
	CustomLog "logs/pla1.pqtm19.local-access.log" common
	<Directory "C:/PQTM19/Projectes/pla1.pqtm19.local">
		DirectoryIndex index.php index.html index.htm
		Options Indexes FollowSymLinks Includes ExecCGI
		AllowOverride All 
		Order allow,deny
		Allow from all
		Require all granted
	</Directory>
</VirtualHost>
```
### 2.3. Abrir el editor Notepad++ en modo administrador y editar el archivo hosts
que está ubicado en C:\Windows\System32\drivers\etc\hosts
y le añadimos al final:
```
127.0.0.1 pla1.pqtm19.local
```
### 2.4. Creamos el directorio:
C:\PQTM19\Projectes\pla1.pqtm19.local

### 2.5. Reiniciamos Apache
### 2.6. Comprobamos que funciona en el navegador

![virtual hosts](./media/virtualhosts.png)

## 3. Instalación de Eclipse

Eclipse es un entorno integrado de desarrollo de código abierto programado principalmente en Java (por tanto es multiplataforma) para desarrollar proyectos en C, C++, COBOL, Perl, PHP y muchos otros.  
Antes de instalar Eclipse debemos tener previamente instalado Java Runtime Environment en nuestro ordenador (en versiones de 32 o 64 bits dependiendo de lo que requiera nuestro Windows)  
Pàgina de descàrrega de Java Runtime Environment 10 (64 bits)  
http://www.oracle.com/technetwork/java/javase/downloads/jre10-downloads-4417026.html  
Pàgina de descàrrega de Java Runtime Environment 8 (32 bits)  
https://java.com/es/download/manual.jsp

Ahora ya estamos preparados para instalar Eclipse. Nos vamos a la pág web:

http://www.eclipse.org/downloads/   y hacemos clic en downloads 64 bits. Una vez descargado el archivo, haremos doble clic en él, entonces nos dará a escoger entre muchas opciones y dependiendo de lo que vayamos a desarrollar elegiremos una u otra. En nuestro caso clicaremos esta:

![opcion php](./media/Install_Eclipse/12_Install_Eclipse.PNG)









## 4. Definición de WorkSpace
## 5. Definición de proyecto
## 6. Definición de repositorio local
## 7. Creación de un Repositorio de GitHub
## 8. Exportación de la rama "master" local sobre el repositorio GitHub




