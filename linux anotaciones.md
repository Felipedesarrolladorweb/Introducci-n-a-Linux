# Introducción a Linux

## El proceso Boot

El proceso Boot es el procedimiento que inicializa el sistema. Abarca todo lo que pasa desde que se enciende la computadora hasta que la interfaz de usuario está completamente funcional.  

Saber todo lo que abarca el proceso de boot puede ayudarlo con problemas de inicio o de ejecución, también como con adminstrar y mantener el rednimiento de la computadora según los requerimientos del usuario.

![modelo conceptual del boot en Linux](bootdiagram.jpg)  

</br>  

### **Primeros pasos**  

</br>  

Encender una computadora con sistema x86(_computadoras de 32bits/ las de 64 bits se les dice x64_) de Linux, requiere una serie de pasos. Cuando la pc es encendida, la Basic Input/Output System(BIOS/Sistema básico de entrada/salida), inicializa el hardware, incluyendo la pantalla y el teclado, y prueba la memoria principal. Este proceso es llamado _**POST**_(Power On Self Test/ Auoprueba de poder o encendido).  
</br>  
![modelo conceptual de la BIOS](BIOSpoweron.jpg)

## Linux command line

### **Comandos comunes**

Aunque Linux Desktop usa GUI(Grafic User Interface) para las gráficas parecido a windows, la mayoría de veces las instalaciones usan un command line, sobre todo en servidores.  
</br>
Un Shell provee al usuario de una interfaz sencilla para el Unix system. Sin embargo Bourne Shell es el que viene preinstalado.

**pwd** - muestra el directorio de la dirección en la que se encuentra el sistema.ejm:

```bash
[root@nombredeusuario Linux lite]# pwd  
/home/linuxlite
[root@nombredeusuario Linux lite]#
```  

</br>

_**cd**_ cambio de directorio:

* _cd.._ (con dos puntos) se usa para mover un directorio hacia la carpeta o directorio que le antecede.  
* _cd_ para ir directamente a la dirección main.  
* _cd-_ (con un guión) para mover el directorio a una dirección previa.  
</br>

_**ls**_ se usa para visualizar el contenido en un directorio:  

* _ls -R_ Enlistará todos los archivos en los subdirectorios también.  
* _ls -a_ muestra los archivos ocultos.  
* _ls -al_ muestra los archivos y los directrios con información detallada como permisos, tamaño, propietario, etc.  
</br>  

_**cat**_ enlista el contenido de un archivo en la salida standar(standard output):  

* _cat > nombrearchivo_ crea un nuevo archivo.  
* _cat nombrearchivo1 nombrearchivo2>nombrearchivo3_ junta los dos primeros archivos descritos en un tercer nuevo archivo.  
</br>

_**cp**_ copia archivos.  
</br>  

_**mv**_ mueve o renombra los archivos.  
</br>  

_**mkdir**_ crea in nuevo directorio en el directorio en el que esté actualmente.  
</br>  

_**rm**_  remueve archivos y directorios:  

* _**rm -r**_ remueve el directorio y los archivos dentro.  
