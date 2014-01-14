    Raúl Sánchez Fuentes Practica 3 IV
    Copyright (C) 2014  Raúl

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <http://www.gnu.org/licenses/>.




RaulSanchez-Practica3-IV-2013
=============================

Repositorio de la práctica 3 de IV del curso 2013/2014

En esta práctica se va a probar diferentes instalaciones de sistemas operativos en máquinas virtuales para probar el funcionamiento de estas con una determinada aplicación.

En mi caso se pondrá un servidor que soporte una página web y de servicio a esta.

Para ello se va a instarlar un sistema ubuntu y se modificará las propiedades de la máquina virtual, que será su número de procesadores y la memoria RAM utilizada.

Pues nada, empecemos con ello.


Máquinas (Todas con un único procesador):

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

![IV](https://dl.dropboxusercontent.com/s/2yr39f8g9lymbmv/41512.png?m=)


Modificamos la máquina para las **otras dos configuraciones**:


![IV](https://dl.dropboxusercontent.com/s/gvsrnhqi6wpful8/16.png)


![IV](https://dl.dropboxusercontent.com/s/a9h4hz3vw3nimv1/17.png)


Y ya por último aquí tenemos los **tiempos**:


|RAM|TIEMPO TOTAL| TIEMPO POR RESPUESTA|
|---|------|--------------|
|512 MB|8.613 seg|861.315 ms|
|256 MB|9.885 seg|988.468 ms|
|1024 MB|6.243|624.341 ms|


Ahora pasamos a instalar Ubuntu. La creación de la máquina virtual es similar a la creada anteriormente, y las configuraciones también son similares, por tanto mostraremos directamente los tiempos.


![IV](https://dl.dropboxusercontent.com/s/a5llhviunqwihzf/30.png)


**Tiempos Ubuntu**:

|RAM|TIEMPO TOTAL| TIEMPO POR RESPUESTA|
|---|------|--------------|
|512 MB|1.921 seg|192.117 ms|
|256 MB|4.389 seg|438.876 ms|
|1024 MB|1.793|179.263 ms|



**Comparativa**

Primero mostramos las gráficas individuales:

**Debian**:

![IV](https://dl.dropboxusercontent.com/s/3ius3mirnikcsrs/debian.png)


**Ubuntu**

![IV](https://dl.dropboxusercontent.com/s/ugznqplt7aruugs/ubuntu.png)


**Conjunto**

![IV](https://dl.dropboxusercontent.com/s/ry38w644t48hda9/ambos.png)



**Concluiones**

Una vez ya hemos instalado y probado todas las máquinas virtuales de este estudio y sus diferentes configuraciones podemos sacar varias conclusiones.

Mirando las gráficas individuales comprobamos que si escogiesemos instalar la máquina Debian, escogeriamos la configuración más alta (1024Mb) aún con el coste que supondría esto, ya que la diferencia de tiempo es considerable.

Sin embargo si decidiesemos isntalar Ubuntu, nos quedaríamos con la configuración intermedia, ya que la diferencia entre esta y la más alta es despreciable, y por ello es innecesario ese uso de memoria extra.

Y como conclusión final se muestra como entre las dos máquina aquí probadas sin duda se escogeria la máquina Ubuntu ya que la diferencia de tiempo es bastante elevada. Así que de todas estas configuraciones nos quedaríamos con la máquina con Ubuntu y una configuración de memoria RAM de 512 MB.
