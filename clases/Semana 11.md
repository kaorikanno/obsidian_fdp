
[[Indice]]

> [!NOTE] Contenidos
> Diseñar e implementar ciclos repetitivos eficientes, utilizando contadores, acumuladores y rangos según sea necesario a través de Python.

---

## Objetivos:

- [ ] Estructuras de control: iterativas
- [ ] for
- [ ] while
- [ ] Contadores e iteraciones. 


---

## Bucles

Como ya vimos, los bucles como su nombre sugiere son estructuras cíclicas que repiten un procedimiento hasta que se cumple cierta condición.

![[Pasted image 20260422175357.png|424]]

---

En el día a día, un bucle es por ejemplo, la rutina que sigues cada día de lunes a viernes, acciones repetidas siguiendo cierto orden hasta que llega el sábado.

---

Digamos por ejemplo que queremos imprimir varias veces una frase:

```python
print("Hola")
print("Hola")
print("Hola")
print("Hola")
print("Hola")
print("Hola")
```

---

Podemos simplemente escribir la misma instrucción varias veces, pero si es un proceso largo o complejo, es algo largo que ocupa bastante espacio, y si tuvimos un error, tendremos que ir modificando la misma línea varias veces.

---

Es más fácil debbugear esto:

``` python
for i in range(6):
    print("Hola")
```

---

Tenemos dos tipos de bucles en python:

- for
- while

---
### for 

Nos permite recorrer listas o rangos hasta que se terminan. Ej:

```python
for i in "Python": 
	print(i)

```

---

Se utiliza entonces for cuando sabemos cuántas veces se va a repetir una tarea.

---

También podemos recorrer la lista al revés:

```python
texto = "Python" 
for i in texto[::-1]: 
	print(i) #n,o,h,t,y,P
```

---

Ej: ¿Qué números se imprimen aquí?

```python
for i in range(5):
    print(i)
```

---

### Range

Significa literalmente rango, nos permite recorrer listas de números ordenados, por ejemplo, se lograría lo mismo que en el código:

```python
for i in (0, 1, 2, 3, 4, 5): 
	print(i)
```

---

Sería lo mismo que hacer:

``` python
for i in range(6): 
	print(i)
```

---

Al igual que con los índices, se le entregan los valores de inicio, fin, y se le puede agregar un salto:

	#range(inicio, fin, salto)

Si no se especifica ni inicio ni salto, se recorrerá desde 0 hasta el número introducido como fin, sin saltos entre números.

---

Ej:

```python
print(list(range(5, 20, 2)))
```

---

O se pueden recorrer de forma inversa los rangos:

```python
for i in range (5, 0, -1): 
	print(i)
```


---

¿Qué más podremos hacer con for? Ej:

```python
suma = 0

for i in range(3):
    numero = int(input("Número: "))
    suma = suma + numero

print("Total:", suma)
```

Permite al usuario ir sumando distintos números que introduzca.

---

Hagan ahora un código que recorra la lista de números del 1 al 5 y entregue la multiplicación de todos esos números, es decir 1* 2* 3 * 4* 5.

---

### while

Se utiliza cuando no sabemos cuántas veces se debe repetir una acción, sino que queremos que se cumpla cierta condición para salir del bucle:

- vamos a hacer empanadas hasta que se acabe el pino (no sabemos cuántas saldrán).
- vamos a tomar agua hasta quedar satisfecho (no sabemos cuánta agua será).

---

Ej:

```python
numero = 0

while numero < 5:
    print(numero)
    numero = numero + 1
```
---

Es **muy** importante siempre colocar una condición para cortar el código con while, sino el código podría correrse infinitamente (o hasta que el computador deje de funcionar).

```python
numero = 0
while numero < 5:
    print(numero)
```

---

Con while también se puede usar else una vez se sale del bucle:

```python
x = 5 
while x > 0: 
	x -=1 
	print(x)
else:
	print("El bucle ha finalizado")
```

---

Una medida que se puede tomar para romper los bucles, es usar el comando "break":

```python
x = 5 
while True: 
	x -= 1 
	print(x) 
	if x == 0: 
		break
else: 
	print("Fin del bucle")
```

Aquí, como se rompió el bucle mediante break, el comando else no se ejecuta.

---

Hay varias cosas que se pueden ejecutar tanto mediante for y while, pero en cada caso habrá que analizar cual conviene más utilizar:

```python
text = "Python" 
i = 0 
while i < len(text): 
	print(text[i]) 
	i += 1
```

```python
text = "Python" 
i = 0 
while i < len(text): 
	print(text[:i + 1]) 
	i += 1
```

---
#### for vs while

| for                   | while              |
| --------------------- | ------------------ |
| sabemos cuántas veces | no sabemos cuántas |
| usa `range()`         | usa condición      |
| más estructurado      | más flexible       |

---

- Hagan un código para sumar los números del 1 al 5 usando for y while.
- Hagan un código que le pida al usuario ingresar un número hasta que ingrese 0.

---

Se pueden utilizar ciclos for anidados:

Ej: Hacer todas las combinaciones de multiplicaciones de números del 1 al 3:

```python
for i in range(1, 4):
    for j in range(1, 4):
        print(i, "x", j, "=", i * j)
```

---

Lo mismo se puede hacer con while:

```python
i = 1

while i <= 3:
    j = 1
    while j <= 3:
        print(i, " x ", j, "=", i*j)
        j = j + 1
    i = i + 1
```
---

Y pueden anidar todos los bucles que necesiten:

```python
i, j, k = 0, 0, 0 
while i < 3: 
	while j < 3: 
		while k < 3: 
			print(i,j,k) 
			k += 1 
			j += 1 
		k = 0 
	i += 1 
	j = 0
```

---

O se pueden mezclar ambos tipos:

```python
for i in range(3):
    numero = -1
    
    while numero < 0:
        numero = int(input("Ingresa un número positivo: "))
    
    print("Número válido:", numero)
    
```
---

Entonces, un bucle dentro de otro, permite repetir un mismo proceso todas las veces que lo necesitemos, para distintos procesos idénticos.

---

Ejercicios:

- Hagan un cuadrado de asteriscos mediante bucles.
- Hagan un rombo de asteriscos mediante bucles (difícil).

---

[[Semana 10 ej]]

---

```python
for i in range(3):
    for j in range(3):
        print("*", end=" ")
    print()
```
```python
print("#"*(5), "#*")
for j in range(1, 6):
	print("#"*(6-j), "*"*2*j,)
for j in range(1, 6):
	print("#"*j, "*"*2*(6-j))
print("#"*(5), "#*")
```

```python
z = 7 
x = 1 
while z > 0: 
	print('#' * z + '*' * x + '#' * z) 
	x+=2 
	z-=1
```

---
### Bucles y condicionales:

Pueden también colocar condicionales if/else dentro de los bucles for y while. Ej:

```python
for i in range(5):
    n = int(input("Número: "))
    if n > 0:
        print(n)
```



---

Ejercicios:

- Pide 4 números al usuario y calcula el total entre los 4 mediante un bucle.
- Pide números al usuario hasta que este ingrese 0, y que se muestren los valores positivos que el usuario ingresó.
- Imprime los números pares entre 1 y 10.
- Pide un número positivo.  Si es negativo, vuelve a pedirlo.
- Calcula la suma de los números del 1 al 100.
- Pide 3 números positivos e imprímelos, pero si alguno es negativo, vuelve a pedirlo.
- Pide 5 números al usuario y cuenta cuántos son pares.
- Pide 5 notas al usuario y saca el promedio solo de las notas mayores a 4.
- Pide 5 números al usuario e imprime solo los que están entre 10 y 50.


---
## Objetivos:

- [ ] Estructuras de control: iterativas
- [ ] for
- [ ] while
- [ ] Contadores e iteraciones. 

---
### Tareas: 

- 

