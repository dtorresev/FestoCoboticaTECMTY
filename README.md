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
3. **Open Project > Project Tree > Project >  Online access**: Verificar que el dispositivo (Robot) están agregados. (min 22.08 Webinar) Si no se muestra la dirección MAC [XX-XX-XX-XX-XX-XX] del dispositivo expandir cada dispositivo individualmente y se despliega la información. </br> <img src = "files/device_verif.png"> </br>
3.1. Verificar que la dirección IPv4 sea fija y esté en la misma red que el PLC y el UR. </br> <img src = "files/IPV4_info.png"  width ="50%">
4. **Accessible Device [XX-XX-XX-XX-XX-XX] > Online & Diagnostics > Functions > Assign IP Address**. Asignar una dirección IP al PLC para estar en la misma red. <img src = "files/IP_assign.png" width = "75%"> </br>
Check azul indica la transferencia correcta de los parámetros (Esquina inferior derecha). Si no aparece la dirección IP en el dispositivo: **Online Access > Ethernet Connection > Update accessible devices.** </br><img src = "files/IP_assign_2.png" width = "75%"> 
5. **Accessible Device [XX-XX-XX-XX-XX-XX] > Online & Diagnostics > Functions > Assign PROFINET Device Name**: Asignar nombre PROFINET (25:49). Introducir un device name. Con la tecla Tab se rellena el nombre convertido. Revisar check azul. El nombre del dispositivo debe haber cambiado al asignado como device name (Ejemplo: **plc_1 [192.168.0.1]** ) </br> <img src = "files/PROFINET_Assign.png" width = "75%">
> Realizar pasos 4 y 5 para el PLC y para UR.
6. Desde el Teach Pendant: Habilitar comunicación PROFINET. <img src = "files/PROFINET_TeachPendant.png" width = "75%"> </br>
> Cómo buena práctica al incluir un robot, renombrar Device Name con la serie del modelo y los últimos 4 dígitos del número de serie. (Ejemplo: **ur5e_0637**)
7. **Project Tree > Project > Add New Device > Controllers > SIMATIC S7-1500 > CPU > Unspecific S7-1500 CPU**: En caso de desconocer el CPU específico, utilizar Unspecific S7-1500 CPU. </br><img src = "files/ADD_PLC.png" width = "75%"> </br>
7.1 Activar licencia de TIA Portal. </br> <img src = "files/license.png" width = "50%">
8. **Project Tree > Project > PLC_1 [Unspecific CPU 1500 > Hardware detection for PLC_1] > Start Search** : Detectar la configuración del PLC de manera automática. </br> <img src = "files/detect_PLC.png" width = "50%"></br> <img src = "files/detect_PLC_2.png" width = "50%"> </br>
9. **PLC_1 > Properties > PROFINET Interface [x1] > Properties > Ethernet Addresses** </br> <img src = "files/PROFINET_Properties.png" width = "50%"> </br>

### FESTO Station


### UR Setup