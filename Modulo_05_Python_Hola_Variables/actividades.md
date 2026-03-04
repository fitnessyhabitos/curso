# 🎯 Módulo 5 – Actividades: ¡Hola, Python! Variables y print

## Actividad 5.1 – ¡Tu primer programa Python! (⭐ Fácil)

**Objetivo:** Escribir y ejecutar tu primer programa en Python.

Abre Thonny (o repl.it), crea un nuevo archivo y escribe:

```python
# Mi primer programa Python
# Creado por: [pon tu nombre aquí]

print("¡Hola, mundo!")
print("Me llamo [pon tu nombre aquí]")
print("Tengo [pon tu edad aquí] años")
print("¡Voy a aprender a programar!")
```

Pulsa **Run** y comprueba que aparece en la consola.

### ✍️ Mejóralo:
Añade 3 líneas más con cosas sobre ti (tu deporte favorito, tu animal preferido, tu película favorita).

---

## Actividad 5.2 – El saludo personalizado (⭐ Fácil)

**Objetivo:** Usar variables para personalizar mensajes.

```python
# El saludo personalizado

nombre = "Ana"
edad = 10
ciudad = "Madrid"

print(f"¡Hola! Me llamo {nombre}.")
print(f"Tengo {edad} años.")
print(f"Vivo en {ciudad}.")
print(f"Cuando tenga {edad + 1} años, tendré {edad + 1} años.")
```

### ✍️ Tu turno:
1. Cambia `nombre`, `edad` y `ciudad` con tus datos reales
2. Añade más variables: `deporte_favorito`, `color_favorito`, `mascota`
3. Crea frases con esas variables usando f-strings

---

## Actividad 5.3 – El programa interactivo (⭐⭐ Medio)

**Objetivo:** Usar input() para hacer un programa que hable con el usuario.

```python
# El programa interactivo

print("=== ¡Hola! Soy un robot amigable ===")
print()

nombre = input("¿Cómo te llamas? ")
print(f"\n¡Encantado de conocerte, {nombre}!")

edad = input("¿Cuántos años tienes? ")
print(f"¡{edad} años! ¡Eres todo un programador!")

ciudad = input("¿De qué ciudad eres? ")
print(f"¡{ciudad}! Debe ser un lugar genial.")

print()
print("=== ¡Hasta pronto! ===")
```

> Nota: `print()` sin nada dentro añade una línea en blanco.
> `\n` dentro de un texto también añade una línea nueva.

### ✍️ Amplíalo:
Añade 3 preguntas más al robot (comida favorita, animal favorito, superhéroe favorito) y termina con un mensaje personalizado que use todas las respuestas.

---

## Actividad 5.4 – Tarjeta de presentación (⭐⭐ Medio)

**Objetivo:** Crear una tarjeta de presentación con recuadro de texto.

```python
# Tarjeta de presentación

nombre = input("Tu nombre: ")
edad = input("Tu edad: ")
hobby = input("Tu hobby favorito: ")
superhereo = input("Tu superhéroe favorito: ")

print()
print("╔════════════════════════════════════╗")
print("║       TARJETA DE PROGRAMADOR       ║")
print("╠════════════════════════════════════╣")
print(f"║  Nombre: {nombre:<26}║")
print(f"║  Edad:   {edad:<26}║")
print(f"║  Hobby:  {hobby:<26}║")
print(f"║  Héroe:  {superhereo:<26}║")
print("╠════════════════════════════════════╣")
print("║     🐍 Programador Python Junior    ║")
print("╚════════════════════════════════════╝")
```

> Nota: `{nombre:<26}` ajusta el texto a 26 caracteres de ancho (alineado a la izquierda).

### ✍️ Personalízala:
- Añade tu ciudad y tu comida favorita
- Cambia el diseño del recuadro (usa `*` en vez de `═`)
- Añade más información

---

## Actividad 5.5 – El generador de historias (⭐⭐⭐ Difícil)

**Objetivo:** Crear una historia que cambia según las respuestas del usuario.

```python
# El generador de historias

print("=== GENERADOR DE HISTORIAS ===")
print("Responde las preguntas y crearé una historia para ti.")
print()

heroe = input("Nombre del héroe/heroína: ")
animal = input("Un animal (cualquiera): ")
lugar = input("Un lugar mágico: ")
objeto = input("Un objeto mágico: ")
villano = input("Nombre del villano: ")
superpoder = input("Un superpoder: ")

print()
print("═" * 50)
print("         ✨ TU HISTORIA ✨")
print("═" * 50)
print()
print(f"Érase una vez {heroe}, un valiente aventurero")
print(f"que vivía en el misterioso {lugar}.")
print()
print(f"Un día, {heroe} encontró un {animal} muy especial")
print(f"que le entregó un {objeto} mágico.")
print()
print(f"Con el poder del {objeto}, {heroe} obtuvo")
print(f"la increíble habilidad de {superpoder}.")
print()
print(f"Justo entonces apareció el temible {villano},")
print(f"que quería robar el {objeto} para siempre.")
print()
print(f"Pero {heroe}, con la ayuda de su amigo el {animal}")
print(f"y usando {superpoder}, derrotó a {villano}.")
print()
print(f"¡Y {heroe} salvó el {lugar} para siempre!")
print()
print("═" * 50)
print("           FIN")
print("═" * 50)
```

### ✍️ Amplíalo:
- Añade 3 personajes más a la historia
- Crea un final diferente con una moraleja
- ¡Inventa tu propia historia completamente diferente!

---

## Actividad 5.6 – RETO: El robot conversador (⭐⭐⭐ Difícil)

**Objetivo:** Crear un chatbot simple que tenga una conversación.

```python
# El robot conversador

print("╔══════════════════════════════╗")
print("║   🤖 ROBOTO - Tu amigo robot  ║")
print("╚══════════════════════════════╝")
print()
print("ROBOTO: ¡Hola! Soy ROBOTO, tu robot amigo.")
print("ROBOTO: ¡Hoy es un gran día para aprender!")
print()

nombre = input("TÚ: ¿Cómo te llamas?\n → ")
print(f"\nROBOTO: ¡{nombre}! ¡Qué nombre tan bonito!")
print()

pregunta = input("TÚ: ¿Cómo estás hoy?\n → ")
print(f"\nROBOTO: ¿{pregunta}? ¡Genial! Yo siempre estoy bien.")
print("ROBOTO: Soy un robot, ¡así que nunca me pongo triste!")
print()

materia = input("TÚ: ¿Cuál es tu asignatura favorita?\n → ")
print(f"\nROBOTO: ¡{materia}! A mí me gusta la programación.")
print(f"ROBOTO: ¡Tú y yo somos muy parecidos, {nombre}!")
print()

print("ROBOTO: Tengo que irme a cargar mis baterías.")
print(f"ROBOTO: ¡Hasta pronto, {nombre}! ¡Sigue programando!")
```

### ✍️ Amplíalo:
Añade 5 preguntas más al robot y haz que recuerde las respuestas anteriores para usarlas en preguntas posteriores.

---

## 📝 Evaluación del Módulo 5

Para considerar terminado este módulo, debes poder:

- [ ] Usar `print()` para mostrar texto
- [ ] Crear variables de texto, número y booleanas
- [ ] Usar `input()` para pedir datos al usuario
- [ ] Usar f-strings para mostrar variables en texto
- [ ] Escribir comentarios con `#`

---

💾 **Guarda tu trabajo** en: `modulo5_ejercicios.py`

---

➡️ **Siguiente:** `Modulo_06_Python_Numeros/teoria.md`
