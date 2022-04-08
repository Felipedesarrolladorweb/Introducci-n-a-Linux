# Introducción a Linux

## El proceso Boot

El proceso Boot es el procedimiento que inicializa el sistema. Abarca todo lo que pasa desde que se enciende la computadora hasta que la interfaz de usuario está completamente funcional.  

Saber todo lo que abarca el proceso de boot puede ayudarlo con problemas de inicio o de ejecución, también como con adminstrar y mantener el rendimiento de la computadora según los requerimientos del usuario.

![modelo conceptual del boot en Linux](bootdiagram.jpg)  

</br>  

### **Primeros pasos**  

</br>  

Encender una computadora con sistema x86(_computadoras de 32bits/ las de 64 bits se les dice x64_) de Linux, requiere una serie de pasos. Cuando la pc es encendida, la Basic Input/Output System(BIOS/Sistema básico de entrada/salida), inicializa el hardware, incluyendo la pantalla y el teclado, y prueba la memoria principal. Este proceso es llamado _**POST**_(Power On Self Test/ Auoprueba de poder o encendido).  
</br>  
![modelo conceptual de la BIOS](BIOSpoweron.jpg)  

</br>  

El software o programa de la BIOS  esta almacenado en un chip _**ROM(Read Only Memory)**_ en la placa madre o motherboard.Luego de esto, lo que queda del encendido lo hace ya, el OS(Operative System/Sistema Operativo).  

</br>  

### **Master Boot Record (MBR) y Boot Loader**  

Una vez que el _**POST**_ es completado, el control del sistema pasa desde la _**BIOS**_ a el _**Boot Loader**_. El _Boot Loader_/ _Cargador de Boot_ es guardado generalmente en uno de los discos duros del sistema(Hard-drive disk), ya sea en la sección Boot( para sistemas tradicionales de BIOS/MBR), o la partición _**EFI / UEFI (Extensible Firmware Interface / Unified Extensible Firmware Interface)**_. En esta parte del proceso de encendido, el sistema aún no accede a ningun archivo de almacenamiento masivo, por eso cualquier información sobre la fecha, hora y los mas esenciales periféricos son cargados desde los valores  CMOS(se usan baterias especiales para mantener la memoria de esta infrmación con tal de que se pueda acceder aún despues de apagar el equipo, sin que se borre).  

Existen varios cargadores de boot(Boot loaders) para Linux; lo smás comunes son **GRUB(Grand Unified Boot loader/cargador)**, **ISOLINUX**(para cargar linux desde almacenamientos externos como usb o disco), y **DASU-Boot**(para cargar o iniciar en dispositivos/aplicaciones embebidos/ embedded devices/appliances). La mayoría de cargadores boot Linux pueden presentar una interfa de usuario para escoger que sistema operativo iniciar ya sea de Linux o algun sistema operativo como windows. El cargador boot de Linux también se encarga de cargar o leer la imagen Kernel y el disco inicial RAM disk(Random Access Memory) o archivo de sistema(Filesystem/ el cual contiene archivos esenciales y drivers de dispositivos que se necesitan para iniciar el sistema) en la memoria.  

![Máster Boot Record MBR](Master-Boot-Record(MBR).jpg)  


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
