# 1-IBM-SLE-Gianca
Este repositorio es para que pueda probar que desde una imagen iso pueda crear una VM en VMware y en VPC

Entender los distintos instaladores de Suse
1. Existen una familia de productos:
- Esto aún no sé para que puede servir

2. Tipos de instalación:
-  Por internet: Utilizado si tienes conexión a SCC, RMT o SMT. Solo contiene el instalador. Durante la instalación, podrás seleccionar el producto a instalar y agregar funcionalidades mediante la activación de módulos adicionales. Requiere acceso a la red.
-  Sin internet: Contiene todos los paquetes, pero es grande. Útil para instalaciones sin acceso a Internet.

3. Existen 2 opciones de paquetes:
- GM (Gold Master): El paquete tal y como se lanzo en la fecha de su creación
  - Caso de uso: Si prefieres la estabilidad de una versión que ha sido ampliamente probada desde su lanzamiento, podrías optar por la versión 'GM'.
- QU (Quarterly Update): El paquete tal y como se lanzo JUNTO CON ACTUALIZACIONES DE SEGURIDAD TRIMESTRALES.
  - Caso de uso: Si tu hardware es más reciente o si simplemente prefieres tener todas las actualizaciones y parches más recientes desde el principio, la versión 'QU' sería la más adecuada.
 
4. Se puede usar en 4 arquitecturas:
- "x86_64": Para plataformas AMD64 e Intel* 64
- "s390x": Para IBM* z System o LinuxONE
- "ppc64le": Para la plataforma IBM* Power LE
- "aarch64": Para la plataforma Arm* 64

5. Para cada arquitectura hay 2 tipos de imágenes:
- Media1: Contiene paquetes binarios, que son versiones precompiladas del software. Los paquetes binarios están listos para ser ejecutados en tu sistema sin necesidad de compilarlos.
  - Caso de uso: Si solo necesitas instalar el sistema operativo, utiliza Media1. Esta te proporcionará todo lo necesario para una instalación estándar, incluyendo las aplicaciones y herramientas del sistema operativo.
- Media2: Esta imagen contiene el código fuente de los paquetes incluidos en el sistema operativo.
  - Caso de uso: Si eres un desarrollador o necesitas personalizar el software, podrías necesitar Media2 para acceder al código fuente de los paquetes y realizar las modificaciones necesarias. Es útil principalmente para desarrolladores o administradores de sistemas que necesitan modificar, personalizar o reconstruir aplicaciones específicas.

**
**
¿Cuál voy a utilizar?
PARA VPC
Sería el: 
- sin internet: ya que no quiero descargar nada y en caso no se pueda
- GM: porque no hay la otra opción para la arquitectura que voy a elegir
- s390x: porque es la única opción que hay para crear la imagen en IBM Cloud
- Media1: ya que no voy a personalizar nada.
Imagen objetivo a tener para subir a VPC: sles-15-sp3-s390x-byol

PARA VMWARE
Sería el:
- debería de funcionar cualquier versión


##Iniciando lo técnico
https://cloud.ibm.com/docs/vpc?topic=vpc-create-linux-custom-image

https://www.ibm.com/docs/en/powervc/1.4.4?topic=linux-installing-configuring-cloud-init-sles
https://softpanorama.org/Net/Linux_networking/Suse_networking/index.shtml
https://www.tencentcloud.com/document/product/213/9929

vboxuser
changeme

Administrador
12S@mir34

265551872
12208570368

VirtualBox convertfromraw file.iso file.vhd

##Probar con el freetrial
https://www.suse.com/products/sles-for-sap/download/index/
