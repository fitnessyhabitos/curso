# 📖 Módulo 3 – Logo: Repetición y Procedimientos

## ⚠️ El problema de copiar y pegar

Hasta ahora, para dibujar un cuadrado escribías esto:
```logo
FD 100
RT 90
FD 100
RT 90
FD 100
RT 90
FD 100
```

¿Y si quisieras dibujar 10 cuadrados? ¿Copiar esto 10 veces? ¡Eso sería muy aburrido!

Los programadores somos "vagos" inteligentes: **si hay que hacer algo repetido, ¡hacemos que el ordenador lo repita por nosotros!**

---

## 🔄 El comando REPEAT

**REPEAT** le dice a Logo: "repite estos comandos tantas veces".

### Sintaxis:
```logo
REPEAT número_de_veces [comandos que se repiten]
```

### Ejemplo: cuadrado con REPEAT
```logo
REPEAT 4 [FD 100 RT 90]
```
¡Esto hace exactamente lo mismo que escribir FD 100 RT 90 cuatro veces! Solo en 1 línea.

### Ejemplo: triángulo con REPEAT
```logo
REPEAT 3 [FD 100 RT 120]
```

### Ejemplo: círculo con REPEAT
```logo
REPEAT 360 [FD 1 RT 1]
```

### Ejemplo: espiral con REPEAT
```logo
REPEAT 100 [FD 5 RT 91]
```
¡Prueba esto! Verás algo sorprendente.

---

## 🌀 Patrones con REPEAT

REPEAT es muy poderoso para crear patrones:

### Flor:
```logo
CS
REPEAT 36 [REPEAT 4 [FD 50 RT 90] RT 10]
```
Repite un cuadrado 36 veces, girando 10° entre cada uno. ¡El resultado es una flor!

### Espiral cuadrada:
```logo
CS
REPEAT 20 [FD 10 RT 91]
REPEAT 20 [FD 30 RT 91]
REPEAT 20 [FD 60 RT 91]
```

### Rueda de rayos:
```logo
CS
REPEAT 12 [FD 80 BK 80 RT 30]
```

---

## 📦 Procedimientos: crea tus propios comandos

Los **procedimientos** son como enseñarle a Logo palabras nuevas. Puedes definir tu propio comando y luego usarlo las veces que quieras.

### Sintaxis:
```logo
TO nombre_del_procedimiento
  ; comandos que forman el procedimiento
END
```

### Ejemplo: procedimiento CUADRADO
```logo
TO CUADRADO
  REPEAT 4 [FD 100 RT 90]
END
```

Ahora, cada vez que escribas `CUADRADO`, la tortuga dibujará un cuadrado de 100.

### Usar el procedimiento:
```logo
CUADRADO          ← Dibuja un cuadrado
PU FD 120 PD
CUADRADO          ← Dibuja otro cuadrado
```

---

## 📦 Procedimientos con parámetros

¿Y si quieres cuadrados de distintos tamaños? Usamos **parámetros** (también llamados variables).

```logo
TO CUADRADO :LADO
  REPEAT 4 [FD :LADO RT 90]
END
```

El `:LADO` es una variable. Cuando llamas al procedimiento, le pasas el valor:
```logo
CUADRADO 50    ← Cuadrado pequeño (lado=50)
CUADRADO 100   ← Cuadrado mediano (lado=100)
CUADRADO 200   ← Cuadrado grande (lado=200)
```

> 💡 **¡Importante!** En Logo, los parámetros llevan dos puntos `:` delante del nombre.

### Procedimiento POLIGONO con lados y ángulo:
```logo
TO POLIGONO :LADOS :TAMANO
  REPEAT :LADOS [FD :TAMANO RT 360 / :LADOS]
END
```

Ahora puedes dibujar cualquier polígono:
```logo
POLIGONO 3 80    ← Triángulo de lado 80
POLIGONO 4 80    ← Cuadrado de lado 80
POLIGONO 6 80    ← Hexágono de lado 80
POLIGONO 8 80    ← Octágono de lado 80
```

---

## 🏗️ Procedimientos que usan otros procedimientos

Lo genial es que un procedimiento puede llamar a otro procedimiento:

```logo
TO CUADRADO :LADO
  REPEAT 4 [FD :LADO RT 90]
END

TO FLOR_CUADRADA :TAMANO :PETALES
  REPEAT :PETALES [CUADRADO :TAMANO RT 360 / :PETALES]
END
```

Ahora:
```logo
FLOR_CUADRADA 80 12    ← Flor con 12 pétalos cuadrados de tamaño 80
```

---

## 🌟 Ejemplo completo: Galaxia de estrellas

```logo
TO ESTRELLA :TAMANO
  REPEAT 5 [FD :TAMANO RT 144]
END

TO GALAXIA
  CS
  HT
  SETPC [255 255 0]
  REPEAT 8 [ESTRELLA 50 RT 45]
END

GALAXIA
```

---

## 💡 Buenas prácticas al escribir procedimientos

1. **Nombres descriptivos:** `CUADRADO` es mejor que `C`
2. **Un procedimiento, una tarea:** cada procedimiento hace solo una cosa
3. **Parámetros para flexibilidad:** si un tamaño puede variar, hazlo parámetro
4. **Comenta tu código:** usa `;` para explicar qué hace cada parte

---

## 📋 Resumen del Módulo 3

| Concepto | Sintaxis | Ejemplo |
|----------|---------|---------|
| Repetir n veces | `REPEAT n [comandos]` | `REPEAT 4 [FD 100 RT 90]` |
| Definir procedimiento | `TO nombre ... END` | `TO CUADRADO ... END` |
| Parámetro | `:nombre` | `TO CUADRADO :LADO` |
| Llamar procedimiento | `nombre` | `CUADRADO` |
| Proc. con parámetro | `nombre valor` | `CUADRADO 100` |

---

## 🧠 ¿Lo entendiste?

1. ¿Qué escribe un programador para no repetir código?
2. Escribe el código para dibujar un hexágono usando REPEAT
3. ¿Qué diferencia hay entre `FD 100` y `:LADO`?
4. ¿Puedes un procedimiento llamar a otro procedimiento?

---

➡️ **Siguiente:** `Modulo_03_Logo_Repeticion_Procedimientos/actividades.md`
