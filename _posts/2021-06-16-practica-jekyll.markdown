---
layout: post
title:  "Practica Jekyll"
date:   2021-06-16 22:22:35 -0500
categories: IAW
---
# Creacion de blogs con Jekyll

## Introducción 

Jekyll es un generador de sitios web estáticos que nos permite crear de forma sencilla blogs, sitios webs personales o webs para proyectos. Los sitios webs generados con Jekyll no usan una base de datos, el contenido del sitio web está escrito en archivos de texto plano en formato Markdown.

## Primeros pasos

Para poder hacer esta practica podemos usar cualquier maquina de ubuntu, simplemente tendremos que abrir el puerto 22 para conectar por SSH y el puerto 4000.

Tambien necesitaremos crear un repositorio en nuestro github que llamaremos "usuario de github".github.io

![alt text](https://github.com/antoniomanu/antoniomanu.github.io/blob/main/capturas/ce5773808c91c4bca1c4a95ca18031eb.png "Captura 1")

Una vez creado el repositorio lo clonamos en la maquina que hemos creado

## Creacion del sitio

Cuando se haya clonado entramos y lanzamos el contenedor de Jekyll con el siguiente comando, que nos creará la infraestructura de nuestro blog.

> sudo docker run -it --rm -v "$PWD:/srv/jekyll" jekyll/jekyll jekyll new blog

Este comando creara un directorio llamado blog, pero nos es mas comodo tenerlo todo en la raiz del repositorio clonado de github asi que vamos a sacar todo el contenido de este y eliminar el directorio.

> sudo mv blog/* ./

> sudo rm -rf blog

Para terminar vamos a subir todos estas cosas que hemos hecho desde consola al repositorio con git add --all, git commit, y git pull.

> git add --all

> git commit -m "Comentario para el commit"

> git push

## Acceso al sitio 

Para poder acceder a nuestro sitio ahora simplemente tendremos que usar el navegador y poner "https:// usuario.github.io"

Deberia de aparecer algo como esto:

![imagen](https://github.com/antoniomanu/antoniomanu.github.io/blob/main/capturas/jekyll.png "Captura 2")

En el archivo creado por defecto te explica como se deben de crear nuevos posts en Jekyll.

