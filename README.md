# Simulación del problema bancario

**Estudiante:** Daniela María Sánchez Sánchez 

**Asignatura:** Simulación

**programa:**  Ingeniería de desarrollo de software y base de datos

**Herramienta utilizada:** Python en Google Colab

## 1. Descripción del proyecto

En esta actividad desarrollé una simulación para analizar la atención de los usuarios de un banco que cuenta con tres cajeros.

El objetivo fue comparar diferentes formas de distribuir los cajeros para realizar pagos y retiros, teniendo en cuenta los tiempos de atención y de espera de los clientes.

Para desarrollar el ejercicio utilicé los datos y las probabilidades proporcionados en el laboratorio del profesor.

## 2. Datos utilizados

El banco trabaja durante ocho horas diarias y tiene tres cajeros disponibles.

Según el enunciado:

- El 70 % de los usuarios realiza retiros.
- El 30 % realiza pagos o consignaciones.
- Los usuarios se clasifican como rápidos, normales, lentos y muy lentos.
- Los tiempos de atención se generan utilizando distribuciones exponenciales.

Cada cajero atiende una persona a la vez y tiene su propia fila.

## 3. Desarrollo de la simulación

Utilicé Python y tomé como referencia el código `BankSimulation` compartido en el laboratorio.

Realicé algunas modificaciones para comparar las diferentes distribuciones de cajeros y calcular sus resultados.

Se ejecutaron **30 réplicas de ocho horas para cada configuración**, utilizando una semilla base de 2026 para poder repetir el ejercicio.

Comparé seis alternativas:

1. Tres cajeros mixtos.
2. Un cajero para retiros y dos para pagos.
3. Dos cajeros para retiros y uno para pagos.
4. Cuatro cajeros mixtos.
5. Dos cajeros para retiros y dos para pagos.
6. Tres cajeros para retiros y uno para pagos.

## 4. Resultados obtenidos

Los tiempos promedio de espera fueron:

| Configuración | Espera promedio |
|---|---:|
| 3 cajas mixtas | 0,66 minutos |
| 1 retiro + 2 pagos | 4,46 minutos |
| 2 retiros + 1 pago | 2,78 minutos |
| 4 cajas mixtas | 0,17 minutos |
| 2 retiros + 2 pagos | 0,59 minutos |
| 3 retiros + 1 pago | 2,50 minutos |

Al comparar los resultados, observé que las tres cajas mixtas ofrecen mejores tiempos de espera que las dos alternativas de cajas exclusivas con tres cajeros.

También encontré que la configuración de cuatro cajas mixtas reduce más la espera, pero sería necesario analizar los costos antes de contratar otro cajero.

## 5. Estrategia propuesta

Mi recomendación es mantener los tres cajeros atendiendo pagos y retiros, distribuyendo a los usuarios entre las filas disponibles.

Si el banco decide trabajar con cajas exclusivas, considero más conveniente asignar dos cajeros a retiros y uno a pagos. Sin embargo, se debe vigilar la fila de pagos, porque en esa configuración los usuarios pueden esperar aproximadamente ocho minutos.

También sería importante revisar los tiempos de espera periódicamente para identificar cuándo se necesita apoyo adicional.

## 6. Archivos del proyecto

En este repositorio se encuentran:

- El cuaderno de Python con el desarrollo de la simulación.
- Las gráficas de tiempos de atención, cantidad de usuarios y comparación de escenarios.
- Los archivos CSV con los resultados estadísticos y las réplicas.
- El documento académico con la metodología, los resultados, las gráficas y las conclusiones.
- El código utiliza las bibliotecas NumPy, Pandas, SciPy y Matplotlib.


## 7. Conclusiones

Con esta actividad pude comprender mejor cómo se utilizan las simulaciones para estudiar los tiempos de espera y la atención de los clientes.

Los resultados muestran que no siempre es necesario aumentar la cantidad de cajeros para mejorar el servicio. También influye la manera en que se organizan las filas y se distribuyen las operaciones.

Para este ejercicio, las tres cajas mixtas representan la alternativa más conveniente entre las opciones de tres cajeros analizadas.

Los datos corresponden a una simulación académica basada en el laboratorio. Para aplicar esta estrategia en un banco real sería necesario validar las llegadas, los tiempos de atención y los costos con información de la operación.
