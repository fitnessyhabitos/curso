# 🎯 Módulo 2 – Actividades: Figuras, Colores y Ángulos

## Actividad 2.1 – El semáforo (⭐ Fácil)

**Objetivo:** Dibujar un semáforo con tres círculos de colores.

Un semáforo tiene:
- Marco gris
- Círculo rojo arriba
- Círculo amarillo en el centro
- Círculo verde abajo

```logo
CS
SETBACKGROUND [200 200 200]

; Marco del semáforo (rectángulo gris oscuro)
SETPC [80 80 80]
SETPENWIDTH 5
FD 120
RT 90
FD 60
RT 90
FD 120
RT 90
FD 60
RT 90

; Círculo rojo (arriba)
PU
FD 20
RT 90
FD 30
LT 90
PD
SETPC [255 0 0]
REPEAT 360 [FD 0.5 RT 1]

; Añade tú los círculos amarillo y verde
; Pista: mueve con PU/PD hacia la posición correcta
```

### ✍️ Tu turno:
Completa el semáforo añadiendo:
1. El círculo amarillo (en el centro)
2. El círculo verde (abajo)

---

## Actividad 2.2 – El arcoíris (⭐⭐ Medio)

**Objetivo:** Dibujar los colores del arcoíris con líneas de colores.

Un arcoíris tiene 7 colores: rojo, naranja, amarillo, verde, azul, índigo, violeta.

```logo
CS
SETBACKGROUND [135 206 235]   ; cielo azul

; Línea roja
SETPC [255 0 0]
SETPENWIDTH 8
FD 200

; Línea naranja
PU
LT 90
FD 10
RT 90
PD
SETPC [255 165 0]
FD 200
```

### ✍️ Tu turno:
Continúa el arcoíris con los 5 colores restantes:
- Amarillo: [255, 255, 0]
- Verde: [0, 200, 0]
- Azul: [0, 0, 255]
- Índigo: [75, 0, 130]
- Violeta: [148, 0, 211]

---

## Actividad 2.3 – Los polígonos mágicos (⭐⭐ Medio)

**Objetivo:** Dibujar el cuadrado de polígonos (de triángulo a octágono).

Dibuja estos polígonos, cada uno de un color diferente:

```logo
CS

; TRIÁNGULO (rojo)
SETPC [255 0 0]
SETPENWIDTH 3
FD 80 RT 120
FD 80 RT 120
FD 80 RT 120

; Muévete a la derecha para el siguiente
PU
RT 90
FD 120
LT 90
PD

; CUADRADO (naranja) - Complétalo tú
SETPC [255 165 0]
; ... escribe el código aquí

; Muévete a la derecha
PU
RT 90
FD 120
LT 90
PD

; PENTÁGONO (amarillo) - Complétalo tú
; Recuerda: 360/5 = 72 grados
SETPC [255 255 0]
; ... escribe el código aquí
```

### ✍️ Tu turno:
Completa el código para dibujar también:
- Cuadrado (naranja)
- Pentágono (amarillo)
- Hexágono (verde)
- Octágono (azul)

---

## Actividad 2.4 – El sol y el cielo (⭐⭐ Medio)

**Objetivo:** Dibujar una escena con sol, cielo y montañas.

```logo
CS
SETBACKGROUND [135 206 235]   ; cielo azul

; El sol (círculo amarillo)
SETPC [255 255 0]
SETPENWIDTH 4
HT
REPEAT 360 [FD 0.3 RT 1]

; Los rayos del sol (líneas desde el centro)
SETPC [255 165 0]
PU
HOME
PD
FD 60
PU HOME PD
RT 45 FD 60
PU HOME PD
RT 90 FD 60
PU HOME PD
RT 135 FD 60
PU HOME PD
RT 180 FD 60
PU HOME PD
RT 225 FD 60
PU HOME PD
RT 270 FD 60
PU HOME PD
RT 315 FD 60
```

### ✍️ Tu turno:
Añade al dibujo:
1. Unas montañas en la parte inferior (triángulos verdes/grises)
2. Unas nubes (círculos blancos superpuestos)

---

## Actividad 2.5 – La bandera de España (⭐⭐⭐ Difícil)

**Objetivo:** Dibujar una bandera de colores.

La bandera española tiene tres franjas horizontales: roja, amarilla, roja.
- Franja roja: 40 de alto
- Franja amarilla: 80 de alto (el doble)
- Total: 160 de alto, 240 de ancho

```logo
CS

; Franja roja superior
SETPC [198 0 0]
SETPENWIDTH 1
; Necesitas dibujar un rectángulo relleno
; Pista: dibuja líneas muy juntas para simular relleno

; Una técnica para rellenar: dibujar muchas líneas horizontales
REPEAT 40 [FD 240 PU BK 240 RT 90 FD 1 LT 90 PD]
```

**Pista para rellenar:** Logo no tiene un fill fácil para rectángulos. La técnica es:
1. Dibujar una línea horizontal
2. Mover un paso hacia abajo
3. Volver al inicio de la fila
4. Repetir

### ✍️ Tu turno:
Dibuja las tres franjas de la bandera española con los colores correctos.

---

## Actividad 2.6 – RETO: El mandala de colores (⭐⭐⭐⭐ Muy difícil)

**Objetivo:** Crear un mandala sencillo con círculos concéntricos de colores.

Un mandala es un diseño circular y simétrico. Empieza con círculos:

```logo
CS
HT

; Círculo 1 - morado, pequeño
SETPC [128 0 128]
SETPENWIDTH 5
REPEAT 360 [FD 0.3 RT 1]

; Círculo 2 - azul, mediano
SETPC [0 0 255]
REPEAT 360 [FD 0.6 RT 1]

; Círculo 3 - verde
SETPC [0 200 0]
REPEAT 360 [FD 0.9 RT 1]

; Círculo 4 - amarillo
SETPC [255 255 0]
REPEAT 360 [FD 1.2 RT 1]

; Círculo 5 - rojo
SETPC [255 0 0]
REPEAT 360 [FD 1.5 RT 1]
```

### ✍️ Tu turno:
Añade más círculos y además añade "pétalos" entre los círculos:
- Un pétalo es un arco pequeño que va y vuelve
- Puedes añadir 8 pétalos alrededor del mandala

---

## 📝 Evaluación del Módulo 2

Para considerar terminado este módulo, debes poder:

- [ ] Cambiar el color del lápiz con SETPC
- [ ] Cambiar el grosor del lápiz con SETPENWIDTH
- [ ] Cambiar el fondo con SETBACKGROUND
- [ ] Dibujar un círculo con REPEAT 360
- [ ] Calcular el ángulo de cualquier polígono regular (360/n)
- [ ] Esconder y mostrar la tortuga

---

💾 **Guarda tu trabajo** en: `modulo2_ejercicios.lgo`

---

➡️ **Siguiente:** `Modulo_03_Logo_Repeticion_Procedimientos/teoria.md`
