![imagen](centos.jpg)
___

# Instalación y configuración de CentOS 8

## Contenido

* [Descarga de recursos](#Recursos)
* [Creación de medio de instalación](#Creación)
* [Componentes del ordenador usado](#Componentes)
* [Estructura de directorios de Linux](#Directorios)
* [Instalación del servidor CentOS](#Instalación)
* [Configuración del servidor CentOS](#Configuración)
* [Añadir puntos de montaje de la partición](#Montaje)
* [Red y Nombre del equipo](#Redes)
* [Configuración de Fecha y Hora](#Fecha)
* [Selección de Software](#Sofware)
* [Creación de usuarios y contaseñas](#Usuarios)

## Recursos

* Descarga de ISO del servidor de la pagina oficial [CentOS][1]
* Descarga de medio de instalación [Ethcer][2]

[1]:http://isoredirect.centos.org/centos/8/isos/x86_64/CentOS-8.1.1911-x86_64-dvd1.iso
[2]: https://www.balena.io/etcher/

## Creación

1. Seleccionar la imagen iso que necesitamos.
2. Seleccionar el pendrive donde se flasherara la imagen ISO.
3. Seleccionamos el botón de Flash.
    * Para poder realizar esto se abre un cuadro de administrador.
    * Autorizamos a Etcher para poder flashear el pendrive.
4. Tiempo de espera aproximado 25 minutos.

## Componentes

| Almacenamiento |   Descripción   | Capacidad     |
|----------------|-----------------|---------------|
| Disco Duro     | Western Digital |    320 GB     |
| Memoria Ram    | Generica        |    2 GB       |
| Memorio Ram    |  Generica       |    2 GB       |

## Directorios

|   Directorio  |       Descripción         |
|---------------|---------------------------|
|   bin         | Binarios de usuario       |
|   boot        | Ejecutables y archivos requeridos para el arranque    |
|   dev         | Archivos de información de todos los volumenes        |
|   etc         | Archivos de información de todos los volumenes        |
|   home        | Directorio personal con los directorios de usuarios   |
|   lib         | Bibliotecas necesarias para la ejecución de binarios  |
|   media       | Directorio de montaje de volumenes extraibles         |
|   opt         | Archivos de aplicaciones externas que no se integran  en /usr|
|   proc        | Archivos de información de procesos                   |
|   root        | Directorio personal del superusuario                  |
|   sbin        | Binarios del sistema                                  |
|   srv         | Archivos relativos a servidores web, ftp, etc         |
|   sys         | Archivos virtuales con información del sistema        |
|   tmp         | Archivos temporales del sistema                       |
|   usr         | Archios de programas                                  |
|   var         | Archivos variables                                    |

## Instalación

1. En el menu de linea de comando, seleccionar la opción de:
    * Test this media install CentOS Linux 8.0.1906
2. En el menu gráfico de bienvenida a centos linux.
    * En el recuadro izquierdo, seleccionar la opción de idioma **Español.**
    * En el recuadro derecho, seleccionar la opción de __Español (México).__

## Configuración

1. En el menu gráfico de resumen de instalación:
    * Seleccionamos la opción de Destino de la instalación en el submenu de Sistema.
    * En el menu gráfico de Destino de la instalación, buscar el apartado denominado **Discos estandares locales**, y selecionar el disco requerido.
    * En el apartado denominado **Configuración de almacenamiento**, seleccionar la opción denominada __Personalizada.__
    * Una vez finalizada la configuración dar click en el boton **Hecho**
2. En el menu grafico de **Pariticionado Manual,** buscar el recuadro denominado __Nueva instalación de CentOS Linux 8.0.1905.__
    * Buscar en el listbox la opción de **Partición Manual.**.
    * Seleccionar el boton de **Añadir un nuevo punto de montaje** que esta caracterizado con el signo de _mas(+)._

## Montaje

1. En la ventana modal denominada **Añadir un punto de montaje nuevo**
    * En la opcion denominada _Punto de montaje:_ Seleccionar la opcción de File system root, identificada con una **diagonal(/).**
    * En la opción **Capacidad Deseada**, escribir **20 GB.**
    * Una vez creada la partición, en el menu gráfico Buscar la opción denominada **Sistemas de Archivos,** cambiar la opción por defecto de _xfs_ a  **ext1,** si no se encuentra esta opción buscar la mas proxima a _ext1._
2. En la ventana modal denominada **Añadir un punto de montaje nuevo**
    * En la opcion denominada _Punto de montaje:_ Seleccionar la opcción de Area de intercambio, identificada como **swap**
    * En la opción **Capacidad Deseada**, escribir **2 GB,** esto se debe asignar a la mitad del total de la memoria **Ram**
3. En la ventana modal denominada **Añadir un punto de montaje nuevo**
    * En la opcion denominada _Punto de montaje:_ Seleccionar la opcción de Archivos Variables, identificada como **/var**, en el **Sistemas de Archivos,** se deja por defecto _xfs._
    * En la opción **Capacidad Deseada**, dejamos en blanco para que tome el resto del almacenamiento.
4. Seleccionamos el boton de **Hecho**
5. Aparece un recuadro titulado **Resumen de cambios** y seleccionamos _aceptar._

## Redes

1. Cambiaremos el nombre del equipo de **localhost.localdomain** a _centos.universidadgj.com_
    * Selecionamos el boton de aplicar.
2. En la parte superios derecha, se debe activar la red Ethernet.

## Fecha

1. Seleccionar la región: **America**
2. Seleccionar la ciudad: **México**
3. Hora de red: Activar

## Software

1. Seleccionar **Servidor con GUI** en el recuadro de _Entorno Base_
2. Seleccionar:
    * Servidor Nativo de almacenamiento
    * Servidor de correo
    * Cliente de sistema de archivos de red
    * Servidores de red
    * Herramienas de rendimiento
    * Servidor web básico
    * Herramientas de desarrollo RPM
    * Herramientas gracias de Administración
    * Herramientas de seguridad
    * Soporte para targeta inteligente.
    * Herramientas del sistema
3. Dar click en **Empezar instalación**

## Usuarios

1. En el recuadro de ajustes de usuario, se debe configurar la contraseña root y la creación de un usuario.
    * Contraseña root: **sistemas12345**
2. Configuración de usuario:
    * Nombre completo: **Alfredo Rosales**
    * Nombre de usuario: **ghernandez**
    * Contraseña: **sistemasgaussjordan2020**
