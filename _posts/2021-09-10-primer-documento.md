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

Puedes elegir el tipo de documento que requieras. Para consultar los tipos de documentos que puedes elegir ingresa al siguiente [link](#){:target="\_blank"}

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
\author{nombre de la autora}\thanks{dedicatoria, afiliación, correo, etc.}
\title{nombre del trabajo}
```

**Forma dos:** con el paquete `authblk`[^1]
```
\usepackage{authblk}
\author[a]{Nombre de la autora}\thanks{agradecimiento}
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

![](https://i.imgur.com/rmoK8Q8.png){:target="\_blank"}


**Guardamos documento**.

Dar formato al texto como cursivas, negritas, volados, versalitas etc., con base en los comandos correspondientes, puedes consurtarlos en el siguiente [link](#){:target="\_blank"}


  [^1]: Usar el paquete de bloque de autor. Este método implica renovar comandos.
