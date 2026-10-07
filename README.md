# 🎙️ ESP32-S3 AI Voice Chatbot

A compact AI voice assistant built around the **ESP32-S3** microcontroller. It captures your voice through a microphone, processes the audio with an AI model, and responds through an OLED display and a speaker.

This repository contains the project and its documentation site.

---

## 📖 Overview

The system combines audio input, wireless connectivity, AI inference, display output, and voice playback in one small device:

1. You speak to the device.
2. The microphone captures the audio and sends it to the ESP32-S3.
3. The ESP32-S3 processes the input and passes it to the AI model.
4. The AI generates a response.
5. The OLED shows status or text, and the speaker plays the answer.

Wi-Fi/BLE provides the wireless connectivity for network access, communication, and updates.

## 🧩 Hardware Components

| Component       | Part                   | Purpose                                                             |
| --------------- | ---------------------- | ------------------------------------------------------------------- |
| 🎙️ Microphone   | MSM261D / INMP441      | Captures sound and provides audio input to the ESP32-S3             |
| 🧠 Controller   | ESP32-S3               | Handles audio data, AI model logic, and peripheral control          |
| 📡 Wireless     | Wi-Fi / BLE            | Network access, communication, updates, and data                    |
| 🤖 AI Model     | DeepSeek / Local AI    | Runs inference and processes voice input and responses              |
| 🖥️ Display      | OLED (I²C / SPI)       | Shows system status, text responses, or audio waveforms             |
| 🔊 Audio Output | MAX98357 + 8 Ω speaker | The amplifier boosts the ESP32-S3 audio signal to drive the speaker |

You will also need Dupont jumper cables, a breadboard, and a sensor breakout board for connections and expansion.

## 🛠️ System Architecture

```
🎙️ Microphone → ESP32-S3 → AI Model → OLED → MAX98357 → 🔊 Speaker
  Voice input    Processing  Inference  Text/status  Audio     Response
```

## 🔧 Hardware Assembly

1. **Connect the microphone**: wire the audio input module to the ESP32-S3.
2. **Connect the OLED**: use the appropriate I²C/SPI connections for visual output.
3. **Connect the amplifier**: connect the MAX98357 between the controller and the speaker.
4. **Complete the wiring**: use Dupont jumper cables and the sensor breakout board for connections and expansion.

> 📷 **Add your circuit diagram and breadboard photo here** (for example in `docs/images/`).

## ▶️ Usage

**Example workflow:** Speak → microphone captures audio → ESP32-S3 processes input → AI generates response → OLED displays information → speaker plays the response.

> 🎬 **Add a demo video or screenshots here.**

## 📚 Documentation Site

The project documentation is a single, self-contained HTML page with no build step and no dependencies.

**Run it locally:**

```bash
# Option 1: open the file directly in your browser
open index.html

# Option 2: serve it locally
python3 -m http.server 8000
# then visit http://localhost:8000
```

**Features:**

- Sidebar navigation with collapsible sections
- "On this page" table of contents with scroll tracking
- Light/dark theme toggle
- Search box (press `Ctrl + K` to focus, `Enter` to jump to the first match)
- Responsive layout with a mobile menu
- Language selector (English / ខ្មែរ / 中文): currently the UI only, translations are not yet implemented

## 📁 Project Structure

```
.
├── index.html        # Documentation site
├── README.md
└── docs/
    └── images/       # Circuit diagram, breadboard photo, demo media
```

Adjust this to match your actual repository layout (add `firmware/`, `hardware/`, etc. as needed).

## 🗺️ Roadmap

- [ ] Add the circuit diagram and breadboard photos
- [ ] Add the demo video or screenshots
- [ ] Add firmware setup and flashing instructions
- [ ] Add wiring tables with pin assignments
- [ ] Complete the Khmer and Chinese translations of the docs

## 👥 Team

| Member      | Role / Responsibility |
| ----------- | --------------------- |
| Member Name | Role / Responsibility |
| Member Name | Role / Responsibility |
| Member Name | Role / Responsibility |
| Member Name | Role / Responsibility |

## 📄 License

Add your license here (for example, MIT).
