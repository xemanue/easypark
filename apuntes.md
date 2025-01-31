# Lista de la compra
## Controladores
- [Arduino Mega][1] = 43.16€
- [Arduino Nano][2] = 22.61€
- [NodeMCU][3] = 3.95€
- [STM32 Blue Pill] = 2.5€ - 3€
- [ATTiny85] = 1.5€ - 3€

## Modulos LoRa
- [SX1278][4] = 7.5€

---

# Como medir espacios


---

# Arquitectura
Cada sensor estaría formado por un ESP8266, un módulo SX1278 y el propio sensor. Habría un Arduino o similar como "nodo maestro", que procesaría la información recopilada por los sensores. Las conexiones se realizarían como en [5][5].

---

# Sensores
La referencia [7][7] contiene información acerca de sensores comerciales como el de [Libelium][10].

## GMR (magnetorresistivo)
Hay dos modelos principales:
- Saturado:
    - Necesita un mayor campo magnético para activarse.
    - Produce una respuesta binaria (on/off).
    - Menos sensible a pequeñas fluctuaciones en el campo magnético.
- Lineal:
    - Muy responsivo a pequeños cambios en el campo magnético.
    - Ofrece una respuesta quasi-lineal, lo que lo hace adecuado para aplicaciones que midan un rango de fuerzas magnéticas.

La referencia [6][6] contiene información acerca del uso de este tipo de sensor. En su introducción se destaca que uno de los principales problemas de usar sensores magnéticos es el delay que presentan las mediciones, llegando a tener problemas para detectar un cambio entre dos coches.

Se podría realizar una serie de pruebas para determinar la carga magnética aproximada de vehiculos de distinto tamaño, similar a [16][16]. De esta forma, basándonos en las mediciones, podríamos estimar con mayor precisión el tamaño del vehículo aparcado.

## Ultrasonidos

La única forma que he encontrado de medir los huecos sería usando un motor, como se muestra en [15][15]

---

# Implementaciones existentes
[Fuente][8]

- Málaga: La empresa encargada es [ParkHelp][9], cuyos sensores combinan tecnología magnética y micro-radar.
- Santander: La empresa encargada es [Libelium][10], cuyos sensores combinan tecnología magnética y micro-radar. Como protocolo de comunicación utilizan LoRaWAN.
- San Francisco: La empresa encargada es [Fybr][11], que usa tecnología magnética e IA.
- Niza, Valencia: La empresa encargada es [Urbiotica][12], que no especifica que tipo de tecnología usan. Tienen sensores para distintos tipos de protocolos, como NB-IoT o LoRa.
- Los Ángeles, Oakland: La empresa encargada es [StreetLine][13]. No proporcionan información acerca de sus sensores aparte de que usan machine learning.
- Londres: La empresa encargada es [SmartParking][14], que no proporciona información acerca de sus sensores.

---

# Enlaces
## Sin referenciar
- Trabajo que estudia distintas soluciones tecnológicas en el entorno del Smart Parking.
    [1]: <https://mdpi-res.com/d_attachment/applsci/applsci-09-04569/article_deploy/applsci-09-04569.pdf?version=1572245758>
- Ejemplos de sistemas reales que usan una arquitectura similar a la planteada.
    [2]: <https://smartparkingsystems.com/en/smart-parking-system/>
    [3]: <https://blog.fleximodo.com/2023/08/15/transforming-parking-with-fleximodos-innovative-iot-solutions/>
- Información acerca de los sensores GMR.
    [4]: <https://www.allaboutcircuits.com/industry-articles/understanding-how-gmr-sensors-enhance-vehicle-performance-and-safety/>
- Proyecto que pretende detectar espacios situando sensores en el coche que va a aparcar.
    [5]: <https://radar.brookes.ac.uk/radar/file/f12128ae-e7e3-4e1a-a630-c06784d075b6/1/fulltext.pdf>
- Información acerca de distintos tipos de sensores con respecto a su uso en exterior.
    [6]: <https://ijees.org/index.php/ijees/article/view/45/21>
- Implementación de Smart Parking usando NodeMCU.
    [7]: <https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8389415>
- Estudio que compara las características de distintos tipos de parkings inteligentes y de los sensores que usan.
    [8]: <https://www.sciencedirect.com/science/article/pii/S2210670718327173>


## Referenciados
[1]: <https://store.arduino.cc/en-es/products/arduino-mega-2560-rev3>
[2]: <https://store.arduino.cc/en-es/products/arduino-nano>
[3]: <https://tienda.bricogeek.com/wifi/1033-nodemcu-v3-wifi-esp8266-ch340.html>
[4]: <https://www.amazon.es/s?k=SX1278+lora>
[5]: <https://how2electronics.com/lora-sx1278-esp8266-transmitter-receiver/>
[6]: <https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6301241>
[7]: <https://www.sciencedirect.com/science/article/pii/S0959652620312282> 
[8]: <https://link.springer.com/content/pdf/10.1007/978-3-319-59513-9.pdf>
[9]: <https://www.parkhelp.com/>
[10]: <https://www.libelium.com/>
[11]: <https://www.fybr.com/>
[12]: <https://urbiotica.com/>
[13]: <https://www.streetline.com/>
[14]: <https://www.smartparking.com/uk>
[15]: <https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8658900>
[16]: <https://journals.sagepub.com/doi/pdf/10.1177/0361198105191700119?download=true>

