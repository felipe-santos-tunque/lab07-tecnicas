# Bitacora de tecnicas avanzadas

Laboratorio 07: Tecnicas Avanzadas de Prompting.
Herramienta de IA usada: (escribe aqui cual usaste)

## Ejercicio 2: Zero-shot, one-shot y few-shot

| Tipo | Aciertos (de 5) | Formato de la respuesta | Todas con el mismo formato (Si/No) |
|------|:-----------------:|:-------------------------:|:------------------------------------:|
| Zero-shot |Sí |Extensa, con explicación |No |
| One-shot | Sí| Concisa, aunque con emojis y mas estilizadas las flechas| No|
| Few-shot | Sí| Exactamente igual a los ejemplo| Sí|


## Ejercicio 3: Chain of Thought
| Pedido | Respuesta de la IA | Muestra los pasos (Si/No) | Correcta (Si/No) |
|:--------:|:--------------------:|:---------------------------:|:------------------:|
| Directo |318.60 | No| Sí|
| Paso a paso | 318.60|Sí |Sí |

## Ejercicio 4: Role prompting
| Version | Vocabulario (sencillo/tecnico) | Usa ejemplos o codigo | A quien le sirve mas |
|:---------|:-------------------------------:|:-----------------------:|:----------------------:|
| A. Sin rol | Sencillo |No |A una persona con cierto conocimiento |
| B. Rol docente |Tecnico |Poco |A alguien que quiere aprender |
| C. Rol senior | Tecnico|Bastante |A alguien en formación profesional |

## Ejercicio 5: Descomposicion
- Paso 1: entrega los requisitos para la creación de un sistema de inventario
- Paso 2: Crea dos clases con sus atributos
- Paso 3: Entrega el código de la clase Producto con su explicación y el código para crear instancias de esa clase. 
- Paso 4: Propone 3 mejoras, con sus codigos y ejemplos de uso. 
## Ejercicio 6: Prompt estructurado y autocritica
| Qué revisar | Cumple (Sí / No) | 
|:---------|:-------------------------------:|
| ¿Tiene las 4 columnas pedidas? | Sí |
| ¿Incluye el bloqueo después de 3 intentos? |Sí |
| ¿Incluye casos con campos vacíos? | Sí|
| ¿Indica qué casos agregó en la autocrítica? | Sí|
| ¿Hay algún caso repetido o que no tenga sentido?| No|
Prompt estrucuturado: 
```text
<rol>Actua como analista de pruebas de software.</rol>

<contexto>Login web con correo y contrasena. La cuenta se bloquea

despues de 3 intentos fallidos.</contexto>

<tarea>Piensa paso a paso que puede fallar y escribe 6 casos de prueba.</tarea>

<formato>Tabla con las columnas: ID, escenario, datos de entrada,
  resultado esperado.</formato>
```
Mensaje de autocrítica:
```text
Revisa tu   tabla: faltan casos limite como campos vacios, correo sin @ o   contrasena con espacios? Agrega los que falten e indica cuales agregaste.
```
