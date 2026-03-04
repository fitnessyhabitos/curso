# 📖 Módulo 9 – Python: Bucles – Repetir sin cansarse

## 🔄 ¿Por qué necesitamos bucles?

Imagina que quieres imprimir los números del 1 al 100. Sin bucles tendrías que escribir:
```python
print(1)
print(2)
print(3)
# ... y así 97 veces más
print(100)
```

¡Con un bucle lo haces en 2 líneas! Los bucles son una de las herramientas más poderosas de la programación.

---

## 🔁 El bucle `while` – Mientras...

`while` repite un bloque de código **mientras** una condición sea verdadera.

```python
while condición:
    # Código que se repite
```

### Ejemplo básico:
```python
contador = 1

while contador <= 5:
    print(f"Número: {contador}")
    contador = contador + 1  # ¡Importante! Si no cambia, bucle infinito

print("¡Terminé!")
```

Resultado:
```
Número: 1
Número: 2
Número: 3
Número: 4
Número: 5
¡Terminé!
```

### ⚠️ Cuidado con el bucle infinito:
```python
# PELIGROSO - nunca termina
while True:
    print("Esto no para nunca")

# Siempre hay que cambiar algo para que la condición llegue a ser False
```

---

## 🔁 El bucle `for` – Para cada uno...

`for` repite el código para cada elemento de una secuencia.

### Con `range()`:

```python
for i in range(5):
    print(i)
# Imprime: 0, 1, 2, 3, 4
```

```python
for i in range(1, 6):
    print(i)
# Imprime: 1, 2, 3, 4, 5
```

```python
for i in range(0, 11, 2):
    print(i)
# Imprime: 0, 2, 4, 6, 8, 10 (de 2 en 2)
```

### Cómo funciona `range()`:
- `range(n)` → del 0 al n-1
- `range(inicio, fin)` → del inicio al fin-1
- `range(inicio, fin, paso)` → del inicio al fin-1, de `paso` en `paso`

### Recorrer texto:
```python
palabra = "Python"

for letra in palabra:
    print(letra)
# Imprime: P, y, t, h, o, n (uno por línea)
```

### Recorrer una lista:
```python
frutas = ["manzana", "naranja", "pera"]

for fruta in frutas:
    print(f"Me gusta la {fruta}")
```

---

## 🛑 break – Salir del bucle

`break` termina el bucle inmediatamente, aunque la condición siga siendo True:

```python
numero = 1

while True:
    print(numero)
    numero += 1
    if numero > 5:
        break    # Para cuando número llega a 6

print("Bucle terminado")
```

---

## ⏭️ continue – Saltar al siguiente

`continue` salta el resto del código de esta iteración y va a la siguiente:

```python
for i in range(10):
    if i % 2 == 0:    # Si es par
        continue      # Salta al siguiente
    print(i)          # Solo imprime los impares
# Imprime: 1, 3, 5, 7, 9
```

---

## 🔄 Bucles anidados (uno dentro de otro)

```python
for fila in range(1, 4):
    for columna in range(1, 4):
        print(f"({fila},{columna})", end=" ")
    print()  # Nueva línea al final de cada fila
```

Resultado:
```
(1,1) (1,2) (1,3)
(2,1) (2,2) (2,3)
(3,1) (3,2) (3,3)
```

### La tabla de multiplicar:
```python
numero = int(input("¿Tabla de qué número? "))

print(f"\n📊 TABLA DEL {numero}:")
print("─" * 20)

for i in range(1, 11):
    resultado = numero * i
    print(f"{numero} × {i:2} = {resultado:3}")
```

---

## 🔢 Acumular con bucles

Los bucles son perfectos para calcular sumas, promedios, etc.:

```python
# Suma de números del 1 al 100
suma = 0

for i in range(1, 101):
    suma += i

print(f"La suma de 1 a 100 es: {suma}")  # → 5050
```

```python
# Promedio de notas que introduce el usuario
notas = []
num_notas = int(input("¿Cuántas notas quieres introducir? "))

for i in range(num_notas):
    nota = float(input(f"Nota {i+1}: "))
    notas.append(nota)

promedio = sum(notas) / len(notas)
print(f"Tu nota media es: {round(promedio, 2)}")
```

---

## 🎮 Ejemplo: El juego de adivinar con intentos

```python
import random

secreto = random.randint(1, 100)
intentos = 0

print("Adivina el número entre 1 y 100")

while True:
    intento = int(input("Tu número: "))
    intentos += 1

    if intento == secreto:
        print(f"¡CORRECTO en {intentos} intento(s)!")
        break
    elif intento < secreto:
        print("Más alto...")
    else:
        print("Más bajo...")
```

---

## 📋 Resumen del Módulo 9

| Concepto | Sintaxis | Uso |
|----------|---------|-----|
| Bucle mientras | `while condición:` | Cuando no sabes cuántas veces |
| Bucle para | `for i in range(n):` | Cuando sabes cuántas veces |
| Recorrer lista | `for x in lista:` | Para cada elemento |
| Salir del bucle | `break` | Cuando se cumple una condición |
| Saltar iteración | `continue` | Para ignorar casos concretos |
| Contar | `contador += 1` | Para llevar la cuenta |
| Acumular | `suma += numero` | Para sumar valores |

---

## 🧠 ¿Lo entendiste?

1. ¿Cuál es la diferencia entre `while` y `for`?
2. ¿Qué pasa si olvidas cambiar la variable en un `while`?
3. ¿Qué números imprime `range(2, 10, 3)`?
4. ¿Para qué sirve `break`?

---

➡️ **Siguiente:** `Modulo_09_Python_Bucles/actividades.md`
