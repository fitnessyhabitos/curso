# 🎯 Módulo 1 – Actividades: ¡Mueve la Tortuga!

## Antes de empezar

Abre FMSLogo o ve a la página online de Logo. Verás:
- Una ventana grande con la tortuga en el centro (la pantalla de dibujo)
- Una ventana pequeña abajo donde escribirás los comandos

Cada vez que escribas un comando y pulses **Enter**, la tortuga lo ejecutará.

---

## Actividad 1.1 – ¡Hola, tortuga! (⭐ Fácil)

**Objetivo:** Hacer que la tortuga se mueva por primera vez.

### Paso 1:
Escribe este comando y pulsa Enter:
```logo
FD 100
```
Deberías ver una línea recta hacia arriba. ¡Felicidades, has programado!

### Paso 2:
Ahora escribe:
```logo
RT 90
```
La tortuga gira sin moverse.

### Paso 3:
```logo
FD 100
```
Ahora hay dos líneas formando una L.

### Paso 4:
Limpia la pantalla y empieza de nuevo:
```logo
CS
```

### ✍️ Tu turno:
Haz que la tortuga dibuje esto (dos líneas formando una L invertida):
```
←──── 150 pasos
     |
     | 100 pasos
     |
```
**Pista:** Necesitas: FD, RT (o LT), FD. Piensa qué ángulo necesitas para hacer una L invertida.

---

## Actividad 1.2 – El cuadrado mágico (⭐ Fácil)

**Objetivo:** Dibujar un cuadrado de 100x100.

### Código:
```logo
CS
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
FD 100
```

### ¿Ves el cuadrado? ¡Genial!

### Variación 1 – Cuadrado más grande:
Copia el código pero cambia todos los `100` por `150`. ¿Qué pasa?

### Variación 2 – Cuadrado más pequeño:
Ahora cambia todos los `100` por `50`. ¿Y ahora?

### ✍️ Tu turno:
¿Puedes dibujar un **rectángulo**? (Lados de 150 y 80)
- Pista: Un rectángulo tiene 2 lados largos y 2 lados cortos
- Los ángulos siguen siendo de 90°

---

## Actividad 1.3 – El triángulo (⭐⭐ Medio)

**Objetivo:** Dibujar un triángulo equilátero.

Recuerda: el ángulo de giro para un triángulo es **120°**.

```logo
CS
FD 100
RT 120
FD 100
RT 120
FD 100
```

### ✍️ Desafío:
¿Puedes dibujar una **flecha** apuntando a la derecha? Usa solo FD, BK, RT, LT.
```
    *
   / \
  /   \
 *─────*─────────*
  \   /
   \ /
    *
```
**Pista:** Empieza dibujando una línea larga (el palo de la flecha), luego añade la punta.

---

## Actividad 1.4 – La escalera (⭐⭐ Medio)

**Objetivo:** Dibujar una escalera con 3 peldaños.

Mira el dibujo:
```
     ___
    |
 ___|
|
```

### Código para UN peldaño:
```logo
FD 30     ← Subida
RT 90
FD 30     ← Peldaño horizontal
LT 90
```

### ✍️ Tu turno:
Dibuja una escalera con **3 peldaños**. Cada peldaño mide 30 de alto y 30 de ancho.

---

## Actividad 1.5 – El lápiz mágico (⭐⭐ Medio)

**Objetivo:** Usar PENUP y PENDOWN para dibujar figuras separadas.

### Prueba este código:
```logo
CS
FD 50
PU
FD 30
PD
FD 50
```
¿Ves dos líneas separadas con un espacio?

### ✍️ Tu turno:
Dibuja tres cuadrados pequeños (30x30) separados entre sí:
```
□   □   □
```
**Pista:**
1. Dibuja el primer cuadrado
2. Sube el lápiz
3. Muévete hacia la derecha
4. Baja el lápiz
5. Dibuja el segundo cuadrado
6. Repite

---

## Actividad 1.6 – Las letras I y L (⭐⭐⭐ Difícil)

**Objetivo:** Dibujar letras usando solo líneas rectas.

### La letra I:
```
 ___
  |
  |
  |
 ___
```

### La letra L:
```
|
|
|
|___
```

### ✍️ Tu turno:
Dibuja la primera letra de tu nombre usando solo líneas rectas y giros de 90°.
- Letras fáciles: I, L, T, H, E, F, C, U
- Letras difíciles: S, R, B, D

---

## Actividad 1.7 – RETO: La casa (⭐⭐⭐ Difícil)

**Objetivo:** Dibujar una casa simple con paredes y tejado.

```
      /\
     /  \
    /    \
   /______\
   |      |
   |      |
   |______|
```

La casa tiene:
- Paredes cuadradas: 100x100
- Tejado triangular: lados de ~70 con ángulo especial

**Pista para el tejado:**
- Después de dibujar las paredes, la tortuga estará en una esquina del tejado
- El tejado es un triángulo, ¡pero no equilátero!
- Prueba con ángulos de 150° para los giros del tejado

**Código del cuadrado (paredes):**
```logo
CS
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
FD 100
```
Ahora tú continúa añadiendo el tejado...

---

## Actividad 1.8 – RETO ESTRELLA: El pentagrama (⭐⭐⭐⭐ Muy difícil)

**Objetivo:** Dibujar una estrella de 5 puntas.

Para dibujar una estrella de 5 puntas, la tortuga gira **144°** en cada punto (no 72°).

```logo
CS
FD 100
RT 144
FD 100
RT 144
FD 100
RT 144
FD 100
RT 144
FD 100
```

¡Inténtalo! ¿Ves la estrella? ¿Entiendes por qué funciona?

---

## 📝 Evaluación del Módulo 1

Para considerar terminado este módulo, debes poder:

- [ ] Usar FD, BK, RT, LT para mover la tortuga
- [ ] Dibujar un cuadrado de cualquier tamaño
- [ ] Dibujar un triángulo equilátero
- [ ] Usar PENUP/PENDOWN para figuras separadas
- [ ] Limpiar la pantalla con CS

---

## 💾 Guardar tu trabajo

En FMSLogo, puedes guardar tu código:
1. Ve al menú **File → Save**
2. Guárdalo como: `modulo1_ejercicios.lgo`

O puedes copiar el código en un archivo de texto (.txt) para guardarlo.

---

➡️ **Siguiente:** `Modulo_02_Logo_Figuras_Colores/teoria.md`
