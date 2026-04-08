
[[Semana 4]]

### Tareas: 

- Dada una lista de 8 temperaturas, diseña un algoritmo con dos subprocedimientos: maximo() y minimo(), de modo que el algoritmo sea capaz de entregar la temperatura más alta y la más baja como salida.
- Prueba primero con una lista dada, como: $[10, 15, 17, 20, 23, 10, 12, 7]$
---

- Te piden programar el agendar ayudantías. 
1. Analiza los distintos subprocedimientos (módulos): validación de la ayudantía, conflicto de horarios del ayudante, confirmación, búsqueda de salas, etc. Describe la interfaz (entradas/salidas) de cada módulo.
2. Propón un diseño del flujo entre los módulos.
3. Piensa en otra situación similar donde también puedas reutilizar este flujo con muy pequeños cambios.

---

1. Leer lista
2. maximo = primera temperatura lista
3. minimo = primera temperatura lista
4. Para cada temperatura en la lista:
5.  si temperatura > maximo:
6.     maximo = temperatura
7.   si temperatura < minimo:
8.     minimo = temperatura
9. Mostrar maximo y minimo

---

1. entradas:

nombre ayudante, curso , curso aprobado o no por ayudante → validar_ayudantia() → aprobado o no
horario de ayudante → ver_conflictos() → seleccionar horarios sin tope si hay
conflictos de horario, sala disponible, ayudantía validada → confirmar_reserva() → aceptar o declinar
 salas disponibles→ buscar_sala() → sala seleccionada

2. validar_ayudantia → buscar_sala → ver_conflictos → confirmar reserva

3. validar_compra → ver dirección → ver día de entrega → confirmar pago
