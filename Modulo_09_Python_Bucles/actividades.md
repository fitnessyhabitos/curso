# 🎯 Módulo 9 – Actividades: Bucles – Repetir sin cansarse

## Actividad 9.1 – Las tablas de multiplicar (⭐ Fácil)

```python
# Tablas de multiplicar

numero = int(input("¿De qué tabla quieres aprender? (1-12): "))

print(f"\n📊 TABLA DEL {numero}")
print("═" * 25)

for i in range(1, 13):
    resultado = numero * i
    print(f"  {numero} × {i:2d} = {resultado:3d}")

print("═" * 25)
```

### ✍️ Amplíalo:
- Crea un "mini examen": el programa hace 5 preguntas aleatorias de la tabla y cuenta los aciertos.

---

## Actividad 9.2 – El contador regresivo (⭐ Fácil)

```python
# Cohete espacial: cuenta atrás

import time

print("🚀 LANZAMIENTO DE COHETE ESPACIAL")
print()

for i in range(10, 0, -1):
    print(f"  {i}...")
    time.sleep(1)   # Espera 1 segundo

print()
print("🔥 ¡¡¡DESPEGUE!!! 🔥")
print("🚀💨 El cohete ha despegado hacia las estrellas")
```

### ✍️ Amplíalo:
- Pide al usuario desde qué número empezar la cuenta atrás
- Añade un mensaje especial cada vez que sea múltiplo de 3

---

## Actividad 9.3 – El validador de contraseña (⭐⭐ Medio)

```python
# Validador de contraseña con while

contrasena_correcta = "python123"
intentos_maximos = 3
intentos = 0

print("🔐 Sistema de seguridad")
print(f"Tienes {intentos_maximos} intentos.\n")

while intentos < intentos_maximos:
    intento = input("Introduce la contraseña: ")
    intentos += 1

    if intento == contrasena_correcta:
        print(f"\n✅ ¡Acceso concedido! Entraste al sistema.")
        break
    else:
        restantes = intentos_maximos - intentos
        if restantes > 0:
            print(f"❌ Contraseña incorrecta. Te quedan {restantes} intento(s).\n")
        else:
            print("\n🚫 ¡ACCESO DENEGADO! Sistema bloqueado.")
```

---

## Actividad 9.4 – El dibujo con asteriscos (⭐⭐ Medio)

```python
# Dibujos con bucles y asteriscos

print("TRIÁNGULO:")
for i in range(1, 6):
    print("*" * i)

print("\nDIAMANTE (mitad superior):")
for i in range(1, 6):
    espacios = " " * (5 - i)
    estrellas = "*" * (2 * i - 1)
    print(espacios + estrellas)

print("\nCUADRADO HUECO (5x5):")
for fila in range(5):
    if fila == 0 or fila == 4:
        print("*" * 5)
    else:
        print("*" + " " * 3 + "*")
```

### ✍️ Tu turno:
Dibuja estos patrones usando bucles (sin copiar asteriscos a mano):

```
Patrón 1:         Patrón 2:         Patrón 3:
*                 * * * * *         *
* *               * * * *           * *
* * *             * * *             * * *
* * * *           * *               * * * *
* * * * *         *                 * * *
                                    * *
                                    *
```

---

## Actividad 9.5 – El menú de opciones (⭐⭐⭐ Difícil)

```python
# Calculadora con menú while

import math

print("╔══════════════════════════════╗")
print("║   🧮 SUPER CALCULADORA       ║")
print("╚══════════════════════════════╝")

while True:
    print("\n¿Qué quieres calcular?")
    print("  1. Suma")
    print("  2. Resta")
    print("  3. Multiplicación")
    print("  4. División")
    print("  5. Potencia")
    print("  6. Raíz cuadrada")
    print("  0. Salir")

    opcion = input("\nOpción: ")

    if opcion == "0":
        print("\n¡Hasta luego! 👋")
        break
    elif opcion == "6":
        num = float(input("Número: "))
        if num >= 0:
            print(f"√{num} = {round(math.sqrt(num), 4)}")
        else:
            print("No puedo calcular la raíz de un número negativo")
    elif opcion in ["1", "2", "3", "4", "5"]:
        num1 = float(input("Primer número: "))
        num2 = float(input("Segundo número: "))

        if opcion == "1":
            print(f"Resultado: {num1 + num2}")
        elif opcion == "2":
            print(f"Resultado: {num1 - num2}")
        elif opcion == "3":
            print(f"Resultado: {num1 * num2}")
        elif opcion == "4":
            if num2 != 0:
                print(f"Resultado: {round(num1 / num2, 4)}")
            else:
                print("¡Error! No se puede dividir entre cero")
        elif opcion == "5":
            print(f"Resultado: {num1 ** num2}")
    else:
        print("Opción no válida, elige entre 0 y 6")
```

---

## Actividad 9.6 – El FizzBuzz (⭐⭐⭐ Difícil)

Este es uno de los ejercicios más famosos en programación. Imprime los números del 1 al 100, pero:
- Si el número es divisible por 3, imprime "Fizz"
- Si el número es divisible por 5, imprime "Buzz"
- Si es divisible por 3 Y por 5, imprime "FizzBuzz"
- Si no, imprime el número

```python
# FizzBuzz clásico

for i in range(1, 101):
    if i % 3 == 0 and i % 5 == 0:
        print("FizzBuzz")
    elif i % 3 == 0:
        print("Fizz")
    elif i % 5 == 0:
        print("Buzz")
    else:
        print(i)
```

### ✍️ Amplíalo:
- Cuenta cuántos "Fizz", "Buzz" y "FizzBuzz" hay del 1 al 100
- Versión personalizada: el usuario elige los dos números divisores y las palabras

---

## Actividad 9.7 – RETO: El juego de adivinar mejorado (⭐⭐⭐⭐ Muy difícil)

```python
# Juego de adivinar número - versión completa

import random

def jugar_partida():
    secreto = random.randint(1, 100)
    intentos = 0
    max_intentos = 7
    historial = []

    print(f"\nHe pensado un número del 1 al 100.")
    print(f"Tienes {max_intentos} intentos. ¡Mucha suerte!\n")

    while intentos < max_intentos:
        try:
            intento = int(input(f"Intento {intentos + 1}/{max_intentos}: "))
        except ValueError:
            print("Por favor, escribe un número entero")
            continue

        intentos += 1
        historial.append(intento)

        if intento == secreto:
            print(f"\n🎉 ¡CORRECTO! ¡Lo adivinaste en {intentos} intento(s)!")
            return intentos

        diferencia = abs(secreto - intento)

        if diferencia <= 3:
            pista = "🔥 ¡ARDIENDO!"
        elif diferencia <= 10:
            pista = "🌡️ Muy caliente"
        elif diferencia <= 25:
            pista = "☁️ Tibio"
        else:
            pista = "❄️ Muy frío"

        direccion = "↑ más alto" if intento < secreto else "↓ más bajo"
        print(f"  {pista} - {direccion}. Intentado: {sorted(historial)}")

    print(f"\n💀 Se acabaron los intentos. El número era {secreto}.")
    return 0

# Partidas
victorias = 0
total_intentos = []

print("╔═══════════════════════════════════╗")
print("║   🎲 ADIVINA EL NÚMERO SECRETO    ║")
print("╚═══════════════════════════════════╝")

while True:
    resultado = jugar_partida()
    if resultado > 0:
        victorias += 1
        total_intentos.append(resultado)

    otra = input("\n¿Quieres jugar otra vez? (s/n): ").lower()
    if otra != "s":
        break

print(f"\n📊 ESTADÍSTICAS FINALES:")
print(f"  Victorias: {victorias}")
if total_intentos:
    print(f"  Mejor partida: {min(total_intentos)} intentos")
    print(f"  Media de intentos: {round(sum(total_intentos)/len(total_intentos), 1)}")
print("¡Hasta pronto!")
```

---

## 📝 Evaluación del Módulo 9

Para considerar terminado este módulo, debes poder:

- [ ] Usar `while` con una condición que cambia
- [ ] Usar `for` con `range()` de una, dos y tres formas
- [ ] Usar `for` para recorrer texto y listas
- [ ] Usar `break` para salir del bucle
- [ ] Usar `continue` para saltar iteraciones
- [ ] Acumular valores con `+=`

---

💾 **Guarda tu trabajo** en: `modulo9_bucles.py`

---

➡️ **Siguiente:** `Modulo_10_Python_Funciones/teoria.md`
