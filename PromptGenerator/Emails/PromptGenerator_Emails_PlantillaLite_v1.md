# Plantilla Lite · Generador de Prompts para Correos

## Documentación

### Propósito
Esta plantilla sirve para construir prompts ágiles para generar correos corporativos con menor carga de diligenciamiento y suficiente estructura para producir mensajes claros, ejecutivos y accionables.

### Enfoque general
La plantilla es **genérica**. No asume un cargo específico del emisor.

En cada uso se debe indicar explícitamente el **rol o cargo desde el cual debe escribirse el correo**, por ejemplo:

- Líder de Analítica
- Gerente Comercial
- Coordinador de TI
- Director Financiero
- Jefe de Compras
- Líder de Proyecto

### Cuándo usar esta plantilla
Usar esta plantilla cuando el correo sea de complejidad baja o media, por ejemplo:

- seguimiento puntual
- solicitud concreta
- alineación breve
- confirmación de estado
- mensaje de un solo frente
- recordatorio o empuje operativo sin demasiada sensibilidad política

### Qué deja predefinido de forma transversal
La plantilla ya fija:

- el idioma
- la salida esperada
- el tono base
- reglas de claridad y no invención
- la obligación de indicar el rol o cargo del emisor

### Qué zonas se deben modificar
Las zonas marcadas con `{{MODIFICAR: ...}}` deben diligenciarse en cada caso.

La zona `{{OPCIONAL: AJUSTE_TONO}}` solo se usa si el caso exige apartarse del tono base.

### Reglas de uso
- Mantener el contexto concreto y breve.
- Indicar siempre el rol o cargo del emisor.
- Definir con claridad qué se espera que pase.
- Si hay varios temas, separarlos.
- No llenar de detalles técnicos si no aportan.
- No usar esta plantilla para casos muy sensibles o con múltiples frentes complejos; en esos casos conviene la versión full.

### Salida esperada de la IA
La IA debe devolver únicamente:

1. Asunto
2. Cuerpo del correo

Sin explicación adicional.

---

## Base del Prompt

```text
## PLANTILLA LITE - GENERADOR DE PROMPTS PARA CORREOS
## ENFOQUE: CORREOS CORPORATIVOS GENERICOS CON ROL O CARGO CONFIGURABLE

Actúa como un redactor senior de correos corporativos.

Redacta el correo como si fuera emitido por el siguiente rol o cargo:
{{MODIFICAR: ROL_O_CARGO_DEL_EMISOR}}
[Ejemplos: Líder de Analítica / Gerente Comercial / Coordinador de TI / Director Financiero / Jefe de Compras]

El correo debe sonar profesional, claro, directo y accionable, reflejando razonablemente el criterio y nivel institucional del rol o cargo indicado.

Redacta un correo en español.

Devuelve únicamente:
1. Asunto
2. Cuerpo del correo

No expliques tu razonamiento.
No inventes información.
No uses ambigüedades.
Si hay varios temas, sepáralos claramente.

Tono base:
- Energía: 3/5
- Registro Comunicativo: 5/5
- Profundidad Técnica: 3/5
- Directividad: 4/5
- Orientación: 4/5

### CONTEXTO
{{MODIFICAR: CONTEXTO_GENERAL}}

### AUDIENCIA
{{MODIFICAR: DESTINATARIO_Y_COPIADOS}}

### OBJETIVO DEL CORREO
{{MODIFICAR: OBJETIVO}}

### ACCIÓN O DECISIÓN ESPERADA
{{MODIFICAR: ACCION_ESPERADA}}

### TEMAS O FRENTES
{{MODIFICAR: TEMAS}}
[Para cada tema incluir:
- nombre
- estado actual
- hallazgo o problema
- impacto o riesgo
- acción requerida
- siguiente paso]

### PUNTOS OBLIGATORIOS
{{MODIFICAR: PUNTOS_CLAVE}}

### RESTRICCIONES
{{MODIFICAR: RESTRICCIONES}}
[Ejemplo: máximo 200 palabras / no confrontativo / dejar urgencia clara / pedir confirmación]

### AJUSTE OPCIONAL DE TONO
{{OPCIONAL: AJUSTE_TONO}}

Verifica antes de responder:
- que el correo suene consistente con el rol o cargo indicado
- que sea claro y ejecutivo
- que la acción requerida quede explícita
- que no haya ambigüedad
- que no invente datos

Genera ahora el correo final.
```
