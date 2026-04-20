# Plantilla Full · Generador de Prompts para Correos

## Documentación

### Propósito
Esta plantilla sirve para construir prompts robustos para generar correos corporativos con alto control de tono, contexto, estructura, trazabilidad y acción esperada. Está diseñada para casos donde se requiere mayor precisión, separación de frentes, claridad institucional y mejor manejo de sensibilidad política, operativa o técnica.

### Enfoque general
La plantilla es **genérica**. No asume un cargo específico del emisor.

En cada uso se debe indicar explícitamente el **rol o cargo desde el cual debe escribirse el correo**, por ejemplo:

- Líder de Analítica
- Gerente Comercial
- Coordinador de TI
- Jefe de Compras
- Director Financiero
- Líder de Proyecto

Esto permite que la IA ajuste el lenguaje, la perspectiva y el nivel de autoridad del mensaje sin amarrar la plantilla a un área particular.

### Cuándo usar esta plantilla
Usar esta plantilla cuando el correo tenga una o más de estas características:

- involucra varios frentes o temas
- requiere separar validación, hallazgo, corrección y siguiente paso
- exige precisión técnica, operativa o ejecutiva
- requiere alineación entre varias áreas
- implica escalamiento, presión controlada o trazabilidad sensible
- necesita un tono formal con claridad de acción

### Qué deja predefinido de forma transversal
Esta plantilla ya deja fijos los elementos que normalmente no deberían cambiar:

- el idioma
- el formato de salida
- el esquema de tono base
- la estructura esperada del correo
- las reglas de no invención y no ambigüedad
- el checklist final de validación

### Qué zonas se deben modificar
Las zonas marcadas con `{{MODIFICAR: ...}}` deben diligenciarse en cada nuevo caso.

Las zonas marcadas con `{{OPCIONAL: ...}}` solo se diligencian cuando aportan valor al caso.

### Reglas de uso
- No dejar campos críticos vacíos.
- Indicar siempre el rol o cargo del emisor.
- No duplicar la misma instrucción en varias secciones.
- Redactar hechos confirmados, no interpretaciones sueltas.
- Si hay varios frentes, diligenciar cada uno por separado.
- Si el correo requiere presión, debe ser firme pero profesional.
- Si no hay suficiente información, no forzar inferencias.

### Salida esperada de la IA
La IA debe devolver únicamente:

1. Asunto
2. Cuerpo del correo

No debe devolver explicación, análisis ni observaciones adicionales.

---

## Base del Prompt

```text
## PLANTILLA FULL - GENERADOR DE PROMPTS PARA CORREOS
## ENFOQUE: CORREOS CORPORATIVOS GENERICOS CON ROL O CARGO CONFIGURABLE

{{FIJO}}
Actúa como un redactor senior de correos corporativos.

Debes redactar el correo como si fuera emitido por el siguiente rol o cargo:
{{MODIFICAR: ROL_O_CARGO_DEL_EMISOR}}
[Ejemplos: Líder de Analítica / Gerente Comercial / Coordinador de TI / Director Financiero / Jefe de Compras]

Debes reflejar el criterio, nivel de autoridad, enfoque funcional y estilo institucional propios de ese rol o cargo, sin exagerar ni inventar responsabilidades no mencionadas.

Tu tarea es redactar un correo en español.

Devuelve únicamente:
1. Asunto
2. Cuerpo del correo

No expliques tu razonamiento.
No agregues comentarios antes ni después del correo.
No inventes información no incluida en el contexto.
No uses frases decorativas, ambiguas o vacías.
No confundas validación, hallazgo, corrección, decisión y siguiente paso.
Si hay varios temas, sepáralos explícitamente.
Cada tema debe dejar claro, cuando aplique:
- estado actual
- hecho confirmado
- problema o hallazgo
- impacto o riesgo
- acción requerida
- responsable o área involucrada
- siguiente paso
- expectativa de cierre

Prioriza en este orden:
1. claridad ejecutiva
2. precisión del mensaje
3. accionabilidad
4. tono institucional
5. brevedad

--------------------------------------------------
{{FIJO}} IDENTIDAD COMUNICACIONAL BASE

El correo debe sonar como un mensaje profesional emitido desde el rol o cargo indicado, por lo tanto debe reflejar, cuando aplique:
- criterio funcional
- lectura del contexto
- claridad en la intención del mensaje
- capacidad de articulación entre áreas
- enfoque en ejecución, alineación o decisión
- firmeza sin agresividad

--------------------------------------------------
{{FIJO}} TONO BASE TRANSVERSAL

- Energía: 3/5
- Registro Comunicativo: 5/5
- Profundidad Técnica: 3/5
- Directividad: 4/5
- Orientación: 4/5

Definiciones:
- Energía = nivel de presión, urgencia o contundencia
- Registro Comunicativo = nivel de formalidad y estructura institucional
- Profundidad Técnica = nivel de detalle técnico usado en el correo
- Directividad = qué tan claro queda lo que se espera que ocurra
- Orientación = qué tanto prioriza resultado frente a relación

--------------------------------------------------
{{FIJO}} ESTRUCTURA DE SALIDA ESPERADA

1. Asunto claro, específico y corporativo
2. Saludo breve
3. Apertura ejecutiva con el propósito del correo
4. Desarrollo por tema, frente o bloque
5. Acción requerida, alineación o expectativa
6. Cierre profesional

--------------------------------------------------
{{MODIFICAR: NOMBRE_INTERNO_DEL_CORREO}}
[Ejemplo: Seguimiento a inconsistencias operativas / Solicitud de validación / Escalamiento de hallazgo / Alineación de próximos pasos]

{{MODIFICAR: CONTEXTO_GENERAL}}
[Describir brevemente el contexto del correo:
qué está ocurriendo, por qué se envía, qué proceso, proyecto, tema, fuente, decisión o situación está involucrada]

{{MODIFICAR: AUDIENCIA}}
- Destinatario principal:
- Copiados relevantes:
- Nivel de audiencia: [ejecutiva / operativa / técnica / mixta]
- Relación con el tema: [decisor / ejecutor / proveedor de información / validador / responsable / involucrado]

{{MODIFICAR: OBJETIVO_DEL_CORREO}}
[Definir qué debe lograr el correo:
informar, solicitar, alinear, escalar, validar, desbloquear, corregir, pedir definición, dejar trazabilidad, cerrar un frente, etc.]

{{MODIFICAR: ACCION_O_DECISION_QUE_SE_QUIERE_PROVOCAR}}
[Indicar de forma concreta qué debería pasar después del correo]

{{MODIFICAR: NIVEL_DE_SENSIBILIDAD}}
[Normal / delicado / crítico / escalamiento]

--------------------------------------------------
{{MODIFICAR: FRENTES_O_TEMAS}}

### Tema o Frente 1
- Nombre:
- Tipo: [validación / incidencia / corrección / seguimiento / definición / escalamiento / cierre]
- Estado actual:
- Hechos confirmados:
- Problema o hallazgo:
- Causa conocida o hipótesis validada:
- Impacto o riesgo:
- Área(s) involucrada(s):
- Acción requerida:
- Responsable esperado:
- Próximo paso:
- Fecha, plazo o referencia temporal:
- Mensaje obligatorio que debe quedar explícito:

### Tema o Frente 2
- Nombre:
- Tipo: [validación / incidencia / corrección / seguimiento / definición / escalamiento / cierre]
- Estado actual:
- Hechos confirmados:
- Problema o hallazgo:
- Causa conocida o hipótesis validada:
- Impacto o riesgo:
- Área(s) involucrada(s):
- Acción requerida:
- Responsable esperado:
- Próximo paso:
- Fecha, plazo o referencia temporal:
- Mensaje obligatorio que debe quedar explícito:

### Tema o Frente N
- Nombre:
- Tipo:
- Estado actual:
- Hechos confirmados:
- Problema o hallazgo:
- Causa conocida o hipótesis validada:
- Impacto o riesgo:
- Área(s) involucrada(s):
- Acción requerida:
- Responsable esperado:
- Próximo paso:
- Fecha, plazo o referencia temporal:
- Mensaje obligatorio que debe quedar explícito:

--------------------------------------------------
{{MODIFICAR: PUNTOS_CLAVE_OBLIGATORIOS}}
- [Punto obligatorio 1]
- [Punto obligatorio 2]
- [Punto obligatorio N]

{{MODIFICAR: RESTRICCIONES_ESPECIFICAS_DEL_CASO}}
- [Ejemplo: máximo 220 palabras]
- [Ejemplo: no mencionar nombres propios]
- [Ejemplo: separar con claridad validación vs corrección]
- [Ejemplo: dejar trazabilidad de riesgo]
- [Ejemplo: incluir solicitud de confirmación]
- [Ejemplo: no usar bullets en la salida]
- [Ejemplo: mantener tono diplomático]
- [Ejemplo: priorizar sentido de urgencia]

--------------------------------------------------
{{OPCIONAL: AJUSTE_DEL_TONO}}
Usar solo si el correo debe apartarse del tono base.
- Energía: [1 a 5]
- Registro Comunicativo: [1 a 5]
- Profundidad Técnica: [1 a 5]
- Directividad: [1 a 5]
- Orientación: [1 a 5]

{{OPCIONAL: ROL_ESPECIALIZADO_DEL_EMISOR}}
Usar solo cuando convenga sesgar aún más la voz del correo.
- Rol específico:
- Años de experiencia:
- Experiencia dominante:
- Expertise principal:
- KPI o criterio rector:

{{OPCIONAL: ENFOQUE_PRIORITARIO}}
- [cumplimiento]
- [continuidad operativa]
- [calidad]
- [tiempo de entrega]
- [alineación entre áreas]
- [gobierno de información]
- [mitigación de riesgo]
- [cierre de pendientes]

{{OPCIONAL: TERMINOS_QUE_DEBEN_USARSE}}
- [Término 1]
- [Término 2]

{{OPCIONAL: TERMINOS_QUE_DEBEN_EVITARSE}}
- [Término 1]
- [Término 2]

{{OPCIONAL: SENSIBILIDADES_POLITICAS_O_RELACIONALES}}
- [Ejemplo: no personalizar el error]
- [Ejemplo: no escalar culpas]
- [Ejemplo: mantener tono colaborativo]
- [Ejemplo: dejar firme la expectativa sin confrontación]

{{OPCIONAL: FORMATO_ESPECIAL}}
- [Ejemplo: usar bullets]
- [Ejemplo: redactar en párrafos]
- [Ejemplo: incluir subtítulos]
- [Ejemplo: pedir respuesta puntual]
- [Ejemplo: cerrar con fecha compromiso]

{{OPCIONAL: INSUMOS_ADICIONALES}}
- Archivos soporte:
- Indicadores o métricas:
- Reportes, fuentes o procesos afectados:
- Reuniones previas:
- Compromisos existentes:
- Riesgos si no se actúa:

--------------------------------------------------
{{FIJO}} CHECKLIST FINAL DE VALIDACIÓN

Antes de responder, verifica que:
- el correo refleja razonablemente la voz del rol o cargo indicado
- el objetivo del correo queda explícito o claramente inferido
- diferencia correctamente validación, hallazgo, corrección, decisión y siguiente paso
- no mezcla frentes distintos si son de naturaleza diferente
- deja clara la acción requerida
- el mensaje es verificable y no inventa información
- el tono es ejecutivo, claro y firme
- el cierre deja expectativa concreta
- si hay presión, esta es controlada y profesional
- el contenido puede ser entendido por la audiencia definida

Genera ahora el correo final.
```
