# 📖 Módulo 10 – Python: Funciones

## 🤔 ¿Por qué necesitamos funciones?

Imagina que quieres saludar a diferentes personas en tu programa:

```python
# Sin funciones - repetimos código
print("¡Hola, Ana!")
print("Bienvenida al programa")
print("Espero que lo disfrutes")

print("¡Hola, Carlos!")
print("Bienvenido al programa")
print("Espero que lo disfrutes")

print("¡Hola, Lucía!")
print("Bienvenida al programa")
print("Espero que lo disfrutes")
```

¿Y si el saludo cambia? Hay que cambiarlo 3 veces. Con funciones, solo una vez.

---

## 📦 Definir una función

```python
def nombre_funcion():
    # Código de la función
```

```python
def saludar():
    print("¡Hola!")
    print("Bienvenido al programa")
    print("Espero que lo disfrutes")
```

### Llamar (usar) la función:
```python
saludar()    # ← Así se llama a la función
saludar()    # ← Puedes llamarla las veces que quieras
```

---

## 🎯 Funciones con parámetros

Los **parámetros** son variables que recibe la función cuando la llamas:

```python
def saludar(nombre):
    print(f"¡Hola, {nombre}!")
    print("Bienvenido al programa")

saludar("Ana")     # nombre = "Ana"
saludar("Carlos")  # nombre = "Carlos"
saludar("Lucía")   # nombre = "Lucía"
```

### Múltiples parámetros:
```python
def presentar(nombre, edad, ciudad):
    print(f"Me llamo {nombre}, tengo {edad} años y vivo en {ciudad}.")

presentar("Ana", 10, "Madrid")
presentar("Carlos", 11, "Barcelona")
```

---

## 🔙 El `return` – Devolver resultados

Una función puede **devolver** un resultado que puedes usar después:

```python
def sumar(a, b):
    resultado = a + b
    return resultado
```

Ahora puedes usar el resultado:
```python
total = sumar(3, 5)
print(total)           # → 8
print(sumar(10, 20))   # → 30
```

### Más ejemplos con return:

```python
def calcular_area_rectangulo(base, altura):
    area = base * altura
    return area

def es_par(numero):
    return numero % 2 == 0    # Devuelve True o False

def mayor_de_dos(a, b):
    if a > b:
        return a
    else:
        return b
```

Usándolas:
```python
area = calcular_area_rectangulo(5, 3)
print(f"El área es: {area}")        # → 15

if es_par(10):
    print("10 es par")

mayor = mayor_de_dos(7, 12)
print(f"El mayor es: {mayor}")       # → 12
```

---

## 💡 Parámetros con valor por defecto

Puedes dar valores por defecto a los parámetros:

```python
def saludar(nombre, saludo="¡Hola"):
    print(f"{saludo}, {nombre}!")

saludar("Ana")                    # Usa el saludo por defecto → ¡Hola, Ana!
saludar("Carlos", "¡Buenos días") # Usa el saludo dado → ¡Buenos días, Carlos!
```

---

## 🔭 Variables locales y globales

Las variables **locales** existen solo dentro de la función:

```python
def mi_funcion():
    x = 10          # Variable local
    print(x)        # ✅ Funciona

mi_funcion()
print(x)            # ❌ ERROR: x no existe fuera de la función
```

Las variables **globales** existen en todo el programa:
```python
nombre = "Ana"      # Variable global

def saludar():
    print(f"Hola, {nombre}")   # Puede leer la variable global

saludar()           # ✅ Funciona
```

---

## 🏗️ Funciones que usan otras funciones

```python
def cuadrado(n):
    return n * n

def suma_cuadrados(a, b):
    return cuadrado(a) + cuadrado(b)    # Llama a cuadrado()

resultado = suma_cuadrados(3, 4)
print(resultado)   # → 9 + 16 = 25
```

---

## 📋 Resumen del Módulo 10

| Concepto | Sintaxis | Ejemplo |
|----------|---------|---------|
| Definir función | `def nombre():` | `def saludar():` |
| Con parámetros | `def nombre(param):` | `def saludar(nombre):` |
| Con valor por defecto | `def nombre(p=valor):` | `def saludar(n="amigo"):` |
| Devolver valor | `return valor` | `return a + b` |
| Llamar función | `nombre()` | `saludar()` |
| Llamar con parámetros | `nombre(valor)` | `saludar("Ana")` |

---

## 🧠 ¿Lo entendiste?

1. ¿Cuál es la diferencia entre definir una función y llamarla?
2. ¿Para qué sirve `return`?
3. ¿Puede una función tener varios `return`?
4. ¿Qué es una variable local?

---

➡️ **Siguiente:** `Modulo_10_Python_Funciones/actividades.md`
