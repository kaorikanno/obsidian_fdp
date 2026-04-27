
def calcular_imc(peso, altura):
    imc = peso / (altura ** 2)
    imc_redondeado = round(imc, 1)
    
    if imc < 18.5:
        categoria = "Bajo peso"
    elif imc < 25:
        categoria = "Normal"
    elif imc < 30:
        categoria = "Sobrepeso"
    else:
        categoria = "Obesidad"
    
    return (imc_redondeado, categoria)

def analizar_numero(n):
    resultado = {
        "es_entero_positivo": False,
        "es_par": False,
        "multiplo_de": []
    }
    
    if isinstance(n, int) and n > 0:
        resultado["es_entero_positivo"] = True
        resultado["es_par"] = n % 2 == 0
        
        if n % 3 == 0:
            resultado["multiplo_de"].append(3)
        if n % 5 == 0:
            resultado["multiplo_de"].append(5)
    
    return resultado

def adivinar_numero(intento, secreto, limite_inferior, limite_superior):
    if intento < limite_inferior or intento > limite_superior:
        return "fuera de rango"
    
    if intento < secreto:
        return "muy bajo"
    elif intento > secreto:
        return "muy alto"
    else:
        return "correcto"

def tipo_triangulo(a, b, c):
    # Verificar que todos los lados sean positivos
    if a <= 0 or b <= 0 or c <= 0:
        return "No es un triángulo válido"
    
    # Verificar desigualdad triangular
    if a + b <= c or a + c <= b or b + c <= a:
        return "No es un triángulo válido"
    
    if a == b == c:
        return "Triángulo equilátero"
    elif a == b or a == c or b == c:
        return "Triángulo isósceles"
    else:
        return "Triángulo escaleno"

def calcular_precio(precio_original, porcentaje_descuento, es_miembro_vip):
    descuento_principal = precio_original * (porcentaje_descuento / 100)
    precio_con_descuento = precio_original - descuento_principal
    
    if es_miembro_vip:
        descuento_vip = precio_con_descuento * 0.05
        precio_final = precio_con_descuento - descuento_vip
        ahorro_total = descuento_principal + descuento_vip
    else:
        precio_final = precio_con_descuento
        ahorro_total = descuento_principal
    
    return (round(precio_final, 2), round(ahorro_total, 2))

def es_bisiesto(anio):
    if anio % 400 == 0:
        return True
    if anio % 100 == 0:
        return False
    if anio % 4 == 0:
        return True
    return False