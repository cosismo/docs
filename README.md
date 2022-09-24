Cosismo | Documentación 
=============

Documentación de productos Cosismo IoT

## Tabla de Contenido
- [Tarjetas de desarrollo / Placas / Dev Kits](#tarjetas-de-desarrollo)
  - [ESP32](#esp32)
    - [ESP32 Devkit](#esp32-devkit)
    - [ESP32 CAM](#esp32-cam)
    - [ESP32 Ethernet](#esp32-ethernet)
- [Sensores](#sensores)
  - [Acelerómetros](#acelerómetros)
  - [Presencia](#presencia)
  - [Distancia](#distancia)
  - [Ambiente](#ambiente)
    - [Temperatura y humedad](#temperatura-y-humedad)
- [Pantallas y LEDs](#pantallas-y-leds)
  - [Pantallas](#pantallas)
  - [LEDs](#leds)
- [Kits](#kits)
  - [ESP32](#esp32)
  - [Componentes](#componentes)
- [Soporte Técnico](#soporte)
  - [Levantar ticket de soporte](#levantar-ticket-de-soporte)


## Tarjetas de desarrollo
### ESP32
#### ESP32 Devkit
* [ESP32 Devkit  (DOIT y tipo C)](https://cosismo.github.io/esp32-devkit/)
* [Página con información sobre el ESP32 S3 Devkit](https://cosismo.github.io/esp32-s3/)
* [ESP32 C3 Devkit](https://cosismo.github.io/docs/) 
#### ESP32 CAM
* [ESP32CAM + tarjeta convertidor USB TTL externa](https://cosismo.github.io/esp32-cam/)
* [ESP32CAM WROVER](https://cosismo.github.io/esp32-cam/)
#### ESP32 Ethernet
* Este módulo originalmente está pensado como un módem ethernet-serial ttl controlado por comandos AT. De fábrica trae instalado un firmware para ello. Puedes leer la documentación aquí (al final hay dos pdfs, datasheet y comandos AT): [ESP32 Ethernet](https://www.seeedstudio.com/Ethernet-module-based-on-ESP32-series-WT32-ETH01-p-4736.html)
 El firmware no es libre, pero existe una librería que permite programar la placa con Arduino. [Librería Arduino](https://github.com/khoih-prog/WebServer_WT32_ETH01) Ten en cuenta que si la programas con Arduino no se podrá recuperar el firmware original, aunque la librería es mucho más completa y flexible. 
Para pogramarlo o interactuar con esta placa necesitas un convertidor USB-TTL a 3.3v como el ch340 o similares.  Para usar el firmware original de comandos AT se conecta a los pines RXD y TXD (cruzados hacia la PC). Si usas el Serial Monitor de Arduino utiliza 115200, "Both NL&CR". Al mandar el comando "AT" te regresará OK si todo es correcto. También al conectar al ethernet tomará una IP por DHCP. Para verificarlo manda el comando "AT+CIPETH_DEF?"  Te regresará añlgo similar a : '+CIPETH_DEF:"192.168.8.128","192.168.8.1","255.255.255.0"'
Para programarlo con Arduino hay que conectarse a los pines TX0 y RX0 y hacer un puente entre GND e IO0 antes de energizar la placa.  
En los dos casos se energiza con 5V. Importante es notar que se energiza con 5V pero los pines GPIO funcionan a 3.3V. No uses 5V para los GPIOs porque puedes dañarlo; así mismo no alimentes con 3.3V porqeu puede ser insuficiente para alimentar el módulo.

## Sensores
### Acelerómetros
* [Acelerómetro](https://cosismo.github.io/docs/)

### Presencia

### Distancia
#### Ultrasónicos
* [RCWL-1601](https://cosismo.github.io/docs/)
### Ambiente
#### Temperatura y humedad
* [DHT11](https://cosismo.github.io/docs/)

## Pantallas y LEDs
### Pantallas
#### ESP32 CAM
* Pantalla Oled Display 0.96 Pulgadas Azul 128x64 I2c Ssd1306 [Ejemplo para conectarla con el ESP32 con Arduino IDE](https://randomnerdtutorials.com/esp32-ssd1306-oled-display-arduino-ide/)
### LEDs
#### Direccionables
* [Aro 12 LEDS WS2812](https://cosismo.github.io/docs/)

## Kits
### Componentes
### ESP32

## Componentes
### Pasivos
### Activos

## Soporte
* [Levantar ticket de soporte]([https://cosismo.github.io/docs/](https://docs.google.com/forms/d/e/1FAIpQLSfQZ-D-aTh0BjX7JpnXqClg9zYEThP5shqdUF2iM632KE8zrA/viewform))


