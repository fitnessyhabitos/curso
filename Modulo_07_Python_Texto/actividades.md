# 🎯 Módulo 7 – Actividades: Texto y Cadenas de Caracteres

## Actividad 7.1 – El analizador de nombres (⭐ Fácil)

```python
# Analizador de nombres

nombre = input("¿Cuál es tu nombre completo? ")

print(f"\n📊 ANÁLISIS DE TU NOMBRE:")
print(f"  Tu nombre: {nombre}")
print(f"  En MAYÚSCULAS: {nombre.upper()}")
print(f"  En minúsculas: {nombre.lower()}")
print(f"  Número de letras (con espacios): {len(nombre)}")
print(f"  Número de letras (sin espacios): {len(nombre.replace(' ', ''))}")
print(f"  Primera letra: {nombre[0]}")
print(f"  Última letra: {nombre[-1]}")
```

### ✍️ Amplíalo:
- Muestra el nombre al revés (pista: `nombre[::-1]`)
- Cuenta cuántas vocales tiene el nombre
- Di si el nombre empieza por vocal o consonante

---

## Actividad 7.2 – El cifrado César (⭐⭐ Medio)

El cifrado César es una técnica de escritura secreta que usaba Julio César. Consiste en desplazar cada letra del alfabeto un número de posiciones.

```python
# El cifrado César básico

print("=== CIFRADO CÉSAR ===\n")

mensaje = input("Escribe el mensaje secreto: ").lower()
desplazamiento = 3

mensaje_cifrado = ""

for letra in mensaje:
    if letra.isalpha():  # Si es una letra (no espacio ni símbolo)
        # Desplaza la letra
        codigo = ord(letra) - ord('a')
        codigo_nuevo = (codigo + desplazamiento) % 26
        letra_nueva = chr(codigo_nuevo + ord('a'))
        mensaje_cifrado += letra_nueva
    else:
        mensaje_cifrado += letra   # Espacios y símbolos sin cambiar

print(f"\nMensaje original:  {mensaje}")
print(f"Mensaje cifrado:   {mensaje_cifrado}")
```

### ✍️ Amplíalo:
- Deja que el usuario elija el desplazamiento
- Crea también la función de descifrado

---

## Actividad 7.3 – El detector de palíndromos (⭐⭐ Medio)

Un palíndromo es una palabra que se lee igual de izquierda a derecha que de derecha a izquierda. Ejemplos: "oso", "Ana", "reconocer".

```python
# Detector de palíndromos

print("=== DETECTOR DE PALÍNDROMOS ===\n")

palabra = input("Escribe una palabra: ").lower().strip()

# Quitamos espacios por si acaso
palabra_limpia = palabra.replace(" ", "")

# Invertimos la palabra
palabra_invertida = palabra_limpia[::-1]

print(f"\nPalabra: {palabra}")
print(f"Al revés: {palabra_invertida}")

if palabra_limpia == palabra_invertida:
    print(f"\n✅ ¡'{palabra}' ES un palíndromo!")
else:
    print(f"\n❌ '{palabra}' NO es un palíndromo.")
```

### ✍️ Amplíalo:
- Haz que compruebe frases enteras (no solo palabras)
- Algunos palíndromos de frase: "Dábale arroz a la zorra el abad"

---

## Actividad 7.4 – El contador de vocales y consonantes (⭐⭐ Medio)

```python
# Contador de vocales y consonantes

texto = input("Escribe un texto: ").lower()

vocales = "aeiouáéíóúü"
num_vocales = 0
num_consonantes = 0
num_espacios = 0
num_numeros = 0
num_otros = 0

for caracter in texto:
    if caracter in vocales:
        num_vocales += 1
    elif caracter.isalpha():  # Es una letra pero no vocal = consonante
        num_consonantes += 1
    elif caracter == " ":
        num_espacios += 1
    elif caracter.isdigit():
        num_numeros += 1
    else:
        num_otros += 1

total_letras = num_vocales + num_consonantes

print(f"\n📊 ANÁLISIS DEL TEXTO:")
print(f"  Total caracteres: {len(texto)}")
print(f"  Letras totales: {total_letras}")
print(f"  Vocales: {num_vocales}")
print(f"  Consonantes: {num_consonantes}")
print(f"  Espacios: {num_espacios}")
print(f"  Números: {num_numeros}")
print(f"  Otros (!, ?, etc.): {num_otros}")

if total_letras > 0:
    porcentaje_vocales = round((num_vocales / total_letras) * 100, 1)
    print(f"\n  Porcentaje de vocales: {porcentaje_vocales}%")
```

---

## Actividad 7.5 – El generador de contraseñas (⭐⭐⭐ Difícil)

```python
# Generador de contraseñas

import random
import string

print("=== GENERADOR DE CONTRASEÑAS ===\n")

longitud = int(input("¿Cuántos caracteres quieres? (mínimo 8): "))
if longitud < 8:
    longitud = 8
    print("(Ajustado a mínimo de 8 caracteres)")

incluir_mayusculas = input("¿Incluir mayúsculas? (s/n): ").lower() == "s"
incluir_numeros = input("¿Incluir números? (s/n): ").lower() == "s"
incluir_simbolos = input("¿Incluir símbolos (!@#$%)? (s/n): ").lower() == "s"

# Construir el conjunto de caracteres
caracteres = string.ascii_lowercase  # minúsculas siempre

if incluir_mayusculas:
    caracteres += string.ascii_uppercase

if incluir_numeros:
    caracteres += string.digits

if incluir_simbolos:
    caracteres += "!@#$%&*"

# Generar contraseña aleatoria
contrasena = ""
for i in range(longitud):
    contrasena += random.choice(caracteres)

print(f"\n🔐 Tu contraseña: {contrasena}")
print(f"📏 Longitud: {len(contrasena)} caracteres")

# Evaluar seguridad
if longitud >= 12 and incluir_mayusculas and incluir_numeros and incluir_simbolos:
    print("🟢 Seguridad: MUY ALTA")
elif longitud >= 10 and (incluir_numeros or incluir_simbolos):
    print("🟡 Seguridad: ALTA")
else:
    print("🔴 Seguridad: MEDIA (considera añadir más tipos de caracteres)")
```

---

## Actividad 7.6 – RETO: El juego del ahorcado (⭐⭐⭐⭐ Muy difícil)

```python
# El juego del ahorcado

import random

palabras = ["programar", "python", "tortuga", "ordenador",
            "teclado", "algoritmo", "variable", "funcion"]

palabra = random.choice(palabras)
letras_adivinadas = []
intentos_restantes = 6

print("╔══════════════════════════════╗")
print("║     🎭 EL AHORCADO           ║")
print("╚══════════════════════════════╝")
print(f"\nHe pensado una palabra de {len(palabra)} letras.")
print("Tienes 6 intentos antes de que el ahorcado sea completo.")

while intentos_restantes > 0:
    # Mostrar la palabra con guiones en las letras no adivinadas
    palabra_mostrar = ""
    letras_adivinadas_ok = 0
    for letra in palabra:
        if letra in letras_adivinadas:
            palabra_mostrar += letra + " "
            letras_adivinadas_ok += 1
        else:
            palabra_mostrar += "_ "

    print(f"\n{palabra_mostrar}")
    print(f"Intentos restantes: {intentos_restantes}")
    print(f"Letras usadas: {', '.join(sorted(letras_adivinadas))}")

    # ¿Ganó?
    if letras_adivinadas_ok == len(palabra):
        print(f"\n🎉 ¡GANASTE! La palabra era '{palabra}'")
        break

    # Pedir letra
    letra = input("\nEscribe una letra: ").lower()

    if len(letra) != 1 or not letra.isalpha():
        print("Por favor, escribe solo una letra.")
        continue

    if letra in letras_adivinadas:
        print("Ya usaste esa letra. Prueba otra.")
        continue

    letras_adivinadas.append(letra)

    if letra in palabra:
        print(f"✅ ¡Bien! La letra '{letra}' está en la palabra.")
    else:
        intentos_restantes -= 1
        print(f"❌ La letra '{letra}' no está en la palabra.")
else:
    print(f"\n💀 ¡Perdiste! La palabra era '{palabra}'")
```

---

## 📝 Evaluación del Módulo 7

Para considerar terminado este módulo, debes poder:

- [ ] Concatenar cadenas con `+` y f-strings
- [ ] Usar `len()` para saber la longitud
- [ ] Convertir entre mayúsculas/minúsculas
- [ ] Buscar texto dentro de una cadena
- [ ] Acceder a caracteres con índices `[0]`, `[-1]`
- [ ] Extraer fragmentos con slice `[inicio:fin]`
- [ ] Reemplazar con `.replace()` y dividir con `.split()`

---

💾 **Guarda tu trabajo** en: `modulo7_texto.py`

---

➡️ **Siguiente:** `Modulo_08_Python_Decisiones/teoria.md`
