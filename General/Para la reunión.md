
¿Quién corrige las pruebas?


---

#### Fácil

> Tienes una lista de temperaturas en Fahrenheit de la ciudad de Nueva York en verano. Sabes que la conversión de Fahrenheit a Celsius es dada por:
>
> °C = (°F - 32) x 5/9
> Donde °F es el valor de temperatura que se quiere transformar a Celsius.
>
>Quieres comparar estas temperaturas con la temperatura promedio en verano en Santiago. Para ello, quieres generar un algoritmo que al introducir una lista como la anterior, sea capaz de mostrar **solo** las temperaturas en Celsius de esa lista que superen los 30°C.

Ej de algunas de las T°:

 59 °F, 110 °F, 21°F, 72 °F, 42 °F.

Se pide entonces 
1. convertir estas temperaturas a °C 
2. que el algoritmo filtre aquellas °T mayores a 30°C


<span class="text-small-red"> 1. Leer lista de temperaturas </span>  
<span class="text-small-red"> 2. Para cada temperatura F en la lista:  </span>
<span class="text-small-red"> 3. C = (F - 32) * 5 / 9  </span> 
<span class="text-small-red"> 4. Si C > 30 entonces: </span>
<span class="text-small-red"> 5. Mostrar C   </span>

---

Trabajas ahora en el negocio de tu tío. Él quiere que cada producto tenga una ganancia del 10% del valor que le costó, pero además el precio final que verá el cliente tiene un impuesto de %15,25 respecto al precio con la ganancia incluida. Tu tío como sabe que eres ingeniero quiere que cada vez que él te pregunte el precio final de un artículo y te diga cuánto le costó, tú le respondas cuánto gana él por el producto, y el precio final de este. Realiza el diagrama IPO de este procedimiento.

Ej:

Leche:
- valor inicial: $800
- ganancia del tío: $80
- precio final que verá el cliente: $1342

El algoritmo entonces debería devolver la ganancia del tío y el precio final que vería el cliente. 

<span class="text-small-red"> Leer valor del producto </span>
<span class="text-small-red"> ganancia = 0.10xvalor </span>
<span class="text-small-red"> Sumar ganancia a valor </span>
<span class="text-small-red"> impuestos = 0.15xvalor </span>
<span class="text-small-red"> Sumar impuestos a valor </span>
<span class="text-small-red"> Mostrar valor </span>

---

#### Medio:

>Te piden hacer un código para simular el retiro de dinero un cajero automático. Para ello, debes comprobar que los 4 dígitos que ingrese el usuario sean los mismos 4 dígitos de su clave de banco. Si la clave es correcta, mostrar el saldo inicial, luego ver el monto de dinero a retirar (cualquier monto) y verificar que exista saldo suficiente como para retirar la cifra pedida, si es que se puede retirar, entonces que se descuente el dinero del monto inicial. 

Ej:

El cliente te entrega el número 1234 y quiere retirar $150.859.
El sistema te entrega la información del usuario, la clave 1234, y el saldo que tiene, que es $150.000.
El sistema debe comparar ambas claves y aprobar el uso del cajero, pero luego analizar si el dinero se puede retirar o no, que en este caso no se puede, pues el usuario quiere retirar más dinero del que posee. Si es que sí se pudiera, entonces descontar el saldo a retirar del monto inicial


<span class="text-small-red"> Leer clave ingresada por usuario y monto a retirar </span>
<span class="text-small-red"> Leer clave real del usuario y saldo inicial </span>
<span class="text-small-red"> Si clave ingresada y clave real son iguales: </span>
<span class="text-small-red"> Mostrar saldo inicial </span>
<span class="text-small-red"> Si saldo inicial es mayor a monto a retirar: </span>
<span class="text-small-red"> Monto inicial = Monto inicial - monto a retirar </span>

---
#### Difícil:

Trabajas en una boletería, donde cobran precios diferentes a sus usuarios según su edad. Si el usuario tiene:

- menos de 12 → entrada gratis
    
- entre 12 y 18 → $5.000
    
- si tiene 18 o más → $10.000

- Si es su mes de cumpleaños, entra gratis.

Los usuarios están registrados en el sistema, por lo que tienes su fecha de nacimiento en el formato mes-año. Debes informarle a cada cliente cuánto debe pagar según esto, sabiendo que el mes actual es abril.

Ej:

Un cliente nació el 01-2000, por lo que actualmente tiene 26 años.
Un cliente nació el 05-1999, por lo que también tiene 26 años.



<span class="text-small-red"> Leer mes de nacimiento y año de nacimiento </span>
<span class="text-small-red"> definir año actual= 2026 </span>
<span class="text-small-red"> definir mes actual = 4 </span>
<span class="text-small-red"> definir edad = año actual - año de nacimiento </span>
<span class="text-small-red"> Si mes actual es menor a mes de nacimiento → edad = edad - 1 </span>
<span class="text-small-red"> Si mes actual es actual a mes de nacimiento: </span>
<span class="text-small-red">     Mostrar "entrada gratis" </span>
<span class="text-small-red"> En otro caso si edad es menor a 12 entonces </span>
<span class="text-small-red">    Mostrar "entrada gratis" </span>
<span class="text-small-red"> O si edad menor a 18 entonces </span>
<span class="text-small-red">     Mostrar "Debe pagar $5000" </span>
<span class="text-small-red"> Sino </span>
<span class="text-small-red">     Mostrar "Debe pagar $10000" </span>


---
