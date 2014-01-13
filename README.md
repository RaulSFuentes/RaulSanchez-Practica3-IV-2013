RaulSanchez-Practica3-IV-2013
=============================

Repositorio de la práctica 3 de IV del curso 2013/2014

En esta práctica se va a probar diferentes instalaciones de sistemas operativos en máquinas virtuales para probar el funcionamiento de estas con una determinada aplicación.

En mi caso se pondrá un servidor que soporte una página web y de servicio a esta.

Para ello se va a instarlar un sistema ubuntu y se modificará las propiedades de la máquina virtual, que será su número de procesadores y la memoria RAM utilizada.

Pues nada, empecemos con ello.


Máquinas:

**Debian 7.3**

	>512 RAM

	>256 RAM

	>1024 RAM

**Ubuntu 12.04**

	>512 RAM
	>256 RAM
	>1024 RAM


Emperzaremos por mostrar como se crea una nueva máquina virtual en VirtualBox.

![IV](https://dl.dropboxusercontent.com/s/ibuts86t3xgbjmo/1.png)

Esta es la ventana de inicio del programa, y para crear una nueva máquina virtual pulsaremos sobre Nueva.


![IV](https://dl.dropboxusercontent.com/s/tk4hfma679lcv4v/2.png)

Aquí daremos nombre a la máquina virtual.

![IV](https://dl.dropboxusercontent.com/s/m2s3f1kwnkmtn25/3.png)

Asignamos la memoria RAM.

![IV](https://dl.dropboxusercontent.com/s/mx2c2ju0qwjnmor/4.png)

He indicamos que vamos a crear un nuevo disco.

![IV](https://dl.dropboxusercontent.com/s/xg36xp6sfjc0tje/5.png)

Seleccionamos el tipo de unidad.

![IV](https://dl.dropboxusercontent.com/s/qevsdwbaw9bvd5v/6.png)

Tamaño del disco duro.

![IV](https://dl.dropboxusercontent.com/s/aeryv4pbcfyzuhn/7.png)

Y finalmente indicamos el disco de instalación del sistema operativo.

![IV](https://dl.dropboxusercontent.com/s/rxj49mpibtonldx/8.png)

Y ya realizar una instalación normal del sistema.


En estos pasos hemos dejado la configuración por defecto que nos índica VirtualBox. Esta configuración la utilizaremos como base, y copiaremos esta máquina virtual para las siguientes, modificando solo los valores que nos interesen.


Una vez ya tenemos la máquina funcionando, pasamos a instalarle los paquetes que necesito para mi aplicación:

**Apache:**

![IV](https://dl.dropboxusercontent.com/s/8fdf0ghk8t365au/10.png)


**Python:**

![IV](https://dl.dropboxusercontent.com/s/2orslkm9nbpr3mo/11.png)

**Apache benchmark:**

![IV](https://dl.dropboxusercontent.com/s/yr30g1x3hfdepo3/13.png)

Ahora copiamos la aplicación en /var/www y la lanzamos: python ej1.py.


Y por último **relanzamos apache**:

![IV](https://dl.dropboxusercontent.com/s/ak9qnbw0jsjd95m/14.png)


Y ahora ya sacar los **tiempos** con ab -n 1000 -c 100 (1000 peticiones con 100 en concurrente):

![IV](https://dl.dropboxusercontent.com/s/eerdvobuf8gsot3/15.png)


Modificamos la máquina para las **otras dos configuraciones**:


![IV](https://dl.dropboxusercontent.com/s/gvsrnhqi6wpful8/16.png)


![IV](https://dl.dropboxusercontent.com/s/a9h4hz3vw3nimv1/17.png)


Y ya por último aquí tenemos los **tiempos**:



