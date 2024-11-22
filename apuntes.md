> [!TODO]
> Echarle un vistazo al trabajo que tengo en marcadores.

# Controladores
- [Arduino Mega][1] - 43.16€
- [Arduino Nano][2] - 22.61€
- [NodeMCU][3] - 3.95€
- [SX1278][4] - 7.5€

---

# Arquitectura
## LoRa
Cda sensor estaría formado por un ESP8266, un módulo SX1278 y el propio sensor. Habría un Arduino o similar como "nodo maestro", que procesaría la información recopilada por los sensores. Las conexiones se realizarían como en [5][5].

---

# Sensores
## GMR (magnetorresistivo)
Hay dos modelos principales:
- Saturado:
    - Necesita un mayor campo magnético para activarse.
    - Produce una respuesta binaria (on/off).
    - Menos sensible a pequeñas fluctuaciones en el campo magnético.
- Lineal:
    - Muy responsivo a pequeños cambios en el campo magnético.
    - Ofrece una respuesta quasi-lineal, lo que lo hace adecuado para aplicaciones que midan un rango de fuerzas magnéticas.

---

# Enlaces
## Sin referenciar
- Proyecto que utiliza un Arduino Mega.
    [1]: <https://iopscience.iop.org/article/10.1088/1757-899X/830/2/022095pdf>
- Proyecto que usa un Arduino Mega como "maestro" y varios Arduinos Nano a los que conectar los sensores de distintos sectores.
    [2]: <blob:https://ijece.iaescore.com/497026f9-d90f-42ca-a4e6-b386e69e6566>
- Trabajo que estudia distintas soluciones tecnológicas en el entorno del Smart Parking.
    [3]: <https://mdpi-res.com/d_attachment/applsci/applsci-09-04569/article_deploy/applsci-09-04569.pdf?version=1572245758>
- Ejemplos de sistemas reales que usan una arquitectura similar a la planteada.
    [4]: <https://smartparkingsystems.com/en/smart-parking-system/>
    [5]: <https://blog.fleximodo.com/2023/08/15/transforming-parking-with-fleximodos-innovative-iot-solutions/>
- Información acerca de los sensores GMR.
    [6]: <https://www.allaboutcircuits.com/industry-articles/understanding-how-gmr-sensors-enhance-vehicle-performance-and-safety/>
 Proyecto que pretende detectar espacios de aparcamiento en la calle.
    [7]: <https://radar.brookes.ac.uk/radar/file/f12128ae-e7e3-4e1a-a630-c06784d075b6/1/fulltext.pdf>

## Referenciados
[1]: <https://store.arduino.cc/en-es/products/arduino-mega-2560-rev3>
[2]: <https://store.arduino.cc/en-es/products/arduino-nano>
[3]: <https://tienda.bricogeek.com/wifi/1033-nodemcu-v3-wifi-esp8266-ch340.html>
[4]: <https://www.amazon.es/s?k=SX1278+lora>
[5]: <https://how2electronics.com/lora-sx1278-esp8266-transmitter-receiver/>
