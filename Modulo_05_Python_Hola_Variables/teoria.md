# 📖 Módulo 5 – Python: ¡Hola, Python! Variables y print

## 🐍 Bienvenido a Python

¡Hola de nuevo, programador! Ahora vamos a aprender **Python**, uno de los lenguajes de programación más usados en el mundo. Python está en:
- Los servidores de **YouTube** y **Google**
- Los robots de **NASA**
- Las aplicaciones de **Instagram**
- Los programas de **inteligencia artificial**

¡Y también en los primeros programas de miles de programadores que empezaron siendo niños como tú!

---

## 🖥️ Cómo usar Python

### Con Thonny:
1. Abre Thonny
2. Verás dos áreas:
   - **Arriba:** el editor (donde escribes el programa)
   - **Abajo:** la consola (donde ves los resultados)
3. Escribe tu código en el editor
4. Pulsa el botón **▶ Run** (o F5) para ejecutarlo

### Online (sin instalar):
- Ve a `https://repl.it`
- Crea un nuevo proyecto Python
- Escribe en el panel izquierdo y ve los resultados a la derecha

---

## 🖨️ El comando print()

El comando más importante en Python para empezar es `print()`. Le dice a Python que muestre algo en la pantalla.

```python
print("¡Hola, mundo!")
```

Cuando ejecutas esto, Python muestra:
```
¡Hola, mundo!
```

### Reglas del print():
- El texto va entre **comillas** (dobles `"` o simples `'`)
- Las instrucciones van entre **paréntesis** `()`
- Python distingue mayúsculas de minúsculas: `print` ≠ `Print` ≠ `PRINT`

### Ejemplos:
```python
print("¡Hola!")
print("Me llamo Python")
print("¡Aprender a programar mola!")
```

---

## 💬 Los comentarios en Python

Los comentarios son notas que tú escribes para explicar el código. Python los ignora completamente.

```python
# Esto es un comentario - Python no lo lee
print("¡Hola!")  # También puedes comentar al final de una línea
```

Usa los comentarios para:
- Explicar qué hace tu código
- Dejar notas para ti mismo
- Desactivar temporalmente una línea de código

---

## 📦 Variables: los cajones de la memoria

Una **variable** es como un cajón donde guardamos información. Le ponemos un nombre y guardamos un valor dentro.

```python
nombre = "Ana"
edad = 10
altura = 1.45
```

### Reglas para nombres de variables:
- ✅ `nombre`, `edad`, `mi_nombre`, `numero1`
- ❌ `1numero` (no puede empezar con número)
- ❌ `mi nombre` (no puede tener espacios)
- ❌ `for`, `if`, `print` (no puede ser palabra reservada de Python)

### Usar una variable en print:
```python
nombre = "Carlos"
print(nombre)           # Muestra: Carlos
print("¡Hola, " + nombre + "!")  # Muestra: ¡Hola, Carlos!
```

---

## 🔢 Tipos de datos

Python tiene diferentes tipos de datos:

### Texto (str – string):
```python
nombre = "María"
ciudad = 'Madrid'
frase = "Me gusta programar"
```

### Números enteros (int):
```python
edad = 10
puntos = 1500
temperatura = -5
```

### Números decimales (float):
```python
altura = 1.65
precio = 9.99
pi = 3.14159
```

### Verdadero/Falso (bool):
```python
es_mayor = True
tiene_mascota = False
```

---

## 🤝 La función input()

`input()` le pregunta algo al usuario y espera que escriba una respuesta.

```python
nombre = input("¿Cómo te llamas? ")
print("¡Hola, " + nombre + "!")
```

Cuando ejecutas esto:
1. Python muestra: `¿Cómo te llamas? `
2. El usuario escribe, por ejemplo: `Lucas`
3. Python guarda "Lucas" en la variable `nombre`
4. Python muestra: `¡Hola, Lucas!`

> ⚠️ **¡Importante!** `input()` siempre devuelve texto, aunque el usuario escriba un número.

---

## 🔗 Las f-strings: la forma elegante de mostrar variables

Las **f-strings** son una forma muy práctica de incluir variables dentro de texto:

```python
nombre = "Sofía"
edad = 11

# Forma complicada (concatenando con +):
print("Me llamo " + nombre + " y tengo " + str(edad) + " años.")

# Forma elegante con f-string:
print(f"Me llamo {nombre} y tengo {edad} años.")
```

La f-string funciona así:
- Pon una `f` antes de las comillas
- Mete las variables entre llaves `{}`
- Python las sustituye automáticamente

---

## 🔄 Cambiar el valor de una variable

Las variables pueden cambiar de valor (por eso se llaman "variables"):

```python
puntos = 0
print(f"Puntos iniciales: {puntos}")

puntos = 10
print(f"Después de nivel 1: {puntos}")

puntos = puntos + 5    # suma 5 a los puntos actuales
print(f"Después de bonus: {puntos}")
```

Resultado:
```
Puntos iniciales: 0
Después de nivel 1: 10
Después de bonus: 15
```

---

## 📋 Resumen del Módulo 5

| Concepto | Ejemplo | Resultado |
|----------|---------|-----------|
| Mostrar texto | `print("Hola")` | `Hola` |
| Variable texto | `nombre = "Ana"` | — |
| Variable número | `edad = 10` | — |
| Mostrar variable | `print(nombre)` | `Ana` |
| Preguntar al usuario | `x = input("Escribe: ")` | Espera input |
| f-string | `print(f"Hola {nombre}")` | `Hola Ana` |
| Comentario | `# Esto es un comentario` | — |

---

## 🧠 ¿Lo entendiste?

1. ¿Cuál es la diferencia entre `print("nombre")` y `print(nombre)`?
2. ¿Qué tipo de dato es `3.14`? ¿Y `"hola"`? ¿Y `7`?
3. ¿Qué pasa si escribes `PRINT("Hola")` en vez de `print("Hola")`?
4. ¿Para qué sirve `input()`?

---

➡️ **Siguiente:** `Modulo_05_Python_Hola_Variables/actividades.md`
