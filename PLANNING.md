# 📅 Planning Detallado del Curso – Logo y Python para Niños

## ⏱️ Distribución de tiempo

- **Total del curso:** 12 semanas
- **Sesiones por semana:** 3 sesiones
- **Duración por sesión:** 45-60 minutos
- **Total de horas:** ~40 horas de aprendizaje

---

## 📊 Resumen de fases

| Fase | Semanas | Contenido | Objetivo |
|------|---------|-----------|----------|
| Preparación | 0 | Instalación y conceptos básicos | Tener el entorno listo |
| Logo | 1-4 | Tortuga, figuras, colores, procedimientos | Pensar como programador |
| Python Básico | 5-8 | Variables, tipos, condiciones | Entender el lenguaje |
| Python Intermedio | 9-12 | Bucles, funciones, listas, proyecto | Crear programas reales |

---

## 🗓️ Semana 0 – Preparación y Bienvenida

**Objetivo:** Conocer el curso, instalar los programas y entender qué es la programación.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 0.1 | Leer la presentación del curso, conocer el plan | 30 min |
| 0.2 | Instalar FMSLogo y/o acceder a Papert online | 30 min |
| 0.3 | Instalar Python y Thonny, hacer el primer "Hola" | 30 min |

**Material:** `Modulo_00_Bienvenida/teoria.md`

---

## 🗓️ Semana 1 – Logo: ¡Mueve la Tortuga!

**Objetivo:** Aprender los primeros comandos de Logo para mover la tortuga.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 1.1 | Teoría: ¿Qué es Logo? Comandos FORWARD y BACK | 45 min |
| 1.2 | Teoría: Giros con LEFT y RIGHT. Dibujar líneas | 45 min |
| 1.3 | Práctica guiada: Dibujar un cuadrado y un triángulo | 45 min |

**Conceptos clave:**
- `FORWARD n` / `FD n` – avanzar n pasos
- `BACK n` / `BK n` – retroceder n pasos
- `RIGHT n` / `RT n` – girar a la derecha n grados
- `LEFT n` / `LT n` – girar a la izquierda n grados
- `PENUP` / `PENDOWN` – subir/bajar el lápiz
- `CLEARSCREEN` / `CS` – limpiar la pantalla

**Actividades:** `Modulo_01_Logo_Comandos_Basicos/actividades.md`
**Ejercicios:** `Modulo_01_Logo_Comandos_Basicos/ejercicios/`

---

## 🗓️ Semana 2 – Logo: Figuras, Colores y Ángulos

**Objetivo:** Dibujar figuras más complejas y añadir color.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 2.1 | Teoría: Ángulos y polígonos regulares | 45 min |
| 2.2 | Teoría: Colores con SETPENCOLOR y rellenos | 45 min |
| 2.3 | Práctica: Dibujar una casa, un sol y un árbol | 60 min |

**Conceptos clave:**
- Ángulos exteriores de polígonos (360/n)
- `SETPENCOLOR [r g b]` / `SETPC n`
- `SETPENWIDTH n` – grosor del lápiz
- `FILL` – rellenar figura
- `SETBACKGROUND n` – color de fondo
- `HIDETURTLE` / `SHOWTURTLE`

**Actividades:** `Modulo_02_Logo_Figuras_Colores/actividades.md`

---

## 🗓️ Semana 3 – Logo: Repetición y Procedimientos

**Objetivo:** Usar REPEAT y crear nuestros propios comandos (procedimientos).

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 3.1 | Teoría: El comando REPEAT – repetir sin cansarse | 45 min |
| 3.2 | Teoría: Crear procedimientos con TO...END | 45 min |
| 3.3 | Práctica: Dibujar flores, espirales y estrellas | 60 min |

**Conceptos clave:**
- `REPEAT n [comandos]` – repetir n veces
- `TO nombre ... END` – definir un procedimiento
- Procedimientos con parámetros (variables)
- Procedimientos que llaman a otros procedimientos

**Actividades:** `Modulo_03_Logo_Repeticion_Procedimientos/actividades.md`

---

## 🗓️ Semana 4 – Proyecto Logo: ¡Mi obra de arte!

**Objetivo:** Crear un dibujo complejo usando todo lo aprendido.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 4.1 | Planificar el proyecto: ¿qué quieres dibujar? | 30 min |
| 4.2 | Crear el código del proyecto | 60 min |
| 4.3 | Retoques finales y presentación | 45 min |

**Ideas de proyecto:**
- Un paisaje con montañas, sol y nubes
- Un robot o personaje dibujado con figuras geométricas
- Un mandala o figura simétrica
- El nombre del alumno en letras decoradas

**Material:** `Modulo_04_Proyecto_Logo/`

---

## 🗓️ Semana 5 – Python: ¡Hola, Python! Variables y print

**Objetivo:** Escribir los primeros programas en Python.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 5.1 | Teoría: ¿Qué es Python? El comando print() | 45 min |
| 5.2 | Teoría: Variables – guardar información | 45 min |
| 5.3 | Práctica: Programas que saludan al usuario | 45 min |

**Conceptos clave:**
- `print("Hola")` – mostrar texto
- Variables: `nombre = "Ana"`
- `input()` – pedir información al usuario
- Tipos básicos: texto (str), números (int, float)
- Comentarios con `#`

**Actividades:** `Modulo_05_Python_Hola_Variables/actividades.md`
**Ejercicios:** `Modulo_05_Python_Hola_Variables/ejercicios/`

---

## 🗓️ Semana 6 – Python: Números y Matemáticas

**Objetivo:** Usar Python como una calculadora inteligente.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 6.1 | Teoría: Operaciones matemáticas básicas | 45 min |
| 6.2 | Teoría: División entera, módulo y potencias | 45 min |
| 6.3 | Práctica: Calculadora de propinas, áreas y más | 60 min |

**Conceptos clave:**
- Operadores: `+`, `-`, `*`, `/`
- División entera: `//`
- Módulo (resto): `%`
- Potencia: `**`
- `int()`, `float()` – convertir tipos
- `round()` – redondear

**Actividades:** `Modulo_06_Python_Numeros/actividades.md`

---

## 🗓️ Semana 7 – Python: Texto y Cadenas

**Objetivo:** Manejar texto con Python.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 7.1 | Teoría: Cadenas de texto y operaciones | 45 min |
| 7.2 | Teoría: Métodos de cadenas: upper, lower, len... | 45 min |
| 7.3 | Práctica: Generar nombres, mensajes secretos | 60 min |

**Conceptos clave:**
- Concatenar con `+`
- f-strings: `f"Hola {nombre}"`
- `len()`, `.upper()`, `.lower()`, `.replace()`
- `.strip()`, `.split()`, `.count()`
- Acceder a caracteres: `texto[0]`

**Actividades:** `Modulo_07_Python_Texto/actividades.md`

---

## 🗓️ Semana 8 – Python: Decisiones con if/else

**Objetivo:** Que el programa tome decisiones según las condiciones.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 8.1 | Teoría: Condiciones y comparaciones | 45 min |
| 8.2 | Teoría: if, elif, else – tomar decisiones | 45 min |
| 8.3 | Práctica: Adivinanzas, semáforos, calificaciones | 60 min |

**Conceptos clave:**
- Operadores de comparación: `==`, `!=`, `>`, `<`, `>=`, `<=`
- `if condición:` / `else:` / `elif condición:`
- Operadores lógicos: `and`, `or`, `not`
- `True` y `False` – valores booleanos

**Actividades:** `Modulo_08_Python_Decisiones/actividades.md`

---

## 🗓️ Semana 9 – Python: Bucles – Repetir sin Cansarse

**Objetivo:** Hacer que el programa repita acciones automáticamente.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 9.1 | Teoría: El bucle while – mientras... | 45 min |
| 9.2 | Teoría: El bucle for – para cada... | 45 min |
| 9.3 | Práctica: Tablas de multiplicar, contadores, juegos | 60 min |

**Conceptos clave:**
- `while condición:` – bucle mientras
- `for i in range(n):` – bucle for con rango
- `for elemento in lista:` – recorrer lista
- `break` – salir del bucle
- `continue` – saltar a siguiente iteración

**Actividades:** `Modulo_09_Python_Bucles/actividades.md`

---

## 🗓️ Semana 10 – Python: Funciones

**Objetivo:** Crear nuestras propias funciones para reusar código.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 10.1 | Teoría: ¿Qué es una función y para qué sirve? | 45 min |
| 10.2 | Teoría: Parámetros y return | 45 min |
| 10.3 | Práctica: Funciones para calcular y jugar | 60 min |

**Conceptos clave:**
- `def nombre_funcion():` – definir función
- Parámetros: `def saludar(nombre):`
- `return valor` – devolver resultado
- Variables locales vs globales (intro)

**Actividades:** `Modulo_10_Python_Funciones/actividades.md`

---

## 🗓️ Semana 11 – Python: Listas

**Objetivo:** Guardar y manejar colecciones de datos.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 11.1 | Teoría: Listas – guardar varias cosas juntas | 45 min |
| 11.2 | Teoría: Añadir, quitar, ordenar listas | 45 min |
| 11.3 | Práctica: Lista de tareas, ranking de puntuaciones | 60 min |

**Conceptos clave:**
- Crear lista: `frutas = ["manzana", "naranja", "pera"]`
- Acceder: `frutas[0]`
- `.append()`, `.remove()`, `.sort()`
- `len()` – longitud de lista
- Recorrer lista con `for`

**Actividades:** `Modulo_11_Python_Listas/actividades.md`

---

## 🗓️ Semana 12 – Proyecto Final: ¡Mi Videojuego de Texto!

**Objetivo:** Crear un juego completo usando todo lo aprendido.

| Sesión | Actividad | Tiempo |
|--------|-----------|--------|
| 12.1 | Diseñar el juego: historia, personajes, reglas | 45 min |
| 12.2 | Programar el juego – primera versión | 60 min |
| 12.3 | Mejoras finales y presentación del proyecto | 60 min |

**Ideas de proyecto:**
- Juego de adivinar un número secreto
- Aventura de texto con decisiones
- Quiz de preguntas y respuestas
- Juego de ahorcado

**Material:** `Modulo_12_Proyecto_Final/`

---

## 📈 Progresión de dificultad

```
Semana:   0    1    2    3    4    5    6    7    8    9   10   11   12
          ▁    ▂    ▃    ▄    ▅    ▃    ▄    ▅    ▅    ▆    ▇    ▇    █
Nivel:  Prep Logo Logo Logo Logo Py  Py  Py  Py  Py  Py  Py  Py
        0    1    2    3  Proj  1    2    3    4    5    6    7  Final
```

---

## ✅ Checklist de progreso

Marca cada módulo cuando lo termines:

**Fase Logo:**
- [ ] Semana 0 – Preparación
- [ ] Semana 1 – Comandos básicos Logo
- [ ] Semana 2 – Figuras y colores Logo
- [ ] Semana 3 – Repetición y procedimientos Logo
- [ ] Semana 4 – Proyecto Logo ⭐

**Fase Python:**
- [ ] Semana 5 – Hola Python, variables
- [ ] Semana 6 – Números y matemáticas
- [ ] Semana 7 – Texto y cadenas
- [ ] Semana 8 – Decisiones if/else
- [ ] Semana 9 – Bucles
- [ ] Semana 10 – Funciones
- [ ] Semana 11 – Listas
- [ ] Semana 12 – Proyecto Final ⭐⭐

---

## 🔗 Recursos adicionales

| Recurso | URL | Tipo |
|---------|-----|------|
| Scratch (programación visual) | scratch.mit.edu | Complementario |
| Hour of Code | hourofcode.com/es | Práctica extra |
| Python para niños (libro) | nostarch.com | Lectura |
| Code.org cursos | code.org/learn | Práctica extra |
| Turtle Python online | trinket.io | Ejercicios |
