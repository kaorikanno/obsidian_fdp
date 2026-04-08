### Tareas: 


- Escribe el pseudocódigo para comparar emisiones de bus vs auto compartido. y decidir cuál opción ocupar.
1. Piensa en los factores como kilómetros recorridos, y emisión de cada tipo de vehículo (no necesitas investigar cuánto emite cada tipo de vehículo, inventa un número).
2. Genera la matriz IPO y el seudocódigo de esto.

---

| **Input**                                             | **Process**                                                                                                                                                                                                                       | **Output**                |
| ----------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------- |
| - km<br>- emision bus por km<br>- emision auto por km | - emisiones totales recorrido bus = km × emision bus por km<br>- emisiones totales recorrido auto = km × emision auto por km<br>- comparar si emisiones totales recorrido bus es mayor o menor a emisiones totales recorrido auto | vehículo de menor emisión |

---

1. Leer km recorridos, emisión del bus por km y del auto por km
2. Calcular las emisiones de todo el recorrido en bus como recorrido_bus = km x emision_bus_km
3. Calcular recorrido_auto = km x emision_auto_km
4. Si recorrido_bus > recorrido_auto:
5. Mostrar "Auto"
6. Si recorrido_auto > recorrido_bus:
7. Mostrar "Bus"
8. En otro caso:
9. Mostrar "Da igual"


---

- Verifica la lógica desk-check del pseudocódigo anterior. 
1. Construye una tabla de trazas con 3 juegos de datos, una donde el auto genere más emisiones, otra donde el bus genere más emisiones y otra donde generen la misma cantidad de emisiones por km. 

---

| km  | emision_bus | emision_auto | recorrido_bus | recorrido_auto | output  |
| --- | ----------- | ------------ | ------------- | -------------- | ------- |
| 10  | 20          | 10           | 200           | 100            | auto    |
| 20  | 5           | 20           | 100           | 400            | bus     |
| 15  | 10          | 10           | 150           | 150            | iguales |

---

- Hacer la matriz IPO de "consumo de agua en casa". Calcular el consumo mensual de agua en $m^3$.
1. Usa la lectura anterior, la lectura actual y el costo del agua por $m^3$, y que de salida tenga el costo total y los $m^3$ consumidos.

---


| input                                                      | process                                                                     | output                                   |
| ---------------------------------------------------------- | --------------------------------------------------------------------------- | ---------------------------------------- |
| - lectura anterior<br>- lectura actual<br>- tarifa mensual | resta = lectura actual - lectura anterior<br>coste = tarifa mensual x resta | resta (es la cantidad de $m^3$)<br>coste |
