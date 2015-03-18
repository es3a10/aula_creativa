===================
Miscelánea
===================

En este apartado se incluyen todas esas actividades que no han podido ser incluidas en otro grupo

Trofeos Scratch
----------------

**Materiales:** Impresora 3D, Programa de diseño 3D, Programa de dibujo vectorial.

El objetivo de la actividad es diseñar una medalla con el logotipo de Scratch. Con esta sencilla idea
podemos construir trofeos o medallas con el dibujo que queramos, y de esta manera premiar al alumnado en
diferentes concursos que se vayan haciendo.   

**Recursos:**   Podemos partir de una imagen vectorial que fácilmente se puede 
encontrar en Internet. Por ejemplo, en este enlace:
    http://upload.wikimedia.org/wikipedia/commons/d/d4/Scratchcat.svg
También podemos encontrar ficheros en 3D para imprimir directamente,
por ejemplo:
    http://www.thingiverse.com/thing:336188/#files
Pero los archivos *stl* son difíciles de importar con los programas de diseño, y por tanto
resulta más interesante diseñarlas nosotros mismos.

Veamos cómo.

Creando un dibujo vectorial
---------------------------

Vamos a utilizar **inkscape** para dibujar la cara de la mascota de Scratch. Una técnica sencilla
para hacer el dibujo consiste en calcar dibujos:

#. Importamos nuestro dibujo vectorial descargado de Internet: Menú **Archivo-Importar**. Navegamos por la estructura de carpetas hasta seleccionar el archivo descargado. 

    .. figure:: ./images/trofeo_scratch.png
        :width: 20000 px
        :align: center 
        
        (Imagen del gato Scratch importada a Inkscape)

#. Creamos una segunda capa, que es la que utilizaremos para calcar. Sobre la segunda capa, calcamos el dibujo. Para ello utilizamos las *curvas de Beziers*. Podemos acceder a esa función con la combinación de teclas **MAYUSC+F6**. Vamos trazando puntos que luego se pueden modificar desde los deslizadores que aparecen al hacer doble click en ellos. 

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
-----------------------
    
Llegados a este punto, vamos a diseñar la medalla.
 


