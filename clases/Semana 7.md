
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

Para usar jupyter:

-> Ctrl + shift + P
-> Create: New jupyter notebook

---


Se puede usar también google colab en drive.


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

print(c + 2)
```

---

Estos son los valores positivos o negativos, no decimales.

---

```python

i = 12 
print(i) 
print(type(i))
```

---

Hay dos tipos de funciones, en este caso, este tipo de función se escribe como: 

funcion(argumentos)

---

Para volver un número a un entero, podemos usar la función int(). Ej:

```python
edad = int(input("Edad: "))
edad_futura = edad + 1
print("El próximo año tendrás", edad_futura)
```

¿Qué pasa si no colocan la función int() aquí?

---

``` python
edad = "20"
print(edad)
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
b = 1.0
suma = a + b

print(type(suma))
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
division = int(a/b)
print(division)
print(type(division))
```
---

Ejercicio:

Calculen el 70% de un número que el usuario introduzca. Ej:

- 100 -> 70
- 50 -> 35
- 1 -> 0,7
- 0,20 -> 0,14

---

```python
numero = int(input())

resultado = numero * 0.7
print(resultado)

```
---

Se puede usar también para notación científica:


```python

f = 1.93e-3 # = 1.93*10^-3
print(f)
```

La mínima precisión es `2.2250738585072014e-308` y la máxima `1.7976931348623157e+308`,

---

Escriban en este formato los números:

- 1 * 10^-2
- 2 * 10^3
- 5,25 * 10 ^4

Y sumen los valores.

---

```python
f1 = 1e-2
f2 = 2e3
f3 = 5.25e4

print(f1 + f2+ f3)
```

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
print(bool(3))      # True
print(bool(0))      # False
```
```python
print(bool("alooo")) # True
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
lista = list("holaaaa")
# lista = [1, "Hola", 3.67, [1, 2, 3]]
print(lista)

```
---

Algunas propiedades de las listas:

- Son **ordenadas**.
- Pueden ser formadas por distintos tipos de datos.
- Se pueden **anidar**.
- Son **mutables**.
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
print(s) 
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

Otra forma de hacer lo mismo es mediante el caracter %, que señala la ubicación para colocar el número inserto:

```python
x = 5 
s = "El número es: %d" % x 
print(s) #El número es: 5
```

---

Esto es útil para insertar varios números distintos a lo largo de tu string:

```python
s = "Los números son %d y %d." % (5, 10) 
print(s)
```

Ojo: Esto solo sirve con números, el método anterior servía con texto.

---

Ejercicio:

Crear código que le pida al usuario ingresar nombre, edad y género y escriba un texto de presentación de esa persona. Ej:

Hola, mi nombre es Juanito Pérez, soy hombre de 20 años, es un placer conocerles!

---

[[Semana 6 ej]]

---

Otra manera de realizar lo mismo es con .format():

```python
nombre = "Juanito Pérez"
genero = "hombre"
edad = 20
s = "Hola, mi nombre es {}, soy {} de {} años, es un placer conocerles!".format(genero, nombre, edad) 
print(s)
```


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
cadena2 = "Holi   "
cadena3 = cadena1 + cadena2
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

Se puede ver si los caracteres están en mayúsculas en la palabra:

``` python
texto = "HOLA"
todo_mayus = texto.isupper()
print(todo_mayus)  # Resultado: True
```

---

Podemos también crear subcadenas a partir de la primera, ej:

```python
cadena1 = "Hola, soy una primera cadena"
subcadena1 = cadena1[0:5]
print(subcadena1)
```
Esta parte en el índice 0 y llega al tercero.

---

¿Cómo podríamos hacer una cadena que parta en el índice 2 y termine en el quinto índice?

---

```python
cadena1 = "Hola, soy una primera cadena"
subcadena1 = cadena1[0:10:3]
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
s = "Mi cadena Mi" 
print(s.count("Mi"))
```
---
##### isalnum()

Devuelve True si la cadena está formada so
lo por números, False en lo contrario.

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
s = "micorreo" 
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
s = ",".join(["1", "2", "3", "..." ])
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

Para convertir algo en string, usamos la función str(). Ej:

```python
num_a = 1
num_A = str(num_a)
print(type(num_a))
print(type(num_A))
```

---

#### Mezclando tipos

¿Qué sale de este código?

```python
x = "5.0"
print(type(x))
```
---
```python
x = "5"
entero_x = int(x)
print(type(entero_x))
```
---
```python
x = "hola"
entero_x = int(x)
print(type(entero_x))
```

---

Al python ser de tipado dinámico, podemos reasignarle los valores a las variables como otros tipos distintos:

compras = "leche, agua"
compras = $['leche', 'agua']$
compras = 3000

---

¿De qué sirve cambiarle el tipo a un dato?

- int a float
- string a int

---
### operaciones con strings...

- Un código que reciba el nombre completo de una persona, y sin importar cómo lo escribió, devuelva el nombre con la primera letra de cada palabra en mayúscula y el resto en minúscula (ej: gerard way -> Gerard Way).
- Haz un código que busque cada vez que se menciona a una persona en un tweet, ej: extraer cada mención al usuario @DonaldTrump en una frase twiteada.

---
## Objetivos:

- [ ]  Datos numéricos, booleanos y cadenas.
- [ ] Conversión de tipos. 
- [ ] Operaciones básicas.
- [ ] Cómo hacer operaciones en cadenas de texto.

---
### Tareas: 

- Convertir UF a CLP

Generen un código que reciba de input el valor de la UF actual, un monto en UF que se quiere transformar, y devuelva la transformación a CLP. 

Input:
- valor UF: 40.000
- monto a transformar: 4,51 UF

Output:
- 178.000

---

Generen un código que reciba un texto y lo normalice, es decir, lo transforme a minúsculas. Luego, que retorne el conteo de cuántas veces aparece otra palabra que se ingrese como input. Ej:

Input:
- "Hola, soy una frase. Tengo algunas letras mayúsculas y minúsculas, pero nada muy feo".

Output:
- "hola, soy una frase. tengo algunas letras mayúsculas y minúsculas, pero nada muy feo".
- contador de la palabra "feo": 1

---

Generen un código que pregunte si posee TNE y utilice booleanos. Si tiene, entonces que aplique tarifa de estudiante.

Ej:

input:
- tne = input("¿Tiene TNE? (s/n):")

output:
print("Aplica tarifa estudiante")
print("No aplica tarifa estudiante")

