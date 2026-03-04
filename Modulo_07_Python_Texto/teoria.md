# 📖 Módulo 7 – Python: Texto y Cadenas de Caracteres

## 🔤 ¿Qué es una cadena de texto (string)?

En programación, al texto lo llamamos **cadena de texto** o **string** (en inglés). Una cadena es simplemente una secuencia de caracteres (letras, números, símbolos, espacios).

```python
nombre = "María"           # texto con comillas dobles
ciudad = 'Sevilla'         # texto con comillas simples (igual de válido)
frase = "Tengo 10 años"    # texto con número dentro
vacio = ""                 # cadena vacía
```

---

## 🔗 Unir cadenas: la concatenación

Puedes unir dos o más cadenas usando el operador `+`:

```python
saludo = "¡Hola, " + "mundo" + "!"
print(saludo)   # → ¡Hola, mundo!

nombre = "Lucía"
mensaje = "Buenos días, " + nombre + ". ¿Cómo estás?"
print(mensaje)  # → Buenos días, Lucía. ¿Cómo estás?
```

> ⚠️ **¡Importante!** No puedes unir texto con números directamente:
> ```python
> edad = 10
> print("Tengo " + edad + " años")    # ❌ ERROR
> print("Tengo " + str(edad) + " años")  # ✅ Correcto
> print(f"Tengo {edad} años")           # ✅ Más fácil con f-string
> ```

---

## 📏 La longitud de una cadena: len()

`len()` cuenta cuántos caracteres tiene una cadena:

```python
nombre = "Alejandro"
print(len(nombre))    # → 9

frase = "Hola mundo"
print(len(frase))     # → 10 (el espacio también cuenta)
```

---

## 🔡 Mayúsculas y minúsculas

```python
texto = "hOlA mUnDo"

print(texto.upper())      # → HOLA MUNDO (todo mayúsculas)
print(texto.lower())      # → hola mundo (todo minúsculas)
print(texto.capitalize()) # → Hola mundo (primera letra mayúscula)
print(texto.title())      # → Hola Mundo (primera de cada palabra)
```

---

## 🔍 Buscar dentro de una cadena

```python
frase = "Me gusta programar con Python"

# ¿Contiene la palabra?
print("Python" in frase)      # → True (sí está)
print("Java" in frase)        # → False (no está)

# ¿Cuántas veces aparece?
print(frase.count("a"))       # → 4

# ¿En qué posición está?
print(frase.find("Python"))   # → 24 (la posición 24)
print(frase.find("Java"))     # → -1 (no está)

# ¿Empieza o termina con...?
print(frase.startswith("Me")) # → True
print(frase.endswith("on"))   # → True
```

---

## ✂️ Acceder a partes de la cadena

### Un solo carácter (índice):
```python
texto = "Python"
#        012345  ← posiciones

print(texto[0])   # → P (primera letra)
print(texto[1])   # → y
print(texto[-1])  # → n (última letra)
print(texto[-2])  # → o (penúltima)
```

### Un fragmento (slice):
```python
texto = "Programar es genial"
#        0123456789...

print(texto[0:9])    # → Programar (del 0 al 8)
print(texto[10:12])  # → es
print(texto[13:])    # → genial (desde el 13 hasta el final)
print(texto[:9])     # → Programar (desde el inicio hasta el 8)
```

---

## 🔧 Modificar cadenas

```python
frase = "  ¡Hola, mundo!  "

# Quitar espacios del principio y del final
print(frase.strip())      # → ¡Hola, mundo!
print(frase.lstrip())     # → ¡Hola, mundo!   (solo del principio)
print(frase.rstrip())     # →   ¡Hola, mundo! (solo del final)

# Reemplazar texto
frase2 = "Me gusta el fútbol"
print(frase2.replace("fútbol", "programar"))  # → Me gusta el programar

# Dividir en partes
frase3 = "manzana,naranja,pera,uva"
frutas = frase3.split(",")   # → ['manzana', 'naranja', 'pera', 'uva']
print(frutas[0])             # → manzana

# Unir una lista de palabras
palabras = ["Hola", "programador"]
resultado = " ".join(palabras)
print(resultado)   # → Hola programador
```

---

## 🎨 Caracteres especiales

```python
print("Línea 1\nLínea 2")    # \n = nueva línea
print("Columna1\tColumna2")  # \t = tabulación (espacio largo)
print("Dijo \"Hola\"")       # \" = comilla dentro de comillas
print("Barra: \\")           # \\ = barra invertida
```

---

## 🔢 Multiplicar cadenas

```python
print("=" * 30)      # → ============================== (30 signos =)
print("Ha" * 3)      # → HaHaHa
separador = "-" * 40
print(separador)
```

---

## 📋 Resumen de métodos de cadenas

| Método | ¿Qué hace? | Ejemplo |
|--------|-----------|---------|
| `.upper()` | Todo mayúsculas | `"hola".upper()` → `"HOLA"` |
| `.lower()` | Todo minúsculas | `"HOLA".lower()` → `"hola"` |
| `.capitalize()` | Primera mayúscula | `"hola".capitalize()` → `"Hola"` |
| `.title()` | Cada palabra mayúscula | `"hola mundo".title()` → `"Hola Mundo"` |
| `.len()` | Longitud | `len("hola")` → `4` |
| `.strip()` | Quitar espacios | `" hola ".strip()` → `"hola"` |
| `.replace(a,b)` | Reemplazar | `"hola".replace("h","g")` → `"gola"` |
| `.split(sep)` | Dividir en lista | `"a,b".split(",")` → `["a","b"]` |
| `.count(x)` | Contar apariciones | `"aaa".count("a")` → `3` |
| `.find(x)` | Buscar posición | `"hola".find("l")` → `2` |
| `x in texto` | ¿Está dentro? | `"ho" in "hola"` → `True` |

---

## 🧠 ¿Lo entendiste?

1. ¿Qué devuelve `len("programar")`?
2. ¿Cómo conviertes "HOLA MUNDO" a "hola mundo"?
3. ¿Cuál es la diferencia entre `.find()` y `in`?
4. ¿Qué hace `"abc" * 3`?

---

➡️ **Siguiente:** `Modulo_07_Python_Texto/actividades.md`
