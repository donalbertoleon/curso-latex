---
layout: post
title: Nuestro primer documento
description: Haremos nuestro primer documento explorando las herramientas básicas de LaTeX que podemos utilizar
summary: Se creará un documento básico de LaTeX
tags: [LaTeX, Taller, Instituto Mora]
---

# Formación de un documento en Latex

* Abre tu editor de texto para $$\LaTeX$$, en este caso *TexStudio*
* Crea un nuevo documento:

![Imágen 1](https://i.imgur.com/F0L6JER.png)

## Preámbulo

Empezamos por el primer código:

```
\documentclass[11pt,letterpaper]{article}
```

Puedes elegir el tipo de documento que requieras. Para consultar los tipos de documentos que puedes elegir ingresa al siguiente [link](https://mrleon.space/curso-latex/2021/09/15/comandos#tipo-de-documento){:target="\_blank"}.

Escribimos nuestro primer código de paquete, este nos ayudará a detectar acentos y caracteres especiales:

```
\usepackage[utf8]{inputenc}
```

Agregamos el paquete de idioma:

```
\usepackage[spanish]{babel}
```

Se establece margen en caso de necesitar modificarlo con el paquete

```
\usepackage[margin=1cm]{geometry}
```

No es obligatorio pero podemos asignar cabeceras y pies personalizados. Tómalo con calma y experimenta mucho con este paquete. Hay que usar los siguientes comandos:

```
\usepackage{fancyhdr}
\pagestyle{fancy}
\lhead[par]{impar}
\rhead[par]{impar}
\chead[par]{impar}
\cfoot[par]{impar}
\lfoot[par]{impar}
\rfoot[par]{impar}
```

Ingresamos los metadatos de autoría (autora, afiliación, correo, agradecimientos). Hay dos maneras de meter estos datos.

**Forma uno:**

```
\author{nombre de la autora\thanks{dedicatoria, afiliación, correo, etc.}}
\title{nombre del trabajo}
```

**Forma dos:** con el paquete `authblk`[^1]
```
\usepackage{authblk}
\author[a]{Nombre de la autora\thanks{agradecimiento}}
\affil[a]{afiliación}
\title{nombre del trabajo}
```

El Documento quedará algo así:

![](https://i.imgur.com/zhzTrZi.png)

**Guardamos documento**.

## Cuerpo

Comenzamos el cuerpo del documento, se escribe el intervalo

```
\begin{document}
  \maketitle

\end{document}
```

Nótese que en el intervalo de documento escribimos `\maketitle` para colocar el título de nuestro trabajo y la autoría del mismo.

En caso de que nuestro trabajo tenga *abstract* este debe ser incluido con el intervalo `\begin{abstract}`. Es importante cerrar este intervalo una vez se haya colocado el texto correspondiente.

```
\begin{document}
  \maketitle

  \begin{abstract}
      Mi Abstract
  \end{abstract}

\end{document}
```

Para agregar secciones o capítulos se usan respectivamente los siguientes comandos: `\section{nombre de la sección}` y `\chapter{título del capítulo}`.

**Aclaración:** Los documentos que son Artículos no pueden tener capítulos, pero los libros y reportes pueden tener secciones, las secciones en los libros están jerárquicamente debajo de los capítulos.

```
\begin{document}
  \maketitle

  \begin{abstract}

      Mi abstract

  \end{abstract}



  \section{Introducción}


    Excepteur eu quis cillum laboris aute laboris culpa qui exercitation enim mollit. Laboris est mollit nisi mollit eu nostrud officia est et eu eu pariatur duis. Mollit elit commodo irure exercitation ullamco dolore pariatur culpa amet. Cillum nisi sunt commodo nostrud velit exercitation labore do id ad veniam culpa ex quis ad. Ea dolore ex laboris qui deserunt eu minim qui non proident officia amet nisi fugiat mollit. Anim anim sint consequat dolore reprehenderit velit ut cillum.

  \section{Desarrollo}

    In aute nisi laboris duis Lorem dolor dolore dolor amet sit. Dolore ullamco cillum est ad esse incididunt culpa deserunt id. Pariatur laborum incididunt fugiat nostrud id fugiat consectetur nisi qui. Consequat qui non et in ullamco esse ex. Magna culpa id in et sunt ullamco laboris ex excepteur sit anim aute consectetur labore esse aliquip in. Occaecat occaecat occaecat adipisicing do aute aute velit esse laboris. In excepteur ea elit elit irure occaecat tempor ad ullamco amet velit incididunt labore laborum.


\end{document}
```

El documento queda de la siguiente forma:

![](https://i.imgur.com/6DRmapI.png){:target="\_blank"}


**Guardamos documento**.

Podemos agregar cuantas secciones y subsecciones queramos, de tal forma que se empiece a estructurar nuestro documento.

La siguiente imagen muestra cómo el documento ya tiene más secciones y subsecciones. Estas se van a representar en la sección en el panel izquierdo de nuestro programa **TeXstudio**:

![](https://i.imgur.com/nLjO8po.png){:target="\_blank"}


## Otros aspectos para el documento

[Formato](https://mrleon.space/curso-latex/2021/09/15/comandos#formato){:target="\_blank"}

[Tamaño de texto](https://mrleon.space/curso-latex/2021/09/15/comandos#tama%C3%B1o-de-texto){:target="\_blank"}

[Alineación del texto](https://mrleon.space/curso-latex/2021/09/15/comandos#alineaci%C3%B3n-del-texto){:target="\_blank"}

[Imágenes](https://mrleon.space/curso-latex/2021/09/15/comandos#im%C3%A1genes){:target="\_blank"}

[Caracteres especiales](https://mrleon.space/curso-latex/2021/09/15/comandos#caracteres-especiales){:target="\_blank"}

# Compilación

Una vez que hemos determinado qué paquetes vamos a usar, y hayamos dado formato al cuerpo del documento, vamos a realizar su "impresión", esto se llama **compilado**. Lo que hará nuestro programa es **interpretar** todas las órdenes que hemos escrito en el documento para que pueda traducirlo a un formato legible y estético.

Para hacer una compilación debemos tener abierto Texstudio, podemos compilar de dos maneras:

  1. Apretar la tecla de nuestro teclado `F6`
  2. Presionar en el programa el botón "Compilar" en la barra de herramientas de TexStudio:

  ![Compilar](https://i.imgur.com/FuS8rhG.png)

Con base en las órdenes que escribimos será nuestro resultado. Si no hubo errores en nuestro documento TexStudio nos marcará que el proceso terminó con normalidad:

  ![Terminado](https://i.imgur.com/CbzPRgJ.png)


Para previsualizar el documento compilado en PDF podemos presionar el botón `F7` en nuestro teclado o seleccionar en la barra de herramientas el botón "Visualizar":

  ![Visualizar](https://i.imgur.com/4Ogl921.png)

Se desplegará en el área de trabajo de TexStudio, del lado derecho, una miniatura con el PDF ya compilado, ahí podremos ver rápidamente el archivo:

  ![Previsualización](https://i.imgur.com/Fhpm8Jk.png)

Si queremos ver el PDF en nuestro lector solo hay que presionar el botón con el símbolo de PDF que hay en la barra de herramientas que se abrió con la Previsualización:

  ![Abrir documento](https://i.imgur.com/AHKof3s.png)


Podemos agregar o quitar contenido, comandos y entornos cada vez que deseemos, para ver los cambios aplicados se debe compilar después de escribirlos. **La compilación se realiza cuantas veces sean necesarias**, hasta que demos el proceso por finalizado.

Si asistimos a la carpeta donde está nuestro trabajo nos daremos cuenta que hay varios documentos, todos estos documentos son generados con la compilación. Los únicos documentos que no deben jamás eliminarse son el archivo con extensión `.tex` y las imágenes, en caso de que tenga nuestro documento imágenes:

  ![Archivos](https://i.imgur.com/oT0qYNC.png)

#### Posibles errores

* Se usaron caracteres reservados de una manera errónea
* No se cerraron los entornos o las llaves de los comandos adecuadamente
* Se escribió mal un comando
* Se escribieron mal las opciones de los comandos

  [^1]: Usar el paquete de bloque de autor. Este método implica renovar comandos.
