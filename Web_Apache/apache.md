# COM INSTAL·LAR UN SERVIDOR APACHE I PUBLICAR LA NOSTRA WEB HUGO


		Primer instal·larem el servidor apache i posteriorment pujarem la web

&nbsp;

1. PAS.   INSTAL·LAR APACHE


> Instal·larem apache amb la següent comanda

```
sudo apt-install apache2
```

&nbsp;


2. PAS.   CAMBIENM EL PROPIETARI DE GRUP

> Cambiem el propietari del grup de la carpeta /var/www/html amb la comanda

```
sudo chgrp www-data var/www/html
```
&nbsp;



3. PAS. 	AGREGUEM EL NOSTRE USUARI AL NOU GRUP PROPIETARI

> Agreguem el noste usuari al grup propietari per evitar errors en permisos amb la comanda

```
sudo usermod -a -G www-data usuario
```
&nbsp;



4. PAS.    CAMBIEM ELS PERMISOS A LA CARPETA

> Cambien els permisos a la carpeta /var/www/html amb la comanda

```			
sudo chmod -R 775 var/www/html
sudo chmod -R g+s var/www/html
```
&nbsp;



5. PAS.    AGREGUEM EL NOSTRE USUARI AL DIRECTORI

> Agreguem el nostre usuari com a propietari del directori per poder editar amb la comanda
```
sudo chown -R usuario var/www/html
```

&nbsp;

**EL RESULTAT DEURÍA SER ALGO AIXÍ**


![Usuari a directori](./img1.png)

&nbsp;



6. PAS.     PASEM LA WEB AMB HUGO AL SERVIDOR

> Pasem la web al servidor apache amb la comanda

```
scp -r public eljust@192.168.1.52:/var/www/html
```
&nbsp;


**EL RESULTAT DEURÍA SER ALGO AIXÍ**

&nbsp;

![Web a servidor](./img2.png)
&nbsp;



7. PAS.		REINICIEM APACHE

> Reiniciem el servidor apache per a veure els canvis realitzats

```
sudo service apache2 restart
```

8. PAS.		Entrem a la web

> Entrem a la web del servidor apache amb la comanda ip/public
```
192.168.1.44/public
```

&nbsp;
**EL RESULTAT DEURÍA SER ALGO AIXÍ**
&nbsp;

![Servidor apache](./img3.png)
&nbsp;


9. PAS. 	Pujem la web a hosting

> Pujem la web a un hosting, en el meu cas a 000webhosting

&nbsp;

**Les carpetes deurien quedar així**
&nbsp;
![Servidor apache](./img4.png)
&nbsp;
**La web es veurá així**
![Servidor apache](./img5.png)
