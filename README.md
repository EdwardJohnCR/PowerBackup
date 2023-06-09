# Encendido Planta Eléctrica / Panel Trasferencia

_Este proyecto integra la planta eléctrica PREDASTOR de 120v,, Node-RED y un
panel de transferencia para crear un sistema de respaldo de energía eficiente y confiable. 
Proporciona una solución automatizada que garantiza un suministro continuo de 
electricidad durante los cortes en la red principal, brindando tranquilidad y 
seguridad en el suministro eléctrico._

## Descripción  🚀

Imagínate que tienes una planta eléctrica instalada para asegurar el suministro
de energía en caso de cortes eléctricos. Para facilitar su funcionamiento, Node-RED,
instalado un panel de transferencia, que permite cambiar automáticamente entre la
electricidad de la red principal y la generada por tu planta.

Cuando ocurre un corte de energía en la red, el panel de transferencia detecta este
evento y envía una señal a Node-RED. que actúa como el cerebro de tu sistema. Este 
flujo está programado para recibir la señal del panel de transferencia y tomar 
medidas inmediatas.

Cuando Node-RED recibe la señal de corte de energía, envía una orden a la planta
eléctrica para que se encienda. La planta se pone en marcha y comienza a generar
electricidad. Al mismo tiempo, Node-RED asegura que la planta esté funcionando 
correctamente y monitorea su rendimiento.

Una vez que la planta está generando energía estable, Node-RED envía una señal al
panel de transferencia para que cambie automáticamente a la electricidad generada
por la planta. Esto garantiza que todos los dispositivos continúen funcionando sin 
interrupción. Además, Node-RED te proporciona información en tiempo real sobre el 
estado de la planta eléctrica y el suministro de energía._


![](https://kikilma.net/transfer/Nodos_NODE_RED.png)



### Pre-requisitos 📋

_Instalacion de librerias_

 -node-red-dashboard
 -node-red-contrib-clock-generator
 -node-red-contrib-ui-clock
 -node-red-contrib-ui-led
 -node-red-node-random


- Abre tu navegador web y accede a la interfaz de Node-RED. Por lo general, 
puedes hacerlo ingresando la dirección IP de tu dispositivo seguida del 
puerto 1880 (por ejemplo, http://<dirección_IP>:1880).
- En la interfaz de Node-RED, haz clic en el botón de menú en la esquina 
superior derecha y selecciona "Manage palette" en el menú desplegable.
- Se abrirá la ventana "Palette Manager" que muestra las librerías actualmente 
instaladas en Node-RED. En esta ventana, selecciona la pestaña "Install" o "Add".
- En el campo de búsqueda, ingresa el nombre de la librería que deseas instalar
y presiona Enter o haz clic en el botón de búsqueda.
Aparecerán los resultados de búsqueda que coincidan con el nombre de la librería.
- Encuentra la librería deseada y haz clic en el botón "Install" junto a ella.
- Node-RED comenzará a descargar e instalar la librería y sus dependencias automáticamente.
- Esto puede llevar algún tiempo dependiendo del tamaño de la librería y la velocidad de tu conexión a Internet.
- Una vez que la instalación se complete sin errores, recibirás una notificación 
de que la librería se ha instalado exitosamente.




### Instalación 🔧


- Descarga el archivo EncendidoPlanta.json
- Abre el entorno de Node-RED en tu navegador web. Puedes acceder a él ingresando 
la dirección IP de tu dispositivo Raspberry Pi seguida por el puerto 1880 (por ejemplo, 
http://<dirección_IP>:1880).
- En la interfaz de Node-RED, haz clic en el botón de menú en la esquina superior 
derecha y selecciona "Import" en el menú desplegable.
- Se abrirá una ventana emergente. En esta ventana, selecciona la pestaña "Clipboard".
- Abre el archivo JSON que deseas importar en un editor de texto. Selecciona todo el
contenido del archivo EncendidoPlanta.json descargado.
- Vuelve a la ventana emergente de Node-RED y pega el contenido JSON en el área de texto.
- Haz clic en el botón "Import" para importar el flujo desde el archivo JSON. Aparecerá 
una vista previa del flujo importado.
- Para completar la importación, haz clic en el botón "Import" nuevamente en la parte 
inferior de la ventana.
- Node-RED procesará el archivo JSON y creará los nodos y conexiones correspondientes 
en el flujo. Una vez que se complete la importación, verás el flujo importado en tu 
área de trabajo principal.



## Construido con 🛠️


En el proyecto de la planta eléctrica y Node-RED, se integran varios componentes clave
para su funcionamiento. Se utiliza una Raspberry Pi 4 como la plataforma de control central,
que ejecuta el software Node-RED y coordina todas las acciones del sistema.
Para controlar el encendido y apagado de diferentes dispositivos, se utilizan dos bloques
de relé de 4 canales cada uno. Estos relés permiten activar o desactivar múltiples circuitos
eléctricos de manera segura y controlada.
Además de los bloques de relé, se emplean dos relés individuales para controlar los contactores.
Los contactores son dispositivos electromecánicos que permiten establecer o interrumpir el
flujo de corriente hacia la planta eléctrica. Los relés individuales se utilizan para activar
las bobinas de los contactores, permitiendo así el encendido o apagado del sistema de respaldo
de energía.
Es importante mencionar que se utiliza una fuente de alimentación de 5V con una capacidad de
corriente de 10A para garantizar un suministro estable y suficiente para todos los componentes
del proyecto. Esta fuente de alimentación proporciona la energía necesaria para alimentar tanto
la Raspberry Pi como los relés y contactores.


_Equipos_

* [PREDATOR](https://www.amazon.com/-/es/Generador-inversor-silencioso-tecnolog%C3%ADa-rodantes/dp/B0B54CV3MX) - Planta Electrica
* [RASPBERRY 4](https://www.amazon.com/-/es/Raspberry-modelos-2019-Quad-Bluetooth/dp/B07TC2BK1X/ref=sr_1_3?crid=1ULBO84TYBTGF&keywords=raspberry%2Bpi%2B4&qid=1686292458&sprefix=ras%2Caps%2C161&sr=8-3&th=1) - Raspberry 4
* [RELAY](https://www.amazon.com/-/es/SunFounder-protector-voltios-Arduino-Raspberry/dp/B00E0NSORY/ref=d_pd_di_sccai_cn_sccl_2_3/145-3560073-2391809?pd_rd_w=hyTBn&content-id=amzn1.sym.e13de93e-5518-4644-8e6b-4ee5f2e0b062&pf_rd_p=e13de93e-5518-4644-8e6b-4ee5f2e0b062&pf_rd_r=MQBKZZ8N1AWPSC677C4B&pd_rd_wg=2Kk9G&pd_rd_r=1a681198-236f-4bd8-8d58-ca89dd64aa47&pd_rd_i=B00E0NSORY&psc=1) - Block de 4 Realy
* [FUENTE DE PODER](https://www.amazon.com/-/es/LRS-50-5-Fuente-alimentaci%C3%B3n-conmutada-pulgadas/dp/B019GYOCMM/ref=sr_1_16?__mk_es_US=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1ATIB4F208XIP&keywords=fuente+de+poder+5v&qid=1686292582&sprefix=fuente+de+poder+5v+%2Caps%2C184&sr=8-16) - Fuente de poder
* [CONTACTORES](https://www.amazon.com/-/es/Shopcorp-Interruptor-contactor-amperios-auxiliar/dp/B07YN79331/ref=sr_1_10?__mk_es_US=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=STG239Y5JG0F&keywords=contactor+bobina+120+snider&qid=1686292925&sprefix=contactor+snyderbobina+120+snider%2Caps%2C126&sr=8-10) - Contactor
* [SERVOMOTOR](https://www.amazon.com/LewanSoul-LD-3015MG-est%C3%A1ndar-engranaje-autom%C3%B3vil/dp/B073F4TRSK/ref=sxin_16_pa_sp_search_thematic_sspa?__mk_es_US=%C3%85M%C3%85%C5%BD%C3%95%C3%91&content-id=amzn1.sym.e8a574bf-253e-499c-93e8-6d35a96f50eb%3Aamzn1.sym.e8a574bf-253e-499c-93e8-6d35a96f50eb&crid=1ARFPPXUWUMWD&cv_ct_cx=servo+motor+9+kilos&keywords=servomotor+9kilos&pd_rd_i=B073F4TRSK&pd_rd_r=1df5e7ca-be6e-40d4-903a-b6fb29f0dd1a&pd_rd_w=T7IuR&pd_rd_wg=lXvQZ&pf_rd_p=e8a574bf-253e-499c-93e8-6d35a96f50eb&pf_rd_r=FQK2KG5EKFM6DEBRQHVX&qid=1686292967&sbo=RZvfv%2F%2FHxDF%2BO5021pAnSA%3D%3D&sprefix=servomotor+9kilos%2Caps%2C173&sr=1-4-be8d29ef-546e-4f38-a2d4-6d64d539234f-spons&psc=1&spLa=ZW5jcnlwdGVkUXVhbGlmaWVyPUEzMzcyWklHTUJBWldNJmVuY3J5cHRlZElkPUEwOTg1OTUzM09GT01aTzJJRzlETyZlbmNyeXB0ZWRBZElkPUEwMDY3ODU1MVI1UUs5N0RIVlYwQiZ3aWRnZXROYW1lPXNwX3NlYXJjaF90aGVtYXRpYyZhY3Rpb249Y2xpY2tSZWRpcmVjdCZkb05vdExvZ0NsaWNrPXRydWU=) - ServoMotor
* [SWITCH](https://www.crcibernetica.com/start-stop-momentary-switch-with-indicator-light/) - Start Stop Switch

DIAGRAMA

![](https://kikilma.net/transfer/DiagramaTransferencia.png)

PROTOTIPO

![](https://kikilma.net/transfer/prototipo.jpeg)

## Instalando 📌
PANEL DE TRASNFERENCIA


![](https://kikilma.net/transfer/tablero1.jpeg)
![](https://kikilma.net/transfer/tablero2.jpeg)


DASHBOARD
![](https://kikilma.net/transfer/dashboard.png)



NODOS
![](https://kikilma.net/transfer/Nodos_NODE_RED.png)


PLANTA ELECTRICA

![](https://kikilma.net/transfer/planta.jpg)



## Licencia 📄

Este proyecto está bajo la Licencia (MIT) - mira el archivo [LICENSE.md](LICENSE.md) para detalles.


## Proxima Actualizacion 

- Coneccion MQTT
- Base de Datos
- Gráficas
- VPN (acceso remoto)

## Expresiones de Gratitud 🎁


* Comenta a otros sobre este proyecto 📢
* Invita una cerveza 🍺 o un café ☕, Gracias ...
* [Buy mea Coffee](https://buymeacoffee.com/edwardjohn)
* Dona con cripto a esta dirección: 1Fu7XSdHJqdwZSxy9zznbzw1iYWDDgupy2
* muchas gracias...

---
⌨️ con ❤️ por [Edward John](https://github.com/EwardJohnCR) 😊 🚀
