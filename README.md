# Festo Cobótica TEC MTY
## About

## Tutorial

### SIEMENS PLC

>Starts at 14:53

UR5 a PLC Siemens

TIA Portal V20 </br>
<a href = "https://www.universal-robots.com/articles/ur/interface-communication/profinet-how-to-guide-e-series/" >  UR PROFINET HOW-TO GUIDE E-SERIES </a>

PLC de la familia 1500

Download: 
- <a href = "https://s3-eu-west-1.amazonaws.com/ur-support-site/160022/GSDML-V2.42-UR-PROFIsafe-20220517.xml.zip"> GSDML-V2.42-UR-PROFIsafe-20220517.xml.zip </a> archivo GSD.
- <a href = "https://s3-eu-west-1.amazonaws.com/ur-support-site/160022/GSDML-0361-0001-UR.bmp"> GSDML-0361-0001-UR.bmp </a> BMP para que se muestre en la interfaz de TIA Portal.
- <a href = "https://s3-eu-west-1.amazonaws.com/ur-support-site/160022/UR_datastruct.udt" >  UR_datastruct.udt </a> Simplifica el proceso de mapeo de los registros a utilizar.
- <a href = "https://s3-eu-west-1.amazonaws.com/ur-support-site/160022/pn-iomessage.pdf" >  pn-iomessage.pdf </a> PROFINET I/O message, describe acerca de los registros que se van a compartir.

Paso a paso:

1. Crear un proyecto nuevo. (V20, V18, V17, V16).
2. Tener conectados: Robot, PLC, PC mediante ethernet o red WiFi.
3. Open Project > Project Tree > Online access: Verificar que el dispositivo (Robot) están agregados. (min 22.08 Webinar) Si no se muestra la dirección MAC [XX-XX-XX-XX-XX-XX] del dispositivo expandir cada dispositivo individualmente y se despliega la información. </br> <img src = "files/device_verif.png"> </br>
3.1. Verificar que la dirección IPv4 sea fija y esté en la misma red que el PLC y el UR. </br> <img src = "files/IPV4_info.png"  width ="50%">
4. Accessible Device [XX-XX-XX-XX-XX-XX] > Online & Diagnostics > Functions > Assign IP Address. Asignar una dirección IP al PLC para estar en la misma red. <img src = "files/IP_assign.png" width = "75%"> </br>
Check azul indica la transferencia correcta de los parámetros (Esquina inferior derecha). Si no aparece la dirección IP en el dispositivo: Online Access > Ethernet Connection > Update accessible devices. </br><img src = "files/IP_assign_2.png" width = "75%">
5. Asignar nombre PROFINET


### FESTO Station


### UR Setup