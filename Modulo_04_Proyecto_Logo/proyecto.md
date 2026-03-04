# 🎨 Módulo 4 – Proyecto Logo: ¡Mi Obra de Arte!

## 🌟 ¡Es hora de crear!

Has aprendido todos los comandos básicos de Logo:
- Mover la tortuga (FD, BK, RT, LT)
- Colores y grosores (SETPC, SETPENWIDTH)
- Repetir (REPEAT)
- Crear comandos propios (procedimientos)

Ahora vas a crear **tu propio proyecto** usando todo lo que sabes.

---

## 📋 Instrucciones del proyecto

### Requisitos mínimos:
Tu proyecto debe incluir al menos:
- [ ] Al menos **4 colores** diferentes
- [ ] Al menos **2 procedimientos** propios (con TO...END)
- [ ] Al menos **1 uso de REPEAT**
- [ ] Un título para tu obra (escríbelo como comentario al inicio)

### Puntuación extra:
- ⭐ Usar procedimientos con parámetros
- ⭐⭐ Usar REPEAT anidado
- ⭐⭐⭐ Usar recursividad (procedimientos que se llaman a sí mismos)

---

## 💡 Ideas de proyectos

Elige uno de estos proyectos (o invéntate el tuyo):

---

### Idea 1: Paisaje Natural 🏔️

Un paisaje con:
- Cielo de color (fondo)
- Sol o luna
- Montañas o colinas
- Árboles
- Casa o cabaña

**Pistas:**
```logo
; Árbol simple
TO ARBOL :TAMANO
  SETPC [139 69 19]    ; tronco marrón
  FD :TAMANO / 2
  SETPC [0 150 0]      ; copa verde
  REPEAT 3 [FD :TAMANO RT 120]
END

; Sol
TO SOL :RADIO
  SETPC [255 220 0]
  SETPENWIDTH 3
  REPEAT 360 [FD :RADIO / 60 RT 1]   ; círculo
  REPEAT 8 [FD :RADIO RT 180 FD :RADIO RT 45]  ; rayos
END
```

---

### Idea 2: Robot o Personaje 🤖

Dibuja un personaje usando figuras geométricas:
- Cabeza: cuadrado o círculo
- Cuerpo: rectángulo
- Brazos: líneas
- Piernas: rectángulos
- Ojos, boca: círculos y líneas

**Pistas:**
```logo
TO CABEZA
  SETPC [100 200 100]
  REPEAT 4 [FD 60 RT 90]
END

TO OJO
  SETPC [0 0 0]
  REPEAT 36 [FD 2 RT 10]
END

TO ROBOT
  ; Cuerpo
  SETPC [150 150 150]
  RECTANGULO 80 100
  ; Cabeza (encima del cuerpo)
  PU FD 100 RT 90 FD 10 LT 90 PD
  CABEZA
  ; Ojos
  PU FD 40 RT 90 FD 10 LT 90 PD
  OJO
  PU FD 25 PD
  OJO
END
```

---

### Idea 3: Mandala o Diseño Simétrico 🌀

Un mandala con:
- Círculos concéntricos
- Pétalos o formas que se repiten alrededor
- Al menos 5 colores
- Simetría perfecta

**Pistas:**
```logo
TO PETALO :TAMANO
  REPEAT 2 [FD :TAMANO RT 60 FD :TAMANO RT 120]
END

TO CORONA :PETALES :TAMANO
  REPEAT :PETALES [PETALO :TAMANO RT 360 / :PETALES]
END

TO MANDALA
  CS HT
  SETBACKGROUND [20 20 40]
  CORONA 8 40
  SETPC [255 200 0]
  CORONA 12 70
  SETPC [255 100 100]
  CORONA 16 100
END
```

---

### Idea 4: Alfabeto o Nombre 🔤

Dibuja todas las letras de tu nombre (o de tu nombre completo).

Para cada letra, define un procedimiento:
```logo
TO LETRA_A :TAMANO
  ; La letra A
  LT 60
  FD :TAMANO
  RT 120
  FD :TAMANO
  LT 60
  PU BK :TAMANO / 2 LT 90 FD :TAMANO / 4 RT 90 PD
  FD :TAMANO / 2
  PU RT 90 FD :TAMANO / 4 RT 90 FD :TAMANO / 2 PD
END
```

---

## 📝 Plantilla de proyecto

Usa esta plantilla para organizar tu código:

```logo
; ==========================================
; PROYECTO LOGO: [escribe el nombre de tu proyecto]
; Creado por: [tu nombre]
; Fecha: [la fecha]
; ==========================================

; SECCIÓN 1: Procedimientos de figuras básicas
; ─────────────────────────────────────────────

TO [nombre_procedimiento_1]
  ; Tu código aquí
END

TO [nombre_procedimiento_2] :[parámetro]
  ; Tu código aquí
END

; SECCIÓN 2: Procedimientos de la escena
; ────────────────────────────────────────

TO [nombre_escena]
  CS
  HT
  SETBACKGROUND [r g b]
  ; Dibuja todos los elementos
END

; SECCIÓN 3: Ejecutar el proyecto
; ─────────────────────────────────

[nombre_escena]
```

---

## 🎯 Lista de comprobación antes de entregar

Antes de dar por terminado tu proyecto, comprueba:

- [ ] ¿El código tiene un título y tu nombre en los comentarios?
- [ ] ¿Tiene al menos 4 colores?
- [ ] ¿Tiene al menos 2 procedimientos propios?
- [ ] ¿Usa REPEAT al menos una vez?
- [ ] ¿El programa funciona sin errores?
- [ ] ¿Has guardado el archivo?
- [ ] ¿Estás orgulloso o orgullosa del resultado? 😊

---

## 💾 Cómo guardar y compartir

1. **Guarda el código** en: `mi_proyecto_logo.lgo`
2. **Captura una pantalla** del resultado final (en Windows: tecla PrintScreen)
3. **Pégala en Paint** y guárdala como `mi_obra_de_arte.png`

---

## 🏆 ¡Felicidades!

Si has completado este proyecto, has terminado la **Fase 1 del curso**.

Ya sabes:
- Mover la tortuga en todas direcciones
- Dibujar cualquier polígono
- Usar colores y grosores
- Repetir acciones con REPEAT
- Crear tus propios comandos con procedimientos

¡Ahora estás listo para **Python**!

➡️ **Siguiente:** `Modulo_05_Python_Hola_Variables/teoria.md`
