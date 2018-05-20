# Maps and graphics with ai2html

*[[Leer en español](#user-content-mapas-y-gráficos-con-ai2html)]*

[ai2html](http://ai2html.org/) is an open source script for Adobe Illustrator created by [Archie Tse](https://twitter.com/archietse) and The New York Times graphics team, which makes it easy to convert our Illustrator projects to HTML documents.

## Installation

Download `ai2html.js` from the [official repo](https://github.com/newsdev/ai2html/raw/master/ai2html.js) and move it to your Adobe installation folder.

- Windows: `C:\Program Files\Adobe\Adobe Illustrator CC 2018\Presets\en_US\Scripts`
- macOS: `Applications/Adobe Illustrator CC 2018/Presets/en_US/Scripts`

## Getting started

This script will let us export our graphics to a web format from Illustrator.

ai2html creates a HTML file where the text is transformed to HTML nodes (`div` with its corresponding `css`). The rest of the elements (lines, circles, maps, etc) will be converted to an image.

To run the script you need to go to `File > Scripts` . If you couldn't move the file to the Illustrator folder you can select `Another script` <kbd>F12</kbd> on the same menu and select the file.

Once the file is exported a new box with options will appear on the left side of your artboard. The script has a series of [options](http://ai2html.org/#settings), some of them enabled and others hidden. You can choose now between the number of colours of the `png`, the quality of the `jpg`, output folder, retina resolution, etc.

It is important to change the colour mode to **RGB** and not use **CMYK**.

Don't forget to add your own font stack in the `ai2html` file.

## Responsive graphics

One of the most important features of ai2html is the ability to export our graphics to different sizes. To get started:

1. Create as many artboards as sizes you need (the script will use those dimensions). We have found that making a graphic between these sizes works well:

  - Desktop: 900-1100px
  - Tablet: 600-700px.
  - Phone: 290-320px.

2. Download [this script](https://github.com/newsdev/ai2html/blob/gh-pages/_includes/resizer-script.html). This is the JavaScript that will switch between the different graphics according to the browser size.

3. Once the design is exported, you need to edit the HTML and add that script. You'll see that ai2html creates only **one** HTML file and as many images as artboards exist on the Illustrator file.

## Sample files

There are sample files that you can use as a starter in the [files](tree/master/files) folder of this repo.

Try to create a design and play with it. You can also use SVGs from Wikipedia ([I](https://upload.wikimedia.org/wikipedia/commons/7/73/Roman_Empire_-_Dacia_(125_AD).svg),[II](https://upload.wikimedia.org/wikipedia/commons/c/c1/Plan_Acropolis_of_Athens.svg),[III](http://en.academic.ru/pictures/enwiki/70/Fukushima_I_nuclear_accidents_diagram.svg)).

If there are strange characters on the browser you may need to declare UTF-8 encoding in your HTML. Add this at the beginning of the document:

```html
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
```

## Cons

1. Despite being an open source script it only works on Adobe Illustrator, which is privative software.

2. You'll need to make a different graphic for each size.

3. Sometimes you will need to make small adjustments to the final output. The position of the text nodes can vary between browsers and configurations.

## Resources

1. [QGIS](http://www.qgis.org/es/site/) free software to create vector maps.
2. [SVG Crowbar](http://nytimes.github.io/svg-crowbar/), a bookmarklet to extract SVGs from websites.  

## Examples

- [What China Has Been Building in the South China Sea](http://www.nytimes.com/interactive/2015/07/30/world/asia/what-china-has-been-building-in-the-south-china-sea.html), The New York Times.    

- [Boko Haram: The Other Islamic State](http://www.nytimes.com/interactive/2014/12/11/world/africa/boko-haram-nigeria-maps.html), The New York Times.  

- [How one economic decision in Flint caused a health crisis](https://www.washingtonpost.com/graphics/health/flint-water-crisis/), The Washington Post.  

- [Iraqi Army Retakes Government Complex in Central Ramadi](http://www.nytimes.com/interactive/2014/06/12/world/middleeast/the-iraq-isis-conflict-in-maps-photos-and-video.html), The New York Times.    

- [Floor plans show interior of Orlando nightclub where 49 were killed](https://www.washingtonpost.com/graphics/national/orlando-shooting/),  The Washington Post.

- [How the Orlando Shooting Unfolded](http://graphics.wsj.com/orlando-shooting/), The Wall Street Journal.  

- [Stowaways and crimes aboard a scofflaw ship](http://www.nytimes.com/2015/07/19/world/stowaway-crime-scofflaw-ship.html), The New York Times.    

- [What Virginia says to the rest of the country](https://www.washingtonpost.com/graphics/politics/2016-election/primaries/super-tuesday-virginia-analysis/), The Washington Post.  

- [Why minority voters matter for Democrats in Nevada and beyond](https://www.washingtonpost.com/graphics/politics/2016-election/primaries/nevada-democratic-analysis/), The Washington Post.  

- [Zika, el punto negro de los diagnósticos](http://reportajes.elespanol.com/diagnosis/zika-punto-negro-diagnosticos/), El Español.    

- [What's that? How earbuds can wreck your hearing (especially for young people)](http://www.chicagotribune.com/news/ct-earphones-could-be-hurting-your-ears-20160229-htmlstory.html?utm_content=buffer5c0fd&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer), The Chicago Tribune.

---

# Mapas y gráficos con ai2html

[ai2html](http://ai2html.org/) es un plugin opensource para Adobe Illustrator desarrollado por [Archie Tse](https://twitter.com/archietse) y el equipo de gráficos del New York Times,
que permite convertir nuestros proyectos Illustrator en documentos `HTML`.

## Instalación

Descarga el archivo `ai2html.js` del [repositorio oficial](http://ai2html.org/#how-to-install-ai2html) e inclúyelo en nuestra carpeta de adobe.  
-`Windows`: `C:\Program Files\Adobe\Adobe Illustrator CC 2018\Presets\es_ES\Secuencias de comandos`  
-`macOS`: `Applications/Adobe Illustrator CC 2018/Presets/en_US/Scripts/ai2html.jsx`

## Utilización

Este script permite exportar nuestros proyectos a un formato web desde Illustrator.

ai2html crea un archivo HTML donde el texto es transformado en nodos HTML (`div` con sus correspondientes estilos `css`). El resto de elementos (líneas, círculos, basemaps, etc.) serán convertidos en una imagen.

Para correr el script tienes que ir a `Archivo > Secuencias de comandos`.

Si no has podido incluirlo en la carpeta de Illustrator puedes seleccionar el script a través de la opcion `otra secuencia de comandos (F12)` del mismo menu.

Una vez exportado, aparecerá un cuadro de opciones a la izquierda de nuestra mesa de trabajo. El plugin incluye una serie de [opciones](http://ai2html.org/#settings), unas activadas y otras _ocultas_. Puedes escoger el número de colores del archivo _png_, calidad del _jpg_, directorio al que exportará los archivos, exportar al doble de resolucion (_retina_), etc.

Es importante tener el modo de color de documento en **RGB** y no en **CMYK**.

No olvides añadir tu propio conjunto de fuentes en el script ai2html.

## Gráficos _responsive_

Una de las grandes virtudes de ai2html es la posibilidad de exportar nuestros graficos a diferentes tamaños. Pasos:

1. Crea tantas mesas de trabajo como diseños quieras obtener (el script usará estas dimensiones). Los siguientes tamaños funcionan bien:

  - Escritorio: 900-1100px
  - Tableta: 600-700px.
  - Teléfono: 290-320px.

2. Descarga este [script ](https://github.com/newsdev/ai2html/blob/gh-pages/_includes/resizer-script.html). Este archivo JavaScript se encargará de cambiar de un diseño a otro en función del tamaño del navegador.

3. Una vez hayamos exportado nuestro diseño deberemos editar el html e incluir este script. También puedes añadir la opción `include_resizer_script: yes` en el cuadro de opciones que genera ai2html dentro de tu proyecto. ai2html creará **un único** archivo HTML y tantas imagenes como mesas de trabajo tenga tu proyecto.

## Archivos de muestra

En la carpeta `files` de este repositorio puedes encontrar diferentes archivos para empezar a practicar así como un proyecto en Illustrator que incluye tres diseños.

Prueba a crear cualquier diseño, puede ser un mapa realizado con QGIS o un svg que hayas descargado por ejemplo de wikipedia ([I](<https://upload.wikimedia.org/wikipedia/commons/7/73/Roman_Empire_-_Dacia_(125_AD).svg>),[II](https://upload.wikimedia.org/wikipedia/commons/c/c1/Plan_Acropolis_of_Athens.svg),[III](http://en.academic.ru/pictures/enwiki/70/Fukushima_I_nuclear_accidents_diagram.svg)).

Si tus textos tienen caracteres que requieren una codificación UTF-8 añade este tag al comienzo de tu html:

```html
<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
```

## Desventajas

1. A pesar de ser un plugin open-source sólo funciona en Adobe Illustrator (software privativo).

2. Necesitas desarrollar manualmente un diseño para cada uno de los dispositivos en que será visualizado.

3. Pequeños fallos: codificación, variación en el posicionamiento de los textos, errores en las posiciones de los textos por la confusion entre decimales y puntos en los estilos css _inline_, etc.

## Recursos

1. [QGIS](http://www.qgis.org/es/site/) programa libre para crear mapas vectoriales.
2. [svg Crowbar](http://nytimes.github.io/svg-crowbar/) permite descargar svg's de cualquier página.

## Ejemplos

- [What China Has Been Building in the South China Sea](http://www.nytimes.com/interactive/2015/07/30/world/asia/what-china-has-been-building-in-the-south-china-sea.html), The New York Times.

- [Boko Haram: The Other Islamic State](http://www.nytimes.com/interactive/2014/12/11/world/africa/boko-haram-nigeria-maps.html), The New York Times.

- [How one economic decision in Flint caused a health crisis](https://www.washingtonpost.com/graphics/health/flint-water-crisis/), The Washington Post.

- [Iraqi Army Retakes Government Complex in Central Ramadi](http://www.nytimes.com/interactive/2014/06/12/world/middleeast/the-iraq-isis-conflict-in-maps-photos-and-video.html), The New York Times.

- [Floor plans show interior of Orlando nightclub where 49 were killed](https://www.washingtonpost.com/graphics/national/orlando-shooting/), [How the Orlando Shooting Unfolded](http://graphics.wsj.com/orlando-shooting/), The Wall Street Journal.

- [Stowaways and crimes aboard a scofflaw ship](http://www.nytimes.com/2015/07/19/world/stowaway-crime-scofflaw-ship.html), The New York Times.

- [What Virginia says to the rest of the country](https://www.washingtonpost.com/graphics/politics/2016-election/primaries/super-tuesday-virginia-analysis/), [Why minority voters matter for Democrats in Nevada and beyond](https://www.washingtonpost.com/graphics/politics/2016-election/primaries/nevada-democratic-analysis/), The Washington Post.

- [Zika, el punto negro de los diagnósticos](http://reportajes.elespanol.com/diagnosis/zika-punto-negro-diagnosticos/), El Español.

- [What's that? How earbuds can wreck your hearing (especially for young people)](http://www.chicagotribune.com/news/ct-earphones-could-be-hurting-your-ears-20160229-htmlstory.html?utm_content=buffer5c0fd&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer), The Chicago Tribune
