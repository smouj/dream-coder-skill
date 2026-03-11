name: Dream Coder
description: Una habilidad especializada para traducir narrativas de sueños abstractos en código ejecutable y funcional en múltiples lenguajes de programación, enfocándose en implementaciones surrealistas e imaginativas.
tags: [sueños, código, surreal, automatización, generación-de-código]
version: 1.2.0
author: Equipo OpenClaw
license: MIT
dependencies:
  - python3 (>=3.8)
  - openai-api (>=1.0.0)
  - surrealdb (>=1.0.0)
  - requests (>=2.25.0)
  - dotenv (>=1.0.0)
environment_variables:
  - DREAM_CODER_API_KEY: Clave de API de OpenAI para interpretación de sueños
  - DREAM_CODER_DB_URL: URL de conexión de SurrealDB (ej. ws://localhost:8000/rpc)
  - DREAM_CODER_MODEL: Modelo de IA a usar (por defecto: gpt-4-turbo)
  - DREAM_CODER_LOG_LEVEL: Nivel de verbosidad de logging (DEBUG, INFO, WARN, ERROR)
requirements:
  - Conexión activa a internet para llamadas API
  - Instancia de SurrealDB ejecutándose para almacenamiento de sueños
  - Entorno virtual de Python recomendado
---

# Habilidad Dream Coder

## Propósito

Dream Coder transforma descripciones de sueños abstractos y surrealistas en código listo para producción. Se especializa en crear soluciones de software innovadoras inspiradas en narrativas subconscientes, puenteando la brecha entre el sueño creativo y la programación práctica. Casos de uso reales incluyen:

- **Componentes UI Surrealistas**: Generar componentes React que imitan interacciones oníricas, como elementos flotantes que se transforman basados en emociones del usuario.
- **Diarios de Sueños Automatizados**: Construir scripts Python que analizan y categorizan entradas de sueños, integrándose con modelos ML para predecir temas recurrentes.
- **Mecánicas de Juegos de Fantasía**: Crear lógica de juego en Unity/C# que implementa física de sueños, como movimientos que desafían la gravedad o habilidades de distorsión temporal.
- **Sueños de Visualización de Datos**: Desarrollar gráficos D3.js que visualizan datos de sueños como fractales en evolución, con animaciones que representan intensidad emocional.
- **Generadores de Historias con IA**: Construir APIs Node.js que convierten fragmentos de sueños en narrativas coherentes, usando NLP para llenar brechas lógicas.

## Alcance

Dream Coder maneja traducción de sueños a código con comandos específicos:

- `dream-coder translate <dream-text>`: Convierte una descripción de sueño en fragmentos de código.
- `dream-coder generate --lang python --type script <dream-text>`: Genera un script completo en el lenguaje especificado.
- `dream-coder surrealize --output surreal.json <dream-text>`: Extrae elementos surrealistas y los almacena en una estructura JSON.
- `dream-coder integrate --framework react --dream-id 123`: Integra código inspirado en sueños en un proyecto existente.
- `dream-coder visualize --format svg <dream-text>`: Crea representaciones visuales de estructuras de código de sueños.
- `dream-coder optimize --dream-id 456 --metric performance`: Refina código generado para métricas específicas.

## Proceso de Trabajo Detallado

1. **Ingesta de Sueños**: Analizar el texto de sueño del usuario usando NLP para identificar elementos clave (personajes, escenarios, acciones, emociones).
2. **Mapeo Surreal**: Mapear conceptos abstractos a construcciones de programación (ej. \"volar\" → funciones asíncronas, \"transformar\" → polimorfismo).
3. **Generación de Código**: Usar modelos de IA para producir borradores iniciales de código en el lenguaje objetivo, asegurando validez sintáctica.
4. **Verificación de Integración**: Verificar compatibilidad con el código base existente usando herramientas de análisis estático.
5. **Mejora Surreal**: Añadir giros creativos como comportamientos aleatorios o condicionales de lógica de sueños.
6. **Simulación de Pruebas**: Ejecutar pruebas unitarias en el código generado para simular escenarios de sueños.
7. **Refinamiento de Salida**: Iterar en el código basado en retroalimentación de IA para legibilidad y eficiencia.
8. **Documentación**: Generar comentarios en línea explicando la lógica inspirada en sueños.

## Reglas de Oro

- **Nunca Generar Código Dañino**: Asegurar que todas las salidas eviten patrones maliciosos, incluso si el sueño los sugiere (ej. redirigir elementos \"pesadilla\" a simulaciones seguras).
- **Preservar Esencia del Sueño**: Mantener la naturaleza surreal del sueño original sin simplificar excesivamente a código mundano.
- **Respetar Privacidad del Usuario**: Nunca almacenar o compartir contenido de sueños más allá de la sesión; usar almacenamiento local encriptado.
- **Priorizar Funcionalidad**: El código generado debe compilar y ejecutar sin errores, priorizando ejecución sobre fidelidad perfecta al sueño.
- **Refinamiento Iterativo**: Siempre ofrecer comandos de seguimiento para ajustes, ya que los sueños evolucionan.
- **Uso Ético de IA**: Limitar llamadas API para prevenir abuso; cachear mapeos surrealistas para eficiencia.
- **Agnosticismo de Lenguaje**: Soportar traducción a cualquier lenguaje mayor (Python, JavaScript, Java, etc.) sin sesgos.

## Ejemplos

### Ejemplo 1: Traducción Básica
**Entrada Prompt**: `dream-coder translate \"Soñé con un árbol que susurraba secretos a nubes pasajeras, creciendo fruta que cantaba nanas.\"`

**Salida**:
```python
import random

class WhisperingTree:
    def __init__(self):
        self.secrets = [\"The wind carries forgotten melodies\", \"Roots remember ancient dances\"]
    
    def whisper_to_cloud(self, cloud):
        secret = random.choice(self.secrets)
        cloud.absorb(secret)
        print(f\"Tree whispers: {secret}\")
    
    def grow_singing_fruit(self):
        fruit = SingingFruit()
        self.fruits.append(fruit)
        return fruit

class SingingFruit:
    def sing_lullaby(self):
        lullabies = [\"Hush now, dream softly\", \"Stars are watching over you\"]
        return random.choice(lullabies)
```

### Ejemplo 2: Generación de Script Completo
**Entrada Prompt**: `dream-coder generate --lang javascript --type web-app \"Un sueño donde botones en una página web se reordenaban solos basados en el latido del corazón del usuario.\"`

**Estructura de Salida**:
- Crea `heartbeat-dream-app.js` con WebSocket para monitoreo de latidos.
- Incluye CSS para posicionamiento dinámico de botones.
- Despliega un servidor local vía Express, escuchando en puerto 3001.

**Fragmento de Código de Muestra**:
```javascript
const express = require('express');
const app = express();
const WebSocket = require('ws');

app.use(express.static('public'));

const wss = new WebSocket.Server({ port: 8080 });

wss.on('connection', (ws) => {
    ws.on('message', (heartbeat) => {
        // Rearrange buttons based on heartbeat rhythm
        rearrangeButtons(parseInt(heartbeat));
    });
});

function rearrangeButtons(rate) {
    const buttons = document.querySelectorAll('.dream-button');
    buttons.forEach(btn => {
        btn.style.transform = `translate(${Math.sin(rate / 100) * 50}px, ${Math.cos(rate / 100) * 50}px)`;
    });
}

app.listen(3001, () => console.log('Dream app running on port 3001'));
```

### Ejemplo 3: Extracción Surreal
**Entrada Prompt**: `dream-coder surrealize --output dream-elements.json \"En mi sueño, el tiempo fluía hacia atrás mientras pintaba con colores invisibles.\"`

**Salida JSON**:
```json
{
  \"elements\": [
    {\"type\": \"time\", \"behavior\": \"reverse\", \"code_analogy\": \"for loop decrementing\"},
    {\"type\": \"painting\", \"material\": \"invisible\", \"code_analogy\": \"transparent canvas API\"},
    {\"type\": \"emotion\": \"confusion\", \"code_analogy\": \"randomized state mutations\"}
  ],
  \"generated_code\": \"time_reversal.py\"
}
```

## Comandos de Retroceso

- `dream-coder rollback --dream-id 123`: Revierte el último código generado para un sueño específico, restaurando versión previa desde SurrealDB.
- `dream-coder purge --all`: Elimina todo el código generado y datos de sueños, reseteando el estado de la habilidad.
- `dream-coder undo-integration --framework react --component DreamButton`: Remueve código integrado de sueños del framework/componente especificado.
- `dream-coder reset-cache`: Limpia mapeos surrealistas en caché, forzando generaciones frescas de IA.

## Pasos de Verificación

1. **Verificación de Sintaxis**: Ejecutar `python -m py_compile generated_script.py` o equivalente para el lenguaje objetivo.
2. **Ejecución de Pruebas Unitarias**: Usar `pytest test_dream_code.py` para validar simulaciones de lógica de sueños.
3. **Prueba de Integración**: Desplegar localmente con `npm start` y verificar errores de runtime en comportamientos surrealistas.
4. **Validación de API**: Confirmar respuestas de OpenAI vía `curl -X POST https://api.openai.com/v1/chat/completions -H \"Authorization: Bearer $DREAM_CODER_API_KEY\"`.
5. **Salud de Base de Datos**: Consultar SurrealDB con `surreal sql --conn $DREAM_CODER_DB_URL \"SELECT * FROM dreams;\"`.

## Solución de Problemas

- **Límites de Tasa de API**: Si error \"Rate limit exceeded\", aumentar delays entre llamadas o actualizar plan de API.
- **Fallos en Análisis de Sueños**: Para sueños vagos, añadir flag `--verbose` para ver desgloses NLP y ajustar entradas manualmente.
- **Errores de Compilación de Código**: Verificar variables de entorno; asegurar dependencias instaladas vía `pip install -r requirements.txt`.
- **Problemas de Conexión SurrealDB**: Verificar URL de DB con `ping $DREAM_CODER_DB_URL`; reiniciar SurrealDB si no responde.
- **Sobrecarga de Memoria**: Para sueños grandes, usar `--chunk-size 500` para procesar en segmentos.
- **Salidas Inconsistentes**: Establecer `DREAM_CODER_MODEL=gpt-3.5-turbo` para generaciones más rápidas y menos creativas.```