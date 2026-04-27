

[[Indice]]

> [!NOTE] Contenidos
> 
Resultado de aprendizaje: Construir estructuras condicionales correctamente indentadas, tomando decisiones computacionales basadas en condiciones múltiples usando Python.

---

## Objetivos:

- [ ] Estructuras de control: secuenciales y condicionales
- [ ] if, elif, else.
- [ ] Expresiones condicionales.

---


##### ¿Cómo les fue en la solemne?



---

### Condicionales:


En la vida, hay que tomar decisiones según las condiciones:

- si llueve → llevo paraguas
- si tengo hambre → como

Los programas de computadores también lo hacen, pero estos siguen las instrucciones que codifiquemos.

---

	if condición:
		instrucción identada
	else:
		instrucción identada

---

Todo entonces lo que esté identado dentro del if será parte de ese proceso:

```python
a = 4
b = 0

if b != 0: 
	c = a/b 
	print("Dentro if") 
print("Fuera if")
```

---

¿Qué pasa si tenemos más de dos condiciones?

- si son antes de las 12:00 → desayuno
- si son entre 12:00 y 16:00 → almuerzo
- si son después de las 17:00 → once

---

Cuando tenemos más de una condición, vamos a utilizar el comando elif:


	if condición:
		instrucción identada
	elif condición:
		instrucción identada
	else:
		instrucción identada

---

Ej: Traten de construir un código donde el usuario ingrese la edad. Si es menor de 12 años, entra gratis al cine, si tiene entre 12 y 18, paga 3.000, y si tiene 18 o más, paga 5000.

---

```python
edad = int(input("Edad: "))

if edad < 12:
    print("gratis")
elif edad <= 18:
    print("5000")
else:
    print("10000")
```


---

OJO: Al hacer igualdades dentro de la condición, tenemos que usar dos signos de igualdad "== " :

```python
numero = 5

if numero < 10:
    print("número pequeño")
elif numero == 10:
    print("número mediano")
else:
    print("número grande")
```

---

Pueden también colocar un if sin un else, pero no viceversa. Ej: Generar un descuento solo para compras sobre 10.000:

```python
monto = int(input("Monto de compra: "))

if monto > 10000:
    descuento = monto * 0.1
    monto = monto - descuento
    print("Descuento:", descuento)

print("Gracias por su compra de", monto)
```

---

Teníamos un caso condicional, donde si se cumplía la condición, entrábamos a un caso, y sino, no ocurría nada, así que el comando else no era necesario.

---

Ejercicio: Hagan un código que le pida su nota al usuario y le indique:

- Si tuvo entre un 1.0 y un 4.0 -> reprobado
- Si tuvo entre 4.0 y 5.0 -> suficiente
- Si tuvo entre 5.0 y 6.0 -> Bueno
- Si tuvo entre un 6.0 y un 7.0 -> Muy bueno
- En otro caso -> Nota inválida

---

```python

nota = float(input("Ingresa tu nota: "))

if 1 < nota < 4:
    print("Reprobado")
elif nota < 5:
    print("Suficiente")
elif nota < 6:
    print("Bueno")
elif nota <= 7:
    print("Muy bueno")
else:
    print("Nota inválida")
```
---

En el código anterior no necesitamos colocar los valores mínimos de los elif, ya que python entra a los condicionales de forma **ordenada**. Si no logró cumplir la primera condición, entra a la siguiente, sino, a la siguiente, y así hasta recorrerlas todas. Si es que logró entrar a una, no entra a las siguientes.

---

No pueden utilizar elif sin antes colocar un if, y tampoco pueden utilizar if en reemplazo de elif, pues se genera entonces otro subproceso, en el caso anterior por ejemplo:


```python

nota = 5

if 1 < nota < 4:
    print("Reprobado")
if nota < 5:
    print("Suficiente")
if nota < 6:
    print("Bueno")
if nota <= 7:
    print("Muy bueno")
else:
    print("Nota inválida")
```

---

También se pueden anidar los if, por ejemplo, hagan un código para revisar si una persona puede votar o no, para ello nos fijamos en si es:

- año de elecciones
- edad

Las dos son variables independientes entre sí.

---
```python
elecciones = True
edad = 20

if edad > 18:
	 if elecciones:
		 print("puede votar")
	else:
		print("no puede votar")
else:
	print("no puede votar")
```
---

if y else se utilizan harto con operadores relacionales, por ejemplo:

```python
a = 4
b = 2 
if b != 0: 
	print(a/b)
```

---

### Un par de ejercicios


Entonces, veamos qué tan bien han aprendido la materia...

¿Qué está mal en este código?

```python
edad = int(input("Edad: "))

if edad <= 18:
    print("Menor o joven")
elif edad < 12:
    print("Niño")
else:
    print("Adulto")
```

---
Orden correcto:

```python
if edad < 12:
    print("Niño")
elif edad <= 18:
    print("Menor o joven")
else:
    print("Adulto")
```

---

¿Qué está mal en este código?

```python
numero = int(input("Número: "))

if numero > 0:
    print("Positivo")

if numero < 0:
    print("Negativo")

else:
    print("Cero")
```

---

¿Qué corregirían de este código?

```python
edad = int(input("Edad: "))

if edad < 12:
    print("Niño")
elif edad > 12 and edad < 18:
    print("Adolescente")
else:
    print("Adulto")
```

---

Si la persona tiene 12 años, entra en la categoría de adulto.

```python
edad = int(input("Edad: "))

if edad < 12:
    print("Niño")
elif edad < 18:
    print("Adolescente")
else:
    print("Adulto")
```
---

### Otras maneras de escribir condicionales:

```python
x = 5 
print("Es 5" if x == 5 else "No es 5")
```
(código si se cumple) if (condición) else (código si no se cumple)


---

Otro ejemplo:

```python
a = 10 
b = 5 
c = a/b if b!=0 else -1 
print(c)
```

---

Ejercicios:

Una persona quiere entrar a un evento, hacer un código que:

- Primero revise si tiene entrada
- Si tiene entrada, se revisa la edad
- Si es mayor de 18 → entra
- Si no → no entra

---

```python

tiene_entrada = input("¿Tiene entrada? (si/no): ")
edad = int(input("Edad: "))

if tiene_entrada == "si":
    if edad >= 18:
        print("Puede entrar")
    else:
        print("No puede entrar por edad")
else:
    print("No puede entrar sin entrada")
    
```
---

Simulen el pago en una máquina expendedora:
- se pide el precio y dinero al usuario
- entregue vuelto si corresponde
- no entregue el producto si el dinero es insuficiente
- entregue el producto en otro caso

---

```python
precio = int(input("Precio: "))
dinero = int(input("Dinero: "))

if dinero >= precio:
    if dinero == precio:
        print("Pago exacto")
    else:
        vuelto = dinero - precio
        print("Vuelto:", vuelto)
else:
    print("Dinero insuficiente")
```





---
## Objetivos:

- [ ]  Estructuras de control: secuenciales y condicionales
- [ ] if, elif, else.
- [ ] Expresiones condicionales.

---
### Tareas: 

![[Pasted image 20260420191438.png]]
![[Pasted image 20260420191454.png]]

