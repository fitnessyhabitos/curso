# 🏆 Módulo 12 – Proyecto Final: ¡Mi Videojuego de Texto!

## 🌟 ¡Ha llegado el gran momento!

Has completado todo el curso. Ahora vas a crear **tu propio videojuego** usando todo lo que has aprendido:
- Variables y tipos de datos
- Cadenas de texto
- Condiciones (if/elif/else)
- Bucles (while y for)
- Funciones (def)
- Listas

---

## 📋 Requisitos del proyecto

Tu juego debe incluir:
- [ ] Al menos **3 funciones** propias
- [ ] Uso de **listas** para guardar datos
- [ ] **Bucle** principal del juego
- [ ] **Condiciones** para tomar decisiones
- [ ] **Entrada del usuario** con `input()`
- [ ] Un **sistema de puntuación** o progreso
- [ ] Mensajes claros y bonitos con decoración

---

## 💡 Ideas de proyectos

### Opción 1: La Aventura de Texto ⚔️

Un juego de aventura donde el jugador toma decisiones:
- Diferentes escenarios y caminos
- Sistema de vida y ataque
- Inventario de objetos
- Al menos 3 enemigos
- Final ganador y perdedor

### Opción 2: El Quiz Definitivo 🧠

Un quiz de preguntas:
- Al menos 15 preguntas de diferentes categorías
- Dificultad progresiva
- Sistema de vidas
- Ranking de puntuaciones
- Preguntas en orden aleatorio

### Opción 3: El Ahorcado Avanzado 🎭

El juego del ahorcado con:
- Varias categorías de palabras
- Sistema de pistas
- Múltiples partidas con estadísticas
- Ranking de mejores puntuaciones
- Opción de añadir palabras propias

### Opción 4: ¡Inventa tu propio juego! 🎮

Si tienes una idea original, ¡adelante! Solo asegúrate de cumplir los requisitos.

---

## 🛠️ Plantilla base: La Aventura de Texto

Aquí tienes una base para empezar la aventura de texto:

```python
# ================================================
# PROYECTO FINAL: [EL NOMBRE DE TU JUEGO]
# Creado por: [Tu nombre]
# Fecha: [La fecha]
# ================================================

import random

# ─────────────────────────────────────────────
# CONFIGURACIÓN DEL JUEGO
# ─────────────────────────────────────────────

VERSION = "1.0"
TITULO = "La Gran Aventura"

# ─────────────────────────────────────────────
# FUNCIONES DE UTILIDAD
# ─────────────────────────────────────────────

def titulo_bonito(texto):
    """Muestra un título decorado"""
    borde = "═" * (len(texto) + 4)
    print(f"\n╔{borde}╗")
    print(f"║  {texto}  ║")
    print(f"╚{borde}╝\n")

def separador(caracter="─", longitud=40):
    """Imprime una línea separadora"""
    print(caracter * longitud)

def pausa():
    """Espera a que el usuario pulse Enter"""
    input("\n[Pulsa Enter para continuar...]")

# ─────────────────────────────────────────────
# FUNCIONES DEL JUEGO
# ─────────────────────────────────────────────

def mostrar_estado(jugador):
    """Muestra el estado actual del jugador"""
    separador()
    print(f"👤 Héroe: {jugador['nombre']}")
    print(f"❤️  Vida: {jugador['vida']}/{jugador['vida_max']}")
    print(f"⚔️  Ataque: {jugador['ataque']}")
    print(f"🏆 Puntos: {jugador['puntos']}")
    if jugador['inventario']:
        print(f"🎒 Inventario: {', '.join(jugador['inventario'])}")
    separador()

def combatir(jugador, enemigo):
    """Sistema de combate simple"""
    titulo_bonito(f"⚔️  COMBATE: {jugador['nombre']} vs {enemigo['nombre']}")

    vida_enemigo = enemigo['vida']

    while jugador['vida'] > 0 and vida_enemigo > 0:
        print(f"\n{jugador['nombre']}: {jugador['vida']} vida | "
              f"{enemigo['nombre']}: {vida_enemigo} vida")
        print("\n¿Qué haces?")
        print("  1. Atacar")
        print("  2. Usar poción (si tienes)")
        print("  3. Huir")

        accion = input("\nAcción: ")

        if accion == "1":
            # Atacas tú
            mi_daño = random.randint(jugador['ataque'] - 2, jugador['ataque'] + 3)
            vida_enemigo -= mi_daño
            print(f"Causas {mi_daño} de daño a {enemigo['nombre']}.")

            if vida_enemigo > 0:
                # Contraataque del enemigo
                daño_enemigo = random.randint(enemigo['ataque'] - 1, enemigo['ataque'] + 2)
                jugador['vida'] -= daño_enemigo
                print(f"{enemigo['nombre']} te causa {daño_enemigo} de daño.")

        elif accion == "2":
            if "poción" in jugador['inventario']:
                jugador['inventario'].remove("poción")
                curacion = random.randint(10, 20)
                jugador['vida'] = min(jugador['vida'] + curacion, jugador['vida_max'])
                print(f"Usas una poción. Recuperas {curacion} de vida.")
            else:
                print("¡No tienes pociones!")

        elif accion == "3":
            print("¡Huyes del combate!")
            return "huida"

    if jugador['vida'] <= 0:
        return "derrota"
    else:
        print(f"\n¡Derrotaste a {enemigo['nombre']}!")
        jugador['puntos'] += enemigo['recompensa']
        print(f"Ganaste {enemigo['recompensa']} puntos.")
        if enemigo.get('drop'):
            jugador['inventario'].append(enemigo['drop'])
            print(f"Encontraste: {enemigo['drop']}")
        return "victoria"

def escena_inicio(jugador):
    """Escena de inicio del juego"""
    titulo_bonito(TITULO)
    print("Eres un valiente aventurero que debe rescatar al reino.")
    print("Tu misión: derrotar al Dragón Oscuro y salvar la princesa.")
    print()
    print("¿Estás preparado para la aventura más grande de tu vida?")
    pausa()

def zona_bosque(jugador):
    """Primera zona: el bosque misterioso"""
    titulo_bonito("🌲 EL BOSQUE MISTERIOSO")
    print("Entras en un bosque oscuro y silencioso.")
    print("Las ramas crujen bajo tus pies...")
    print()
    print("¿Qué camino tomas?")
    print("  1. El camino iluminado (más seguro)")
    print("  2. El sendero oscuro (más peligroso pero con recompensa)")
    print("  3. Explorar el bosque (aventurero)")

    eleccion = input("\nElección: ")

    if eleccion == "1":
        print("\nSigues el camino seguro y encuentras un mercader.")
        print("Te vende una poción a buen precio.")
        jugador['inventario'].append("poción")
        jugador['puntos'] += 5

    elif eleccion == "2":
        goblin = {
            'nombre': 'Goblin feroz',
            'vida': 20,
            'ataque': 5,
            'recompensa': 20,
            'drop': 'espada mágica'
        }
        resultado = combatir(jugador, goblin)
        if resultado == "victoria":
            jugador['ataque'] += 3    # La espada mágica mejora el ataque
        elif resultado == "derrota":
            return False

    elif eleccion == "3":
        evento = random.randint(1, 3)
        if evento == 1:
            print("\nEncuentras un cofre abandonado con una poción dentro.")
            jugador['inventario'].append("poción")
        elif evento == 2:
            print("\nCaes en una trampa. Pierdes 5 de vida.")
            jugador['vida'] -= 5
        else:
            print("\nEncuentras un mapa del tesoro. +10 puntos.")
            jugador['puntos'] += 10

    return jugador['vida'] > 0

def zona_castillo(jugador):
    """Segunda zona: el castillo del dragón"""
    titulo_bonito("🏰 EL CASTILLO DEL DRAGÓN")
    print("Llegas a un castillo sombrío rodeado de niebla.")
    print("Las puertas están custodiadas por dos guardianes.")

    guardian = {
        'nombre': 'Guardián del Castillo',
        'vida': 35,
        'ataque': 8,
        'recompensa': 30,
        'drop': None
    }

    print("\nDebes pasar por la guardia. ¿Cómo lo haces?")
    print("  1. Luchar contra los guardianes")
    print("  2. Intentar engañarlos")
    print("  3. Buscar una entrada secreta")

    eleccion = input("\nElección: ")

    if eleccion == "1":
        resultado = combatir(jugador, guardian)
        if resultado == "derrota":
            return False

    elif eleccion == "2":
        if jugador['puntos'] >= 20:
            print("\nCon tu experiencia, los convences de que eres un inspector real.")
            print("¡Entras sin pelear! +15 puntos extra.")
            jugador['puntos'] += 15
        else:
            print("\nLos guardianes no te creen. ¡Al combate!")
            resultado = combatir(jugador, guardian)
            if resultado == "derrota":
                return False

    elif eleccion == "3":
        print("\nEncuentras una grieta en la pared. Te cuelas por ella.")
        jugador['vida'] -= 3
        print("Te arañas un poco pero llegas dentro. -3 vida.")

    return jugador['vida'] > 0

def jefe_final(jugador):
    """Batalla contra el jefe final"""
    titulo_bonito("🐉 EL DRAGÓN OSCURO")
    print("¡Al fin llegas a la sala del trono!")
    print("El Dragón Oscuro abre sus ojos rojos...")
    print('"¿Otro héroe inútil? ¡Os destrozo a todos!"')
    pausa()

    dragon = {
        'nombre': 'Dragón Oscuro',
        'vida': 60,
        'ataque': 12,
        'recompensa': 100,
        'drop': 'corona del reino'
    }

    resultado = combatir(jugador, dragon)
    return resultado

def final_victoria(jugador):
    titulo_bonito("🎉 ¡VICTORIA!")
    print("¡Has derrotado al Dragón Oscuro!")
    print("La princesa es liberada y el reino está a salvo.")
    print()
    print("Los habitantes del reino te aclaman como HÉROE.")
    print()
    separador("═")
    print(f"  ESTADÍSTICAS FINALES DE {jugador['nombre'].upper()}")
    separador("═")
    print(f"  Puntos totales: {jugador['puntos']}")
    print(f"  Vida restante: {jugador['vida']}/{jugador['vida_max']}")
    print(f"  Objetos recogidos: {len(jugador['inventario'])}")
    separador("═")

def final_derrota(jugador):
    titulo_bonito("💀 DERROTA")
    print("Has caído en combate...")
    print("Pero los héroes no mueren, ¡solo aprenden!")
    print()
    print("Inicia una nueva partida para vengarte.")
    print(f"\nPuntos conseguidos: {jugador['puntos']}")

# ─────────────────────────────────────────────
# FUNCIÓN PRINCIPAL
# ─────────────────────────────────────────────

def iniciar_juego():
    titulo_bonito(f"⚔️  {TITULO.upper()} ⚔️")
    print("Versión:", VERSION)

    nombre = input("Introduce el nombre de tu héroe: ").strip()
    if not nombre:
        nombre = "Aventurero"

    jugador = {
        'nombre': nombre,
        'vida': 50,
        'vida_max': 50,
        'ataque': 8,
        'puntos': 0,
        'inventario': ['poción']    # Empiezas con una poción
    }

    print(f"\n¡Bienvenido, {nombre}! Tu aventura comienza...")
    mostrar_estado(jugador)
    pausa()

    # Escena de inicio
    escena_inicio(jugador)

    # Zona 1: Bosque
    if not zona_bosque(jugador):
        final_derrota(jugador)
        return

    mostrar_estado(jugador)
    pausa()

    # Zona 2: Castillo
    if not zona_castillo(jugador):
        final_derrota(jugador)
        return

    mostrar_estado(jugador)
    pausa()

    # Jefe final
    resultado = jefe_final(jugador)

    if resultado == "victoria":
        final_victoria(jugador)
    else:
        final_derrota(jugador)

# ─────────────────────────────────────────────
# INICIO DEL PROGRAMA
# ─────────────────────────────────────────────

while True:
    iniciar_juego()
    otra = input("\n¿Quieres jugar otra vez? (s/n): ").lower()
    if otra != "s":
        print("\n¡Hasta pronto, héroe! 🗡️")
        break
```

---

## 🎯 Lista de comprobación final

Antes de dar por terminado tu proyecto, verifica:

**Código:**
- [ ] ¿Tienes al menos 3 funciones propias?
- [ ] ¿Usas listas en el juego?
- [ ] ¿Hay un bucle principal?
- [ ] ¿Hay condiciones if/elif/else?
- [ ] ¿El programa funciona sin errores?

**Diseño:**
- [ ] ¿Los mensajes son claros y fáciles de entender?
- [ ] ¿Hay una pantalla de inicio?
- [ ] ¿Hay un final (ganador o perdedor)?
- [ ] ¿Hay un sistema de puntuación?

**Calidad:**
- [ ] ¿El código tiene comentarios que explican qué hace?
- [ ] ¿Los nombres de variables y funciones son descriptivos?
- [ ] ¿Has probado diferentes caminos del juego?

---

## 🏆 ¡Felicidades! Completaste el curso

Has aprendido:

**Logo:**
- ✅ Comandos básicos (FD, BK, RT, LT)
- ✅ Colores y figuras
- ✅ Repetición con REPEAT
- ✅ Procedimientos propios

**Python:**
- ✅ print(), input() y variables
- ✅ Números y matemáticas
- ✅ Cadenas de texto
- ✅ Condiciones if/elif/else
- ✅ Bucles while y for
- ✅ Funciones
- ✅ Listas

**¿Qué puedes aprender a continuación?**
- 🐢 **Turtle Python** – Dibujar como en Logo pero con Python
- 🌐 **HTML/CSS** – Crear páginas web
- 🎮 **Pygame** – Crear videojuegos con gráficos
- 🤖 **Scratch avanzado** – Animaciones y juegos visuales

---

💾 **Guarda tu proyecto** en: `mi_videojuego.py`

🌟 **¡Eres un programador!** 🌟
