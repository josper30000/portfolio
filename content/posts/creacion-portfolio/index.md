+++
title = 'Creacion Portafolio'  
date = 2026-08-13T09:24:37Z  
draft = true
showAuthor= true
+++

Aquí vamos a ver como crear nuestra web portafolio con HUGO y Blowfish, para posteriormente subirlo a github vía github pages.

Requisitos previos:

- Tener un repositorio de Github

- Tener docker instalado o hacerlo en una máquina Linux

Este tutorial es para Linux, yo todo este tutorial lo voy a hacer en un contenedor LXC de mi Proxmox.

Lo primero será instalar HUGO, actualizamos repositorios y luego lo instalamos

```bash
sudo apt update && sudo apt install git hugo
```
<img class="" src="images/instalar-hugo.png"/>

![imagen instalar hugo](./images/instalar-hugo.png)

Con esto tendremos instalado tanto Git para poder subir la página a github vía Github pages.

Ahora que tenemos esto instalado, podemos crear el proyecto base. 

```bash
hugo new site portafolio
cd portafolio
git init
```
![imagen arrancar proyecto hugo](./images/arrancar-portfolio.png)

Vamos a probar si Hugo está desplegado correctamente con el comando:

```bash
hugo server --bind 0.0.0.0 --baseURL http://[mi_ip]:1313 -D
```

Con esto desplegamos nuestra web de Hugo en local. Ahora mismo como no tenemos ninguna plantilla, al buscar la dirección nos saldrá la siguiente captura.

![alt image](./images/web-hugo.png)

Esto muestra, que aunque no hay ninguna página, Hugo ya está corriendo en local. Ahora vamos a añadirle un tema, en este caso añadiremos el tema de blowfish que es muy personalizable y con una gran cantidad de documentación (abajo dejo el enlace).

#### [Enlace a Blowfish](https://blowfish.page/)

Para añadir el tema de Blowfish

Fase 2: Instalar y configurar Blowfish
Añade la plantilla como submódulo de Git:
Esto te permite recibir actualizaciones del tema en el futuro sin romper tu código.

Bash
git submodule add https://github.com/nunocoracao/blowfish.git themes/blowfish
Importar la configuración de ejemplo (El truco para no empezar de cero):
Blowfish es muy personalizable y usa varios archivos de configuración. Lo más rápido es usar los que traen de ejemplo:

Borra el archivo hugo.toml que se creó por defecto en la raíz de tu carpeta mi-portafolio.

Ve a la ruta themes/blowfish/exampleSite/ y copia la carpeta completa llamada config.

Pégala en la raíz de tu proyecto mi-portafolio.