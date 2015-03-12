========================
Actividades de Funciones
========================
En este bloque se agrupan aquellas actividades relacionadas con las funciones
   
Programando Fractales
======================

Con Scratch
------------    

**Material necesario:** Impresora 3D o Scratch. cabezal de Plotter para transformar la impresora en una máquina de dibujar

En esta actividad vamos a dibujar el Fractal de Koch:

Para programar el *fractal de Koch*, tenemos que realizar un proceso recursivo, de manera que cuántas más veces iteremos la recursividad mayor nivel de detalle obtendremos.

La idea del fractal es la siguiente: Se parte de un segmento, pero en lugar de trazarse recto, se divide en tres partes. La primera y la tercera se trazan rectas, pero la segunda se divide en dos trazos en forma de pico en forma de lados de triángulo equilatero. Una vez hecho esto, el proceso se repite recursivamente.


.. figure:: ./images/fractal1.png
    :width: 2000px
    :align: center
    :alt: alternate text
    :figclass: align-center
    
    (detalle de la función *linea_koch*)

Con un plotter
---------------

Las únicas órdenes que conoce el Plotter son las que vienen en el lenguaje *Gcodes* del *MIT*, y que constituye el estándar
para programar cualquier máquina de control numérico en general. Puesto que el conjunto de ordenes puede ser muy grande,
desde el punto de vista abstracto un fractal es una figura infinita, no nos queda más remedio que hacer un programa que 
genere los gcodes por nosotros. El código del programa podemos hacerlo en *Python*, y una posible implementación sería:
    
.. code-block:: python
  
        from itertools import chain
        from math import sin,cos,radians
        
        def mover(angulo,distancia):
        	nx = round(cos(radians(angulo)),9)*distancia
        	ny = round(sin(radians(angulo)),9)*distancia
        	return (nx,ny)
        
        def hacer_linea(i,j,fname,giros,grado_inicial):
        	# i iteracion, j longitud, fname fichero gcode, giros lista de giros, grado_inicial
        	for g in giros:
        		if i == 1:
        			posicion = mover(grado_inicial+g,j/(len(giros)-1))
        			gcodes = "G1 X{0} Y{1} \n".format(posicion[0],posicion[1])
        			print gcodes
        			#print j
        			#print " "
        			f = open(fname,'a')
        			f.write(gcodes)
        		else:
        			hacer_linea(i-1,j/(len(giros)-1),fname,giros,grado_inicial+g)
        		
        	
        def prod(i,j):
        	print(i*j)
        	return i*j
        	
        def koch_ant(i,j,fname):
        	resultado = i*j
        	s = "G1 X{0} \n".format(resultado)
        	print(s)
        	f = open(fname,'a')
        	f.write(s)
        	f.close
        	return resultado  
 
Para ejecutar el programa usamos lo siguientes comandos::

    minideb@minideb:~/migit/fractals_gcodes$ python koch.py
    
Esto nos creará un archivo llamado koch.gcode
