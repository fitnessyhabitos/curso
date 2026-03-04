# 🎯 Módulo 3 – Actividades: Repetición y Procedimientos

## Actividad 3.1 – REPEAT básico (⭐ Fácil)

**Objetivo:** Usar REPEAT para dibujar figuras sin repetir código.

### Ejercicio 1: Reescribe con REPEAT

Transforma estas instrucciones largas usando REPEAT:

**Original (largo):**
```logo
FD 80
RT 90
FD 80
RT 90
FD 80
RT 90
FD 80
RT 90
```

**Con REPEAT (corto):** (escríbelo tú)
```logo
REPEAT __ [__ __ __ __]
```

### Ejercicio 2: Hexágono
Dibuja un hexágono de lado 70 usando REPEAT (360/6 = 60 grados):
```logo
CS
REPEAT __ [FD 70 RT __]
```

### Ejercicio 3: Octágono
Dibuja un octágono de lado 50 (360/8 = 45 grados):
```logo
CS
REPEAT __ [FD 50 RT __]
```

---

## Actividad 3.2 – Patrones con REPEAT (⭐⭐ Medio)

**Objetivo:** Crear patrones artísticos con REPEAT anidado.

### La espiral cuadrada:
```logo
CS
HT
SETPC [0 0 255]
SETPENWIDTH 2
REPEAT 50 [FD 5 RT 89]
```
Prueba cambiando el 89 por 91, por 92, por 88. ¿Qué ocurre?

### La flor de cuadrados:
```logo
CS
HT
SETPC [255 0 128]
REPEAT 12 [REPEAT 4 [FD 60 RT 90] RT 30]
```

### ✍️ Tu turno: La flor de triángulos
Modifica el código de la flor de cuadrados para que use triángulos en vez de cuadrados:
- En vez de `REPEAT 4 [FD 60 RT 90]` usa `REPEAT 3 [FD 60 RT 120]`
- Cambia también los colores

### ✍️ Tu turno: La espiral de colores
Crea una espiral donde el color cambie cada vuelta:
```logo
CS
HT
SETPC [255 0 0]
REPEAT 30 [FD 5 RT 91]
SETPC [0 0 255]
REPEAT 30 [FD 8 RT 91]
SETPC [0 200 0]
REPEAT 30 [FD 11 RT 91]
```

---

## Actividad 3.3 – Mis primeros procedimientos (⭐⭐ Medio)

**Objetivo:** Definir y usar procedimientos propios.

### Paso 1: Define el procedimiento CUADRADO

En el editor de FMSLogo (o en el área de código), escribe:
```logo
TO CUADRADO
  REPEAT 4 [FD 100 RT 90]
END
```

Luego ejecuta:
```logo
CS
CUADRADO
```

### Paso 2: Define TRIANGULO

```logo
TO TRIANGULO
  REPEAT 3 [FD 100 RT 120]
END
```

### Paso 3: Define CIRCULO (aproximado)
```logo
TO CIRCULO
  REPEAT 36 [FD 5 RT 10]
END
```

### Paso 4: ¡Úsalos juntos!

```logo
CS
CUADRADO
PU FD 50 RT 90 FD 50 LT 90 PD
TRIANGULO
PU FD 150 PD
CIRCULO
```

### ✍️ Tu turno: Define ESTRELLA
Crea un procedimiento llamado ESTRELLA que dibuje una estrella de 5 puntas.
- Pista: REPEAT 5 [FD 80 RT 144]

---

## Actividad 3.4 – Procedimientos con parámetros (⭐⭐ Medio)

**Objetivo:** Hacer procedimientos flexibles con parámetros.

### El cuadrado flexible:
```logo
TO CUADRADO :LADO
  REPEAT 4 [FD :LADO RT 90]
END
```

Prueba:
```logo
CS
CUADRADO 40
PU FD 60 PD
CUADRADO 70
PU FD 100 PD
CUADRADO 100
```

### ✍️ Tu turno: Completa estos procedimientos

**Procedimiento RECTANGULO:**
```logo
TO RECTANGULO :ANCHO :ALTO
  FD :ALTO
  RT 90
  FD :ANCHO
  RT 90
  FD :ALTO
  RT 90
  FD :ANCHO
  RT 90
END
```

Llámalo con:
```logo
RECTANGULO 150 80
```

**Procedimiento ESTRELLA con parámetro:**
```logo
TO ESTRELLA :TAMANO
  REPEAT 5 [FD :TAMANO RT 144]
END
```

Llámalo con:
```logo
ESTRELLA 50
ESTRELLA 80
ESTRELLA 120
```

---

## Actividad 3.5 – La ciudad de figuras (⭐⭐⭐ Difícil)

**Objetivo:** Construir una escena usando procedimientos.

Primero define todos los procedimientos que necesitarás:

```logo
; Procedimiento: edificio
TO EDIFICIO :ANCHO :ALTO
  REPEAT 2 [FD :ALTO RT 90 FD :ANCHO RT 90]
END

; Procedimiento: ventana
TO VENTANA
  REPEAT 4 [FD 15 RT 90]
END

; Procedimiento: puerta
TO PUERTA
  FD 30 RT 90 FD 20 RT 90 FD 30
END
```

### ✍️ Tu turno: La ciudad

Usando los procedimientos anteriores, crea una ciudad con al menos 3 edificios de distintos tamaños. Añade ventanas y puertas.

```logo
CS
SETBACKGROUND [50 100 200]   ; noche azul
SETPC [200 200 200]          ; edificios grises

; Edificio 1
PU SETPOS [-150 -80] PD
EDIFICIO 60 150

; Edificio 2 - ¡tú lo haces!

; Edificio 3 - ¡tú lo haces!
```

---

## Actividad 3.6 – RETO: El copo de nieve (⭐⭐⭐⭐ Muy difícil)

**Objetivo:** Crear un copo de nieve fractal usando procedimientos.

El copo de nieve se basa en repetir la misma forma a diferentes escalas.

```logo
TO RAMA :LONGITUD
  IF :LONGITUD < 5 [STOP]
  FD :LONGITUD
  RT 30
  RAMA :LONGITUD / 2
  LT 60
  RAMA :LONGITUD / 2
  RT 30
  BK :LONGITUD
END

CS
HT
SETPC [200 220 255]
SETBACKGROUND [0 0 50]
RAMA 80
```

> ⚠️ Este ejercicio usa recursividad (un procedimiento que se llama a sí mismo). ¡Es avanzado pero muy bonito!

### ✍️ Experimenta:
- Cambia el número `80` por otros valores
- Cambia el `5` del `IF :LONGITUD < 5` por `10` o `2`
- Cambia los ángulos `30` y `60`

---

## 📝 Evaluación del Módulo 3

Para considerar terminado este módulo, debes poder:

- [ ] Usar REPEAT para dibujar cualquier polígono
- [ ] Crear patrones con REPEAT anidado
- [ ] Definir un procedimiento simple con TO...END
- [ ] Definir procedimientos con parámetros (`:variable`)
- [ ] Llamar a procedimientos desde otros procedimientos

---

💾 **Guarda tu trabajo** en: `modulo3_procedimientos.lgo`

---

➡️ **Siguiente:** `Modulo_04_Proyecto_Logo/`
