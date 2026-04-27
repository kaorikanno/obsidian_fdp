
[[Indice]]

> [!NOTE] Contenidos
> Aplicar operadores aritméticos y lógicos en expresiones correctamente estructuradas, evaluando su impacto en el flujo del programa en Python.

---

## Objetivos:

- [ ] Operadores: + - * / % // ** 
- [ ] Operadores lógicos: and, or, not
- [ ] Precedencia y evaluación.

---

### Operadores aritméticos:

| Operador | Nombre         | Ejemplo |
| -------- | -------------- | ------- |
| +        | Suma           | x + y   |
| -        | Resta          | x - y   |
| *        | Multiplicación | x * y   |
| /        | División       | x/y     |
| %        | Módulo         | x%y     |
| **       | Exponente      | x ** y  |
| //       | Cociente       | x//y    |

---
Ejercicio:

Generen un algoritmo que verifique si un número es entero o float, que indique si es par o impar, si es múltiplo de 3 o no, y genere una frase con las respuestas. Ej:

42 es un número entero, par, múltiplo de 3.

---

Se sigue la misma precedencia que las calculadoras y PAPOMUDAS. Es decir:

- ()
- **
- *,/,  //, %
- +, -

---

### Operadores relacionales:

Son aquellos operadores que nos permiten hacer comparaciones entre números:

- x == y
- x != y
- x > y
- x < y
- x >= y
- x <= y

---

Creen un algoritmo que reciba dos números y retorne si uno es mayor o menor. Ej: 

x = 2, y = 3

x es menor que 3.

---

### Operadores lógicos

Nos permiten relacionar diferentes afirmaciones o elementos entre sí:

| Operador | Nombre                                              | Ejemplo              |
| -------- | --------------------------------------------------- | -------------------- |
| and      | Devuelve True si ambos elementos son True           | True and True = True |
| or       | Devuelve True si al menos un elemento es True       | True or False = True |
| not      | Devuelve el contrario, True si es Falso y viceversa | not True = False     |

---

- and revisa si tanto lo de la izquierda y derecha son ciertos o se cumplen
- or revisa si al menos uno es cierto
- not revisa que no se cumpla

---

Ej: Un código que revise cómo abrigarme. Si está lloviendo, me pondré una chaqueta de agua, si no está lloviendo, pero hace frío, me pondré un chaleco. Si no hace frío y no llueve, no me abrigaré:

```python
lloviendo = True
frio = True

if lloviendo:
    print("Me pondré la chaqueta de agua")
elif frio and not lloviendo:
    print("Me pondré un chaleco")
else:
    print("No me abrigaré")

```

---

- Haz un código que revise nuevamente números. Si el número es divisible entre 3 y 5, que retorne "divisible entre 15". Si es 0 o negativo, que retorne, "no natural". Si es positivo y divisible entre 2, que retorne "es par".

Ej: 
- 60 es divisible entre 3 y 5, así que es "divisible entre 15", y también es par.
- -14 es "no natural"

---

- Haz una calculadora de IMC ($IMC = \frac{peso}{ altura^2}$), que entregue:

- Bajo peso: < 18.5
    
- Normal: 18.5 - 24.9
    
- Sobrepeso: 25 - 29.9
    
- Obesidad: >= 30

---

Haz un código que revise si alguien puede subirse o no a una atracción de fantasilandia:
Requisitos obligatorios:
    
- altura >= 1.20 **y** edad >= 12
- **o** (edad >= 8 **y** altura >= 1.0 **y** acompañado)

---
## Objetivos:

- [ ] Operadores: + - * / % // ** 
- [ ] Operadores lógicos: and, or, not
- [ ] Precedencia y evaluación.

---
### Tareas: 


Para que 3 números formen un triángulo, los dos lados menores deben cumplir que a + b > c, la desigualdad triangular. Haz un código que reciba 3 números y vea si pueden formar un triángulo, y si es equilátero (3 lados iguales), isósceles (2 lados iguales) o escaleno (todos diferentes). Si no es triángulo, devolver "No es un triángulo válido".

---

- Calcular el impuesto del 8% sobre un producto, y descontar un 5% en caso de ser estudiante.

---

- Dado el promedio de notas y la asistencia, calcular si la persona aprueba el ramo, va a la prueba recuperativa o reprueba:
	- si el promedio es mayor o igual a 4,0 y la asistencia al 70%, aprueba.
	- si el promedio es mayor o igual a 3,5 y la asistencia al 80%. va a la recuperativa.
	- en otro caso, reprueba.





