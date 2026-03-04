# 🎯 Módulo 11 – Actividades: Listas

## Actividad 11.1 – Mi lista de la compra (⭐ Fácil)

```python
# Lista de la compra interactiva

lista_compra = []

print("=== LISTA DE LA COMPRA ===")
print("Escribe los productos que necesitas comprar.")
print("Escribe 'listo' cuando hayas terminado.\n")

while True:
    producto = input("¿Qué necesitas comprar? ").strip()

    if producto.lower() == "listo":
        break

    if producto == "":
        print("Por favor, escribe algo")
        continue

    lista_compra.append(producto)
    print(f"✅ '{producto}' añadido a la lista")

print(f"\n📋 TU LISTA DE LA COMPRA ({len(lista_compra)} productos):")
print("─" * 30)

for i, producto in enumerate(lista_compra, 1):
    print(f"  {i}. {producto}")

print("─" * 30)
print("¡No olvides nada!")
```

### ✍️ Amplíalo:
- Permite eliminar elementos de la lista
- Permite marcar elementos como "comprados" (√)

---

## Actividad 11.2 – El ranking de puntuaciones (⭐⭐ Medio)

```python
# Ranking de puntuaciones

puntuaciones = []
nombres = []

print("=== RANKING DE VIDEOJUEGO ===\n")

num_jugadores = int(input("¿Cuántos jugadores hay? "))

for i in range(num_jugadores):
    print(f"\nJugador {i+1}:")
    nombre = input("  Nombre: ")
    puntos = int(input("  Puntuación: "))
    nombres.append(nombre)
    puntuaciones.append(puntos)

# Ordenar de mayor a menor (manual con listas paralelas)
# Usamos zip para ordenar ambas listas juntas
combinado = list(zip(puntuaciones, nombres))
combinado.sort(reverse=True)

print(f"\n{'='*35}")
print("   🏆  RANKING FINAL")
print(f"{'='*35}")

medallas = ["🥇", "🥈", "🥉"]

for i, (puntos, nombre) in enumerate(combinado):
    if i < 3:
        medalla = medallas[i]
    else:
        medalla = f"{i+1}."

    print(f"  {medalla} {nombre}: {puntos} puntos")

print(f"{'='*35}")
print(f"Mejor puntuación: {combinado[0][0]} puntos ({combinado[0][1]})")
print(f"Peor puntuación: {combinado[-1][0]} puntos ({combinado[-1][1]})")
print(f"Puntuación media: {round(sum(puntuaciones)/len(puntuaciones), 1)}")
```

---

## Actividad 11.3 – El gestor de tareas (⭐⭐ Medio)

```python
# Gestor de tareas pendientes

tareas_pendientes = []
tareas_completadas = []

def mostrar_tareas():
    print(f"\n📋 TAREAS PENDIENTES ({len(tareas_pendientes)}):")
    if tareas_pendientes:
        for i, tarea in enumerate(tareas_pendientes, 1):
            print(f"  {i}. {tarea}")
    else:
        print("  ¡No tienes tareas pendientes! 🎉")

    print(f"\n✅ TAREAS COMPLETADAS ({len(tareas_completadas)}):")
    if tareas_completadas:
        for tarea in tareas_completadas:
            print(f"  ✓ {tarea}")
    else:
        print("  Ninguna completada todavía")

def agregar_tarea(tarea):
    tareas_pendientes.append(tarea)
    print(f"✅ Tarea '{tarea}' añadida")

def completar_tarea(numero):
    if 1 <= numero <= len(tareas_pendientes):
        tarea = tareas_pendientes.pop(numero - 1)
        tareas_completadas.append(tarea)
        print(f"🎉 ¡Tarea '{tarea}' completada!")
    else:
        print("Número de tarea no válido")

print("╔══════════════════════════════╗")
print("║    📝 GESTOR DE TAREAS       ║")
print("╚══════════════════════════════╝")

while True:
    print("\n¿Qué quieres hacer?")
    print("  1. Ver tareas")
    print("  2. Agregar tarea")
    print("  3. Completar tarea")
    print("  4. Eliminar tarea")
    print("  0. Salir")

    opcion = input("\nOpción: ")

    if opcion == "0":
        print(f"\n¡Hasta pronto! Completaste {len(tareas_completadas)} tarea(s) hoy.")
        break
    elif opcion == "1":
        mostrar_tareas()
    elif opcion == "2":
        nueva = input("Nueva tarea: ").strip()
        if nueva:
            agregar_tarea(nueva)
    elif opcion == "3":
        mostrar_tareas()
        if tareas_pendientes:
            num = int(input("¿Qué tarea completaste? (número): "))
            completar_tarea(num)
    elif opcion == "4":
        mostrar_tareas()
        if tareas_pendientes:
            num = int(input("¿Qué tarea eliminas? (número): "))
            if 1 <= num <= len(tareas_pendientes):
                eliminada = tareas_pendientes.pop(num - 1)
                print(f"Tarea '{eliminada}' eliminada")
    else:
        print("Opción no válida")
```

---

## Actividad 11.4 – El buscador de estadísticas (⭐⭐⭐ Difícil)

```python
# Calculador de estadísticas de una lista de números

def pedir_numeros():
    """Pide números al usuario hasta que escriba 'fin'"""
    numeros = []
    print("Escribe números (uno por línea). Escribe 'fin' para terminar:")

    while True:
        entrada = input("Número: ").strip()
        if entrada.lower() == "fin":
            break
        try:
            numero = float(entrada)
            numeros.append(numero)
        except ValueError:
            print("Eso no es un número válido")

    return numeros

def calcular_media(numeros):
    return sum(numeros) / len(numeros)

def calcular_mediana(numeros):
    ordenados = sorted(numeros)
    n = len(ordenados)
    if n % 2 == 0:
        return (ordenados[n//2 - 1] + ordenados[n//2]) / 2
    else:
        return ordenados[n//2]

def calcular_moda(numeros):
    """El número que más se repite"""
    return max(numeros, key=numeros.count)

def mostrar_estadisticas(numeros):
    print(f"\n{'═'*40}")
    print("         📊 ESTADÍSTICAS")
    print(f"{'═'*40}")
    print(f"Números introducidos: {len(numeros)}")
    print(f"Lista ordenada: {sorted(numeros)}")
    print(f"Mínimo: {min(numeros)}")
    print(f"Máximo: {max(numeros)}")
    print(f"Rango: {max(numeros) - min(numeros)}")
    print(f"Suma: {sum(numeros)}")
    print(f"Media: {round(calcular_media(numeros), 2)}")
    print(f"Mediana: {calcular_mediana(numeros)}")
    print(f"Moda: {calcular_moda(numeros)}")
    print(f"{'═'*40}")

# Programa principal
print("=== CALCULADOR DE ESTADÍSTICAS ===\n")
mis_numeros = pedir_numeros()

if mis_numeros:
    mostrar_estadisticas(mis_numeros)
else:
    print("No introdujiste ningún número")
```

---

## Actividad 11.5 – RETO: El juego de Snake (texto) (⭐⭐⭐⭐ Muy difícil)

```python
# Snake de texto simplificado

import random
import time

def crear_tablero(ancho, alto):
    """Crea un tablero vacío"""
    tablero = []
    for fila in range(alto):
        fila_actual = []
        for col in range(ancho):
            fila_actual.append(" ")
        tablero.append(fila_actual)
    return tablero

def mostrar_tablero(tablero, serpiente, comida, puntos):
    """Muestra el tablero en pantalla"""
    ancho = len(tablero[0])
    print("╔" + "═" * ancho + "╗")

    for fila_idx, fila in enumerate(tablero):
        linea = "║"
        for col_idx, celda in enumerate(fila):
            pos = (fila_idx, col_idx)
            if pos == serpiente[0]:
                linea += "O"  # Cabeza
            elif pos in serpiente[1:]:
                linea += "o"  # Cuerpo
            elif pos == comida:
                linea += "*"  # Comida
            else:
                linea += " "
        linea += "║"
        print(linea)

    print("╚" + "═" * ancho + "╝")
    print(f"Puntos: {puntos} | Longitud: {len(serpiente)}")
    print("Direcciones: w=arriba, s=abajo, a=izquierda, d=derecha, q=salir")

# Configuración
ANCHO, ALTO = 20, 10
serpiente = [(ALTO//2, ANCHO//2)]
comida = (random.randint(0, ALTO-1), random.randint(0, ANCHO-1))
puntos = 0
direccion = "d"

print("╔══════════════════════════════╗")
print("║   🐍 SNAKE DE TEXTO          ║")
print("╚══════════════════════════════╝")
print("\n¡En este juego de texto, el movimiento es manual!")
print("Escribe una dirección y presiona Enter para mover la serpiente.\n")

tablero = crear_tablero(ANCHO, ALTO)
jugando = True

while jugando:
    mostrar_tablero(tablero, serpiente, comida, puntos)
    mov = input("Movimiento: ").lower().strip()

    if mov == "q":
        print("¡Juego terminado!")
        break
    elif mov in ["w", "s", "a", "d"]:
        direccion = mov

    # Calcular nueva posición de la cabeza
    cabeza = serpiente[0]
    if direccion == "w":
        nueva_cabeza = (cabeza[0] - 1, cabeza[1])
    elif direccion == "s":
        nueva_cabeza = (cabeza[0] + 1, cabeza[1])
    elif direccion == "a":
        nueva_cabeza = (cabeza[0], cabeza[1] - 1)
    else:
        nueva_cabeza = (cabeza[0], cabeza[1] + 1)

    # Comprobar colisiones con paredes
    if (nueva_cabeza[0] < 0 or nueva_cabeza[0] >= ALTO or
            nueva_cabeza[1] < 0 or nueva_cabeza[1] >= ANCHO):
        print("💀 ¡Chocaste con la pared! Game Over")
        break

    # Comprobar colisión con la serpiente
    if nueva_cabeza in serpiente:
        print("💀 ¡Te mordiste a ti mismo! Game Over")
        break

    # Mover serpiente
    serpiente.insert(0, nueva_cabeza)

    # ¿Comió?
    if nueva_cabeza == comida:
        puntos += 10
        print("😋 ¡Yum! +10 puntos")
        # Nueva comida en posición aleatoria libre
        while True:
            nueva_comida = (random.randint(0, ALTO-1), random.randint(0, ANCHO-1))
            if nueva_comida not in serpiente:
                comida = nueva_comida
                break
    else:
        serpiente.pop()   # Elimina la cola

print(f"\n🏆 PUNTUACIÓN FINAL: {puntos} puntos")
```

---

## 📝 Evaluación del Módulo 11

Para considerar terminado este módulo, debes poder:

- [ ] Crear listas de distintos tipos
- [ ] Acceder a elementos por índice (incluyendo índices negativos)
- [ ] Añadir elementos con `.append()` e `.insert()`
- [ ] Eliminar elementos con `.remove()`, `del`, y `.pop()`
- [ ] Ordenar listas con `.sort()`
- [ ] Recorrer listas con `for`
- [ ] Comprobar pertenencia con `in`

---

💾 **Guarda tu trabajo** en: `modulo11_listas.py`

---

➡️ **Siguiente:** `Modulo_12_Proyecto_Final/`
