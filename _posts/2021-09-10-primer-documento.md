---
layout: post
title: Nuestro primer documento
description: Haremos nuestro primer documento explorando las herramientas básicas de LaTeX que podemos utilizar
summary: Se creará un documento básico de LaTeX
tags: [LaTeX, Taller, Instituto Mora]
---

# Formación de un documento en Latex

* Abre tu editor de texto para $$\LaTeX$$, en este caso *TexStudio*
* Crea un nuevo documento

![Imágen 1](https://i.imgur.com/F0L6JER.png)

## Nuestro preámbulo
* Empezamos por el primer código:

```
\documentclass[11pt,letterpaper]{article}
```

* Puedes elegir el tipo de documento que requieras. Para consultar los tipos de documentos que puedes elegir ingresa al siguiente [link](#)
* Escribimos nuestro primer código de paquete, este nos ayudará a detectar acentos y caracteres especiales:

```
\usepackage[utf8]{inputenc}
```

* Agregamos el paquete de idioma:

```
\usepackage[spanish]{babel}
```

* Se establece margen en caso de necesitar modificarlo con el paquete

```
\usepackage[margin=1cm]{geometry}
```

* No es obligatorio pero podemos asignar cabeceras y pies personalizados. Tómalo con calma y experimenta mucho con este paquete. Hay que usar los siguientes comandos:

```
\usepackage{fancyhdr}
\pagestyle{fancy}
\lhead[par]{impar}
\rhead[par]{impar}
\chead[par]{impar}
\cfoot[par]{impar}
\lfoot[par]{impar}
\rfoot[par]{impar}
\cfoot[par]{impar}
```

* Ingresamos los metadatos de autoría (autora, afiliación, correo, agradecimientos). Hay dos maneras de meter estos datos.

**Forma uno:**

```
\author{nombre de la autora}\thanks{dedicatoria, afiliación, correo, etc.}
\title{nombre del trabajo}
```

**Forma dos:**[^1]
```
\usepackage{authblk}
\author[a]{Nombre de la autora}\thanks{agradecimiento}
\affil[a]{afiliación}
\title{nombre del trabajo}
```

9. Comenzamos el cuerpo del documento, se escribe el intervalo `\begin{document}` y `\end{document}`.

10. Entre el intervalo de documento escribimos `\maketitle` para colocar el título de nuestro trabajo y la autoría del mismo.

11. En caso de que nuestro trabajo tenga *abstract* este debe ser incluido con el intervalo `\begin{abstract}`. Es importante cerrar este intervalo una vez se haya colocado el texto correspondiente.

12. Para agregar secciones o capítulos se usan respectivamente los siguientes comandos: `\section{nombre de la sección}` y `\chapter{título del capítulo}`
  * **Aclaración:** Los documentos que son Artículos no pueden tener capítulos, pero los libros y reportes pueden tener secciones, las secciones en los libros están jerárquicamente debajo de los capítulos.

13. Dar formato al texto como cursivas, negritas, volados, versalitas etc., con base en los comandos correspondientes


  [^1]: Usar el paquete de bloque de autor. Este método implica renovar comandos.
