# 📖 Módulo 6 – Python: Números y Matemáticas

## 🧮 Python como calculadora

Python es una calculadora increíblemente potente. Puede hacer desde sumas simples hasta cálculos científicos complejos.

---

## ➕ Operaciones básicas

```python
print(5 + 3)      # Suma → 8
print(10 - 4)     # Resta → 6
print(3 * 7)      # Multiplicación → 21
print(15 / 4)     # División → 3.75
```

### Operadores especiales:

```python
print(15 // 4)    # División entera → 3  (solo el cociente, sin decimales)
print(15 % 4)     # Módulo (resto) → 3   (lo que sobra de la división)
print(2 ** 8)     # Potencia → 256       (2 elevado a 8)
```

> 💡 **¿Para qué sirve el módulo (%)?**
> - Para saber si un número es par: `numero % 2 == 0`
> - Para saber la hora con formato de 24h
> - Para crear patrones cíclicos

---

## 🔄 Convertir entre tipos de datos

Cuando usas `input()`, obtienes **texto** aunque el usuario escriba un número. Hay que convertirlo:

```python
# Sin convertir → ERROR al intentar sumar
edad_texto = input("¿Cuántos años tienes? ")
# edad_texto es "10" (texto), no 10 (número)

# Convertir texto a número entero:
edad = int(edad_texto)

# O en una sola línea (más fácil):
edad = int(input("¿Cuántos años tienes? "))
altura = float(input("¿Cuánto mides en metros? "))
```

### Conversiones más usadas:

| Función | ¿Qué hace? | Ejemplo |
|---------|-----------|---------|
| `int("10")` | Texto a número entero | `int("10")` → `10` |
| `float("3.14")` | Texto a número decimal | `float("3.14")` → `3.14` |
| `str(42)` | Número a texto | `str(42)` → `"42"` |
| `round(3.7)` | Redondea al entero más cercano | → `4` |
| `round(3.14159, 2)` | Redondea a 2 decimales | → `3.14` |

---

## 📐 Funciones matemáticas de Python

Python tiene funciones matemáticas muy útiles incluidas:

```python
print(abs(-5))       # Valor absoluto → 5
print(max(3, 7, 2))  # El mayor → 7
print(min(3, 7, 2))  # El menor → 2
print(sum([1,2,3]))  # Suma de lista → 6
print(round(3.6))    # Redondea → 4
```

### La librería math (más funciones):
```python
import math

print(math.sqrt(25))      # Raíz cuadrada → 5.0
print(math.pi)            # El número π → 3.14159...
print(math.floor(3.9))    # Redondear abajo → 3
print(math.ceil(3.1))     # Redondear arriba → 4
print(math.pow(2, 10))    # Potencia → 1024.0
```

---

## 🎲 Números aleatorios

Los números aleatorios son muy útiles para juegos. Python los genera con la librería `random`:

```python
import random

print(random.randint(1, 10))     # Número entero aleatorio entre 1 y 10
print(random.random())           # Número decimal entre 0.0 y 1.0
print(random.choice([1,2,3,4]))  # Elige uno al azar de la lista
```

---

## 🔢 Operadores de asignación compuestos

Son atajos para modificar variables:

```python
puntos = 100

puntos += 10    # Equivale a: puntos = puntos + 10  → 110
puntos -= 5     # Equivale a: puntos = puntos - 5   → 105
puntos *= 2     # Equivale a: puntos = puntos * 2   → 210
puntos //= 3    # Equivale a: puntos = puntos // 3  → 70
```

---

## 🧮 Ejemplo: Calculadora de notas

```python
# Calculadora de nota media

print("=== CALCULADORA DE NOTA MEDIA ===")

nota1 = float(input("Nota 1: "))
nota2 = float(input("Nota 2: "))
nota3 = float(input("Nota 3: "))

media = (nota1 + nota2 + nota3) / 3
media_redondeada = round(media, 2)

print(f"\nTus notas: {nota1}, {nota2}, {nota3}")
print(f"Media: {media_redondeada}")
```

---

## 🧮 Ejemplo: Calculadora de IMC

```python
import math

print("=== CALCULADORA DE IMC ===")

peso = float(input("¿Cuánto pesas en kg? "))
altura = float(input("¿Cuánto mides en metros? "))

imc = peso / (altura ** 2)
imc_redondeado = round(imc, 2)

print(f"\nTu IMC es: {imc_redondeado}")
```

---

## 📋 Resumen del Módulo 6

| Operador | Significado | Ejemplo | Resultado |
|----------|------------|---------|-----------|
| `+` | Suma | `5 + 3` | `8` |
| `-` | Resta | `10 - 4` | `6` |
| `*` | Multiplicación | `3 * 7` | `21` |
| `/` | División | `15 / 4` | `3.75` |
| `//` | División entera | `15 // 4` | `3` |
| `%` | Módulo (resto) | `15 % 4` | `3` |
| `**` | Potencia | `2 ** 8` | `256` |

---

## 🧠 ¿Lo entendiste?

1. ¿Cuál es el resultado de `17 % 5`?
2. ¿Qué diferencia hay entre `/` y `//`?
3. ¿Qué función usas para obtener la raíz cuadrada de un número?
4. ¿Por qué hay que usar `int()` cuando lees un número con `input()`?

---

➡️ **Siguiente:** `Modulo_06_Python_Numeros/actividades.md`
