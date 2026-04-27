
[[Indice]]

> [!NOTE] Contenidos
> 
Emplear diccionarios y conjuntos en la resolución de problemas que requieran relaciones clave‑valor y operaciones de pertenencia usando Python.

---
## Objetivos:

- [ ] Diccionarios y conjuntos 
- [ ] Diccionarios (clave–valor). 
- [ ] Conjuntos. 
- [ ] Aplicaciones prácticas

---

### Diccionarios

Los diccionarios sin estructuras de almacenamiento de datos (igual que las listas), sin embargo, tienen la característica de almacenar parejas de datos, en el formato de llave y valor.

---
#### ¿Cómo declarar un diccionario?

```python
dicc1 = { 
	"Nombre": "Sara", 
	"Edad": 27, 
	"Documento": 1003882 } 
print(dicc1)
```

---

O pueden ocupar la función dict():

```python
d3 = dict(
	Nombre='Sara', 
	Edad=27, 
	Documento=1003882) 

print(d3)
```

---

Algunas características:

- Son **dinámicos**, pueden crecer o decrecer, se pueden añadir o eliminar elementos.
- Son **indexados**, los elementos del diccionario son accesibles a través del `key`.
- Y son **anidados**, un diccionario puede contener a otro diccionario en su campo `value`.

---

Usualmente los 'values' son los valores que vamos almacenando, los 'keys' son los tipos de datos que son.

```python
d1 = dict(
	Nombre='Sara', 
	Edad=27, 
	Documento=1003882) 

print(d1['Nombre'])
print(d1.get('Nombre'))
```

Podemos acceder a los valores usando las llaves. Siempre se necesita una llave, que llevará un valor.

---

#### Modificar diccionarios

Si queremos modificar un valor del diccionario, podemos usar el siguiente comando:

```python
d1['Nombre'] = "Laura"
d1['Direccion'] = "Calle 123"
print(d1)
```

Si es que esta llave no existe, se crea en el momento.

---

Ejercicio:

1. Crea un diccionario con tus datos:

- nombre
- edad
- carrera

2. Cambia la edad a 55
3. Agrega la comuna de donde eres


---

Para imprimir solo las llaves, usamos:

```python
for x in d1: 
	print(x)
```

Para imprimir solo los valores usamos:

```python

for x in d1: 
	print(d1[x])

```
---

Podemos colocar varios diccionarios dentro de otro:

```python

d = { "anidado1" : d1, "anidado2" : d3 }
print(d)
```
---

Ejercicio:

Crea un bucle donde pueda almacenar mediante inputs en un mismo diccionario:

- nombre
- edad
- carrera

de 3 personas diferentes.


---

#### Métodos en diccionarios:

##### clear:

Sirve para limpiar el contenido de un diccionario:

```python
d = {'a': 1, 'b': 2} 
d.clear() 
print(d)
```
---
##### get:

Nos permite acceder al valor de una llave:

```python
d = {'a': 1, 'b': 2} 
print(d.get('a'))
print(d.get('z', 'No encontrado'))
```

---
##### item:

Permite mostrar todos los datos almacenados dentro, tanto llaves como valores. Genera junto con la función list() una lista de listas a partir de los datos dentro del diccionario:

```python
d = {'a': 1, 'b': 2} 
it = d.items() 
print(it)
print(type(it))
print(list(it))
print(list(it)[0][0])
```

O podemos recorrer los valores:

```python
for clave, valor in persona.items():  
	print(clave, valor)
```

---

##### keys:

Permite acceder a las llaves. Nuevamente se puede usar list para volverlo lista:

```python
d = {'a': 1, 'b': 2} 
k = d.keys() 
print(k) 
print(list(k))
```

##### values:

Permite acceder a los valores:

```python
d = {'a': 1, 'b': 2} 
print(list(d.values()))
```
---
##### pop:

Permite eliminar algún dato del diccionario si es que el valor entregado coincide con una llave:

```python
d = {'a': 1, 'b': 2} 
d.pop('a') 
print(d)
```

En caso de que no se encuentre la llave, genera un error, para evitar esto se puede pasar un segundo argumento al método que se imprimirá en ese caso:

```python
d = {'a': 1, 'b': 2} 
print(d.pop('c', -1)) 
print(d)
```
---
##### popitem:

Este método elimina aleatoriamente un elemento:

```python
d = {'a': 1, 'b': 2} 
d.popitem() 
print(d)
```
##### update:

Permite añadir elementos de un diccionario en otro diccionario. Si ya hay elementos presentes, estos no se duplican, pero sí se actualizan:

```python
d1 = {'a': 1, 'b': 2} 
d2 = {'a': 0, 'd': 400} 
d1.update(d2) 
print(d1)

```

---

Ejercicios:

1. Haz un diccionario donde almacenes 3 notas de alumnos y las promedies.
2. Almacena los números telefónicos de 3 personas en un diccionario, y haz un código donde el usuario pueda preguntar por una persona y se le devuelva su número telefónico.
3. Mostrar cuántas personas apruebas del diccionario: notas = {"Ana": 5.5, "Luis": 3.8, "Marta": 6.1}
4. Haz un inventario donde se pueda cambiar la cantidad de stock de algún producto, eliminar productos y mostrar el inventario.


---

```python

dict1 = {
		"N1": 5.9,
		"N2": 5.6,
		"N3": 6.3
		}

suma = 0

for i in dict1:
	suma = suma + dict1[i]

promedio = suma/3
print(promedio)

```

---

```python
dict2 = {
		"P1": "+5691111111",
		"P2": "+5692222222",
		"P3": "+5693333333" }

consulta = input("P1/P2/P3:" )

print(dict2[consulta])

```

---

```python
notas = {"Ana": 5.5, "Luis": 3.8, "Marta": 6.1}

for i in notas:
	if notas[i] >= 4:
		print(i)

```


---

### Sets

Los sets o conjuntos también son estructuras para almacenar datos, pero al igual que con las tuplas, son inmutables:

- Los elementos de un set son **único**, lo que significa que no puede haber elementos duplicados.
- Los set son **desordenados**, lo que significa que no mantienen el orden de cuando son declarados.
- Sus elementos deben ser **inmutables**.

---
#### ¿Cómo declarar un set?

Se pueden usar los corchetes {} o la función set():

```python
s = {5, 4, 6, 8, 8, 1}
s = set([5, 4, 6, 8, 8, 1]) 
print(s)
print(type(s))
```

---

Vemos que el orden fue modificado a menor a mayor, y los elementos duplicados fueron eliminados, y como se mencionaba, no se pueden modificar los elementos... de la misma forma que antes.

---

Los sets, al ser inmutables, no revisen ni listas ni diccionarios como elementos, pero sí tuplas:

``` python
s = {(1, 2), 3, 4, 6, 5, 5, 5}
print(s)

```

```python
s = {[1, 2], 3, 4, 6, 5, 5, 5}

```
---

Se pueden iterar como en los casos anteriores:

```python
s = set([5, 6, 7, 8]) 
for ss in s: 
	print(ss)

```

---
Se puede usar también la función len() para ver la longitud del set:

```python
s = set([1, 2, 2, 3, 4]) 
print(len(s))
```

---

O podemos ver si un elemento está en el set o no:

```python
s = set(["Guitarra", "Bajo"]) 
print("Guitarra" in s)
```
---

Y podemos juntar dos sets en un tercero:

```python
s1 = set([1, 2, 3]) 
s2 = set([3, 4, 5])
s3 = s1 | s2
print(s3)
```
---
#### Métodos en sets:

##### add:

Permite agregar un elemento al set:

``` python
s = {1, 2, 2, 5, 4, 3, 5, 6}
s.add(8)
print(s)
```

##### remove:

Elimina algún elemento del set, pero tira error si es que no existe:

``` python
s = {1, 2, 2, 5, 4, 3, 5, 6}
s.remove(2)
print(s)
```

``` python
s = {1, 2, 2, 5, 4, 3, 5, 6}
s.remove(8)
print(s)
```


---
##### discard:


``` python
s = {1, 2, 2, 5, 4, 3, 5, 6}
s.discard(8)
print(s)
```


##### pop:



---
##### clear:


##### union:


---

|Método|¿Qué hace?|Ejemplo|Resultado|
|---|---|---|---|
|`union()`|Une dos sets|`a.union(b)`|todos los elementos|
|`intersection()`|Elementos comunes|`a.intersection(b)`|solo comunes|
|`difference()`|Elementos de uno que no están en otro|`a.difference(b)`|solo de `a`|
|`symmetric_difference()`|Elementos que no se repiten|`a.symmetric_difference(b)`|distintos|

---

- Un diccionario entonces nos sirve para guardar la información con nombre. Por ejemplo, si queremos guardar la misma información de varias personas.
- Un conjunto en cambio, sirve para guardar información que no queremos que se repita, por ejemplo para una base de datos.


---
## Objetivos:

- [ ] Diccionarios y conjuntos 
- [ ] Diccionarios (clave–valor). 
- [ ] Conjuntos. 
- [ ] Aplicaciones prácticas

---
### Tareas: 

- 

