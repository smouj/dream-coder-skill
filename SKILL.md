name: Dream Coder
description: A specialized skill for translating abstract dream narratives into executable, functional code across multiple programming languages, focusing on surreal and imaginative implementations.
tags: [dreams, code, surreal, automation, generative-coding]
version: 1.2.0
author: OpenClaw Team
license: MIT
dependencies:
  - python3 (>=3.8)
  - openai-api (>=1.0.0)
  - surrealdb (>=1.0.0)
  - requests (>=2.25.0)
  - dotenv (>=1.0.0)
environment_variables:
  - DREAM_CODER_API_KEY: OpenAI API key for dream interpretation
  - DREAM_CODER_DB_URL: SurrealDB connection URL (e.g., ws://localhost:8000/rpc)
  - DREAM_CODER_MODEL: AI model to use (default: gpt-4-turbo)
  - DREAM_CODER_LOG_LEVEL: Logging verbosity (DEBUG, INFO, WARN, ERROR)
requirements:
  - Active internet connection for API calls
  - SurrealDB instance running for dream storage
  - Python virtual environment recommended
---

# Dream Coder Skill

## Purpose

Dream Coder transforms abstract, surreal dream descriptions into production-ready code. It specializes in creating innovative software solutions inspired by subconscious narratives, bridging the gap between creative dreaming and practical programming. Real use cases include:

- **Surreal UI Components**: Generate React components that mimic dream-like interactions, such as floating elements that morph based on user emotions.
- **Automated Dream Journals**: Build Python scripts that parse and categorize dream entries, integrating with ML models to predict recurring themes.
- **Fantasy Game Mechanics**: Create game logic in Unity/C# that implements dream physics, like gravity-defying movements or time-warping abilities.
- **Data Visualization Dreams**: Develop D3.js charts that visualize dream data as evolving fractals, with animations representing emotional intensity.
- **AI-Powered Story Generators**: Construct Node.js APIs that turn dream fragments into coherent narratives, using NLP to fill logical gaps.

## Scope

Dream Coder handles dream-to-code translation with specific commands:

- `dream-coder translate <dream-text>`: Converts a dream description into code snippets.
- `dream-coder generate --lang python --type script <dream-text>`: Generates a full script in specified language.
- `dream-coder surrealize --output surreal.json <dream-text>`: Extracts surreal elements and stores them in a JSON structure.
- `dream-coder integrate --framework react --dream-id 123`: Integrates dream-inspired code into an existing project.
- `dream-coder visualize --format svg <dream-text>`: Creates visual representations of dream code structures.
- `dream-coder optimize --dream-id 456 --metric performance`: Refines generated code for specific metrics.

## Detailed Work Process

1. **Dream Ingestion**: Parse the user's dream text using NLP to identify key elements (characters, settings, actions, emotions).
2. **Surreal Mapping**: Map abstract concepts to programming constructs (e.g., "flying" → asynchronous functions, "morphing" → polymorphism).
3. **Code Generation**: Use AI models to produce initial code drafts in the target language, ensuring syntax validity.
4. **Integration Check**: Verify compatibility with existing codebase using static analysis tools.
5. **Surreal Enhancement**: Add creative twists like randomized behaviors or dream-logic conditionals.
6. **Testing Simulation**: Run unit tests on generated code to simulate dream scenarios.
7. **Output Refinement**: Iterate on code based on AI feedback for readability and efficiency.
8. **Documentation**: Generate inline comments explaining the dream-inspired logic.

## Golden Rules

- **Never Generate Harmful Code**: Ensure all outputs avoid malicious patterns, even if the dream suggests them (e.g., redirect "nightmare" elements to safe simulations).
- **Preserve Dream Essence**: Maintain the original dream's surreal nature without over-simplifying to mundane code.
- **Respect User Privacy**: Never store or share dream content beyond the session; use encrypted local storage.
- **Prioritize Functionality**: Generated code must compile and run without errors, prioritizing execution over perfect dream fidelity.
- **Iterative Refinement**: Always offer follow-up commands for tweaking, as dreams evolve.
- **Ethical AI Use**: Limit API calls to prevent overuse; cache surreal mappings for efficiency.
- **Language Agnosticism**: Support translation to any major language (Python, JavaScript, Java, etc.) without bias.

## Examples

### Example 1: Basic Translation
**Input Prompt**: `dream-coder translate "I dreamt of a tree that whispered secrets to passing clouds, growing fruit that sang lullabies."`

**Output**:
```python
import random

class WhisperingTree:
    def __init__(self):
        self.secrets = ["The wind carries forgotten melodies", "Roots remember ancient dances"]
    
    def whisper_to_cloud(self, cloud):
        secret = random.choice(self.secrets)
        cloud.absorb(secret)
        print(f"Tree whispers: {secret}")
    
    def grow_singing_fruit(self):
        fruit = SingingFruit()
        self.fruits.append(fruit)
        return fruit

class SingingFruit:
    def sing_lullaby(self):
        lullabies = ["Hush now, dream softly", "Stars are watching over you"]
        return random.choice(lullabies)
```

### Example 2: Full Script Generation
**Input Prompt**: `dream-coder generate --lang javascript --type web-app "A dream where buttons on a webpage rearranged themselves based on the user's heartbeat."`

**Output Structure**:
- Creates `heartbeat-dream-app.js` with WebSocket for heartbeat monitoring.
- Includes CSS for dynamic button positioning.
- Deploys a local server via Express, listening on port 3001.

**Sample Code Snippet**:
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

### Example 3: Surreal Extraction
**Input Prompt**: `dream-coder surrealize --output dream-elements.json "In my dream, time flowed backwards while I painted with invisible colors."`

**Output JSON**:
```json
{
  "elements": [
    {"type": "time", "behavior": "reverse", "code_analogy": "for loop decrementing"},
    {"type": "painting", "material": "invisible", "code_analogy": "transparent canvas API"},
    {"type": "emotion": "confusion", "code_analogy": "randomized state mutations"}
  ],
  "generated_code": "time_reversal.py"
}
```

## Rollback Commands

- `dream-coder rollback --dream-id 123`: Reverts the last generated code for a specific dream, restoring previous version from SurrealDB.
- `dream-coder purge --all`: Deletes all generated code and dream data, resetting the skill state.
- `dream-coder undo-integration --framework react --component DreamButton`: Removes integrated dream code from the specified framework/component.
- `dream-coder reset-cache`: Clears cached surreal mappings, forcing fresh AI generations.

## Verification Steps

1. **Syntax Check**: Run `python -m py_compile generated_script.py` or equivalent for the target language.
2. **Unit Test Execution**: Use `pytest test_dream_code.py` to validate dream logic simulations.
3. **Integration Test**: Deploy locally with `npm start` and check for runtime errors in surreal behaviors.
4. **API Validation**: Confirm OpenAI responses via `curl -X POST https://api.openai.com/v1/chat/completions -H "Authorization: Bearer $DREAM_CODER_API_KEY"`.
5. **Database Health**: Query SurrealDB with `surreal sql --conn $DREAM_CODER_DB_URL "SELECT * FROM dreams;"`.

## Troubleshooting

- **API Rate Limits**: If "Rate limit exceeded" error, increase delays between calls or upgrade API plan.
- **Dream Parsing Failures**: For vague dreams, add `--verbose` flag to see NLP breakdowns and manually adjust inputs.
- **Code Compilation Errors**: Check environment variables; ensure dependencies are installed via `pip install -r requirements.txt`.
- **SurrealDB Connection Issues**: Verify DB URL with `ping $DREAM_CODER_DB_URL`; restart SurrealDB if unresponsive.
- **Memory Overload**: For large dreams, use `--chunk-size 500` to process in segments.
- **Inconsistent Outputs**: Set `DREAM_CODER_MODEL=gpt-3.5-turbo` for faster, less creative generations.