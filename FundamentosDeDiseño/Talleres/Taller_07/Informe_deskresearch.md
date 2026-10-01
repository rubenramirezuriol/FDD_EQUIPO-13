<div align="center">


<strong>UNIVERSIDAD PERUANA CAYETANO HEREDIA</strong>


Facultad de Ciencias e Ingeniería

<br>

<img src="../../Recursos/Imagenes/logo-upch.jpg"
     alt="Logo UPCH"
     width="150">

<br><br>
FUNDAMENTOS DE DISEÑO

TALLER 03
<br><br>
INFORME- DESKRESEARCH

<br>

PROFESORES:

<br>

<em>Marco Antonio Mugaburu Celi</em>

<em>Jose Luiz Da Silva</em>

<em>Jhomer Rodrigo Contreras Paucca</em>
<br><br><br>

PRESENTADO POR:

RAMIREZ URIOL RUBEN MOISES ENMANUEL



PUMA CUTIPA WILL ALEX



CHAVEZ ALIAGA ALDAIR ALEXANDER



ALVAREZ HANAMPA YESSICA



SÁNCHEZ MORÓN ANGELI DARIANA

<br><br><br><br>
2026

<br><br>

</div>

**Índice** 

1.Problemática……………………………………………………………  
	1.2 Pregunta de Diseño………………………………………….  
2.Matriz Desk Research…………………………………………………..  
3.Lista de Exigencias……………………………………………………..  
4.Caja negra………………………………………………………………  
5.Identificación preliminar de funciones principales…………………….  
6.Conclusión……………………………………………………………...

**1\. Problemática.**

La agricultura desarrollada en la zona costera del valle Chancay-Huaral, provincia de Huaral, departamento de Lima, se desarrolla bajo condiciones climáticas áridas y depende del riego para satisfacer las necesidades hídricas de los cultivos. En esta zona se encuentra la Estación Experimental Agraria Donoso del Instituto Nacional de Innovación Agraria (INIA), donde se han desarrollado investigaciones relacionadas con cultivos hortícolas y manejo agrícola. Asimismo, existen antecedentes experimentales específicos del cultivo de lechuga (*Lactuca sativa* L.) realizados en las instalaciones de la EEA Donoso, lo que sustenta la selección de este cultivo como caso de estudio para el proyecto \[1,2\].

Para el presente proyecto se delimita el sistema a una parcela de cultivo de lechuga (*Lactuca sativa* L.) en campo abierto, ubicada en la zona agrícola del valle Chancay-Huaral. Como condición edáfica de referencia se consideran suelos agrícolas de origen aluvial asociados a Fluvisoles y Regosoles éutricos, reportados en la EEA Donoso, con predominancia de características arenosas y variabilidad espacial en propiedades relacionadas con la fertilidad y disponibilidad de agua \[3\]. Esta condición resulta relevante para la gestión del riego, debido a que las propiedades físicas del suelo influyen en la capacidad de almacenamiento y disponibilidad de agua para el cultivo.

En este contexto, el problema técnico se centra en la dificultad para determinar de manera dinámica cuándo y cuánto regar una parcela de lechuga considerando simultáneamente las condiciones actuales del suelo, las variables microclimáticas, las condiciones meteorológicas y el comportamiento histórico del cultivo. Una programación de riego basada principalmente en frecuencias o cantidades preestablecidas puede no representar adecuadamente las variaciones temporales y espaciales de las condiciones de la parcela. Esta necesidad adquiere relevancia en un contexto nacional donde, según la Encuesta Nacional Agropecuaria 2023, sólo el 15,8 % de la superficie agrícola presentó riego tecnificado \[4\].

Por ello, el desafío de diseño consiste en desarrollar un sistema capaz de adquirir información directamente de la parcela mediante sensado inalámbrico, integrar dicha información con datos meteorológicos e históricos y procesarla de manera centralizada en un Gateway. El SENAMHI dispone de datos hidrometeorológicos y estaciones de monitoreo para el departamento de Lima, los cuales pueden utilizarse como fuente complementaria de información meteorológica para el sistema \[5\].

A partir de la integración de estas fuentes de información, HydroAdapt plantea incorporar modelos de Machine Learning para identificar relaciones entre las condiciones de la parcela y su comportamiento hídrico, con el objetivo de estimar la demanda hídrica y apoyar la generación de decisiones adaptativas de riego. La literatura reciente señala que los sistemas de riego inteligente basados en IoT y Machine Learning pueden integrar información del suelo y del ambiente para apoyar la toma de decisiones; sin embargo, también identifica como desafíos la calidad de los datos, la generalización de los modelos y su validación en condiciones reales \[6\].

En consecuencia, el problema técnico de HydroAdapt no se limita a la medición de variables agrícolas, sino a la integración de adquisición de datos, comunicación inalámbrica, procesamiento, predicción, decisión, actuación y retroalimentación dentro de un sistema adaptativo de gestión hídrica.

### **1.2 Pregunta de diseño**

> ¿Cómo diseñar un sistema inalámbrico y adaptativo de gestión hídrica para una parcela de cultivo de lechuga (*Lactuca sativa* L.) en la zona costera del valle Chancay-Huaral, que integre las condiciones edáficas, variables microclimáticas, información meteorológica e históricos de la parcela mediante procesamiento local en un Gateway y modelos de Machine Learning, con el fin de generar decisiones de riego ajustadas a las condiciones cambiantes del cultivo?

**Delimitación Técnica del Proyecto**

| Aspecto | Delimitación |
| :---- | :---- |
| Ubicación | Zona agrícola costera del valle Chancay-Huaral, provincia de Huaral, Lima  |
| Unidad de estudio | Parcela agrícola de campo abierto  |
| Cultivo | Lechuga (*Lactuca sativa* L.)  |
| Tipo de suelo de referencia | Suelo agrícola de origen aluvial, asociado a Fluvisoles y Regosoles éutricos; se considerará como referencia una condición de textura predominantemente arenosa/franco-arenosa, sujeta a caracterización de la parcela.  |
| Gestión evaluada | Riego agrícola  |
| Variables locales  | Variables edáficas y microclimáticas relevantes para estimar la disponibilidad y demanda hídrica  |
| Información externa | Datos meteorológicos de SENAMHI  |
| Información Histórica | Registros de condiciones de la parcela, eventos de riego y respuesta del sistema  |
| Comunicación | Adquisición y transmisión inalámbrica de información  |
| procesamiento  | Concentrado principalmente en un Gateway  |
| inteligencia del sistema | Modelos de Machine Learning para estimación/apoyo a la decisión de riego  |
| Actuación | Generación de una señal de decisión o control sobre el sistema de riego  |
| Retroalimentación | Uso de nuevas mediciones y resultados del riego para actualizar el proceso de decisión  |

**2\. Matriz de Desk Research en el marco de metodología VDI**

| Nº | Fuente  | Autor/Ins titución  | Año | Referencia  | Estado de tecnología encontrado  | Exigencia o requisito identificado  | Restricción o limitación  | Función principal  | Aplicación al proyecto  |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| 1 | Patente | Manna Irrigation Ltd. Inventores: Ofer Beeri y Shay Mey-Tal  | 2025 | EP 3 648 574 B1  \[7\] | Riego de precisión con sensores, datos meteorológicos e históricos.  | Integrar datos del cultivo, clima e historial de riego.  | Sensores puntuales pueden no representar toda la parcela; algunos métodos son costosos.  | Determinar cuándo y cuánto regar.  | Base para integrar sensores, clima e históricos en HydroAdapt.  |
| 2 | Patente | Taizhou Suzhong Horticulture Co., Ltd.  | 2025 | CN119739078A  \[8\] | Sistema de riego por zonas con Machine Learning.  | Usar humedad, temperatura, lluvia, tipo y etapa del cultivo.  | Diseñado para invernaderos y con varios módulos, aumentando la complejidad.  | Predecir y ajustar automáticamente el agua de riego.  | Referencia para ML y manejo por microzonas en HydroAdapt.  |
| 3 | Patente | Northwest A\&F University  | 2026 | CN121303433A \[9\]  | Predicción diaria de demanda de riego con teledetección y datos meteorológicos.  | Integrar ET₀, lluvia, Kc, etapa del cultivo y datos históricos/meteorológicos.  | Requiere múltiples fuentes de datos y corrección de errores entre ellas.  | Calcular la necesidad neta de riego por parcela.  | Aporta a HydroAdapt el uso de datos meteorológicos y del cultivo para anticipar la demanda hídrica.  |
| 4 | Producto Comercial | CropX Technologies  | 2024  | Strato 1 (CropX) \[10\] | Estación agrícola con sensores de clima, energía solar y transmisión celular.  | Medir temperatura, humedad, viento, precipitación y radiación.  | Depende de conectividad celular y alimentación propia.  | Obtener datos meteorológicos hiperlocales.  | Referencia para integrar variables climáticas al modelo de riego de HydroAdapt.  |
| 5 | Producto Comercial | FloraPulse  | 2026 | FloralPulse \[11\] | Microtensiómetro instalado en la planta para medir continuamente su estado hídrico.  | Medir potencial hídrico del tallo de forma continua.  | Requiere instalación directa en el tejido vegetal y está orientado principalmente a árboles y vides.  | Detectar estrés hídrico de la planta.  | Referencia para decidir el riego según el estado real del cultivo.  |
| 6 | Producto Comercial | CropX Technologies  | 2026 | CropX soil sen-sor \[12\] | Sensor de suelo que mide humedad, temperatura y conductividad eléctrica y transmite los datos a una plataforma.  | Medir condiciones de la zona radicular a diferentes profundidades.  | Requiere instalación en suelo, batería y sistema de telemetría.  | Monitorear disponibilidad de agua y condiciones del suelo.  | Referencia directa para sensores de humedad de HydroAdapt y monitoreo por microzonas.  |
| 7 | Tesis | Atoccsa Gomez, R. B.  | 2025 | Atoccsa Gomez \[13\] | Riego deficitario aplicado por goteo para reducir el uso de agua.  | Controlar el volumen de agua aplicado y comparar tratamientos de riego.  | Estudio específico en durazno y bajo condiciones experimentales concretas.  | Reducir aportes hídricos sin afectar excesivamente el rendimiento.  | Aporta una referencia para evaluar ahorro de agua y comparar estrategias de riego.  |
| 8 | Tesis | Anci Yep, J. A.  | 2025 | Tesis Univ. de Lima \[14\] | Sistema de riego automatizado con IoT y ML para Solanum lycopersicum.  | Medir humedad del suelo y temperatura, y usar datos para calcular el agua de riego.  | Aplicado a tomate y a agricultura urbana.  | Ejecutar el riego automatizado mediante microcontroladores e integración de modelos predictivos de consumo hídrico | Aporta el diseño del algoritmo predictivo para estimar la cantidad exacta de agua a regar según variables del microclima local  |
| 9 | Tesis | Lavado Tisza, K., & Moran Retamozo, G. L.  | 2025 | Tesis UNH  \[15\] | Sistema IoT con ESP32, sensores, válvulas solenoides y plataforma web.  | Integrar sensores de flujo, sensores ultrasónicos, actuadores y conectividad Wi-Fi.  | Depende de conectividad y de una red de sensores/actuadores.  | Monitorear y controlar el riego desde una plataforma centralizada.  | Ofrece un diseño de arquitectura de hardware/software de bajo costo frente a problemas de escasez hídrica. |
| 10 | Artículo científico | Puig et al.  | 2025 | Puig et al.  \[16\] | Plataforma AquaCrop-IoT  | Requiere cámaras RGB, imágenes de cobertura del dosel y pronósticos climáticos a 7 días. | Limitado a rangos de temperatura de 8.4 a 28.1 ºC y ET de 1.1 a 7.6 mm/dia en el estudio | Integrar AquaCrop con visión artificial para ajustar el riego según el estado real del cultivo  | Referencia para integrar visión artificial y datos climáticos para reducir hasta 32% de agua.  |
| 11 | Artículo científico | Custódio y Prati.  | 2025 | Custódio y Prati \[17\] | Predicción de humedad del suelo con IoT y Machine Learning.  | Necesidad de series temporales de datos de humedad/temperatura a distintas profundidades  | Requiere conjuntos de datos continuos (datos de 2 años); algoritmos complejos no siempre superan modelos simples. | Comparar modelos tradicionales (ARIMA) y de ML para predecir humedad del suelo  | Proporciona criterios para elegir modelos predictivos sencillos y efectivos en la toma de decisiones de riego  |
| 12 | Artículo científico | Gupta et al.  | 2024 | Gupta et al. \[18\] | Automatización de riego mediante IoT y algoritmos predictivos  | Sensores conectados a microcontroladores (Arduino) y procesamiento en tiempo real.  | Consumo energético del sistema ($\approx 13.1W$)  | Predecir necesidades de riego y controlar el suministro para optimizar consumo hídrico y energético  | Demuestra la factibilidad de ahorrar agua (aprox. 30%) con microcontroladores de bajo costo y baja variación de error (\<5%).  |
| 13 | Plataforma / fuente de datos institucional  | SENAMHI  | Actual | SENAMHI  \[5\] | SENAMHI dispone de datos meteorológicos descargables a nivel nacional.  | El sistema debe poder incorporar información meteorológica como variable contextual.  | Los datos de una estación meteorológica no necesariamente representan exactamente el microclima de una parcela.  | Adquirir/integrar información meteorológica  | Los datos de SENAMHI pueden utilizarse como fuente externa para contextualizar y entrenar/validar modelos.  |
| 14 | Artículo científico / revisión sistemática  | Autores del estudio  | 2025 | Revisión sistemática \[6\] | Se integran sensores IoT, comunicación y modelos de IA para monitoreo y toma de decisiones.  | La solución debe integrar adquisición, comunicación, análisis y actuación.  | Complejidad, costos, interoperabilidad y condiciones de conectividad pueden limitar la implementación.  | Integrar y decidir  | Refuerza la arquitectura multidisciplinaria propuesta por HydroAdapt.  |

**3\. Lista de exigencias**

| *LISTA DE EXIGENCIAS* |  |  | PÁGINAS: 6 |
| ----- | :---- | :---- | ----- |
|  |  |  | Edición: 2 |
| Proyecto: |  | Hydro Adapt – Sistema adaptativo de gestión hídrica para riego de precisión  | Fecha: |
|  |  |  | Revisado: |
| Cliente: |  | \- Mugaburu Celi, Marco Antonio \- Huanambal Sovero, Victor Alberto \- Zevillanos Begazo, Christian Giovanni \- Productor agrícola / Responsable de la parcela de lechuga | Elaborado por: Ramirez Uriol Ruben Moises Enmanuel (R.R) Puma Cutipa, Will Alex (W.P) Chavez Aliaga, Aldair Alexander (A.C) Alvarez Hanampa, Yessica (Y.A) Sánchez Móron, Angeli Dariana (A.S) |
| Fecha (cambios) | Deseo o Exigencia | Descripción | Responsable |
|  | E | FUNCIÓN PRINCIPAL: Gestionar adaptativamente el riego de una parcela de 24 m² de lechuga, dividida en 3 zonas de 8 m², mediante adquisición inalámbrica, procesamiento local, decisión, actuación y retroalimentación.  | Todos |
|  | E | GEOMETRÍA: El prototipo trabajará en una parcela de 6 × 4 m, con 3 zonas de 8 m². Los puntos de monitoreo deberán representar cada zona y el Gateway permanecer protegido del agua.  | A.S |
|  | E | CINEMÁTICA: El sistema deberá permitir controlar el suministro de agua correspondiente a cada una de las 3 zonas de riego. Como mínimo deberá contemplar los estados riego detenido y riego activo. El cambio entre ambos estados deberá realizarse mediante una señal de actuación generada por el sistema de control. La actuación hidráulica deberá evitar movimientos bruscos, desconexiones o condiciones que comprometan las conducciones durante el funcionamiento.  | A.C |
|  | E | FUERZAS: Los elementos instalados en campo deberán soportar las condiciones mecánicas propias de la parcela y mantenerse estables durante el funcionamiento. Las estructuras de soporte deberán resistir peso propio, manipulación, presión y vibraciones asociadas al sistema de riego, evitando desplazamientos que alteren la posición de los puntos de monitoreo. El sistema hidráulico deberá soportar las condiciones de presión requeridas para distribuir agua a las 3 zonas de 8 m² sin pérdidas que comprometan la operación.  | R.R |
|  | E | ENERGÍA: El sistema deberá disponer de energía suficiente para garantizar el funcionamiento continuo de sus subsistemas. Se considera:   1\) alimentación eléctrica: suministro para Gateway, adquisición y comunicaciones. 2\) energía para procesamiento: requerida para integrar y procesar los datos. 3\) energía para comunicación: requerida para transmitir información inalámbricamente. 4\) energía para actuación: requerida para ejecutar las órdenes de riego. 5\) pérdidas: considerar disipación de energía principalmente en forma de calor. Como referencia para el prototipo podrá emplearse una alimentación de 220 V AC / 60 Hz, sin definir aún la arquitectura energética final.  | W.P |
|  | E | MATERIA: La materia de ingreso al sistema será agua destinada al riego del cultivo de lechuga, la cual deberá ser distribuida hacia las tres zonas de la parcela. El cultivo de referencia estará constituido por aproximadamente 24 m² de lechuga, considerando una densidad preliminar de aproximadamente 22 plantas/m², equivalente a unas 528 plantas en total, aproximadamente 176 plantas por zona. La materia de salida será el agua aplicada al cultivo. El volumen de agua suministrado deberá responder a las condiciones determinadas por el sistema y no únicamente a un horario fijo. La demanda hídrica deberá considerar que los requerimientos de la lechuga varían según su etapa de desarrollo y las condiciones ambientales.  | A.S |
|  | E | Señales de entrada: Condiciones edáficas: información sobre el estado hídrico del suelo en cada zona de la parcela. Variables microclimáticas: información de las condiciones ambientales presentes en la parcela que pueden modificar la demanda hídrica. Datos meteorológicos: información proveniente de SENAMHI, utilizada como complemento para caracterizar las condiciones ambientales. Históricos de la parcela: registros previos de condiciones del suelo, variables ambientales, eventos de riego y respuesta del sistema. Información del cultivo: características y condiciones de desarrollo de la lechuga (*Lactuca sativa L.*) utilizadas para estimar sus necesidades hídricas. Disponibilidad hídrica: información sobre el agua disponible para determinar las condiciones de ejecución del riego. Configuración y condiciones de operación: identificación de las zonas y parámetros establecidos para el funcionamiento del sistema. Señales de salida: Decisión de riego: determina si una zona requiere riego según las condiciones analizadas. Activación/regulación del riego: señal enviada al sistema de actuación para iniciar, detener o regular el suministro de agua en la zona correspondiente. Estado del sistema: información sobre el estado operativo de las zonas, como stand-by o riego activo. Alertas: información generada ante condiciones anómalas, fallas o situaciones que requieran atención. Retroalimentación: información obtenida de la respuesta del sistema después del riego, utilizada para apoyar las siguientes decisiones y el aprendizaje del modelo.  | Y.A |
|  | E | CONTROL: El sistema de control deberá permanecer estable durante las etapas de adquisición, transmisión, procesamiento, decisión, actuación y verificación. Deberá permitir generar decisiones diferenciadas para las 3 zonas de riego. La decisión no deberá depender exclusivamente de una medición instantánea, sino que deberá considerar la información disponible de la parcela y, cuando corresponda, información meteorológica e histórica. Después de la actuación, el sistema deberá verificar la respuesta obtenida y registrar esta información como retroalimentación. El control básico deberá mantenerse aun cuando no exista conexión a Internet.  | R.R |
|  | E | ELECTRÓNICO (HARDWARE): Se deberá utilizar el hardware necesario para adquirir las variables de las tres zonas, acondicionar y procesar las señales, realizar la comunicación inalámbrica, almacenar información, ejecutar el procesamiento local y generar las señales necesarias para la actuación del riego. El Gateway deberá funcionar como unidad central de procesamiento, integrando la información proveniente de los puntos distribuidos de monitoreo y ejecutando localmente el procesamiento necesario para generar las decisiones. La selección del modelo específico de microcontrolador, sensores y dispositivos de comunicación se realizará posteriormente en la etapa de selección de principios tecnológicos.  | W.P |
|  | E | SOFTWARE: El software deberá permitir recibir, organizar y almacenar los datos actuales e históricos provenientes de las tres zonas, integrar información meteorológica, procesar las variables adquiridas y generar la decisión de riego. Se deberá incorporar un modelo adaptativo basado en Machine Learning que utilice información histórica y actual para mejorar la estimación de las necesidades de riego. El software deberá permitir registrar las decisiones generadas y la respuesta posterior de la parcela. La selección del algoritmo específico de Machine Learning se realizará después de evaluar las características y disponibilidad de los datos.  | A.C |
|  | E | COMUNICACIONES: Los puntos de monitoreo distribuidos en las tres zonas deberán comunicarse con el Gateway mediante un sistema inalámbrico, evitando la necesidad de utilizar cableado de comunicación distribuido por toda la parcela. La comunicación deberá permitir transmitir la identificación de la zona, los datos adquiridos y el estado de los puntos de monitoreo. El Gateway deberá asociar correctamente cada información recibida con su respectiva zona. El funcionamiento básico del sistema de control no deberá depender de una conexión permanente a Internet.  | Y.A |
|  | E | SEGURIDAD: Deberá existir una separación física entre el circuito hidráulico y el gabinete de control electrónico, evitando que salpicaduras, fugas o humedad entren en contacto con los elementos eléctricos y electrónicos. El usuario no deberá estar expuesto a conexiones eléctricas durante la manipulación normal del sistema hidráulico. El diseño deberá considerar protección frente a condiciones anormales de operación y evitar cortocircuitos ocasionados por contacto con agua.  | A.S |
|  | E | ERGONOMÍA: La disposición de los elementos deberá permitir que el usuario pueda instalar los puntos de monitoreo, energizar el sistema, iniciar una prueba, verificar el estado de las tres zonas, revisar la decisión de riego y detener el sistema sin procedimientos excesivamente complejos. La interfaz deberá presentar de manera comprensible el estado del sistema y la decisión correspondiente a cada zona. Los elementos de interacción deberán ubicarse de manera que no obliguen al usuario a manipular simultáneamente conexiones eléctricas y componentes hidráulicos húmedos.  | R.R |
|  | E | FABRICACIÓN: El prototipo deberá poder fabricarse mediante materiales, herramientas y procesos disponibles para el equipo en el contexto académico. Los componentes deberán ser adquiribles localmente, priorizando tiendas de electrónica y proveedores disponibles en Lima, y deberán poder reemplazarse individualmente en caso de falla. La fabricación deberá permitir separar físicamente la estructura, el sistema hidráulico, los elementos electrónicos y los puntos de monitoreo. Se evitará depender de procesos industriales especializados que dificulten la fabricación o reparación del prototipo.  | W.P |
|  | E | CONTROL DE CALIDAD: El diseño y fabricación deberán verificarse frente a las exigencias establecidas en esta lista. Antes de las pruebas integrales se deberá comprobar el funcionamiento de cada punto de adquisición, la transmisión y recepción de información, la identificación correcta de las tres zonas, el procesamiento de datos y la actuación del riego. Cada sensor utilizado deberá contar con un procedimiento de calibración en 2 puntos, tal como se establece en la lista preliminar del equipo. También deberán realizarse pruebas de comunicación antes de la instalación definitiva en la parcela.  | A.C |
|  | E | MONTAJE: El sistema deberá contar con conexiones desmontables que permitan armar y desarmar el prototipo sin deteriorar cables ni conexiones. Cada punto de monitoreo deberá poder identificarse durante el montaje para evitar que los datos de una zona sean asociados incorrectamente con otra. Los puntos de adquisición deberán instalarse de forma estable en el suelo. El Gateway deberá instalarse en una posición estable y protegida del agua. Las conexiones hidráulicas y electrónicas deberán poder manipularse sin comprometer la integridad de los demás subsistemas.  | R.R |
|  | E | TRANSPORTE: El prototipo completo deberá poder trasladarse entre la universidad y el lugar de pruebas. Los elementos electrónicos, hidráulicos y de adquisición deberán quedar protegidos durante el transporte. Las conexiones deberán organizarse de manera que no se produzcan roturas de cables, deformaciones de conducciones o daños en los puntos de monitoreo. El prototipo completo deberá ser transportable en un maletín o mochila estándar, manteniendo como condición que pueda ser posteriormente desplegado para trabajar en las tres zonas de la parcela.  | A.C |
|  | D | USO: El prototipo deberá utilizarse en una parcela experimental de 24 m², dividida en tres zonas de riego de 8 m², destinada al cultivo de lechuga (*Lactuca sativa L.*). El sistema estará orientado a condiciones agrícolas de la zona costera del valle Chancay-Huaral. Durante una prueba, el usuario deberá desplegar los puntos de monitoreo, energizar el sistema y permitir que HydroAdapt adquiera la información de las zonas para determinar si corresponde activar, mantener o detener el riego. La información meteorológica de SENAMHI será utilizada como información complementaria a las mediciones locales.  | A.S |
|  | E | MANTENIMIENTO: Los puntos de monitoreo deberán poder retirarse para realizar limpieza, inspección, calibración, reparación y sustitución. Los elementos que entren en contacto con suelo o ambiente agrícola deberán poder limpiarse después de cada prueba. El Gateway deberá permitir el acceso a sus componentes electrónicos para inspección y reemplazo. El diseño deberá facilitar la identificación de fallas asociadas a adquisición, comunicación, alimentación, procesamiento o actuación. La falla de un único punto de monitoreo no deberá implicar necesariamente el reemplazo completo del sistema.  | Y.A |
|  | E | COSTOS: El presupuesto total de materiales para el prototipo funcional de 3 zonas de riego deberá mantenerse entre S/ 250 y S/ 350, de acuerdo con la restricción económica establecida por el equipo. El presupuesto deberá considerar los elementos necesarios para adquisición de información, comunicación inalámbrica, procesamiento, alimentación, actuación, conexiones, estructura y sistema hidráulico. Se deberán priorizar componentes disponibles en el mercado nacional y evitar tecnologías cuyo costo sea incompatible con el presupuesto académico.  | W.P |
|  | E | PLAZOS: El proyecto deberá completar dentro de los plazos establecidos por la asignatura las etapas de diseño, selección de principios tecnológicos, adquisición de materiales, fabricación, programación, integración, calibración y pruebas. El prototipo deberá encontrarse operativo antes de la sustentación correspondiente y deberá ser capaz de demostrar el ciclo completo de adquisición → procesamiento → decisión → actuación → retroalimentación.  | Y.A |

**4\. Caja Negra**
<div align="center"><img src="../../Recursos/Imagenes/cajanegra.png" alt="Patente 2" width="240"></div><br><em>

# **5\. Identificación preliminar de funciones principales**

A partir del problema técnico definido, la información obtenida mediante el Desk Research, la lista de exigencias y la abstracción realizada mediante la caja negra, se identifican preliminarmente las funciones que debe cumplir HydroAdapt. Estas funciones se plantean independientemente de la selección de componentes o tecnologías específicas, de manera que posteriormente puedan asociarse con diferentes principios tecnológicos durante la fase de concepción.

La función general del sistema se establece como:

> Gestionar adaptativamente el riego de una parcela de cultivo de lechuga mediante la adquisición, integración y procesamiento de información agrícola y meteorológica, generando decisiones de riego ajustadas a las condiciones cambiantes de la parcela.

| Código | Función principal | Descripción |
| :---- | :---- | :---- |
| F1 | Adquirir información de la parcela  | Obtener información representativa de las condiciones edáficas y microclimáticas de la parcela de cultivo de lechuga.  |
| F2 | Adquirir información meteorológica y contextual  | Incorporar información meteorológica proveniente de fuentes externas, principalmente datos disponibles mediante SENAMHI, para complementar las mediciones locales.  |
| F3 | Transmitir información de manera inalámbrica  | Transferir los datos obtenidos desde los puntos de monitoreo hacia la unidad central del sistema mediante comunicación inalámbrica.  |
| F4 | Integrar y almacenar información  | Centralizar las mediciones locales, información meteorológica, registros históricos y parámetros de operación en el Gateway, manteniendo la trazabilidad de los datos.  |
| F5 | Procesar y analizar información  | Procesar la información integrada para identificar las condiciones actuales de la parcela y las relaciones relevantes para la gestión del riego.  |
| F6 | Estimar la demanda hídrica  | Emplear modelos de análisis y Machine Learning para estimar el comportamiento de la demanda hídrica del cultivo a partir de la información disponible.  |
| F7 | Determinar la decisión de riego  | Generar una decisión de riego considerando la información procesada, la estimación de demanda hídrica y las condiciones de operación del sistema.  |
| F8 | Ejecutar o regular el riego  | Transformar la decisión generada en una acción de control sobre el sistema de riego, de acuerdo con las condiciones establecidas.  |
| F9 | Monitorear la respuesta del sistema  | Obtener nueva información después de la aplicación del riego para verificar las condiciones resultantes en la parcela.  |
| F10 | Retroalimentar el proceso de decisión  | Utilizar los resultados obtenidos y los registros históricos para actualizar el análisis y mejorar progresivamente la capacidad adaptativa del sistema.  |
| F11 | Informar el estado del sistema  | Comunicar al usuario la condición del sistema, las decisiones generadas, el estado del riego y posibles situaciones que requieran atención.  |

### **6\. Conclusión**

El Desk Research permitió establecer los criterios técnicos y funcionales que orientarán la concepción de HydroAdapt. La revisión de artículos científicos, patentes, tesis y productos comerciales permitió identificar alternativas para integrar el monitoreo de la parcela, la información meteorológica y el análisis de datos en la gestión del riego. Asimismo, los antecedentes evidencian la necesidad de considerar la calidad de los datos, la conectividad y la validación de los modelos en las condiciones del cultivo.

A partir de estos hallazgos, se delimitó la propuesta a una parcela experimental de 24 m² de lechuga en el valle Chancay-Huaral, dividida en tres zonas de riego. El sistema deberá integrar adquisición inalámbrica de información, datos de SENAMHI y registros históricos mediante un Gateway de procesamiento local. El uso de Machine Learning estará orientado a estimar la demanda hídrica y apoyar decisiones de riego diferenciadas por zona, incorporando nuevas mediciones como retroalimentación.

La lista de exigencias, la caja negra y las funciones identificadas constituyen la base para comparar alternativas de solución durante la siguiente etapa de diseño. Esta selección deberá considerar seguridad, calibración, mantenimiento, operación básica sin conexión permanente a Internet y presupuesto disponible. La capacidad adaptativa y el posible ahorro de agua deberán comprobarse posteriormente mediante pruebas del prototipo.

### **Referencias bibliográficas**

1. Trujillo Ipanaque SE. Efecto de microorganismos benéficos como promotores de crecimiento y rendimiento en el cultivo de lechuga (*Lactuca sativa* L.), en el Valle de Huaral 2016 \[tesis en Internet\]. Chimbote: Universidad San Pedro; 2020 \[citado 24 sep 2026\]. Disponible en: [Efecto de Microorganismos Benéficos como promotores de crecimiento y rendimiento en el cultivo de Lechuga (Lactuca sativa L.), en el Valle de Huaral 2016](https://repositorio.usanpedro.edu.pe/items/2911adf4-9135-4eb7-b234-b71f868eddb4)  
2. Pinchi Torres CC. Determinación del comportamiento de cinco variedades de lechuga roja (*Lactuca sativa* L.) en el rendimiento bajo condiciones agroecológicas del valle Huaral 2015 \[tesis en Internet\]. Chimbote: Universidad San Pedro; 2019 \[citado 24 sep 2026\]. Disponible en: [Determinación del comportamiento de cinco variedades de lechuga roja (Lactuca sativa L.) en el rendimiento bajo, condiciones agroecológicas del valle Huaral 2015"](https://repositorio.usanpedro.edu.pe/items/2265730c-47af-4ed3-8bbf-0325492df141)  
3. Quispe-Matos KR, Carbajal-Llosa CM, Mejia-Maita SY, Chuchon-Remon RJ, Quiñones-Trejo RA, Samaniego-Vivanco TD, et al. Variación espacial de la fertilidad del suelo en la EEA Donoso \[Internet\]. Lima: Instituto Nacional de Innovación Agraria; 2026 \[citado 24 sep 2026\]. Disponible en: [Variación espacial de la fertilidad del suelo en la EEA Donoso](https://repositorio.inia.gob.pe/items/39a3868c-c2b8-4b2a-83a9-652a5450abe4)  
4. Instituto Nacional de Estadística e Informática. Encuesta Nacional Agropecuaria 2023 \[Internet\]. Lima: INEI; 2024 \[citado 24 sep 2026\]. Disponible en:  [https://proyectos.inei.gob.pe/iinei/srienaho/Descarga/DocumentosMetodologicos/2023-62/05\_PUBLICACION\_ENA\_2023.pdf?utm\_source](https://proyectos.inei.gob.pe/iinei/srienaho/Descarga/DocumentosMetodologicos/2023-62/05_PUBLICACION_ENA_2023.pdf?utm_source)  
      
5. Servicio Nacional de Meteorología e Hidrología del Perú. Descarga de datos meteorológicos e hidrometeorológicos \[Internet\]. Lima: SENAMHI; \[citado 24 sep 2026\]. Disponible en:  [https://proyectos.inei.gob.pe/iinei/srienaho/Descarga/DocumentosMetodologicos/2023-62/05\_PUBLICACION\_ENA\_2023.pdf?utm\_source](https://proyectos.inei.gob.pe/iinei/srienaho/Descarga/DocumentosMetodologicos/2023-62/05_PUBLICACION_ENA_2023.pdf?utm_source)

 

6. Younes A, Elamrani Abou Elassad Z, Meslouhi OE, Elamrani Abou Elassad D, Ed-dahbi AM. The application of machine learning techniques for smart irrigation systems: a systematic literature review. *Smart Agric Technol* \[Internet\]. 2024;7:100425 \[citado 24 sep 2026\]. doi:10.1016/j.atech.2024.100425. Disponible en: [La aplicación de técnicas de aprendizaje automático para sistemas de riego inteligentes: una revisión sistemática de la literatura \- ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2772375524000303)  
7. Beeri, O., & Mey-Tal, S. (2025). *Methods and systems for irrigation guidance* (European Patent No. EP 3 648 574 B1). European Patent Office [https://patents.google.com/patent/EP3648574B1/en?oq=EP3648574B1](https://patents.google.com/patent/EP3648574B1/en?oq=EP3648574B1)    
8. 仲少华, 周丽霞, & 阮剑平. (2025). *一种大棚节能用水监控系统* \[Sistema de monitoreo de ahorro de energía y agua para invernadero\] (Chinese Patent Application No. CN 119739078 A). China National Intellectual Property Administration. [https://patents.google.com/patent/CN119739078A/en](https://patents.google.com/patent/CN119739078A/en)   
9. 孙世坤, 武亚伟, 李冲, 葛茂生, 曹红霞, 陈俊英, & 边江. (2026). *多源遥感日尺度地块级作物灌溉需水预报方法及系统* \[Método y sistema de pronóstico diario de requerimientos de agua de riego a escala de parcela mediante teledetección multifuente\] (Chinese Patent Application No. CN 121303433 A). China National Intellectual Property Administration. [https://patents.google.com/patent/CN121303433A/en?oq=CN121303433A](https://patents.google.com/patent/CN121303433A/en?oq=CN121303433A)   
10. [CropX Hardware. CropX Digital Agronomy Platform and Farm Management System \[Internet\]. \[citado 3 de septiembre de 2026\]. Disponible en:](https://www.zotero.org/google-docs/?nUIc5F) [https://cropx.com/cropx-system/hardware/](https://cropx.com/cropx-system/hardware/)    
11. [Plant-Based Irrigation Sensors for Orchards & Vineyards \- FloraPulse \[Internet\]. \[citado 3 de septiembre de 2026\]. Disponible en:](https://www.zotero.org/google-docs/?nUIc5F)  [https://florapulse.com/](https://florapulse.com/)    
12. [CropX Digital Agronomy Platform and Farm Management System \[Internet\]. \[citado 3 de septiembre de 2026\]. Home. Disponible en:](https://www.zotero.org/google-docs/?nUIc5F) [https://cropx.com/](https://cropx.com/)  
13. Atoccsa Gomez, R. B. (2015). *Aplicación de riego deficitario de secado parcial de la zona de raíces en el cultivo de durazno mediante el riego por goteo* \[Tesis\]. [https://hdl.handle.net/20.500.12996/924](https://hdl.handle.net/20.500.12996/924)   
14. Anci Yep, J. A. (2025). *Sistema de riego automatizado para Solanum lycopersicum con IoT y modelos predictivos para el ahorro de agua en entornos urbanos* [https://repositorio.ulima.edu.pe/item/4aacc455-aca0-4e22-aeee-c7d89acc5dbe](https://repositorio.ulima.edu.pe/item/4aacc455-aca0-4e22-aeee-c7d89acc5dbe)  
15. Lavado Tisza, K., & Moran Retamozo, G. L. (2025). *Diseño de un sistema de IoT para optimizar el riego de la agricultura en el distrito de Viñas* \[Tesis\]. [https://hdl.handle.net/20.500.14597/26882](https://hdl.handle.net/20.500.14597/26882)   
16. Puig F, Garcia-Vila M, Soriano MA, Rodríguez-Díaz JA. AquaCrop-IoT: A smart irrigation platform integrating real-time images and weather forecasting. *Comput Electron Agric*. 1 de agosto de 2025;235:110372. doi:10.1016/j.compag.2025.110372  
17. Custódio G, Prati RC. Comparing modern and traditional modeling methods for predicting soil moisture in IoT-based irrigation systems. *Smart Agric Technol*. 1 de marzo de 2024;7:100397. doi:10.1016/j.atech.2024.100397  
18. Gupta S, Chowdhury S, Govindaraj R, Amesho KTT, Shangdiar S, Kadhila T, et al. Smart agriculture using IoT for automated irrigation, water and energy efficiency. *Smart Agric Technol*. 1 de diciembre de 2025;12:101081. doi:10.1016/j.atech.2025.101081