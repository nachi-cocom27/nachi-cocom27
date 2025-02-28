🌡️ Monitor de Temperatura IoT con Raspberry Pi Pico W y ThingSpeak

📌 Descripción del Proyecto:
Este proyecto implementa un sistema de monitoreo de temperatura en tiempo real utilizando una Raspberry Pi Pico W y un sensor LM35. Los datos capturados se transmiten a la plataforma ThingSpeak, donde se visualizan en gráficos y se procesan mediante MATLAB Analysis para generar alertas cuando la temperatura supera un umbral predefinido. El objetivo principal es proporcionar una solución sencilla y eficiente para el monitoreo ambiental utilizando tecnologías de Internet de las Cosas (IoT).

🛠 Componentes Utilizados:
Raspberry Pi Pico W: Microcontrolador con Wi-Fi integrado, ideal para proyectos IoT.
Sensor de temperatura LM35: Sensor analógico que proporciona una salida proporcional a la temperatura ambiente.
ThingSpeak: Plataforma en la nube para almacenamiento y visualización de datos en tiempo real.
MATLAB Analysis: Herramienta de ThingSpeak para el procesamiento y análisis de datos utilizando MATLAB.

⚙ Instalación y Configuración:
1. Configuración del Hardware
Conectar el sensor LM35 a la Raspberry Pi Pico W según el siguiente esquema:

VCC: Conectar a VBUS (5V) en la Pico W.

GND: Conectar a GND en la Pico W.

VOUT: Conectar a GP26 (ADC0) en la Pico W.

3. Código en MicroPython:
El código en MicroPython se encarga de:
Conectar la Raspberry Pi Pico W a una red Wi-Fi.
Leer la temperatura en °C utilizando el sensor LM35.
Convertir la señal analógica del sensor a temperatura.
Enviar los datos a ThingSpeak en el campo field1.
Enviar datos cada 180 segundos.

Instrucciones:
Instalar MicroPython en la Raspberry Pi Pico W:
Descargar la última versión de MicroPython para Pico W desde el sitio oficial.
Seguir las instrucciones para instalar MicroPython en tu dispositivo.

Subir el código:
Utilizar el IDE Thonny para subir el archivo main.py al dispositivo.
Asegurarse de reemplazar los siguientes valores en el script:
WIFI_SSID: IZZ-48CC
WIFI_PASSWORD: PCH190808
API_KEY: Z2AIVYMSW6SGW3PF


5. Configurar ThingSpeak:
Crear un Canal en ThingSpeak.
Ingresar a ThingSpeak y crear una cuenta si aún no tienes una.
Crear un nuevo canal y habilitar Field1 para almacenar los datos de temperatura.
Agregar Gráficos para Visualización:
Crear una nueva gráfica en el canal y seleccionar Field1 para visualizar los datos de temperatura en tiempo real.
Configurar MATLAB Analysis:
Crear un nuevo script de MATLAB Analysis en ThingSpeak.
<img width="554" alt="image" src="https://github.com/user-attachments/assets/714e2c45-9f89-4874-8028-5d7461c91a23" />

Implementar el siguiente código para calcular el promedio de los últimos 10 datos y generar alertas si la temperatura supera 35°C:

4. Ejecutar el Sistema:
 Iniciar la Raspberry Pi Pico W  : 
 Encender el dispositivo y verificar que se conecta a la red Wi-Fi. 
 Comprobar que los datos se envían correctamente a ThingSpeak. 
 Monitorear los Datos en ThingSpeak  : 
 Acceder al canal de ThingSpeak y verificar que los datos de temperatura se actualicen en tiempo real. 
 Observar las alertas generadas por MATLAB Análisis en caso de que la temperatura supere el umbral. 

📷 Capturas de Pantalla:
Código en Thonny IDE
 <img width="800" alt="image" src="https://github.com/user-attachments/assets/d0653f4b-1312-4abf-a0f1-8d1056a7a6c9" />

Gráfica en ThingSpeak
 capturas de pantalla/thingspeak_chart.png 
MATLAB Análisis en ThingSpeak
 capturas de pantalla/matlab_analysis.png 

📜 Licencia:
 EEste proyecto es de código abierto y puedes modificarlo según tus necesidades.
 
📧 Contacto:
 Para cualquier duda o sugerencia, no hay tipos en contacto en   15210298@unimodelo.com . 

