## FUNCIÓN
|Característica principal |	Característica secundaria | Estudio del caso industrial |
|--------------------------|---------------------------|-----------------------------|
|  **Material** |PLA (polímero termoplástico): para el sistema de monitoreo.| Se utilizará para la carcasa del dispositivo de monitoreo, ofreciendo protección a los sensores, elementos de comunicación y componentes electrónicos contra condiciones ambientales externas como humedad y polvo. Este material termoplástico es adecuado para crear una estructura duradera y resistente para el equipo.|
|             |  Acero: para sujetar el sistemas un poste  |  Se utilizará acero para sujetar el sistema de monitoreo a un poste, asegurando la estabilidad y durabilidad de los sensores. Este material proporciona una base robusta y resistente a las condiciones ambientales, garantizando un montaje seguro y prolongado del dispositivo.|
| **Energía**              |Corriente continua (baterías de litio recargables)  | El sistema de monitoreo y control funcionará con energía proporcionada por baterías de litio recargables, las cuales serán alimentadas por un panel solar. Esto asegura un suministro energético autónomo y sostenible para el funcionamiento continuo del dispositivo, incluso en ubicaciones remotas. |  
|    **Señal**             | Analógica: para el registro de datos por parte de los sensores.| Los sensores que medirán los parámetros de calidad del aire emitirán señales analógicas continuas. Estos parámetros podrían incluir: Partículas en suspensión (PM2.5, PM10), Monóxido de carbono (CO).|
|                          |  Digital: transmisión vía Wi-Fi.| Los sensores de calidad del aire enviarán los datos a una plataforma en la nube a través de Wi-Fi, donde serán almacenados en una base de datos para su análisis y monitoreo en tiempo real. |
|**Definición de interfaces**  | Software en la nube  |   Los datos de los sensores de calidad del aire serán visualizados a través de un software o plataforma en la nube, accesible desde cualquier dispositivo con conexión a internet, permitiendo el control y monitoreo en tiempo real del sistema. |
|                          |   Interfaz manual |Se proporcionará una guía paso a paso para el uso, instalación y mantenimiento del dispositivo de monitoreo de calidad del aire, facilitando su correcta implementación y operación por parte del usuario. |
|     **Costos**           |        Regular                   |  El costo del sistema se mantiene dentro del alcance de los materiales o componentes utilizados, como los sensores, módulos de comunicación (Wi-Fi), y la infraestructura para el almacenamiento y visualización de los datos (plataforma en la nube). Esto garantiza que el sistema sea accesible y económicamente viable.                |


<p align="justify">
En esta sección, se detalla el comportamiento del sistema diseñado, que permite controlar el brillo de un LED mediante un potenciómetro y enviar los datos de manera remota a la plataforma ThingSpeak. Los datos se enviaron cada 15 segundos, y fueron visualizados mediante gráficas en la nube, donde La imagen muestra dos gráficos: uno para el brillo del LED (Campo 1) y otro para el potenciómetro (Campo 2). Los valores del potenciómetro oscilan entre 30 y 150, mientras que el brillo del LED fluctúa entre 20 y 60. Estos datos fueron capturados y enviados a ThingSpeak, lo que permitió su monitoreo remoto y en tiempo real. Los gráficos están alineados temporalmente, demostrando la relación directa entre los cambios en la resistencia del potenciómetro y el ajuste del brillo del LED, como se muestras continuación:
</p>

| Gráficas de ThingSpeak para el control del LED y potenciómetro.  | sfsfsffs|
|----------------------|--------------------------------------------|
|  https://github.com/user-attachments/assets/fe079d2d-f8fd-4d41-af07-30c82d5e0f4d |<img src="https://github.com/user-attachments/assets/1721ac16-f1f1-4fa7-a102-f23368447065" alt="ESP32 DEVKIT V1" width="8000"/> | 

 https://github.com/user-attachments/assets/fe079d2d-f8fd-4d41-af07-30c82d5e0f4d


<img src="https://github.com/nardyliz12/Proyectos_Para_Ingenieria_1/blob/main/Informes%20de%20laboratorio/Entregable_5/20240919_145938.jpg?raw=true" alt="Descripción de la imagen" width="550" />

<a href="https://github.com/nardyliz12/Proyectos_Para_Ingenieria_1/blob/main/Informes%20de%20laboratorio/20240919_154812~2.mp4?raw=true" style="padding: 10px 20px; background-color: #4CAF50; color: white; text-decoration: none; border-radius: 5px;">Ver Video</a>


|Node-Red|Flujo|
|---|----|
|Con los nodos y mqtt nosotros estamos publicando el mensaje equipo 10 por él tópico equipo 4, para luego poder recepcionar este mensaje en el sp32 e imprimirlo por el monitor serie, además, con los nodos de mqtt y debug nos suscribimos al topico "OutTopic" y mostramos el mensaje en la sección debug de mensajes, ya que a través de este topico estariamos enviando desde el ESP32 el mensaje "equipo 4" más un número que indica la cantidad de mensajes que podríamos mandar al ejecutarlo.    |<img src="https://github.com/user-attachments/assets/3adf020f-b44f-4ca9-8c46-0b71dc4cf365" alt="ESP32 DEVKIT V1" width="5000"/> |
