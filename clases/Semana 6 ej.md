
### Tareas: 

- Haz un código que calcule para 3 departamentos distintos la cuenta del agua. Para ello, de input ten el consumo de $m^3$ de agua de cada departamento, calcula el costo según una tarifa de dinero por $m^3$, y devuelve como salida la cuenta de cada departamento y la cuenta total de los 3. Sigue un formato de este estilo:

```python
# inputs
metros_depto1 = int(input())
metros_depto2 = int(input())
metros_depto3 = int(input())
tarifa =

# process

cuenta_depto1 =
cuenta_depto2 =
cuenta_depto3 = 

# outputs

print("La tarifa del primer departamento es:", )
print("La tarifa del segundo departamento es:", )
print("La tarifa del tercero departamento es:", )
print("La tarifa total de los departamentos es:", )

```


- Queremos calcular el gasto semanal y mensual de ti y tu hermano, que ya salió de la universidad y ahora debe pagar pasaje adulto. Pide como input la cantidad de viajes que tú realizas a la semana, y la cantidad de viajes que tu hermano realiza, define como variable el pasaje que debe pagar cada uno, imprime el gasto semanal de cada uno, y el gasto mensual que tienen entre los dos. Usa una estructura de este estilo:

```python
# inputs


# process


# outputs

```

- Es final de semestre y te preocupa tu aprobación de todos los ramos. Por ello, generas un algoritmo que: pide como input 3 valores distintos de puntajes de solemnes obtenidos por ti. Define un puntaje total para todas las pruebas, y calcula la nota obtenida en cada una. Muestra el promedio entre las 3 solemnes.

```python
# inputs


# process


# outputs

```


-  Te importa el alza de la luz y quieres analizar tu consumo mensual. Pide 2 valores de consumo de kWh a lo largo de un mes. Muestra el promedio entre ambos y muestra el mayor valor de consumo entre los 2:

```python
# inputs


# process


# outputs

```

---



#### Semana 6 - Básico: Costo de agua por departamento

Enunciado: Pide al usuario los consumos de agua (m³) de tres departamentos y una tarifa ($/m³). Muestra el costo de cada departamento y el total.

m3_d1 = float(input("m³ Depto 1: "))
m3_d2 = float(input("m³ Depto 2: "))
m3_d3 = float(input("m³ Depto 3: "))
tarifa = float(input("Tarifa ($/m³): "))

costo_d1 = m3_d1 * tarifa
costo_d2 = m3_d2 * tarifa
costo_d3 = m3_d3 * tarifa
total = costo_d1 + costo_d2 + costo_d3

print("\n-- Resumen de costos --")
print("Depto 1: $", round(costo_d1, 0))
print("Depto 2: $", round(costo_d2, 0))
print("Depto 3: $", round(costo_d3, 0))
print("TOTAL:   $", round(total, 0))

# Semana 6 - Intermedio: Gasto en transporte RED


Enunciado: Solicita viajes por semana y tarifa (CLP por viaje). Calcula el gasto semanal y el gasto mensual asumiendo 4 semanas.

viajes_semana_mio = int(input("Viajes por semana: "))
viajes_semana_hermano = int(input("Viajes por semana: "))
tarifa_mio = int(input("Tarifa por viaje (CLP): "))
tarifa_hermano = int(input("Tarifa por viaje (CLP): "))

gasto_semana_mio = viajes_semana_mio * tarifa_mio
gasto_semana_hermano = viajes_semana_hermano * tarifa_hermano
gasto_mes_mio = gasto_semana_mio * 4 
gasto_mes_hermano = gasto_semana_hermano * 4 

print("\n-- Gasto estimado --")
print("Semanal: $", gasto_semana_mio + gasto_semana_hermano)
print("Mensual: $", gasto_mes_mio + gasto_mes_hermano)


# Bonus

puntaje_1 = int(input("Puntaje prueba 1: "))
puntaje_2 = int(input("Puntaje prueba 2: "))
puntaje_3 = int(input("Puntaje prueba 3: "))
puntaje_total = 100

nota_1 = puntaje_1 * 6/100 + 1
nota_2 = puntaje_2 * 6/100 + 1
nota_3 = puntaje_3 * 6/100 + 1

promedio = (nota_1 + nota_2 + nota_3)/3
print("Promedio es:", promedio)

# Semana 6 - Avanzado: Promedio y máximo de consumo eléctrico
Objetivo: Practicar múltiples entradas, un cálculo agregado y una salida clara, manteniéndolo simple (sin listas ni bucles todavía).
Enunciado: Lee cuatro valores de kWh (de cuatro semanas) y muestra el promedio y el consumo máximo.
k1 = float(input("kWh semana 1: "))
k2 = float(input("kWh semana 2: "))
k3 = float(input("kWh semana 3: "))
k4 = float(input("kWh semana 4: "))

promedio = (k1 + k2 + k3 + k4) / 4

max1 = k1 if k1 >= k2 else k2
max2 = k3 if k3 >= k4 else k4
maximo = max1 if max1 >= max2 else max2

print("\n-- Consumo --")
print("Promedio mensual (kWh):", round(promedio, 1))
print("Máximo semanal (kWh):  ", maximo)