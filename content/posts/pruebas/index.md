+++
title = 'Pruebas'  
date = 2026-08-13T09:24:37Z  
draft = false
featureimage = "./images/arrancar-portfolio.png"
summary = "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque purus nisl, imperdiet at hendrerit id, laoreet ut nulla. Maecenas vitae massa bibendum, feugiat lorem sed, fermentum diam. Nullam ut lacus justo. Vestibulum lectus ex, mollis vitae sapien sed, dictum aliquam enim. Donec egestas dictum tellus, non maximus dui laoreet eu. Nulla sed nisl porttitor velit iaculis euismod. Integer dapibus mi quis nunc suscipit, eu faucibus ex convallis. Mauris sollicitudin euismod aliquam. Fusce facilisis ante ullamcorper, facilisis ligula sed, commodo odio. Proin in iaculis quam, vitae elementum felis. Curabitur gravida, ligula sit amet finibus tincidunt, arcu lectus tincidunt tellus, vel venenatis libero ligula vel risus. Morbi consectetur nibh eget turpis malesuada feugiat. Mauris tortor diam, feugiat nec est vitae, pretium hendrerit nulla. Cras aliquet vel diam nec ultrices. In sed ullamcorper arcu. Pellentesque nec leo neque. "
tags = ["patata"]
showAuthor= true
+++

Aquí vamos a ver como crear nuestra web portafolio con HUGO y Blowfish, para posteriormente subirlo a github vía github pages.

Requisitos previos:

Tener un repositorio de Github

Tener docker instalado o hacerlo en una máquina Linux

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