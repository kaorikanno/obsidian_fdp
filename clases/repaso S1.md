
---

##### Matriz IPO

> [!STICKY|green right title]
> Matriz IPO
> Esto es una matriz IPO:
> Input – Process – Output



| Entrada:           | Proceso:                    | Salida |
| ------------------ | --------------------------- | ------ |
| - base<br>- altura | - multiplicar base × altura | - área |

---
##### Diagrama de flujo:

```mermaid
graph TD
A[Leer numero] --> B{n = 0?}
B -- Si --> E[Mostrar vale 0]
B -- No --> F{n > 0?}
F -- Si --> J[Mostrar positivo]
F -- No --> K[Mostrar no positivo]

```

---

##### pseudocódigo:

1. Leer dígitos
2. si a > b entonces
    mostrar a
3. si a < b
	mostrar b
4. si a = b
	decir que ambos son iguales