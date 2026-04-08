
[[Indice]]

> [!NOTE] Contenidos
> Seleccionar y utilizar tipos de datos adecuados para representar información usando Python, justificando la elección según el contexto del problema.


---

## Objetivos:

- [ ] Datos numéricos, booleanos y cadenas.
- [ ] Conversión de tipos. 
- [ ] Operaciones básicas.
- [ ] Cómo hacer operaciones en cadenas de texto.

---

¿Nos quitará el trabajo la IA?


---

Para usar jupyter:

-> Ctrl + shift + P
-> Create: New jupyter notebook



---

Existen dos tipos de lenguajes:

- Lenguajes tipados
- Lenguajes no tipados

En el primero, las variables y constantes se deben declarar indicando el tipo de dato. En el segundo, esto no es necesario. Python es el segundo.

---
### Tipos de datos:

- int (enteros)
- float (punto flotante)
- bool (booleanos)
- lists (listas)
- strings (cadenas)

---

Existen muchos otros!

- complex
- dict
- tuple
- set

---

### Enteros

Estos, como su nombre sugiere, son los números enteros. Ej:

1, 2, 3, 4, ...

---


```python
a = 1
b = -42
c = 1000

print(a + 2)
```

---

Estos son los valores positivos o negativos, no decimales.

---

```python

i = 12 
print(i) #12 
print(type(i)) #<class 'int'>
```

---

### Punto flotante

Este es el tipo de datos decimal. Ej:

- 4,5
- -10,6
- 1,0

---

¿Por qué será de utilidad separar los datos de tipo int y tipo float, si int también se puede representar como float?

---

Ej:

``` python
a = 20
b = 0.5
suma = a + b

print(suma)
```
---

¿Qué tipo de dato es la suma de estos dos tipos?

```python

print(suma)
print(type(suma))
```

---

¿Y en este caso?


```python

a = 12
b = 4.0
division = a/b
print(division)
print(type(division)) #<class 'int'>
```
---

Ejercicio:

Calculen el 70% de un número que el usuario introduzca.

---


```python
numero = int(input())

resultado = numero * 0.7
print(resultado)

```
---

Se puede usar también para notación científica:


```python

f = 1.93e-3
print(f)
```

La mínima precisión es `2.2250738585072014e-308` y la máxima `1.7976931348623157e+308`,

---

Podemos también volver un número entero a float:

b = float(1)


---

### Booleanos

Permiten hacer afirmaciones binarias.


- True
- False


---

```python

a = 10
if a == 5:
    print(True)
else:
    print(False)
```

---

O podemos convertir valores a booleanos:

```python
print(bool(1))      # True
print(bool(0))      # False
```
```python
print(bool("Hola")) # True
print(bool(""))     # False
```
```python
print(bool(3.5))    # True
print(bool(0.0))    # False
```
¿Qué hace que un valor sea True y otro False?

---

Los valores vacíos generan False, como 0, 0.0, "", [].

---

```python
texto = input("Escribe algo: ")

print(bool(texto))

```

---

```python

f = 0.99999999999999999
print(f)
print(1 == f)

```


---
### Listas

Permiten almacenar varios datos en un mismo conjunto. Ej:

lista_supermercado = $[leche, azucar, miel, galletas, te, cafe, jugo]$

---

```python
lista = list("1234")
lista = [1, "Hola", 3.67, [1, 2, 3]]
print(lista)

```
---

Algunas propiedades de las listas:

- Son **ordenadas**.
- Pueden ser formadas por distintos tipos de datos.
- Se pueden **anidar**.
- Son **mutables**
- Son **dinámicas**, ya que se pueden añadir o eliminar elementos.

---
### Cadenas

Las cadenas o *strings* son cadenas de caracteres. 

- Van entre comillas '', ""

Pueden analizar distintas operaciones entre cadenas en: https://ellibrodepython.com/cadenas-python

---

Ej:

```python
s = "Hola! Yo soy un string c:" 
print(s) #Esto es una cadena 
print(type(s)) #<class 'str'>
```

---

También podemos guardar saltos de línea:

```python
s = "Primera linea\nSegunda linea" 
print(s)
```

---

Como ocupamos las comillas para abrir y cerrar strings, ¿Cómo se escribiría una dentro del string?

---

```python
s = "Soy una cadena que quiere citar a alguien: \"Soy una cita dentro de una cadena\" "
print(s)

```

---

Se pueden también unir diferentes cadenas en una sola:

```python

x = 5
s = "El número es: " + str(x) 
print(s) #El número es: 5
```
---

Otra forma de hacer lo mismo es mediante el caracter %, que señala la ubicación para colocar el texto inserto:

```python
x = 5 
s = "El número es: %d" % x 
print(s) #El número es: 5
```

---

Esto es útil para insertar varios textos distintos a lo largo de tu string:

```python
s = "Los números son %d y %d." % (5, 10) 
print(s)
```

note:
escribir numero1 = 5 y reemplazar por el 5

---

Ejercicio:

Crear código que le pida al usuario ingresar nombre, edad y género y escriba un texto de presentación de esa persona.

---

Otra manera de realizar lo mismo es con .format():

```python
s = "Los números son {} y {}".format(5, 10) 
print(s)
```

note:

cambiar el 5 por un string

---

```python
s = "Los números son {a} y {b}".format(a=5, b=10) 
print(s) #Los números son 5 y 10
```

---
f-strings:

```python
a = 5
b = 10
s = f"Los números son {a} y {b}"
print(s)
```

---

Y esto nos permite hacer operaciones dentro de nuestro string:

```python
a = 5
b = 10
s = f"a + b = {a+b}"
print(s)
```

---

Ej:

Define las cadenas:

"Hola, soy una primera cadena"
"Hola"

Genera una cadena que sume ambos strings para generar una sola cadena con ambas. ¿Qué pasa si multiplicas una cadena por 3?

---

```python
cadena1 = "Hola, soy una primera cadena"
cadena2 = "Hola"
cadena3 = cadena1 + cadena2*3
print(cadena3)
```

---

Se puede también ver si una cadena está dentro de otra:

``` python
print(cadena2 in cadena1)
```

---

Se puede medir el largo de una cadena:

```python
print(len(cadena2))
```

---

Ej:

¿Cuál es el largo total entre las cadenas 1 y 2? Haz un código para calcularlo.

---

Haz un código que le pida al usuario su nombre y que le retorne el largo de su nombre.

---

```python
nombre = input("Ingresa tu nombre: ")

largo = len(nombre)

print("Tu nombre tiene", largo, "caracteres")
```

---

Así como podemos medir el largo de una cadena, podemos ver qué valor está en cada posición:

```python
x = "abcde" 
print(x[0])
print(x[1])
print(x[2])
```
---
Para llegar a los valores del final, podemos usar:

```python
x = "abcde" 
print(x[-1])
print(x[-2])
```
---

Haz un código que le pida al usuario ingresar su nombre y le retorne su inicial.

---

Podemos también crear subcadenas a partir de la primera, ej:

```python
cadena1 = "Hola, soy una primera cadena"
subcadena1 = cadena1[0:4]
print(subcadena1)
```
Esta parte en el índice 0 y llega al tercero.

---

¿Cómo podríamos hacer una cadena que parta en el índice 2 y termine en el quinto índice?

---

```python
cadena1 = "Hola, soy una primera cadena"
subcadena1 = cadena1[0:10:2]
print(subcadena1)
```

Se saltan los segundos elementos entre el índice 0 a 10.

---

¿Qué hace este código?

```python
cadena1 = "Hola, soy una primera cadena"
subcadena1 = cadena1[0::2]
print(subcadena1)
```

note:
nos fuimos saltando los segundos elementos, pero de todo el string, no necesitamos definir un largo.

---

### Métodos en cadenas:


##### capitalize()

Devuelve la cadena con su primera letra en mayúscula:

```python
s = "mi cadena" 
print(s.capitalize())
```

##### lower()

Convierte todas las letras en minúscula:

```python
s = "Mi CadenA" 
print(s.lower())
```
---
##### swapcase()

Intercambia las mayúsculas y minúsculas:

```python
s = "Mi CadenA" 
print(s.swapcase())
```

##### upper()

Convierte todas las letras en mayúscula

```python
s = "mi cadena" 
print(s.upper())
```

---
##### count()

Permite contar las veces que una cadena está dentro de otra.


```python
s = "Mi cadena" 
print(s.count("Mi"))
```

```python
s = "Mi cadena" 
print(s.count("Mi", [0 : 5]))
```

note: sirve para contar letras también, algo falla aquí.

---
##### isalnum()

Devuelve True si la cadena está formada solo por números, False en lo contrario.

```python
s = "mi.correo1234" 
print(s.isalnum())
```
```python
s = "1234" 
print(s.isalnum())
```

```python
s = "1234@" 
print(s.isalnum())
```

---
##### isalpha()

Devuelve True si todos los caracteres son letras o False de lo contrario.

```python
s = "mi.correo1234" 
print(s.isalpha())
```

```python
s = "mi.correo" 
print(s.isalnum())
```

```python
s = "micorreo@" 
print(s.isalnum())
```

---
##### strip()

Elimina a la izquierda y derecha el caracter que se le pide. Sin parámetros elimina los espacios. Es útil para limpiar data.

```python
s = "mi.correo1234 " 
print(s.strip("mi"))
```

```python
s = " mi.correo1234 " 
print(s.strip())
```

---
##### zfill()

rellena con ceros a la izquierda hasta llegar a la longitud total indicada.

```python
s = "mi.correo1234" 
print(s.zfill(20))
```

##### join()

Toma una cadena y una lista, y une entremedio la cadena entre la lista:

```python
s = " , ".join(["1", "2", "3", "..." ])
print(s)
```
---

##### split()

Divide una cadena en subcadenas y las devuelve como lista.

```python
s = " 1 , 2 , 3 , ..." 
print(s.split(" , "))
```

---

Algunos ejemplos con los tipos...



---


---




Al python ser de tipado dinámico, podemos reasignarle los valores a las variables como otros tipos distintos:

compras = "leche, agua"
compras = $['leche', 'agua']$
compras = 3000

---

¿De qué sirve cambiarle el tipo a un dato?

int a float
string a int

x = str(10.4) print(x) #10.4 print(type(x)) #<class 'str'>

---

operaciones con strings...


---

operaciones con números, listas y strings...

---

1. Determine el número más grande de la siguiente lista $[1, 5, 7, 4, 6, 5, 2]$.
2. Genere un algoritmo que recorra la lista y guarde el elemento más grande.
3.  Verifica tu algoritmo con las siguientes listas:
	1. $[1, -1, 3, 5, 2]$
	2. $[1, 2, 3, 4, 5, 6, 7]$
	3. $[3, 2]$

---

mayor = primer número de la lista

para cada número
    si número > mayor
        mayor = número



---
## Objetivos:

- [ ] 

---
### Tareas: 

- 

