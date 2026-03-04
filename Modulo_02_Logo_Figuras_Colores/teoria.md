# 📖 Módulo 2 – Logo: Figuras, Colores y Ángulos

## 🎨 ¡Vamos a añadir color!

Ya sabes mover la tortuga. Ahora vamos a hacer nuestros dibujos más bonitos con colores.

---

## 🖊️ Cambiar el color del lápiz: SETPENCOLOR

```logo
SETPENCOLOR [255 0 0]     ← Rojo
SETPC [0 255 0]           ← Verde  (SETPC es la forma corta)
SETPC [0 0 255]           ← Azul
SETPC [255 255 0]         ← Amarillo
SETPC [255 165 0]         ← Naranja
SETPC [128 0 128]         ← Morado
SETPC [0 0 0]             ← Negro
SETPC [255 255 255]       ← Blanco
```

### ¿Cómo funcionan los colores RGB?

Los colores en el ordenador se hacen mezclando tres colores:
- 🔴 **R** = Red (Rojo): del 0 al 255
- 🟢 **G** = Green (Verde): del 0 al 255
- 🔵 **B** = Blue (Azul): del 0 al 255

```
[0, 0, 0]       = Negro (sin luz)
[255, 255, 255] = Blanco (toda la luz)
[255, 0, 0]     = Rojo puro
[0, 255, 0]     = Verde puro
[0, 0, 255]     = Azul puro
[255, 255, 0]   = Amarillo (rojo + verde)
[0, 255, 255]   = Cian (verde + azul)
[255, 0, 255]   = Magenta (rojo + azul)
```

### Algunos colores favoritos:

| Color | Código RGB |
|-------|-----------|
| Rojo | [255, 0, 0] |
| Naranja | [255, 165, 0] |
| Amarillo | [255, 255, 0] |
| Verde | [0, 128, 0] |
| Azul | [0, 0, 255] |
| Morado | [128, 0, 128] |
| Rosa | [255, 192, 203] |
| Marrón | [139, 69, 19] |
| Gris | [128, 128, 128] |

---

## 🖌️ Cambiar el grosor del lápiz: SETPENWIDTH

```logo
SETPENWIDTH 1    ← Lápiz muy fino (por defecto)
SETPENWIDTH 3    ← Más grueso
SETPENWIDTH 10   ← Muy grueso
```

---

## 🎨 Cambiar el fondo: SETBACKGROUND

```logo
SETBACKGROUND [0 0 0]      ← Fondo negro
SETBACKGROUND [135 206 235] ← Fondo azul cielo
```

---

## 🐢 Esconder/mostrar la tortuga: HIDETURTLE / SHOWTURTLE

```logo
HIDETURTLE   ← Esconde la tortuga (el dibujo queda más limpio)
HT           ← Forma corta

SHOWTURTLE   ← Muestra la tortuga
ST           ← Forma corta
```

---

## 🔵 Polígonos regulares y el truco de 360°

Ya aprendiste que para un cuadrado giras 90° y para un triángulo giras 120°. Existe un truco matemático increíble:

> **Ángulo exterior = 360° / número de lados**

### Tabla de polígonos:

| Figura | Lados | Ángulo exterior | Código |
|--------|-------|-----------------|--------|
| Triángulo | 3 | 120° | `RT 120` |
| Cuadrado | 4 | 90° | `RT 90` |
| Pentágono | 5 | 72° | `RT 72` |
| Hexágono | 6 | 60° | `RT 60` |
| Heptágono | 7 | ~51.4° | `RT 51.43` |
| Octágono | 8 | 45° | `RT 45` |
| Decágono | 10 | 36° | `RT 36` |
| Círculo (aprox.) | 360 | 1° | `RT 1` |

### El círculo:

Para dibujar un círculo, hacemos 360 pasos de 1 grado cada uno:
```logo
REPEAT 360 [FD 1 RT 1]
```

(¡Aquí usamos REPEAT, que aprenderemos mejor en el Módulo 3!)

---

## 🏠 Ejemplo completo: Casa colorida

```logo
CS
SETBACKGROUND [135 206 235]    ← Cielo azul

; Dibuja las paredes en marrón
SETPC [139 69 19]
SETPENWIDTH 3
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90

; Dibuja el tejado en rojo
SETPC [200 0 0]
FD 100
RT 150
FD 70
RT 120
FD 70
RT 90
```

> 💡 Las líneas que empiezan con `;` son **comentarios**. Logo las ignora, son solo para que nosotros entendamos el código.

---

## 📐 El ángulo del tejado

Para una casa, el tejado es un triángulo isósceles. Para calcular los ángulos:
- Subimos por el lado de la pared: `FD 100`
- La tortuga ya mira hacia arriba (norte)
- El tejado va hacia la derecha en diagonal

Los ángulos del tejado dependen de qué tan puntiagudo lo queramos:
- Tejado muy puntiagudo: `RT 150` y `RT 120`
- Tejado normal: gira según el ángulo del triángulo

---

## 🌟 Ejemplo: Estrella de colores

```logo
CS
; Cada punta en un color diferente
SETPC [255 0 0]
FD 80 RT 144
SETPC [255 165 0]
FD 80 RT 144
SETPC [255 255 0]
FD 80 RT 144
SETPC [0 200 0]
FD 80 RT 144
SETPC [0 0 255]
FD 80 RT 144
```

---

## 📋 Resumen de comandos del Módulo 2

| Comando | Forma corta | ¿Qué hace? |
|---------|-------------|-----------|
| `SETPENCOLOR [r g b]` | `SETPC [r g b]` | Cambia el color del lápiz |
| `SETPENWIDTH n` | — | Cambia el grosor del lápiz |
| `SETBACKGROUND [r g b]` | `SETBG [r g b]` | Cambia el color del fondo |
| `HIDETURTLE` | `HT` | Esconde la tortuga |
| `SHOWTURTLE` | `ST` | Muestra la tortuga |

---

## 🧠 ¿Lo entendiste todo?

1. ¿Qué código RGB da el color amarillo?
2. Si quieres dibujar un hexágono, ¿cuántos grados giras en cada esquina?
3. ¿Qué comando usas para hacer el lápiz más grueso?
4. ¿Cómo haces un círculo aproximado en Logo?

---

➡️ **Siguiente:** `Modulo_02_Logo_Figuras_Colores/actividades.md`
