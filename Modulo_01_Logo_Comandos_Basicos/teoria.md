# 📖 Módulo 1 – Logo: ¡Mueve la Tortuga!

## 🐢 Conoce a tu tortuga

Cuando abres Logo, verás una pantalla con una pequeña **tortuga** en el centro (a veces parece un triángulo). Esta tortuga es tu artista: le darás órdenes y ella las cumplirá dibujando en la pantalla.

```
        ▲
       /|\       ← Esta es tu tortuga (mirando hacia arriba)
      / | \
     /  |  \
```

La tortuga siempre:
- Empieza en el **centro** de la pantalla
- Mira hacia **arriba** (el norte)
- Lleva un lápiz que puede estar **bajado** (dibuja) o **subido** (no dibuja)

---

## 📝 Tu primer comando: FORWARD

El comando más importante en Logo es **FORWARD** (que significa "adelante" en inglés). Le dice a la tortuga cuántos pasos debe avanzar.

### Sintaxis:
```logo
FORWARD 100
```
También puedes escribirlo de forma corta:
```logo
FD 100
```

**¿Qué hace?** La tortuga avanza 100 pasos hacia adelante y dibuja una línea.

### Prueba esto:
```logo
FD 100
```
Deberías ver una línea recta.

---

## 🔙 El opuesto: BACK

**BACK** (o **BK**) hace que la tortuga retroceda.

```logo
BACK 50
```
```logo
BK 50
```

La tortuga se mueve hacia atrás sin girar, como si caminara de espaldas.

---

## 🔄 Los giros: RIGHT y LEFT

Para girar la tortuga usamos **RIGHT** y **LEFT** con el número de **grados** que queremos girar.

```logo
RIGHT 90    ← Gira 90 grados a la derecha (un cuarto de vuelta)
LEFT 45     ← Gira 45 grados a la izquierda
```

Formas cortas: **RT** y **LT**

```logo
RT 90
LT 45
```

### 🎯 Los grados más importantes

| Grados | ¿Qué es? |
|--------|----------|
| 90° | Un cuarto de vuelta (esquina de un cuadrado) |
| 180° | Media vuelta (dar la vuelta completamente) |
| 360° | Una vuelta completa (volver al mismo lugar) |
| 120° | Un tercio de vuelta (ángulo de un triángulo equilátero) |
| 45° | Un octavo de vuelta (diagonal) |

### Visualización de giros:

```
  Norte (0°)
      ↑
      |
Oeste ←───→ Este
      |
      ↓
  Sur (180°)

RT 90 → giras hacia el Este
LT 90 → giras hacia el Oeste
```

---

## ✏️ El lápiz: PENUP y PENDOWN

La tortuga siempre lleva un lápiz. Puedes subirlo o bajarlo.

```logo
PENUP       ← Sube el lápiz: la tortuga se mueve SIN dibujar
PU          ← Forma corta

PENDOWN     ← Baja el lápiz: la tortuga dibuja
PD          ← Forma corta
```

### Ejemplo:
```logo
FD 50       ← Dibuja una línea de 50
PU          ← Sube el lápiz
FD 30       ← Se mueve 30 sin dibujar (salto)
PD          ← Baja el lápiz
FD 50       ← Dibuja otra línea de 50
```
¡Obtendrás dos líneas separadas!

---

## 🏠 Volver al inicio: HOME y CLEARSCREEN

```logo
HOME        ← La tortuga vuelve al centro sin borrar lo dibujado
CLEARSCREEN ← Borra todo y vuelve al inicio (forma corta: CS)
```

---

## 🔤 Las mayúsculas y minúsculas en Logo

En Logo, no importa si escribes en mayúsculas o minúsculas. Estas tres instrucciones hacen exactamente lo mismo:

```logo
FORWARD 100
forward 100
Forward 100
```

Por costumbre, en este curso usaremos **mayúsculas** para los comandos de Logo.

---

## 🟥 Dibujando tu primer cuadrado

Un cuadrado tiene **4 lados iguales** y **4 ángulos de 90 grados**. Para dibujarlo:

1. Avanza 100
2. Gira 90° a la derecha
3. Avanza 100
4. Gira 90° a la derecha
5. Avanza 100
6. Gira 90° a la derecha
7. Avanza 100

### En código Logo:
```logo
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
FD 100
```

O si queremos cerrarlo completamente, añadimos un giro final:
```logo
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
```

---

## 🔺 Dibujando tu primer triángulo

Un triángulo equilátero tiene 3 lados iguales. El ángulo **exterior** que gira la tortuga es de **120°** (no 60°).

> 💡 **Truco:** Para calcular el ángulo de giro exterior de cualquier polígono regular, usa: **360 / número de lados**
> - Cuadrado: 360 / 4 = **90°**
> - Triángulo: 360 / 3 = **120°**
> - Pentágono: 360 / 5 = **72°**

```logo
FD 100
RT 120
FD 100
RT 120
FD 100
RT 120
```

---

## 📋 Resumen de comandos del Módulo 1

| Comando | Forma corta | ¿Qué hace? |
|---------|-------------|-----------|
| `FORWARD n` | `FD n` | Avanza n pasos |
| `BACK n` | `BK n` | Retrocede n pasos |
| `RIGHT n` | `RT n` | Gira n grados a la derecha |
| `LEFT n` | `LT n` | Gira n grados a la izquierda |
| `PENUP` | `PU` | Sube el lápiz (no dibuja) |
| `PENDOWN` | `PD` | Baja el lápiz (dibuja) |
| `HOME` | — | Vuelve al centro |
| `CLEARSCREEN` | `CS` | Borra la pantalla |

---

## 🧠 ¿Lo entendiste todo?

Antes de ir a las actividades, responde estas preguntas:

1. Si la tortuga mira hacia el norte y escribes `RT 90`, ¿hacia dónde mirará?
2. ¿Cuántos `FD` y `RT` necesitas para dibujar un cuadrado?
3. ¿Cuántos grados gira la tortuga al dibujar un triángulo equilátero?
4. ¿Qué comando usas para que la tortuga se mueva sin dibujar?

---

➡️ **Siguiente:** `Modulo_01_Logo_Comandos_Basicos/actividades.md`
