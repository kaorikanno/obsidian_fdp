
[[Semana 2]]

### Tareas: 

- Escribir un algoritmo para "Cargar TNE y verificar que el saldo sea suficiente para 2 viajes". 
1. Debe ingresar la carga y sumarla al saldo que ya tenía la tarjeta.
2. Debe revisar que el monto final sea suficiente para dos viajes.

---

- Hacer el pseudocódigo para "reservar la sala de estudio en biblioteca". Para ello debe cumplir con:
1. Ingresar la solicitud (analizar qué información debe incluir la solicitud)
2. verificar disponibilidad
3. ver alternativas y elegir la primera
4. confirmar la reserva
5. incluir un bucle de búsqueda de horarios si no hay disponibilidad en el horario.

Por último, descríbele a alguien tu código y ve si siguiendo los pasos es posible o no concretar la acción.

---

- Hacer el pseudocódigo del proceso de elección de distintos productos para almorzar. Para esto, el algoritmo de entrada recibirá un presupuesto diario, una lista de items por comprar y de sus precios.
1. El proceso debe ser seleccionar ítems sin superar el presupuesto
2. La salida debe ser una lista de elementos y el saldo que quedó.


---

#### Soluciones:

TNE:

1. leer saldo actual y monto a cargar
2. ValorDePasaje = 880
3. sumar ambos montos
4. Si monto >= 2 * ValorDePasaje → Aprobar
5. Si monto < 2 * ValorDePasaje → No Aprobar

---

1. Ingresar la solicitud de día y hora de la reserva
2. mientras no se encuentre una reserva:
3.   verificar disponibilidad de alguna sala ese día y hora
4.   mostrar alternativas
5.   Si alternativas > 0 → reservar la primera
6.   confirmar la reserva
7.   Fin

---

1. Ingresar presupuesto, precios e items
2. crear una lista de compras
3. recorremos los items de la lista de precios:
4.   si precio_item < presupuesto:
5.     presupuesto = presupuesto - precio_item
6.     agregamos a la lista de compras el item
7.  si precio_item > presupuesto:
8.     saltar elemento

---

[[Semana 3]]