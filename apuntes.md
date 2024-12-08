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

## Implementaciones existentes
[Fuente][8]

- Malaga: La empresa encargada es [ParkHelp][9], cuyos sensores combinan tecnología magnética y micro-radar.
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


## Referenciados
[1]: <https://store.arduino.cc/en-es/products/arduino-mega-2560-rev3>
[2]: <https://store.arduino.cc/en-es/products/arduino-nano>
[3]: <https://tienda.bricogeek.com/wifi/1033-nodemcu-v3-wifi-esp8266-ch340.html>
[4]: <https://www.amazon.es/s?k=SX1278+lora>
[5]: <https://how2electronics.com/lora-sx1278-esp8266-transmitter-receiver/>
[6]: <https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6301241>
[7]: <https://pdf.sciencedirectassets.com/271750/1-s2.0-S0959652620X00138/1-s2.0-S0959652620312282/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEIL%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJIMEYCIQCBs%2BJRJVMRAnzUnOcsB5O%2BBha7n7%2BG%2BJVOzyYwBZovdQIhAN1yee4s3wMmz3iXI7jH558L1dDnIl9HreWRZTcTf4tUKrMFCCsQBRoMMDU5MDAzNTQ2ODY1IgwXIL16mx0kdm7y0KsqkAWtrWBBimjlHUQs8h0U9MUsU%2BitHZOp%2FPJTb4vA0qzMO4yQDT9qg6zBWF2E1Xg96OuKonT4TQ2ODKCcRPAXX0WtiOBkIQckwy9Qwd7DLTj8kEd8HgiLe6x%2BZdfIpOI93QztHJ02IUQlHmuILId6ngli8SusTcXFMBcXdsr0BzPQHwOh%2B3LTFYcvaMjkqo5P9BhokId1gpdD2npw25VP9JqkUkAmrclXRWDHkj0HPRoVz%2FXPuqoOafsuqygRe9ZV4qZpR6odJOndS11nMIzxV1W4oH4ECw9y3jDL0PSN2flQrjpETR%2Bv4rEcqUw3gGQfGMRXeGEGxC%2FvQXfvGisOnwCZkPZOH25mQJIIkarZFLXmKjYfcNqtXG%2F6e6hdDXVNiUY0IuHVmvTU8mYFI3Vuab0L%2F8nQw5Z3ATIX7FXYQ9uQskHg7oMdAA5HRJSgpW%2F%2BzNQtRpHFmN90kBNaRbjzlR7fT%2BuMdhG4ExRgNQ7NSbI2AV3LweFQO845LcEKJHGmknx9t0ctTyI0U8x2r7edyaClB6bp5go4quOSijj4Y2Xipr8YvSwkOVjwKodjyqmuTLXV4zbTNMCM90Ci8A3laRG7iMbYTKfZTYWE7swgPfY7kz2Yu%2FGR0SZtd9V6xNQobzDurMQY31vbaOgSgKva9n5keUX9siy%2FUHiOhgl7x6GcaRdRWNeTO9UnlnS37ZZlFVCu7pB9w%2FfYffsaBFOx1WRPEBLB1IUqBZzKW1zdjpWsFAmqyPLOA8ztmjKP73cn5kURLcNfZ4czCA7hlL84s5XDfL7dXCGJGJ0NHLT92dtZ4jg0IMO0dpONtZ%2F7Oqd6GKbXjL54HBDMnnI642qR153Qzpxlmrgi%2FyOmnJLy1OqsOzDip5a6BjqwAeNg7STKc2wzfoe1AZOnNp2yZE77i3kUFg%2BuWr348TVk%2BVS38fT7kMfOp2VhB6WJqVpZ%2FU8yxnKrP9LiXmH%2Bpr%2B4%2FDJ7mMQhXN4rVJRWZzX9nYGoYlOpfSzBs3TUBZbUI53eTH1MZ4DtYlRdSkbRaN2e9tCwmB%2BvPTyhdZNEyGXf46dfFA3mS%2FN%2BMEwrIWN4NzDewy2VNabyXADldFyab2UGCIIMdtR4Am%2FOSv1tZkiH&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20241126T101825Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTY4QFCRHOB%2F20241126%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=6450df8926d973bbee9d01a8137757ed5757914951ac1fc15b98195f4567b9ee&hash=96fdf27651f4316ba89d02c435b0849316b916c6ed534418628b99307e5267ca&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S0959652620312282&tid=spdf-f6fa78f6-c338-4194-b218-586cb5e67d7c&sid=97a30216900c964be76bf555a9fbcaa5df19gxrqb&type=client&tsoh=d3d3LnNjaWVuY2VkaXJlY3QuY29t&ua=1f155e01585b5351525352&rr=8e8922630aa8e3b8&cc=es>
[8]: <https://link.springer.com/content/pdf/10.1007/978-3-319-59513-9.pdf>
[9]: <https://www.parkhelp.com/>
[10]: <https://www.libelium.com/>
[11]: <https://www.fybr.com/>
[12]: <https://urbiotica.com/>
[13]: <https://www.streetline.com/>
[14]: <https://www.smartparking.com/uk>
