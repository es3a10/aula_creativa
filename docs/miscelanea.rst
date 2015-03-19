===================
Miscelánea
===================

En este apartado se incluyen todas esas actividades que no han podido ser incluidas en otro grupo

Trofeos Scratch
----------------

Materiales 
__________
Impresora 3D, Programa de diseño 3D, Programa de dibujo vectorial.

Objetivo
________
El objetivo de la actividad es diseñar una medalla con un logotipo, por ejemplo el de **Scratch**.
La excusa para es diseñar una con motivo del 
Scratch Day. A partir de esta sencilla idea podemos construir trofeos, placas o medallas con el dibujo o 
dibujos que queramos. De esta manera se pueden utilizar para premiar al alumnado en diferentes concursos 
que se vayan haciendo. También puede ser interesante que sea el propio alumnado quien diseñe y construya 
sus propios trofeos. 

    .. figure:: ./images/trofeo_scratch7.jpg
        :width: 400 px
        :align: center 
        
        (Imagen de una medalla con el gato de Scratch impreso en 3D)


Recursos
________
Podemos partir de una imagen vectorial que fácilmente se puede 
encontrar en Internet. Por ejemplo, en este enlace:

    http://upload.wikimedia.org/wikipedia/commons/d/d4/Scratchcat.svg

También podemos encontrar ficheros en 3D para imprimir directamente,
por ejemplo:

    http://www.thingiverse.com/thing:336188/#files

Pero los archivos *stl* son difíciles de importar y manipular con los programas de diseño, y por tanto
resulta más interesante diseñarlos nosotros mismos.

Veamos cómo.

Creando un dibujo vectorial
___________________________

Vamos a utilizar **Inkscape** para dibujar la cara de la mascota de Scratch. Una técnica sencilla
para hacer el dibujo consiste en calcar dibujos:

#. Importamos nuestro dibujo vectorial descargado de Internet: Seleccionamos **Menú-Archivo-Importar**. Navegamos por la estructura de carpetas hasta seleccionar el archivo descargado en el epígrafe anterior. 

    .. figure:: ./images/trofeo_scratch.png
        :width: 400 px
        :align: center 
        
        (Imagen del gato Scratch importada a Inkscape)

#. Creamos una segunda capa, que es la que utilizaremos para calcar. Sobre esta segunda capa, calcamos el dibujo utilizando la herramienta de *Curvas de Beziers*. Podemos acceder a esa función con la combinación de teclas **MAYUSC+F6**. Vamos trazando puntos que luego se pueden modificar y manipular desde los deslizadores que aparecen al hacer doble click en ellos. 

    .. figure:: ./images/trofeo_scratch2.png
        :width: 400 px
        :align: center 

        (Trazo del calco)
        
#.  Al acabar el calco, borramos la capa del dibujo original, para quedarnos solo con el trazo calcado. Por otro lado, la esquina superior izquierda del documento será interpretada como origen de coordenadas al exportarlo a **FreeCAD**, por lo que conviene trasladar el dibujo a esa posición.

    
    .. figure:: ./images/trofeo_scratch3.png
        :width: 400 px
        :align: center 

        (Nuestra cara de Scratch en la esquina superior izquierda)
        
#.  Guardamos nuestro dibujo con formato vectorial. Por ejemplo: **scratch_face.svg**

Construyendo la medalla
_______________________
    
Llegados a este punto, vamos a diseñar la medalla.
Lo vamos a hacer con FreeCAD, pero podrías usar cualquier otro programa de diseño:

#.  Con FreeCAD abierto, seleccionamos **Menú-Archivo-Nuevo**. De nuevo menú **Archivo-Importar**. Seleccionamos el archivo creado en el epígrafe del directorio de carpetas. Por ejemplo */home/usuario/images/scratch_face.svg*. Nos aparecerá un cuadro de diálogo  indicando si queremos importarlo como dibujo o como geometría SVG. Tenemos que seleccionar como geometría SVG, ya que si no lo importa como dibujo

    .. figure:: ./images/trofeo_scratch4.png
        :width: 400 px
        :align: center
        
        (Trazos importados a **FreeCAD**)

#.  Tenemos que extruir los trazos para obtener una figura en 3 dimensiones. Esto se hace desde el banco de trabajo **Part**. La altura de extrusóin hay que ir adaptándola según los trazos, para obtener finalmente el relieve necesario

    .. figure:: ./images/trofeo_scratch5.png
        :width: 400 px
        :align: center
        
        (La cara de Scratch extruida)
        
#. Ya solo queda poner una base a la medalla y el texto que queramos. Desde el banco de trabajo **Part** podemos añadir un cilindro que hará de base, y desde el banco **Part Design** podremos añadir texto para después extruirlo.

    .. figure:: ./images/trofeo_scratch6.png
        :width: 400 px
        :align: center
        
        (La medalla-trofeo Scratch terminada)
        
#.  Guardamos el archivo en formato *stl* y lo imprimimos desde nuestra **impresora 3D**






 


