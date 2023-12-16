# Practica ESP32 con DHT11
En este repositorio se muestra como usando la plataforma Wokwi programando una ESP32 con el sensor DHT11.
## Introducción 
### Descripción 
La *Esp32* la utilizamos en un entorno de adquision de datos, lo cual en esta practica ocuparemos un sensor (DTH11) para adquirir temperatura y humedad del entorno; Cabe aclarar que esta practica se usara un simulador llamado WOKWI.
### Material Necesario
Para realizar esta practica necesitas lo siguiente:
ºWOKWI
ºTarjeta ESP 32
ºSensor DHT11
### Instrucciones
Requisitos previos
Para poder usar este repositorio necesitas entrar a la plataforma WOKWI.
### Instrucciones de preparación de entorno
- 1.Abrir la terminal de programación y colocar la siguente programación:

-#include "DHTesp.h"
-#include <LiquidCrystal_I2C.h>

-const int DHT_PIN = 15;
-DHTesp dhtSensor;


void setup() {

Serial.begin(115200);
dhtSensor.setup(DHT_PIN, DHTesp::DHT22);
}

void loop() {

  TempAndHumidity  data = dhtSensor.getTempAndHumidity();
    Serial.println("Temp: " + String(data.temperature, 1) + "°C");
    Serial.println("Humidity: " + String(data.humidity, 1) + "%");
    Serial.println("---");
   delay(1000);
    }
- 2.Instalar la libreria de DHT sensor library for ESPx como se muestra en la siguente imagen.
![](https://github.com/AmaiCisneros/Practica-2/blob/main/Screenshot_20231216-090032.png)

-Hacer la conexion de DHT11 con la ESP32 como se muestra en la siguente imagen.

![](https://github.com/AmaiCisneros/Practica-2/blob/main/Screenshot_20231216-091256~2.png)
Instrucciónes de operación
Iniciar simulador.
Visualizar los datos en el monitor serial.
Colocar la temperatura y humedad dando doble click al sensor DHT11
Resultados
-
- Cuando haya funcionado, verás los valores dentro del monitor serial como se muestra en la siguente imagen:
![](https://github.com/AmaiCisneros/Practica-2/blob/main/Screenshot_20231216-091038.png)




