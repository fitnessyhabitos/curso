# 🎯 Módulo 10 – Actividades: Funciones

## Actividad 10.1 – Mis primeras funciones (⭐ Fácil)

```python
# Mis primeras funciones

def bienvenida():
    print("╔══════════════════════════╗")
    print("║  ¡BIENVENIDO AL PROGRAMA  ║")
    print("╚══════════════════════════╝")

def despedida():
    print("\n¡Hasta luego! Gracias por usar el programa.")

def linea_separadora():
    print("─" * 40)

# Usar las funciones
bienvenida()
linea_separadora()
print("Este es el contenido del programa")
linea_separadora()
despedida()
```

### ✍️ Tu turno:
Crea estas funciones:
- `titulo(texto)` – muestra un texto enmarcado con `═`
- `error(mensaje)` – muestra un mensaje de error con ❌ delante
- `exito(mensaje)` – muestra un mensaje de éxito con ✅ delante

---

## Actividad 10.2 – Calculadora con funciones (⭐⭐ Medio)

```python
# Calculadora organizada con funciones

def sumar(a, b):
    return a + b

def restar(a, b):
    return a - b

def multiplicar(a, b):
    return a * b

def dividir(a, b):
    if b == 0:
        print("Error: no se puede dividir entre cero")
        return None
    return a / b

def potencia(base, exponente):
    return base ** exponente

def mostrar_resultado(operacion, a, b, resultado):
    if resultado is not None:
        print(f"{a} {operacion} {b} = {round(resultado, 4)}")

# Usar las funciones
print("=== CALCULADORA CON FUNCIONES ===\n")

num1 = float(input("Número 1: "))
num2 = float(input("Número 2: "))

print()
mostrar_resultado("+", num1, num2, sumar(num1, num2))
mostrar_resultado("-", num1, num2, restar(num1, num2))
mostrar_resultado("×", num1, num2, multiplicar(num1, num2))
mostrar_resultado("÷", num1, num2, dividir(num1, num2))
mostrar_resultado("^", num1, num2, potencia(num1, num2))
```

---

## Actividad 10.3 – Funciones de texto (⭐⭐ Medio)

```python
# Librería personal de funciones de texto

def contar_vocales(texto):
    """Cuenta las vocales de un texto"""
    vocales = "aeiouáéíóúü"
    return sum(1 for c in texto.lower() if c in vocales)

def es_palindromo(texto):
    """Comprueba si un texto es palíndromo"""
    limpio = texto.lower().replace(" ", "")
    return limpio == limpio[::-1]

def invertir(texto):
    """Devuelve el texto al revés"""
    return texto[::-1]

def centrar_texto(texto, ancho=40):
    """Centra un texto en un ancho dado"""
    return texto.center(ancho)

def titulo_bonito(texto):
    """Muestra un título decorado"""
    separador = "═" * (len(texto) + 4)
    print(separador)
    print(f"║ {texto} ║")
    print(separador)

# Probar las funciones
palabras = ["oso", "Python", "reconocer", "programar", "Ana"]

titulo_bonito("ANALIZADOR DE PALABRAS")
print()

for palabra in palabras:
    vocales = contar_vocales(palabra)
    palindromo = "Sí ✅" if es_palindromo(palabra) else "No ❌"
    inverso = invertir(palabra)
    print(f"'{palabra}':")
    print(f"  Vocales: {vocales}, Palíndromo: {palindromo}, Al revés: {inverso}")
    print()
```

---

## Actividad 10.4 – El banco virtual (⭐⭐⭐ Difícil)

```python
# Banco virtual con funciones

saldo = 0.0

def mostrar_saldo():
    print(f"\n💰 Saldo actual: {saldo:.2f}€")

def depositar(cantidad):
    global saldo
    if cantidad <= 0:
        print("❌ La cantidad debe ser positiva")
        return False
    saldo += cantidad
    print(f"✅ Depositados {cantidad:.2f}€")
    mostrar_saldo()
    return True

def retirar(cantidad):
    global saldo
    if cantidad <= 0:
        print("❌ La cantidad debe ser positiva")
        return False
    if cantidad > saldo:
        print(f"❌ Saldo insuficiente. Solo tienes {saldo:.2f}€")
        return False
    saldo -= cantidad
    print(f"✅ Retirados {cantidad:.2f}€")
    mostrar_saldo()
    return True

def aplicar_interes(porcentaje=2.0):
    global saldo
    interes = saldo * (porcentaje / 100)
    saldo += interes
    print(f"💹 Interés del {porcentaje}% aplicado: +{interes:.2f}€")
    mostrar_saldo()

# Menú del banco
print("╔══════════════════════════════╗")
print("║   🏦 BANCO PYTHÓNICO S.A.    ║")
print("╚══════════════════════════════╝")

while True:
    print("\n¿Qué deseas hacer?")
    print("  1. Ver saldo")
    print("  2. Depositar dinero")
    print("  3. Retirar dinero")
    print("  4. Aplicar interés")
    print("  0. Salir")

    opcion = input("\nOpción: ")

    if opcion == "0":
        print(f"\n¡Hasta pronto! Tu saldo final es {saldo:.2f}€")
        break
    elif opcion == "1":
        mostrar_saldo()
    elif opcion == "2":
        cant = float(input("¿Cuánto quieres depositar? "))
        depositar(cant)
    elif opcion == "3":
        cant = float(input("¿Cuánto quieres retirar? "))
        retirar(cant)
    elif opcion == "4":
        aplicar_interes()
    else:
        print("Opción no válida")
```

---

## Actividad 10.5 – RETO: El juego de adivinanzas con funciones (⭐⭐⭐⭐ Muy difícil)

```python
# Sistema de quiz con funciones

import random

def mostrar_pregunta(pregunta, opciones, numero):
    """Muestra una pregunta numerada con sus opciones"""
    print(f"\n📋 Pregunta {numero}: {pregunta}")
    for i, opcion in enumerate(opciones, 1):
        print(f"  {i}. {opcion}")

def obtener_respuesta(num_opciones):
    """Pide y valida la respuesta del usuario"""
    while True:
        try:
            resp = int(input(f"Tu respuesta (1-{num_opciones}): "))
            if 1 <= resp <= num_opciones:
                return resp
            else:
                print(f"Por favor elige entre 1 y {num_opciones}")
        except ValueError:
            print("Escribe un número")

def verificar_respuesta(respuesta, correcta):
    """Comprueba si la respuesta es correcta"""
    return respuesta == correcta

def mostrar_puntuacion(aciertos, total):
    """Muestra la puntuación final con un mensaje"""
    porcentaje = (aciertos / total) * 100
    print(f"\n{'═'*40}")
    print(f"RESULTADO FINAL: {aciertos}/{total} ({porcentaje:.0f}%)")
    print(f"{'═'*40}")

    if porcentaje == 100:
        print("🏆 ¡PERFECTO! ¡Eres un genio!")
    elif porcentaje >= 80:
        print("⭐ ¡Muy bien! ¡Casi perfecto!")
    elif porcentaje >= 60:
        print("👍 ¡Bien! Pero puedes mejorar")
    elif porcentaje >= 40:
        print("📚 Regular. ¡A estudiar más!")
    else:
        print("💪 ¡Ánimo! La próxima irá mejor")

# Las preguntas del quiz
preguntas = [
    {
        "pregunta": "¿Qué es una variable en Python?",
        "opciones": ["Un tipo de bucle", "Un cajón donde guardar datos", "Una función especial", "Un error"],
        "correcta": 2
    },
    {
        "pregunta": "¿Qué símbolo usamos para comentarios en Python?",
        "opciones": ["//", "/*", "#", "--"],
        "correcta": 3
    },
    {
        "pregunta": "¿Cuál es el resultado de 10 % 3?",
        "opciones": ["3", "1", "0", "30"],
        "correcta": 2
    },
    {
        "pregunta": "¿Qué hace la función len()?",
        "opciones": ["Convierte a mayúsculas", "Cuenta la longitud", "Repite texto", "Ordena texto"],
        "correcta": 2
    },
    {
        "pregunta": "¿Cuántos lados tiene un hexágono?",
        "opciones": ["5", "7", "6", "8"],
        "correcta": 3
    }
]

# Jugar
print("╔══════════════════════════════════╗")
print("║      🎓 QUIZ DE PROGRAMACIÓN     ║")
print("╚══════════════════════════════════╝")
print(f"\nHay {len(preguntas)} preguntas. ¡Buena suerte!")

preguntas_mezcladas = preguntas.copy()
random.shuffle(preguntas_mezcladas)

aciertos = 0

for i, datos in enumerate(preguntas_mezcladas, 1):
    mostrar_pregunta(datos["pregunta"], datos["opciones"], i)
    respuesta = obtener_respuesta(len(datos["opciones"]))

    if verificar_respuesta(respuesta, datos["correcta"]):
        print("✅ ¡CORRECTO!")
        aciertos += 1
    else:
        opcion_correcta = datos["opciones"][datos["correcta"] - 1]
        print(f"❌ Incorrecto. La respuesta era: {opcion_correcta}")

mostrar_puntuacion(aciertos, len(preguntas))
```

---

## 📝 Evaluación del Módulo 10

Para considerar terminado este módulo, debes poder:

- [ ] Definir funciones con `def`
- [ ] Llamar funciones correctamente
- [ ] Pasar parámetros a una función
- [ ] Usar `return` para devolver valores
- [ ] Entender la diferencia entre variables locales y globales
- [ ] Organizar un programa usando múltiples funciones

---

💾 **Guarda tu trabajo** en: `modulo10_funciones.py`

---

➡️ **Siguiente:** `Modulo_11_Python_Listas/teoria.md`
