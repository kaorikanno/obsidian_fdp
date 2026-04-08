

[[Indice]]

> [!NOTE] Contenidos
> Implementar algoritmos en Python utilizando estructuras básicas de un programa, entradas, salidas y pruebas simples.

---

## Objetivos:

- [ ] Aprender sobre Python como lenguaje introductorio.
- [ ] Analizar la estructura básica de un programa.
- [ ] Construir códigos con entradas y salidas.
- [ ] Correr nuestro primer código.

---

### ¿Qué es un lenguaje de programación?

Los lenguajes de programación son similares a nuestros idiomas; cuentan con un conjunto de reglas y su propio vocabulario, y debemos seguir estas reglas para que el nuestro código pueda entenderse.


---
## Python

![[Pasted image 20260406152838.png|217]]

Python es un lenguaje de programación interpretado, fácil de entender, versátil, utilizado para backend, inteligencia artificial, análisis de datos, etc. El software es gratuito y puede utilizar otros programas de programación por detrás.

---

![[Pasted image 20260406153935.png|321]]

Nació en los años 80 en los países bajos.

El nombre se basa en un grupo de comediantes llamado Monty Python.

---

- Bello es mejor que feo.
- Explícito es mejor que implícito.
- Simple es mejor que complejo.
- Complejo es mejor que complicado.
- Disperso es mejor que denso.
- Los errores nunca deberían dejarse pasar silenciosamente.
- A menos que hayan sido silenciados explícitamente.
- Si la implementación es difícil de explicar, es una mala idea.
- Si la implementación es fácil de explicar, puede que sea una buena idea.

---
#### Ventajas de Python

```python

print("Hello World")

```

---
#### ¿Qué diferencia hay entre pseudocódigo y Python?

¿Cómo harían un algoritmo en pseudo-código que diferencie entre un mayor o menor de edad?

---

Leer edad
Si edad > 18 entonces
    Mostrar "adulto"

---

```python
edad = 20
if edad > 18:
    print("es adulto")
```
---

Estamos logrando lo mismo que con pseudocódigo, pero con una sintaxis definida.

---
### Compiladores e intérpretes
   
El código de los programas que elaboramos se conoce como código fuente, pues este tomará un "traductor" para generar el código que la máquina pueda comprender.

Nuestros programas deben tratar de ser fáciles de leer para otros programadores, y fáciles de entender para los usuarios que van a ocuparlos. Debe entenderse qué datos deben ingresar, los errores que el usuario tiene, actividades que lleva a cabo el programa, errores durante la ejecución.

[[Compiladores vs intérpretes]]

---

### Variables:


Las variables son valores que vamos a asignar nosotros.

Ej:

	edad = 20

---
#### Algunas reglas...

- Pueden contener números y letras.
- No pueden comenzar con números.
- No pueden contener tildes o caracteres como @, :, ;, ¨, [,], etc


---

No pueden ser:

|                                                                                     |                                                                                       |                                                                                    |                                                                                   |                                                                                      |
| ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | --------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| - `and`<br>- `as`<br>- `assert`<br>- `async`<br>- `await`<br>- `break`<br>- `class` | - `continue`<br>- `def`<br>- `del`<br>- `elif`<br>- `else`<br>- `except`<br>- `False` | - `finally`<br>- `for`<br>- `from`<br>- `global`<br>- `if`<br>- `import`<br>- `in` | - `is`<br>- `lambda`<br>- `None`<br>- `nonlocal`<br>- `not`<br>- `or`<br>- `pass` | - `raise`<br>- `return`<br>- `True`<br>- `try`<br>- `while`<br>- `with`<br>- `yield` |

---

	y = 20
es menos entendible que:
	temperatura_inicial = 20

---

Algunas convenciones son:

- Comenzar con una letra minúscula
- Si consta de dos o más palabras, las siguientes parten con mayúscula
- No contener tildes, guiones altos u otros caracteres no alfanuméricos.

---

Ej:

- temperatura_inicial
- VelocidadMaxima
- numero1
- numeroDeEstudiantes

---

 Ej incorrectos:

- Temperatura
- Velocidadmaxima
- numero-de-estudiantes

---

### Instalación de python

Está en los compus, pero si quieren probar en sus casas
en estos compus, usar visual studio code, o el idle de python, pero ese se ejecuta línea por línea.



---
### ¿Cómo programar?

Intenten ahora ustedes escribir esto:

```python

print("Hello World")

```

Y ejecuten su código.

---

Escriban ahora esto:

```python
nombre = input("¿Cómo te llamas? ")
print("Hola", nombre)
```

---

Nuestro algoritmo anterior recibió un input y generó un output a partir de ello.

---

¿Cómo harían un algoritmo que recoja su edad y les diga que el próximo año tendrán 1 año más?

```python
edad = int(input("Edad: "))
edad_futura = edad + 1
print("El próximo año tendrás", edad_futura)
```

---
### Debuggeo

Uno puede entonces cometer errores ortográficos o gramaticales (de sintaxis) o errores de lógica.

``` python

nota1 = 7.0
nota2 = 6.0
promedio = nota1 + nota2 / 2
print(promedio)

```

---


El código debe probarse mediante el debuggeo (bugs= insectos), una verificación de nuestro código.

Donald Knuth comenta que los algoritmos no se leen, se siguen y se prueban. Debemos seguir nuestro código paso a paso, línea a línea, para descubrir errores y mejoras.

---

El proceso de verificación implica tres tareas:

- Prueba con datos convencionales: Ej: edad, 20 años.
- Prueba con datos no convencionales: Ej: edad, 105 años.
- Prueba con datos no válidos: Ej: edad, -20 años o ventite años.

---

```python
edad = int(input("Edad: "))
edad_futura = edad + 1
print("El próximo año tendrás", edad_futura)
```
---
Algo que podría ser útil para debuggear es analizar línea por línea el código: https://pythontutor.com/visualize.html#mode=edit



---
#### identación

```python
edad = 20
if edad > 18:
    print("es adulto")
```

---

#### ¿Por qué es útil?

- ayuda visualmente para saber qué idea es cuál.
- separa trozos de código.

---

#### Notas:

Pueden escribir comentarios en python que *no* van a ser leídos por el intérprete, ej:

---

``` python

# Este es un código para calcular el promedio de mis notas c:
nota1 = 7.0
nota2 = 6.0
promedio = (nota1 + nota2 / 2 # hay algo mal en esta línea, no sé qué será :c
print(promedio)

```

---
### Probemos cosas...

---

1.  Haz un algoritmo que pida el precio, pago y vuelto.
2. Haz un algoritmo que le pida a alguien su edad y calcule en qué año debería haber nacido aprox.
3. calcula el cambio de temperatura a celsius desde fahrenheit.
4. Pide las horas trabajadas, el salario por hora y calcula el pago.
5. Pide la cantidad de minutos que han pasado y calcula la cantidad de horas y minutos extra. 

---
## Objetivos:

- [ ] Aprender sobre Python como lenguaje introductorio.
- [ ] Analizar la estructura básica de un programa.
- [ ] Construir códigos con entradas y salidas.
- [ ] Correr nuestro primer código.

---
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

