

## Pensamiento computacional


[[Indice]]

> [!NOTE] Contenidos
> Aprenderemos lo que es la programación a grandes rasgos, y el tipo de pensamiento y análisis necesario para aprender a programar.
> 

---
### Objetivos:

- Aprender qué es la programación
- Aprender sobre reconocimiento de patrones
- Descomponer problemas
- Entender lo que es un algoritmo

---

### ¿Qué es programar?

> Cómo definirían ustedes lo que es programar?




![[Pasted image 20260305185444.png|355]]

---


> [!STICKY|green center title]
> ¿Qué es programar?.
> 
> Programar es **dar instrucciones claras y ordenadas a un computador para resolver o automatizar un problema.**


---

Programar a fin de cuentas es como aprender un segundo lenguaje. 

Cambia la sintaxis, la forma lógica de estructurar las oraciones.

Es aprender un lenguaje que puede entender un computador para que este ejecute tareas que nosotros queramos.

note:

Mientras más uno se expone a un segundo lenguaje, más fácil se vuelve

---

>[!CITE] "Programar es codificar el conocimiento referente a un proceso de datos para la generación de información. Es construir un modelo de un proceso de la vida real para automatizarlo y hacer que la computadora lo ejecute tantas veces como queramos".
>                                        Gerardo Ayala 

---

Programar a fin de cuentas es como aprender un segundo lenguaje. 

Cambia la sintaxis, la forma lógica de estructurar las oraciones.

Es aprender un lenguaje que puede entender un computador para que este ejecute tareas que nosotros queramos.

note:

Mientras más se exponen a un segundo lenguaje, más fácil se vuelve

---

> Ejemplos de la vida real:
> - receta de cocina
> - instrucciones para armar un mueble
> - pasos para llegar a un lugar

---


Estas son series de instrucciones que nos permiten a nosotros humanos resolver un problema. Tomemos otro ejemplo:

---



> ¿Cómo darían instrucciones para abrir una botella?


---

Para dar instrucciones a un ordenador, a diferencia de un humano, necesitamos:

- ser *precisos*, dar las instrucciones con suficiente *detalle*
- dar las instrucciones de forma *ordenada*
- tratar de dar la *cantidad* de reglas justas (abstracción) para realizar la acción deseada, la cual debe ser capaz de concretar el computador.

<!-- .element: class="fragment" --> **Siempre** comprueben que el código que hicieron realmente hace lo que quieren y no otra cosa.


---
#### Pensamiento computacional


El pensamiento computacional es una forma de resolver problemas aplicando una lógica y técnicas similares a las que utiliza un computador para resolver tareas.

 Si queremos que el computador "cocine la receta", tenemos que entregarle las instrucciones en un lenguaje que este maneje. <!-- .element: class="fragment" -->

---

Algunos pilares de este son:


|                                                                                 |                                                                                                              |
| ------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------ |
| **Reconocimiento de Patrones**<br><br>Identificar elementos que se repiten.     | **Abstracción**<br><br>Simplificar lo más posible un problema complejo.                                      |
| **Descomposición de Problemas**<br><br>Dividir un problema en partes pequeñas.  | **Debugging**<br><br>Solucionar los problemas en el código para que este haga exactamente lo que debe hacer. |
| **Algoritmization**<br><br>Definir los pasos exactos para resolver el problema. |                                                                                                              |

---
### Reconocimiento de Patrones

Si les muestro esta secuencia...

2, 4, 6, 8, x

¿Qué valor tiene x?

---
O esta otra...

0, 1, 1, 2, 3, 5, 8, 13, ...

¿Les suena?

---

Ahora... ¿Por qué sería útil reconocer patrones en programación?


---

### Descomposición de problemas

Es dividir una gran tarea en las pequeñas tareas que lo componen.

Ej:

> Eres un programador para una Pime y te piden diseñar la página web donde los usuarios podrán crear sus cuentas y en ellas hacer las compras. ¿Cómo dividirías esta tarea?

---

Algunas subtareas que tendrías que hacer serían:

1. Generar la interfaz de la página web
2. Generar la página de registro de usuarios
3. Almacenar la información de cada usuario
4. Generar las ventanas de búsqueda de productos
5. Añadir productos a un carro
6. Ir a la página de pago

---

Entonces, descomponer un problema es listar los pasos que hay que seguir para lograr el objetivo final, subdividir la tarea en tareas más pequeñas. 

---
### Definir un algoritmo

Esto es ya la instrucción exacta que se le introduciría al computador, como una receta que debe seguir.

El algoritmo entonces consiste de una "entrada" o "input", y una función que ejecuta los pasos de forma ordenada para generar una "salida" o "output".

note:
 hacer dibujo y comparación con una función matemática.

---

- El algoritmo debe tener **pasos claros**, tratando de tener el mayor nivel de abstracción posible para ser eficiente.
- Debe tratar de ser lo más completo posible, es decir, teniendo en cuenta todas las posibilidades del problema para arrojar una salida.
- Debe tener un número finito de pasos.
- Puede ser determinista o no, es decir, arrojar siempre la misma solución al mismo input o no.

---
De acuerdo a Donald Knuth, los algoritmos tienen 5 características:

1. Finitud
2. Proceso definido
3. Datos de entrada
4. Información de salida
5. Efectividad

---

#### Problema

> Diseñar un sistema para calcular el promedio de notas de un estudiante. Digamos que tenemos las notas 5.8, 6.3, 5.3.

---

Para esto... 

- ¿Qué datos necesitamos?
- ¿Qué queremos que haga el programa?
- ¿Cómo el programa podría llevar a cabo lo que queremos que haga?

---

Una lógica sería:

1. pedir las notas
2. sumar las notas
3. contar cuántas hay en total
4. dividir la suma entre el total
5. mostrar resultado final

---

Un algoritmo sería:

1. Introducir N1, N2, N3
2. Sumar N1 + N2 + N3
3. Dividir el total de la suma en 3
4. Mostrar el resultado final

note:

comparar con una receta de cocina

---

Aquí no necesitamos saber qué alumno es el que obtuvo esas notas, qué ramo es el cursado, estamos simplificando el problema lo más posible.

---

¿Es este un algoritmo determinista?


---
Y en el caso anterior... ¿Qué pasa si en vez de 3 notas tenemos 4?, ¿Y si tenemos 20?, ¿Y qué pasa si no sabemos cuántas notas se van a introducir?

note:

Aquí entra el reconocimiento de patrones. 

---

El algoritmo anterior entonces debe ser capaz de calcular el número de notas que se le ha introducido y dividir por ese número.

1. Introducir N1, N2, N3, ..., Nx
2. Sumar N1 + N2 + N3 + ... + Nx
3. Calcular el número total de notas x
4. Dividir el total de la suma en x
5. Mostrar el resultado final

---

#### Problema:

> Diseñar un algoritmo que determine si un número es par o impar.


---

Para esto... 

- ¿Qué datos necesitamos?
- ¿Qué queremos que haga el programa?
- ¿Cómo el programa podría llevar a cabo lo que queremos que haga?

---

1. leer número  (input)
2. dividir en 2  y sacar el módulo o resto
3. si el resultado es 0 → par (output)
4. si no → impar (output)

Esto es lo que en programación llamamos **pseudocódigo**.

---
### Objetivos:

- [ ] Aprender qué es la programación
- [ ] Aprender sobre reconocimiento de patrones
- [ ] Descomponer problemas
- [ ] Entender lo que es un algoritmo

note:

dejar las tareas para la otra clase, leer lo "importante"

---

### Tareas: 

- Piensa en el proceso de "comprar desayuno en el kiosko del campus".

1. Lista al menos 6 pasos del proceso (cómo dividirías la tarea). 
2. Analiza si estás omitiendo algún detalle irrelevante o si estás incorporándolos sin darte cuenta (vamos a analizar el nivel de abstracción de nuestra solución).
3. Identifica los patrones (¿Qué se repetiría si eliges una opción del menú u otra?)
4. Redacta el algoritmo del proceso.

---

- Es hora de llegar a la universidad a tu primera clase. 
1. Escribe tres variantes de movilidad que puedes tomar (ej: bus, metro, bici).
2. Marca los patrones comunes al tomar cada ruta y las diferencias.
3. Define al menos 6 pasos que sirvan en común a las tres variantes de movilidad con un nivel alto de abstracción.


---
#### Importante:

- Para esta parte del curso, les recomiendo hacer las actividades primero a mano, aunque desde la segunda unidad será necesario que sí o sí utilicen los computadores.
- No olvidar que la asistencia es obligatoria, deben tener al menos un 70%.
- Programar no es algo que uno nace sabiendo (es un segundo lenguaje), hay que estudiarlo mucho!
- Tratar de hablar con otra persona ayuda mucho a ordenar sus ideas.


