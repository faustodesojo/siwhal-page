---
name: creador-habilidades
description: Crea, actualiza y mejora habilidades de agente en idioma español. Utiliza esta habilidad cuando el usuario te pida crear o modificar una habilidad en español.
risk: low
---

# Creador de Habilidades (Skill Writer en Español)

Esta habilidad debe utilizarse como el flujo de trabajo principal para la creación y mejora de habilidades (skills) dentro del entorno de trabajo, operando exclusivamente en idioma español. Su propósito es asegurar que las habilidades generadas sigan las mejores prácticas y estructura de Antigravity.

## Pasos para crear o actualizar una habilidad:

### Paso 1: Comprender el objetivo
1. Identifica qué tipo de habilidad quiere crear el usuario (ej. documentación, automatización, seguridad, etc.).
2. Si los requisitos son ambiguos, haz una pregunta directa al usuario antes de continuar.

### Paso 2: Definir la estructura
1. Crea una carpeta para la nueva habilidad. Si es local al proyecto, guárdala en `.gemini/skills/nombre-de-habilidad/`.
2. Todo el contenido principal debe ir en un archivo llamado `SKILL.md`.
3. Utiliza YAML frontmatter al inicio del archivo `SKILL.md` con los siguientes campos requeridos:
   - `name`: (obligatorio) nombre de la habilidad en minúsculas y con guiones.
   - `description`: (obligatorio) descripción clara y orientada a la acción.

Ejemplo de Frontmatter:
```yaml
---
name: nombre-de-la-habilidad
description: Breve descripción de 1 o 2 oraciones sobre lo que hace y cuándo invocarla.
---
```

### Paso 3: Redactar el contenido de SKILL.md
1. **Título Principal:** Usa un `# Título` descriptivo.
2. **Contexto/Objetivo:** Escribe un párrafo breve explicando el propósito de la habilidad.
3. **Instrucciones paso a paso:** Redacta instrucciones en modo imperativo (ej. "Usa esta herramienta para...", "Valida los datos antes de...").
4. **Reglas estrictas:** Define límites claros de lo que el agente NO debe hacer.
5. **Formato de salida:** Especifica exactamente cómo quieres que el agente devuelva la información al usuario.

### Paso 4: Optimizar la descripción
Asegúrate de que el campo `description` del frontmatter contenga palabras clave exactas de cuándo el sistema de enrutamiento debería activar esta habilidad. Mientras más precisa sea la descripción, mejor sabrá el agente principal cuándo usarla.

### Paso 5: Validar
Revisa que el archivo `SKILL.md` contenga el frontmatter correcto y que todas las instrucciones estén completamente en español.

## Reglas de esta habilidad:
- Todo el código o documentación generada debe estar en español (salvo palabras clave de código o librerías).
- Mantén las instrucciones claras y directas para evitar ambigüedades en la interpretación del agente.
