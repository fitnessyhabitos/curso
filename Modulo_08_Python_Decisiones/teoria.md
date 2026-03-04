# 📖 Módulo 8 – Python: Decisiones con if/else

## 🚦 El semáforo de la programación

En la vida real tomamos decisiones todo el tiempo:
- **Si** llueve, cojo el paraguas. **Si no**, no lo cojo.
- **Si** tengo hambre, como. **Si no**, espero.

Los programas también necesitan tomar decisiones. Para eso usamos `if`, `elif` y `else`.

---

## ❓ Condiciones y comparaciones

Antes de ver `if`, necesitamos entender las **condiciones**. Una condición es algo que puede ser **Verdadero** (`True`) o **Falso** (`False`).

### Operadores de comparación:

| Operador | Significado | Ejemplo | Resultado |
|----------|------------|---------|-----------|
| `==` | igual a | `5 == 5` | `True` |
| `!=` | distinto de | `5 != 3` | `True` |
| `>` | mayor que | `10 > 3` | `True` |
| `<` | menor que | `3 < 10` | `True` |
| `>=` | mayor o igual | `5 >= 5` | `True` |
| `<=` | menor o igual | `3 <= 5` | `True` |

> ⚠️ **¡Cuidado!** `=` asigna valor, `==` compara.
> ```python
> edad = 10     # Asigna 10 a edad
> edad == 10    # Compara: ¿es edad igual a 10? → True
> ```

---

## 🔀 La estructura if básica

```python
if condición:
    # Código que se ejecuta si la condición es True
    # (debe estar indentado con 4 espacios o 1 tabulador)
```

### Ejemplo:
```python
edad = 10

if edad >= 18:
    print("Eres mayor de edad")

print("Esta línea siempre se ejecuta")
```

> 💡 **La indentación es CRUCIAL en Python.** El código dentro del `if` debe estar indentado (desplazado hacia la derecha). Si no, Python dará error.

---

## 🔀 if / else

```python
if condición:
    # Se ejecuta si la condición es True
else:
    # Se ejecuta si la condición es False
```

### Ejemplo:
```python
numero = int(input("Escribe un número: "))

if numero % 2 == 0:
    print(f"{numero} es un número PAR")
else:
    print(f"{numero} es un número IMPAR")
```

---

## 🔀 if / elif / else

Cuando hay más de dos opciones, usamos `elif` (else if = si no, si):

```python
if condición1:
    # Si condición1 es True
elif condición2:
    # Si condición1 es False Y condición2 es True
elif condición3:
    # Si condición1 y 2 son False Y condición3 es True
else:
    # Si ninguna condición anterior es True
```

### Ejemplo: Calificación escolar
```python
nota = float(input("¿Cuál es tu nota? "))

if nota >= 9:
    calificacion = "Sobresaliente"
elif nota >= 7:
    calificacion = "Notable"
elif nota >= 6:
    calificacion = "Bien"
elif nota >= 5:
    calificacion = "Suficiente"
else:
    calificacion = "Insuficiente"

print(f"Tu calificación es: {calificacion}")
```

---

## 🔗 Operadores lógicos: and, or, not

Puedes combinar condiciones:

### `and` – Las dos condiciones deben ser True:
```python
edad = 12
tiene_permiso = True

if edad >= 10 and tiene_permiso:
    print("Puedes entrar")
```

### `or` – Al menos una condición debe ser True:
```python
dia = "sabado"

if dia == "sabado" or dia == "domingo":
    print("¡Es fin de semana!")
else:
    print("Es día de colegio")
```

### `not` – Invierte la condición:
```python
lloviendo = False

if not lloviendo:
    print("¡Perfecto para salir a jugar!")
```

### Tabla de verdad:

| A | B | A and B | A or B | not A |
|---|---|---------|--------|-------|
| True | True | True | True | False |
| True | False | False | True | False |
| False | True | False | True | True |
| False | False | False | False | True |

---

## 📦 if dentro de if (if anidado)

Puedes poner un `if` dentro de otro `if`:

```python
edad = 15
tiene_carnet = False

if edad >= 18:
    if tiene_carnet:
        print("Puedes conducir")
    else:
        print("Eres mayor de edad pero no tienes carnet")
else:
    print("Eres menor de edad, no puedes conducir")
```

---

## 🔍 Comprobar si algo está en una lista o texto

```python
frutas = ["manzana", "naranja", "pera"]

fruta = input("¿Qué fruta tienes? ").lower()

if fruta in frutas:
    print(f"¡{fruta} es una fruta de nuestra lista!")
else:
    print(f"{fruta} no está en nuestra lista.")
```

---

## 💡 Ejemplo completo: El semáforo

```python
color = input("¿De qué color está el semáforo? ").lower()

if color == "verde":
    print("🟢 ¡Puedes pasar!")
elif color == "amarillo":
    print("🟡 Prepárate para parar")
elif color == "rojo":
    print("🔴 ¡PARA! No puedes pasar")
else:
    print("❓ Ese no es un color válido de semáforo")
```

---

## 📋 Resumen del Módulo 8

| Concepto | Sintaxis |
|----------|---------|
| Si... | `if condición:` |
| Si no... | `else:` |
| Si no, si... | `elif condición:` |
| Y además | `condición1 and condición2` |
| O también | `condición1 or condición2` |
| No es | `not condición` |
| Está en | `elemento in colección` |

---

## 🧠 ¿Lo entendiste?

1. ¿Qué diferencia hay entre `=` y `==`?
2. ¿Qué pasa si una condición `if` es `False` y no hay `else`?
3. ¿Cuántos `elif` puede tener un bloque `if`?
4. ¿Qué devuelve `True and False`?

---

➡️ **Siguiente:** `Modulo_08_Python_Decisiones/actividades.md`
