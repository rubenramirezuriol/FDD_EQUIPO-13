# LISTA DE EXIGENCIAS

**Proyecto:** HidroAdapt - Sistema Adaptativo de Riego Asistido por IA  
**Fecha:** 10/09/2026  
**Edición:** 01  
**Página:** 1 de 1  
**Revisado:** …......  
**Elaborado:** Ramirez, Puma, Chavez, Alvarez, Sánchez  

## Cliente

- Marco Antonio Mugaburu Celi
- José Luiz Da Silva
- Jhomer Rodrigo Contreras Paucca
- John Edward Esquiagola Aranda
- Agricultores pequeños y empresas agrícolas

## Lista de exigencias

| Fecha | Tipo | Categoría | Descripción | Responsable |
|---|---|---|---|---|
| 10/09/2026 | E | **FUNCIÓN PRINCIPAL** | Monitorear en tiempo real variables hídricas y ambientales en 3 microzonas de una parcela con riego, aplicando modelos adaptativos de IA para predecir la demanda de agua, autocalibrarse y automatizar el riego, logrando reducir el consumo hídrico en aproximadamente 30%. | Todos |
| 10/09/2026 | E | **GEOMETRÍA** | Envolvente de control central ensamblada en una caja de paso comercial estanca IP65 con dimensiones no mayores a 20 cm × 15 cm × 10 cm. | AS, AC, YA |
|  | E | **GEOMETRÍA** | Sensores de humedad de suelo colocados a una profundidad fija de la zona radicular, entre 10 cm y 20 cm, en macetas o parcelas de prueba. |  |
|  | D | **GEOMETRÍA** | Soportes o estacas impresas en 3D (PETG o ABS) para sostener y proteger los sensores de humedad y cables en la tierra. |  |
|  | E | **MATERIA** | Uso exclusivo de sensores de humedad para evitar la corrosión rápida por electrólisis en el suelo. | WP |
|  | E | **ENERGÍA** | Alimentación por batería. | RR |
|  | E | **SEÑALES - Entradas** | Señal de encendido: permite energizar el sistema electrónico, sensores y unidad de procesamiento. | YA, AC, RR |
|  | E | **SEÑALES - Salidas** | Señal de estado (Stand-by / Riego Activo): muestra la condición operativa del prototipo. | YA, AC, RR |
|  | E | **SEÑALES - Salidas** | Señal de actuación: activa o corta el flujo hídrico. | YA, AC, RR |
|  | E | **CONTROL** | Servidor web local. | AC |
|  | E | **ELECTRÓNICA (Hardware)** | Microcontrolador con conectividad Wi-Fi y Bluetooth. | WP |
|  | E | **SOFTWARE** | Modelo adaptativo que utilice datos históricos y actuales para ajustar futuras decisiones de riego. | AS |
|  | E | **COMUNICACIONES** | Mantener el control básico de riego aun cuando no exista conexión a Internet. | WP |
|  | E | **SEGURIDAD** | Separación física del circuito de agua y el gabinete de control electrónico para evitar cortocircuitos por salpicaduras. | RR |
|  | E | **FABRICACIÓN** | Todos los componentes deben ser adquiribles localmente (tiendas de electrónica de Lima / Mercado Libre) con presupuesto total del prototipo bajo. | AS |
|  | E | **CONTROL DE CALIDAD** | Proceso de calibración en 2 puntos para cada sensor. | AC |
|  | E | **MONTAJE** | Conexiones desmontables para poder armar, desarmar y transportar el prototipo a la universidad sin romper cables. | RR, YA, AS |
|  | E | **TRANSPORTE** | El prototipo completo debe ser transportable en un maletín/mochila estándar. | AC, WP |
|  | E | **USO** | El prototipo será colocado en un determinado espacio, se desplegarán los sensores y, luego de obtener la información, decidirá si se riega o no. | RR, YA |
|  | E | **MANTENIMIENTO** | Facilidad de limpieza de sensores con paño húmedo tras cada prueba de campo/maceta. | Todos |
|  | E | **COSTOS** | Presupuesto total de materiales para el prototipo funcional de 3 zonas de riego por debajo de S/ 250 - S/ 350, financiable entre los 5 integrantes del grupo. | Todos |
|  | E | **PLAZOS** | Ensamblaje, programación y pruebas del prototipo concluidos dentro de los plazos fijados por la asignatura. | Todos |

## Leyenda

- **E:** Exigencia
- **D:** Deseo
