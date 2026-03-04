# 🎯 Módulo 8 – Actividades: Decisiones con if/else

## Actividad 8.1 – ¿Par o impar? (⭐ Fácil)

```python
# ¿Par o impar?

numero = int(input("Escribe un número entero: "))

if numero % 2 == 0:
    print(f"{numero} es PAR")
else:
    print(f"{numero} es IMPAR")

# Bonus: ¿es positivo, negativo o cero?
if numero > 0:
    print(f"{numero} es positivo")
elif numero < 0:
    print(f"{numero} es negativo")
else:
    print(f"{numero} es cero")
```

### ✍️ Amplíalo:
- Comprueba si el número es divisible por 3, por 5, y por ambos a la vez
- (Esta es la base del famoso problema "FizzBuzz" de programación)

---

## Actividad 8.2 – El clasificador de edades (⭐ Fácil)

```python
# Clasificador de edades

nombre = input("¿Cómo te llamas? ")
edad = int(input(f"¿Cuántos años tienes, {nombre}? "))

if edad < 0:
    print("Eso no puede ser una edad válida 🤔")
elif edad < 3:
    print(f"{nombre} es un bebé 👶")
elif edad < 6:
    print(f"{nombre} es un niño pequeño 🧒")
elif edad < 12:
    print(f"{nombre} es un niño o niña 🧒‍♂️")
elif edad < 18:
    print(f"{nombre} es un adolescente 🧑")
elif edad < 65:
    print(f"{nombre} es un adulto 🧑‍💼")
else:
    print(f"{nombre} es una persona mayor 👴")
```

### ✍️ Amplíalo:
- Añade en qué ciclo escolar estaría (infantil, primaria, secundaria, etc.)
- Calcula cuántos años faltan para ser mayor de edad (18)

---

## Actividad 8.3 – El adivino de animales (⭐⭐ Medio)

```python
# El adivino de animales

print("=== EL ADIVINO DE ANIMALES ===")
print("Piensa en un animal y yo lo adivinaré haciendo preguntas.\n")

resp1 = input("¿Tiene 4 patas? (s/n): ").lower()

if resp1 == "s":
    resp2 = input("¿Es un animal doméstico? (s/n): ").lower()
    if resp2 == "s":
        resp3 = input("¿Ladra? (s/n): ").lower()
        if resp3 == "s":
            print("\n¡Es un 🐕 PERRO!")
        else:
            print("\n¡Es un 🐱 GATO!")
    else:
        resp3 = input("¿Es grande (más de 100kg)? (s/n): ").lower()
        if resp3 == "s":
            print("\n¡Es un 🦁 LION o un 🐘 ELEFANTE!")
        else:
            print("\n¡Es un 🦊 ZORRO o un 🐰 CONEJO!")
else:
    resp2 = input("¿Puede volar? (s/n): ").lower()
    if resp2 == "s":
        resp3 = input("¿Tiene plumas de colores brillantes? (s/n): ").lower()
        if resp3 == "s":
            print("\n¡Es un 🦜 LORO!")
        else:
            print("\n¡Es un 🦅 ÁGUILA o una 🕊️ PALOMA!")
    else:
        print("\n¡Es un 🐟 PEZ o una 🐍 SERPIENTE!")
```

### ✍️ Amplíalo:
- Añade más animales y más preguntas para afinar la predicción

---

## Actividad 8.4 – La calculadora de notas con consejo (⭐⭐ Medio)

```python
# Calculadora de notas con consejo

print("=== CALCULADORA DE NOTAS ===\n")

nombre = input("¿Cómo te llamas? ")

nota_mates = float(input("Nota de Matemáticas (0-10): "))
nota_lengua = float(input("Nota de Lengua (0-10): "))
nota_ingles = float(input("Nota de Inglés (0-10): "))
nota_naturales = float(input("Nota de Ciencias Naturales (0-10): "))

media = (nota_mates + nota_lengua + nota_ingles + nota_naturales) / 4
media = round(media, 2)

print(f"\n📊 BOLETÍN DE {nombre.upper()}")
print("=" * 35)
print(f"  Matemáticas:         {nota_mates}")
print(f"  Lengua:              {nota_lengua}")
print(f"  Inglés:              {nota_ingles}")
print(f"  Ciencias Naturales:  {nota_naturales}")
print("─" * 35)
print(f"  MEDIA:               {media}")
print("=" * 35)

# Calificación y consejo
if media >= 9:
    calificacion = "⭐ SOBRESALIENTE"
    consejo = "¡Eres increíble! Sigue así."
elif media >= 7:
    calificacion = "👍 NOTABLE"
    consejo = "¡Muy bien! Un poco más de esfuerzo y llegarás al sobresaliente."
elif media >= 6:
    calificacion = "✅ BIEN"
    consejo = "¡Bien! Pero puedes mejorar si estudias un poco más."
elif media >= 5:
    calificacion = "🟡 SUFICIENTE"
    consejo = "Has aprobado, pero hay que estudiar más para mejorar."
else:
    calificacion = "❌ INSUFICIENTE"
    consejo = "¡Ánimo! Con más esfuerzo y práctica mejorarás."

print(f"\nCalificación: {calificacion}")
print(f"Consejo: {consejo}")

# Asignaturas que necesitan repaso
asignaturas_repaso = []
if nota_mates < 5:
    asignaturas_repaso.append("Matemáticas")
if nota_lengua < 5:
    asignaturas_repaso.append("Lengua")
if nota_ingles < 5:
    asignaturas_repaso.append("Inglés")
if nota_naturales < 5:
    asignaturas_repaso.append("Ciencias Naturales")

if asignaturas_repaso:
    print(f"\n⚠️  Necesitas repasar: {', '.join(asignaturas_repaso)}")
else:
    print("\n✅ ¡Ninguna asignatura suspendida!")
```

---

## Actividad 8.5 – El juego piedra, papel o tijera (⭐⭐⭐ Difícil)

```python
# Piedra, papel o tijera

import random

print("╔══════════════════════════════════╗")
print("║   ✊✋✌️  PIEDRA, PAPEL O TIJERA  ║")
print("╚══════════════════════════════════╝\n")

opciones = ["piedra", "papel", "tijera"]
jugador = input("Elige piedra, papel o tijera: ").lower().strip()

if jugador not in opciones:
    print("Opción no válida. Elige entre piedra, papel o tijera.")
else:
    ordenador = random.choice(opciones)

    print(f"\nTú elegiste: {jugador}")
    print(f"El ordenador eligió: {ordenador}")

    if jugador == ordenador:
        resultado = "¡EMPATE!"
    elif (jugador == "piedra" and ordenador == "tijera") or \
         (jugador == "tijera" and ordenador == "papel") or \
         (jugador == "papel" and ordenador == "piedra"):
        resultado = "¡GANASTE! 🎉"
    else:
        resultado = "Perdiste 😞"

    print(f"\n{resultado}")
```

---

## Actividad 8.6 – RETO: La aventura de texto (⭐⭐⭐⭐ Muy difícil)

```python
# Mini aventura de texto

print("╔══════════════════════════════════════╗")
print("║       🗡️  LA AVENTURA DEL HÉROE       ║")
print("╚══════════════════════════════════════╝\n")

nombre = input("¿Cuál es el nombre de tu héroe? ")
print(f"\nBienvenido, {nombre}. Tu aventura comienza...\n")

print("Estás en un bosque oscuro. Ves dos caminos:")
print("  1. El camino de la izquierda, que lleva a una cueva oscura")
print("  2. El camino de la derecha, que lleva a un río brillante")

camino = input("\n¿Qué camino eliges? (1/2): ")

if camino == "1":
    print(f"\n{nombre} entra en la cueva oscura...")
    print("De repente, ves un dragón dormido y un cofre del tesoro.")
    accion = input("¿Qué haces? (1: Coger el tesoro, 2: Despertar el dragón): ")

    if accion == "1":
        print(f"\n{nombre} se acerca sigilosamente al cofre...")
        print("¡Lo consigues! El cofre contiene 1000 monedas de oro.")
        print("¡HAS GANADO! Eres rico y saliste sin despertar al dragón.")
    elif accion == "2":
        print(f"\n{nombre} grita '¡DRAGÓN!'...")
        print("El dragón se despierta furioso y te persigue.")
        huir = input("¿Corres o luchas? (1: Correr, 2: Luchar): ")
        if huir == "1":
            print("\nCorres a toda velocidad y logras escapar. ¡Sobreviviste!")
        else:
            print("\n¡Eres valiente! Luchas contra el dragón...")
            print("Tras una batalla épica, ¡derrota al dragón! ¡HÉROE!")
    else:
        print("No sabes qué hacer y te quedas paralizado. FIN.")

elif camino == "2":
    print(f"\n{nombre} camina hacia el río brillante...")
    print("Junto al río hay un anciano sabio y un barco.")
    accion = input("¿Qué haces? (1: Hablar con el anciano, 2: Coger el barco): ")

    if accion == "1":
        print("\nEl anciano te da un mapa del tesoro y una espada mágica.")
        print("Con el mapa, encuentras el tesoro sin peligro. ¡GANASTE!")
    elif accion == "2":
        print("\nNavegás río abajo y encuentras una ciudad de oro.")
        print("¡Eres el rey de la ciudad! ¡GANASTE!")
    else:
        print("Te quedas mirando el río hasta que anochece. FIN.")

else:
    print("No eliges ningún camino y se hace de noche. FIN.")

print("\n═══ FIN DE LA AVENTURA ═══")
```

---

## 📝 Evaluación del Módulo 8

Para considerar terminado este módulo, debes poder:

- [ ] Usar `if`, `elif` y `else` correctamente
- [ ] Usar todos los operadores de comparación (`==`, `!=`, `>`, `<`, etc.)
- [ ] Combinar condiciones con `and`, `or`, `not`
- [ ] Anidar bloques `if` dentro de otros `if`
- [ ] Saber que la indentación es obligatoria en Python

---

💾 **Guarda tu trabajo** en: `modulo8_decisiones.py`

---

➡️ **Siguiente:** `Modulo_09_Python_Bucles/teoria.md`
