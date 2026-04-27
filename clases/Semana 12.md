
[[Indice]]

> [!NOTE] Contenidos
> 
Implementar y manipular listas y tuplas para almacenar, recorrer y modificar colecciones de datos usando Python.

---

## Objetivos:

- [ ] Listas y tuplas 
- [ ] Listas. 
- [ ] Tuplas. 
- [ ] Manejo de índices.

---

### ¿Qué es una lista?

Un conjunto de datos que pueden ser de distintos tipos:

```python
[1, 2, 3, 4]
["h", "o", "l", "a"]
[[1, 2, 3], [4, 5, 6], 1.5, True, 3]
[]
```

---

Algunas características son:

- Son **ordenadas**, mantienen el orden en el que han sido definidas
- Pueden ser formadas por tipos **arbitrarios**
- Pueden ser **indexadas** con `[i]`.
- Se pueden **anidar**, es decir, meter una dentro de la otra.
- Son **mutables**, ya que sus elementos pueden ser modificados.
- Son **dinámicas**, ya que se pueden añadir o eliminar elementos.

---

#### Crear listas

```python
lista = list("1234")
lista = [1, 2, 3, 4]

```
---
### Índices de listas

```python
a = [90, "Python", 3.87] 
print(a[0]) 
print(a[1])
print(a[2])
print(a[-1])
print(a[-2])
```
---

¿Y qué pasa en el caso de una lista dentro de otra lista?

```python
x = [1, 2, 3, ['p', 'q', [5, 6, 7]]]
```

---

```python
x = [1, 2, 3, ['p', 'q', [5, 6, 7]]]
print(x[3][0])
print(x[3][2][0])
print(x[3][2][2])
```
---

#### Modificar listas

Se pueden añadir elementos a una lista mediante el método append. Ej:

```python
lista = [1, 2, 3, 4]
lista.append(5)
print(lista)
```

---


Ejercicio: Creen una lista vacía y permitan que el usuario añada 3 elementos en la lista.


---

```python
numeros = []

for i in range(3):
    n = int(input("Número: "))
    numeros.append(n)

print(numeros)
```

---

También pueden eliminar elementos de una lista conociendo su índice, por ejemplo:

```python
l = [1, 2, 3, 4, 5] 
del l[1] 
print(l)
```

Esto cambia los índices de los siguientes elementos, así que ojo con ello.

---

Pueden también crear sublistas a partir de una lista:

```python
lista = [1, 2, 3, 4, 5, 6]
sublista1 = lista[0:2]
sublista2 = lista[2:6]
print(sublista1)
print(sublista2)

```

---

O pueden modificar los elementos de la lista original:

```python
l = [1, 2, 3, 4, 5, 6] 
l[0:3] = [0, 0, 0] 
print(l)
```

Pedimos aquí que se modifiquen los elementos de los índices 0 hasta 2.

---

O podemos sumar dos listas entre ellas con "+":

```python
l1 = [1, 2, 3] 
l2 = l1 + [4, 5] 
print(l2)
```
---

Ejercicios: 

- Dada la lista `[10, 20, 30]`, cambia el segundo valor por 99.
- Que el usuario ingrese 5 dígitos para generar una lista y se elimine el penúltimo elemento de esta.

---

Y pueden también asignar los valores de la lista a variables:

```python
l = [1, 2, 3] 
x, y, z = l 
print(x, y, z)
```

---

### Métodos de listas

##### append:

Sirve para agregar elementos a la lista

```python

lista = [1, 2, 3, 4]
lista.append(5)
print(lista)

```

---
##### extend:

Sirve para añadir una lista a otra

```python

lista = [1, 2, 3, 4]
lista.extend([5, 6])
print(lista)

```

---
##### insert:

Coloca un nuevo elemento en cierta posición de la lista, lo que desplaza el resto de elementos

```python

lista = [1, 2, 3, 4]
lista.insert(1, 5)
print(lista)

```

---

##### remove:

Sirve para remover cierto elemento que le entreguemos de la lista la primera vez que aparece

```python

lista = [1, 2, 3, 4, 2]
lista.remove(2)
print(lista)

```


---
##### pop

Este método elimina un elemento según su posición o índice en la lista. Si no se le entrega argumento, elimina el último elemento

```python

lista = [1, 2, 3, 4]
lista.pop()
print(lista)

```

---

##### reverse

Sirve para revertir el orden de la lista

```python

lista = [1, 2, 3, 4]
lista.reverse()
print(lista)

```
---

##### sort

Este comando ordena de menor a mayor los elementos, o de mayor a menor si es que se le comanda ello

```python

lista = [1, 4, 3, 2, 5]
lista.sort()
print(lista)

```

```python

lista = [1, 4, 3, 2, 5]
lista.sort(reverse = True)
print(lista)

```
---

##### index

Muestra el índice de la primera aparición de un elemento

```python

lista = [1, 4, 3, 2, 5]
print(lista.index(3))

```

---

- Crea la lista `["daniel", "javier", "fernanda", "luisa"]` y permite que el usuario borre uno de los elementos de la lista que quiera borrar.
- Dada la lista `[1, 3, 7, 2, 2, 8, 4, 5, ,5 , 3, 6, 8, 11]`, elimina el valor de la mediana.
- haz una lista y un código donde el usuario pueda preguntar si cierto elemento está contenido en la lista o no.

---
##### Recorrer una lista mediante for

Pueden ir recorriendo los elementos de una lista, ej:

```python
lista = list("Python")
for i in lista:
	print(i)
```
De este modo recorrimos cada elemento de la lista, 

---

Si queremos que se iteren los elementos de la lista y también los índices, podemos hacer eso:

```python
lista = [5, 9, 10] 
for index, l in enumerate(lista): 
	print(index, l)
```

Mediante enumerate.

---

También se puede iterar sobre dos listas a la vez mediante el comando zip, que agrupa las listas:

```python
lista1 = [5, 9, 10] 
lista2 = ["Jazz", "Rock", "Djent"] 
for l1, l2 in zip(lista1, lista2): 
	print(l1, l2)
```

---
Ejercicios:

1. Haz un algoritmo capaz de determinar el número más grande de una lista y que lo devuelva. Ej: $[1, 5, 7, 4, 6, 5, 2]$.
2.  Verifica tu algoritmo con las siguientes listas:
	1. $[1, -1, 3, 5, 2]$
	2. $[1, 2, 3, 4, 5, 6, 7]$
	3. $[3, 2]$

---

3. Haz un código que recorra las listas $[1, 2, 3, 4, 5]$ y $[6, 7, 8, 9, 10]$ y entregue una nueva lista con la suma de ambas elemento a elemento.

---

```python
lista = [1, 5, 7, 4, 6, 5, 2]
maximo = lista[0]
for i in lista:
	if i > maximo:
		maximo = i
print(maximo)
```

```python
resultado = []

for i in range(len(a)):
    resultado.append(a[i] + b[i])

print(resultado)
```

---

4. Pide 3 números al usuario, pero si ingresa números negativos, pídele que vuelva a introducir el número hasta que ingrese 3 positivos.
5. Guarda en una lista todos los números que el usuario ingrese hasta que ingrese el número 0. Muestra los valores mayores y menores de la lista generada.

- Dada la lista `[1, 5, 7, 8, 9, 10, 15]`, haz un código que elimine los elementos múltiplos de 5.

---

```python
lista = []
indice = 0
while indice < 3:
	numero = int(input())
	if numero > 0:
		indice = indice + 1
		lista.append(numero)
```

```python
numero = 1
lista = []
while numero != 0:
	numero = int(input())
	lista.append(numero)

lista.sort()
print("maximo:", lista[0], "minimo:", lista[-1])

```
``` python
lista = [1, 5, 7, 8, 9, 10, 15]
new_lista = []
for i in lista:
	if i%5 != 0:
		new_lista.append(i)
print(new_lista)
```

---

### Tuplas

Las tuplas son estructuras de datos similares a las listas; sirven para almacenar datos. Sin embargo, estas son **inmutables**.


---
#### Crear tuplas

Las tuplas se escriben con paréntesis o solo con comas en vez de corchetes cuadrados:

```python
tupla = (1, 2, 3) 
print(tupla)
```
```python
tupla = 1, 2, 3
print(type(tupla))
```


---

Si tratamos de modificar el valor de una tupla, nos arrojará un error:

```python
tupla = (1, 2, 3)
tupla[0] = 5
```

De este modo, tenemos listas que el usuario no podrá manipular por error.

---

Podemos anidar tuplas

```python
tupla = 1, 2, ('a', 'b'), 3 
print(tupla)
print(tupla[2][0])
```
---

Y podemos convertir una lista en tupla:

```python
lista = [1, 2, 3] 
tupla = tuple(lista) 
print(type(tupla)) 
print(tupla)
```

---

Y se pueden hacer cosas bastante similares a las listas:

```python
tupla = [1, 2, 3] 
for t in tupla: 
	print(t)
```
```python
l = (1, 2, 3) 
x, y, z = l 
print(x, y, z)
```

Entre otras funciones que también se repiten con las listas! Ej: len

---

### Métodos

##### count

Permite contar la cantidad de veces que aparece un elemento

```python
l = [1, 1, 1, 3, 5] 
print(l.count(1))
```

---
##### index

Nos muestra el índice de la primera vez que aparece un elemento

```python
l = [7, 7, 7, 3, 5] 
print(l.index(5))
```

---

Ejercicios:

- Haz un código que reciba una tupla y retorne el largo de esta.
- Dada la tupla `(1, 2, 3)`, crea una nueva tupla donde el primer valor sea 10.
- Calcula la suma de todos los valores de una tupla.
- Guarda una fecha como (día, mes, año) y muestra el año.
- Crea una lista que almacene las tuplas (4.4, 5.2), (5.6, 7.0), (3.0, 6.3), que son las notas de 3 estudiantes distintos, y calcula el promedio de cada estudiante.
- Encuentra el número mayor en una tupla.
- Dada la lista de tuplas `[("Ana", 5.5), ("Luis", 3.8), ("Marta", 6.1)]`, muestra el nombre de los estudiantes que aprobaron el curso.

---

## Objetivos:

- [ ] Listas y tuplas 
- [ ] Listas. 
- [ ] Tuplas. 
- [ ] Manejo de índices.

---
### Tareas: 

- 

