# 📄 Hoja de Referencia Rápida

## 🐢 LOGO – Comandos esenciales

| Comando | Forma corta | Descripción |
|---------|-------------|-------------|
| `FORWARD n` | `FD n` | Avanza n pasos |
| `BACK n` | `BK n` | Retrocede n pasos |
| `RIGHT n` | `RT n` | Gira n grados a la derecha |
| `LEFT n` | `LT n` | Gira n grados a la izquierda |
| `PENUP` | `PU` | Sube el lápiz |
| `PENDOWN` | `PD` | Baja el lápiz |
| `CLEARSCREEN` | `CS` | Borra la pantalla |
| `HOME` | — | Vuelve al centro |
| `HIDETURTLE` | `HT` | Esconde la tortuga |
| `SHOWTURTLE` | `ST` | Muestra la tortuga |
| `SETPENCOLOR [r g b]` | `SETPC [r g b]` | Color del lápiz |
| `SETPENWIDTH n` | — | Grosor del lápiz |
| `SETBACKGROUND [r g b]` | `SETBG [r g b]` | Color de fondo |
| `REPEAT n [cmds]` | — | Repite n veces |
| `TO nombre ... END` | — | Define procedimiento |

### Ángulos de polígonos:
| Polígono | Lados | Ángulo de giro |
|----------|-------|----------------|
| Triángulo | 3 | 120° |
| Cuadrado | 4 | 90° |
| Pentágono | 5 | 72° |
| Hexágono | 6 | 60° |
| Octágono | 8 | 45° |
| n-ágono | n | 360°/n |

---

## 🐍 PYTHON – Conceptos esenciales

### Tipos de datos:
```python
texto = "Hola"          # str
entero = 10             # int
decimal = 3.14          # float
booleano = True         # bool
lista = [1, 2, 3]       # list
```

### Entrada y salida:
```python
print("Texto")                    # Mostrar
print(f"Hola {nombre}")           # f-string
x = input("Pregunta: ")           # Pedir texto
n = int(input("Número: "))        # Pedir número entero
f = float(input("Decimal: "))     # Pedir decimal
```

### Operadores matemáticos:
```python
a + b    # suma
a - b    # resta
a * b    # multiplicación
a / b    # división
a // b   # división entera
a % b    # módulo (resto)
a ** b   # potencia
```

### Condiciones:
```python
if condicion:
    # código
elif otra_condicion:
    # código
else:
    # código

# Operadores de comparación:
== != > < >= <=

# Operadores lógicos:
and  or  not
```

### Bucles:
```python
# While
while condicion:
    # código
    # (recuerda cambiar la condición)

# For con range
for i in range(10):        # 0 a 9
for i in range(1, 11):     # 1 a 10
for i in range(0, 10, 2):  # 0,2,4,6,8

# For con lista
for elemento in lista:
    # código

# Salir del bucle
break

# Saltar iteración
continue
```

### Funciones:
```python
def mi_funcion():
    # código

def con_parametros(a, b):
    return a + b

# Llamar:
mi_funcion()
resultado = con_parametros(3, 5)
```

### Listas:
```python
lista = [1, 2, 3]

lista[0]             # primer elemento
lista[-1]            # último elemento
lista[1:3]           # slice

lista.append(x)      # añadir al final
lista.insert(i, x)   # insertar en posición
lista.remove(x)      # eliminar por valor
del lista[i]         # eliminar por posición
lista.pop()          # eliminar y devolver último

len(lista)           # longitud
lista.sort()         # ordenar
x in lista           # ¿está?

for x in lista:      # recorrer
    print(x)
```

### Cadenas de texto:
```python
texto = "Hola Mundo"

len(texto)           # 10
texto.upper()        # "HOLA MUNDO"
texto.lower()        # "hola mundo"
texto.replace(a, b)  # reemplazar
texto.split(" ")     # dividir
texto.strip()        # quitar espacios
texto[0]             # primera letra
texto[-1]            # última letra
texto[0:4]           # slice → "Hola"
"Mundo" in texto     # True
```

### Librerías útiles:
```python
import random
random.randint(1, 10)     # entero aleatorio
random.choice(lista)      # elemento aleatorio

import math
math.sqrt(25)             # raíz cuadrada
math.pi                   # 3.14159...
math.floor(3.9)           # 3
math.ceil(3.1)            # 4

import time
time.sleep(1)             # espera 1 segundo
```

---

## 🎨 Colores RGB más usados

| Color | Código |
|-------|--------|
| Negro | [0, 0, 0] |
| Blanco | [255, 255, 255] |
| Rojo | [255, 0, 0] |
| Verde | [0, 200, 0] |
| Azul | [0, 0, 255] |
| Amarillo | [255, 255, 0] |
| Naranja | [255, 165, 0] |
| Morado | [128, 0, 128] |
| Rosa | [255, 192, 203] |
| Marrón | [139, 69, 19] |
| Gris | [128, 128, 128] |
| Cielo | [135, 206, 235] |

---

## ⌨️ Atajos en Thonny

| Atajo | Acción |
|-------|--------|
| F5 | Ejecutar programa |
| Ctrl+Z | Deshacer |
| Ctrl+S | Guardar |
| Ctrl+C | Copiar |
| Ctrl+V | Pegar |
| Tab | Indentar (4 espacios) |
| Ctrl+/ | Comentar/descomentar |
