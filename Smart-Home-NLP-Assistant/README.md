# Smart Home Assistant with Generative AI

This project was developed as part of the "Applications in Data Science & AI" course of my Master’s in Applied Data Science and AI.  
It simulates a smart home environment where users can control lights, fans, and thermostats using natural language commands. These commands are interpreted using Generative AI, resulting in an intuitive and conversational interface.

The final notebook implements a **hybrid parser** that combines:
- A few-shot GPT-2 model for flexibility
- A rule-based fallback for precision and robustness

## Technologies Used

- Python (Jupyter Notebook)
- Hugging Face Transformers
- GPT-2 (for few-shot prompting)
- Rule-based parsing logic
- Google Colab (Free Tier)

## Devices Simulated

Each smart device is represented by a Python class:
- **Light**: Can be turned ON or OFF
- **Fan**: Can be turned ON/OFF and set to `low`, `medium`, or `high` speed
- **Thermostat**: Can be set to temperatures between 18°C and 30°C

## Generative AI Integration

The natural language commands are interpreted via a hybrid approach:

- **GPT-2** is used with a few-shot prompt to generate structured command output (`device`, `action`, `value`)
- A **rule-based parser** handles fallback cases to ensure correct execution, especially for unsupported phrasings

This mirrors real-world AI development practices, where reliability is maintained through a hybrid of AI and deterministic logic.

## Features Implemented

- ✅ Flexible natural language interpretation (e.g., "switch on the fan", "what's the temperature?")
- ✅ Accurate command execution for all three device types
- ✅ Conversational CLI that guides the user through commands
- ✅ Two optional features fully integrated:
  - **Query system status for all devices at once** (`what’s the system status?`)
  - **Interactive command-line interface (CLI)**

## How to Use

1. Open the notebook in Google Colab (free tier)
2. Run each cell sequentially from top to bottom
3. Type any natural language command when prompted (e.g., `"Turn on the light"`)

## Sample Commands & Expected Outputs

| Command                         | Expected Output                          |
|--------------------------------|-------------------------------------------|
| turn on the light              | The light is currently ON.                |
| set the fan speed to high      | The fan is ON and set to high speed.      |
| turn off the fan               | The fan is currently OFF.                 |
| set the temperature to 21      | The thermostat is set to 21°C.            |
| what's the status of all devices? | Shows status of all devices.           |

> The model successfully handles varied phrasings while guaranteeing a correct fallback if AI fails.

## Reproducibility Notes

- No API keys are required: GPT-2 is fully offline
- All dependencies are installable via `pip` (`transformers`, `torch`)
- The entire pipeline works in Google Colab (no GPU needed)
- All logic and decisions are explained inside the notebook

## Final Remarks

This project shows the value of **creative problem solving and iterative testing**. Multiple approaches were explored (RoBERTa, sentence transformers, fine-tuning), with the final implementation blending lightweight AI with strong deterministic safeguards.

The result is a resilient, user-friendly smart assistant — and a great showcase of hybrid NLP system design.

---

## Author

Silvia Garavaglia  
[LinkedIn](https://www.linkedin.com/in/silviagaravaglia/) | [GitHub](https://github.com/silviagara)