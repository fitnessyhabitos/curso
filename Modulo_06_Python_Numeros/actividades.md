# 🎯 Módulo 6 – Actividades: Números y Matemáticas

## Actividad 6.1 – La calculadora básica (⭐ Fácil)

```python
# La calculadora básica

print("=== MI CALCULADORA ===")

num1 = float(input("Escribe el primer número: "))
num2 = float(input("Escribe el segundo número: "))

print(f"\n{num1} + {num2} = {num1 + num2}")
print(f"{num1} - {num2} = {num1 - num2}")
print(f"{num1} × {num2} = {num1 * num2}")

# Ojo: hay que comprobar que no dividimos entre cero
if num2 != 0:
    print(f"{num1} ÷ {num2} = {round(num1 / num2, 2)}")
else:
    print("¡No se puede dividir entre cero!")
```

### ✍️ Amplíala:
Añade también:
- División entera (`//`)
- Módulo (`%`)
- Potencia (`**`)

---

## Actividad 6.2 – El calculador de propinas (⭐⭐ Medio)

```python
# Calculador de propinas para restaurante

print("=== CALCULADOR DE PROPINAS ===\n")

precio_total = float(input("¿Cuánto costó la comida (€)? "))
num_personas = int(input("¿Cuántas personas sois? "))

propina_10 = precio_total * 0.10
propina_15 = precio_total * 0.15
propina_20 = precio_total * 0.20

total_10 = precio_total + propina_10
total_15 = precio_total + propina_15
total_20 = precio_total + propina_20

print(f"\nPrecio de la comida: {precio_total:.2f}€")
print(f"\nCon propina del 10%: {round(propina_10, 2):.2f}€ → Total: {round(total_10, 2):.2f}€")
print(f"Con propina del 15%: {round(propina_15, 2):.2f}€ → Total: {round(total_15, 2):.2f}€")
print(f"Con propina del 20%: {round(propina_20, 2):.2f}€ → Total: {round(total_20, 2):.2f}€")
print(f"\nPor persona (15% propina): {round(total_15 / num_personas, 2):.2f}€")
```

---

## Actividad 6.3 – Conversor de unidades (⭐⭐ Medio)

```python
# Conversor de unidades

print("=== CONVERSOR DE UNIDADES ===\n")

# Temperatura: Celsius a Fahrenheit y Kelvin
celsius = float(input("Temperatura en Celsius: "))

fahrenheit = (celsius * 9/5) + 32
kelvin = celsius + 273.15

print(f"\n{celsius}°C = {round(fahrenheit, 2)}°F = {round(kelvin, 2)}K")
print()

# Longitud
metros = float(input("Longitud en metros: "))

centimetros = metros * 100
kilometros = metros / 1000
pies = metros * 3.28084
pulgadas = metros * 39.3701

print(f"\n{metros} metros = {centimetros} cm = {kilometros} km")
print(f"{metros} metros = {round(pies, 2)} pies = {round(pulgadas, 2)} pulgadas")
```

### ✍️ Añade más conversiones:
- Kilogramos a libras (1 kg = 2.20462 lb)
- Litros a galones (1 litro = 0.264172 galones)

---

## Actividad 6.4 – El calculador de la merienda (⭐⭐ Medio)

```python
# ¿Cuántas calorías tiene mi merienda?

print("=== CALCULADOR DE CALORÍAS ===\n")
print("Calorías por 100g:")
print("  Pan: 270 kcal")
print("  Mantequilla: 720 kcal")
print("  Jamón: 145 kcal")
print("  Queso: 400 kcal")
print("  Leche: 65 kcal")
print()

# Pan
gramos_pan = float(input("¿Cuántos gramos de pan? "))
cal_pan = (gramos_pan * 270) / 100

# Mantequilla
gramos_mant = float(input("¿Cuántos gramos de mantequilla? "))
cal_mant = (gramos_mant * 720) / 100

# Leche
ml_leche = float(input("¿Cuántos ml de leche? "))
cal_leche = (ml_leche * 65) / 100

total_cal = cal_pan + cal_mant + cal_leche

print(f"\n📊 RESUMEN:")
print(f"  Pan ({gramos_pan}g): {round(cal_pan)} kcal")
print(f"  Mantequilla ({gramos_mant}g): {round(cal_mant)} kcal")
print(f"  Leche ({ml_leche}ml): {round(cal_leche)} kcal")
print(f"\n  TOTAL: {round(total_cal)} kcal")
```

---

## Actividad 6.5 – El juego del número secreto (⭐⭐⭐ Difícil)

```python
# El juego del número secreto

import random

print("╔══════════════════════════════════╗")
print("║   🎲 EL NÚMERO SECRETO           ║")
print("╚══════════════════════════════════╝")
print()
print("He pensado un número del 1 al 100.")
print("¿Puedes adivinarlo?\n")

secreto = random.randint(1, 100)
intentos = 0
maximo_intentos = 7

print(f"Tienes {maximo_intentos} intentos. ¡Buena suerte!")
print()

# Por ahora usamos un bucle simple (aprenderemos while en el módulo 9)
for intento_num in range(1, maximo_intentos + 1):
    intento = int(input(f"Intento {intento_num}/{maximo_intentos}: "))
    intentos += 1

    diferencia = abs(secreto - intento)

    if intento == secreto:
        print(f"\n🎉 ¡CORRECTO! ¡Lo adivinaste en {intentos} intentos!")
        break
    elif diferencia <= 5:
        if intento < secreto:
            print("🔥 ¡MUY CALIENTE! Es un poco más alto.")
        else:
            print("🔥 ¡MUY CALIENTE! Es un poco más bajo.")
    elif diferencia <= 15:
        if intento < secreto:
            print("🌡️ Tibio... es más alto.")
        else:
            print("🌡️ Tibio... es más bajo.")
    else:
        if intento < secreto:
            print("❄️ ¡Frío! Es bastante más alto.")
        else:
            print("❄️ ¡Frío! Es bastante más bajo.")
else:
    print(f"\n😞 ¡Se acabaron los intentos! El número era {secreto}.")
```

---

## Actividad 6.6 – RETO: Calculadora de figuras geométricas (⭐⭐⭐⭐ Muy difícil)

```python
# Calculadora de figuras geométricas

import math

print("=== CALCULADORA DE FIGURAS ===\n")
print("¿Qué figura quieres calcular?")
print("1. Cuadrado")
print("2. Rectángulo")
print("3. Círculo")
print("4. Triángulo")
print()

opcion = input("Elige una opción (1-4): ")

if opcion == "1":
    lado = float(input("Lado del cuadrado: "))
    area = lado ** 2
    perimetro = lado * 4
    print(f"\nCuadrado de lado {lado}:")
    print(f"  Área: {area}")
    print(f"  Perímetro: {perimetro}")

elif opcion == "2":
    ancho = float(input("Ancho: "))
    alto = float(input("Alto: "))
    area = ancho * alto
    perimetro = 2 * (ancho + alto)
    print(f"\nRectángulo {ancho}x{alto}:")
    print(f"  Área: {area}")
    print(f"  Perímetro: {perimetro}")

elif opcion == "3":
    radio = float(input("Radio del círculo: "))
    area = math.pi * radio ** 2
    perimetro = 2 * math.pi * radio
    print(f"\nCírculo de radio {radio}:")
    print(f"  Área: {round(area, 2)}")
    print(f"  Perímetro (circunferencia): {round(perimetro, 2)}")

elif opcion == "4":
    base = float(input("Base del triángulo: "))
    altura = float(input("Altura del triángulo: "))
    area = (base * altura) / 2
    print(f"\nTriángulo de base {base} y altura {altura}:")
    print(f"  Área: {area}")

else:
    print("Opción no válida")
```

---

## 📝 Evaluación del Módulo 6

Para considerar terminado este módulo, debes poder:

- [ ] Usar los 7 operadores matemáticos (`+`, `-`, `*`, `/`, `//`, `%`, `**`)
- [ ] Convertir texto a número con `int()` y `float()`
- [ ] Redondear con `round()`
- [ ] Usar `abs()`, `max()`, `min()`
- [ ] Importar y usar la librería `math`
- [ ] Generar números aleatorios con `random`

---

💾 **Guarda tu trabajo** en: `modulo6_numeros.py`

---

➡️ **Siguiente:** `Modulo_07_Python_Texto/teoria.md`
