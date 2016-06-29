# mapas y gráficos con ai2html
d3.js? no thanks (©jk)

[ai2html](http://ai2html.org/) es un plugin opensource para Adobe Illustrator desarrollado por [Archie Tse](https://twitter.com/archietse), del equipo gráfico del New York Times,
que permite convertir nuestros proyectos illustrator en documentos ```html```.  


## instalación  

Debemos descargar el archivo ```ai2html.js``` de la [página oficial](http://ai2html.org/#how-to-install-ai2html) e incluirlo en nuestra carpeta de adobe.  
-```windows```: ```C:\Program Files\Adobe\Adobe Illustrator CC 2015\Presets\es_ES\Secuencias de comandos```  
-```Mac OS```: ```Applications/Adobe Illustrator CC 2014/Presets/en_US/Scripts/ai2html.jsx```  

## uso  

Este script nos permite **EXPORTAR** nuestros proyectos a un formato web por lo que hasta el momento trabajaremos con naturalidad en illustrator.  
Es importante tener el modo de color de documento en **rgb** y no en ~~CMYK~~.  
ai2html creara un archivo html en el que todos los textos seran nodos html (```div``` con sus correspondientes estilos ```css```) y el resto de elementos (lineas, circulos, mapas, etc.) quedaran reflejados en una imagen.  
Cuando hayamos terminado sólo tendremos que seleccionar la opción ```secuencias de comandos``` del menú ```archivo```.  
Si no hemos podido incluirlo en la carpeta podemos seleccionar la opcion ```otra secuencia de comandos (F12)``` del mismo menu y seleccionar el script.
Una vez exportado, aparecerá un cuadro de opciones a la izquierda de nuestra mesa de trabajo. El plugin incluye una serie de [opciones](http://ai2html.org/#settings) preestablecidas y otras *ocultas* (con unos valores por defecto). Podremos escoger número de colores del archivo *png*, calidad del *jpg*, directorio al que exportará los archivos, exportar al doble de resolucion (*retina*), etc.


## gráficos *responsive* (adaptativos)  

Un de las grandes virtudes de ai2html es la posibilidad de exportar nuestros graficos a diferentes tamaños. De esta manera  lograremos que nuestros diseños se vean a la perfección en todos los dispositivos. Pasos:  
1. Crea tantas mesas de trabajo como diseños quieras obtener (deberan tener estas dimensiones en pixeles). Para escritorio unos 900-1100px, tablet 600-700px y móvil 290-320px.
2. Descargar este [script ](https://github.com/newsdev/ai2html/blob/gh-pages/_includes/resizer-script.html) desarrollado por [Gregor Aisch ](https://twitter.com/driven_by_data). Este archivo javascript se encarga de mantener la apariencia de nuestro diseño en cada uno de los diferentes tamaños y cambiar la imagen que corresponde a cada uno.  
3. Una vez hayamos exportado nuestro diseño deberemos editar el html e incluir este script. ai2html creará **un único** archivo ```.html``` y tantas imagenes como mesas de trabajo tengamos.  


## desventajas  

1. A pesar de ser un pugin open-source está desarrollado para funcionar en Adobe Illustrator (software privativo).
2. Necesidad de desarrollar manualmente un diseño para cada uno de los dispositivos en que será visualizado.
3. Pequeños fallos: codificación, variación en el posicionamiento de los textos, errores en las posiciones de los textos por la confusion entre decimales y puntos en los estilos css *inline*, etc.  


## crea tu propio diseño con ai2html  

1. Crea un nuevo proyecto en Adobe Illustrator. Puedes descargar varias plantillas en la carpeta ```files``` del repo.
2. Prueba a crear cualquier diseño, puede ser un mapa realizado con QGIS o un svg que hayas descargado por ejemplo de wikipedia ([I](https://upload.wikimedia.org/wikipedia/commons/7/73/Roman_Empire_-_Dacia_(125_AD).svg),[II](https://upload.wikimedia.org/wikipedia/commons/c/c1/Plan_Acropolis_of_Athens.svg),[III](http://en.academic.ru/pictures/enwiki/70/Fukushima_I_nuclear_accidents_diagram.svg)).  
3. Si deseas ir hasta el final e intentar desarrollar un gráfico *adaptativo* o  *responsive*, imagina cómo te gustaría visualizar esos contenidos en cada una de las plataformas (escritorio, tableta, móvil).
4. Utiliza ai2html para exportar tus diseños.
5. Incluye el script [*resizer*](https://github.com/newsdev/ai2html/blob/gh-pages/_includes/resizer-script.html) que descargaste anteriormente al comienzo de tu nuevo archivo ai2html.
6. Si tus textos tienen caracteres que requieren una codificación UTF-8 añade este tag al comienzo de tu html:  
  ```<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">```
7. Felicidades! ya sabes utilizar ai2html!  

## Recursos
1. [QGIS](http://www.qgis.org/es/site/) programa libre para crear mapas vectoriales con archivos shape (```.shp```).
2. [svg Crowbar](http://nytimes.github.io/svg-crowbar/) permite descargar svg's de cualquier página.  

## Ejemplos
[What China Has Been Building in the South China Sea](http://www.nytimes.com/interactive/2015/07/30/world/asia/what-china-has-been-building-in-the-south-china-sea.html), The New York Times.    
[Boko Haram: The Other Islamic State](http://www.nytimes.com/interactive/2014/12/11/world/africa/boko-haram-nigeria-maps.html), The New York Times.  
[How one economic decision in Flint caused a health crisis](https://www.washingtonpost.com/graphics/health/flint-water-crisis/), The Washington Post.  
[Iraqi Army Retakes Government Complex in Central Ramadi](http://www.nytimes.com/interactive/2014/06/12/world/middleeast/the-iraq-isis-conflict-in-maps-photos-and-video.html), The New York Times.    
[Floor plans show interior of Orlando nightclub where 49 were killed](https://www.washingtonpost.com/graphics/national/orlando-shooting/), [How the Orlando Shooting Unfolded](http://graphics.wsj.com/orlando-shooting/), The Wall Street Journal.  
[Stowaways and crimes aboard a scofflaw ship](http://www.nytimes.com/2015/07/19/world/stowaway-crime-scofflaw-ship.html), The New York Times.    
[What Virginia says to the rest of the country](https://www.washingtonpost.com/graphics/politics/2016-election/primaries/super-tuesday-virginia-analysis/), [Why minority voters matter for Democrats in Nevada and beyond](https://www.washingtonpost.com/graphics/politics/2016-election/primaries/nevada-democratic-analysis/), The Washington Post.  
[Zika, el punto negro de los diagnósticos](http://reportajes.elespanol.com/diagnosis/zika-punto-negro-diagnosticos/), El Español.    
[What's that? How earbuds can wreck your hearing (especially for young people)](http://www.chicagotribune.com/news/ct-earphones-could-be-hurting-your-ears-20160229-htmlstory.html?utm_content=buffer5c0fd&utm_medium=social&utm_source=twitter.com&utm_campaign=buffer), The Chicago Tribune
