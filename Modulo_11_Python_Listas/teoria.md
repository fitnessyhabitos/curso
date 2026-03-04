# 📖 Módulo 11 – Python: Listas

## 📋 ¿Qué es una lista?

Hasta ahora, con las variables solo guardábamos **una cosa** a la vez:
```python
fruta1 = "manzana"
fruta2 = "naranja"
fruta3 = "pera"
```

¿Y si queremos guardar 100 frutas? ¡Eso sería imposible así! Las **listas** nos permiten guardar **muchas cosas en una sola variable**:

```python
frutas = ["manzana", "naranja", "pera", "uva", "fresa"]
```

---

## 🔨 Crear listas

```python
# Lista de textos
colores = ["rojo", "verde", "azul"]

# Lista de números
notas = [8.5, 7.0, 9.5, 6.0]

# Lista mixta
datos = ["Ana", 10, True, 1.75]

# Lista vacía
lista_vacia = []
```

---

## 🔍 Acceder a los elementos

Cada elemento tiene una **posición** (índice) que empieza en **0**:

```python
frutas = ["manzana", "naranja", "pera", "uva"]
#           0            1         2       3    ← índices

print(frutas[0])    # → manzana
print(frutas[1])    # → naranja
print(frutas[-1])   # → uva (el último)
print(frutas[-2])   # → pera (el penúltimo)
```

### Fragmentos de lista (slice):
```python
numeros = [1, 2, 3, 4, 5, 6, 7, 8]

print(numeros[2:5])   # → [3, 4, 5] (del índice 2 al 4)
print(numeros[:3])    # → [1, 2, 3] (los 3 primeros)
print(numeros[5:])    # → [6, 7, 8] (del 5 al final)
```

---

## ➕ Añadir elementos

```python
frutas = ["manzana", "naranja"]

frutas.append("pera")         # Añade al final
print(frutas)                 # → ['manzana', 'naranja', 'pera']

frutas.insert(1, "fresa")     # Inserta en posición 1
print(frutas)                 # → ['manzana', 'fresa', 'naranja', 'pera']
```

---

## ➖ Eliminar elementos

```python
colores = ["rojo", "verde", "azul", "rojo"]

colores.remove("rojo")    # Elimina el PRIMER "rojo"
print(colores)            # → ['verde', 'azul', 'rojo']

del colores[0]            # Elimina por posición
print(colores)            # → ['azul', 'rojo']

ultimo = colores.pop()    # Elimina y devuelve el último
print(ultimo)             # → 'rojo'
print(colores)            # → ['azul']
```

---

## 🔧 Operaciones con listas

```python
numeros = [5, 3, 8, 1, 9, 2, 7]

print(len(numeros))       # → 7 (longitud)
print(max(numeros))       # → 9 (el mayor)
print(min(numeros))       # → 1 (el menor)
print(sum(numeros))       # → 35 (la suma)

numeros.sort()            # Ordena de menor a mayor
print(numeros)            # → [1, 2, 3, 5, 7, 8, 9]

numeros.sort(reverse=True)  # Ordena de mayor a menor
print(numeros)            # → [9, 8, 7, 5, 3, 2, 1]

numeros.reverse()         # Invierte el orden
print(numeros)            # → [1, 2, 3, 5, 7, 8, 9]

print(numeros.count(5))   # → 1 (cuántas veces está el 5)
print(numeros.index(7))   # → 4 (en qué posición está el 7)
```

---

## 🔄 Recorrer listas con for

```python
frutas = ["manzana", "naranja", "pera"]

# Recorrer elementos
for fruta in frutas:
    print(f"Me gusta la {fruta}")

# Recorrer con índice
for i, fruta in enumerate(frutas):
    print(f"{i+1}. {fruta}")
```

---

## ➕ Unir y copiar listas

```python
lista1 = [1, 2, 3]
lista2 = [4, 5, 6]

# Unir listas
lista3 = lista1 + lista2
print(lista3)    # → [1, 2, 3, 4, 5, 6]

# Extender una lista
lista1.extend(lista2)
print(lista1)    # → [1, 2, 3, 4, 5, 6]

# Repetir lista
lista4 = [0] * 5
print(lista4)    # → [0, 0, 0, 0, 0]
```

---

## ✅ Comprobar si un elemento está en la lista

```python
frutas = ["manzana", "naranja", "pera"]

if "naranja" in frutas:
    print("¡Tenemos naranjas!")

if "mango" not in frutas:
    print("No tenemos mangos")
```

---

## 📋 Resumen del Módulo 11

| Operación | Código | Ejemplo |
|-----------|--------|---------|
| Crear lista | `lista = [a, b, c]` | `numeros = [1, 2, 3]` |
| Acceder | `lista[i]` | `lista[0]` |
| Añadir al final | `lista.append(x)` | `frutas.append("uva")` |
| Insertar | `lista.insert(i, x)` | `lista.insert(0, "X")` |
| Eliminar por valor | `lista.remove(x)` | `lista.remove("pera")` |
| Eliminar por posición | `del lista[i]` | `del lista[0]` |
| Longitud | `len(lista)` | `len(frutas)` |
| Ordenar | `lista.sort()` | `numeros.sort()` |
| ¿Está? | `x in lista` | `"pera" in frutas` |
| Recorrer | `for x in lista:` | — |

---

## 🧠 ¿Lo entendiste?

1. ¿Cuál es el índice del primer elemento de una lista?
2. ¿Qué diferencia hay entre `.append()` e `.insert()`?
3. ¿Cómo eliminas el último elemento de una lista?
4. ¿Cómo recorres una lista mostrando el número de posición?

---

➡️ **Siguiente:** `Modulo_11_Python_Listas/actividades.md`
