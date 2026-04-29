1"}
# ESP32-S3 Voice Assistant (Waveshare ESP32-S3-AUDIO)

This project turns the Waveshare ESP32-S3-AUDIO board into a fully working voice assistant using ESPHome and Home Assistant.

✅ Microphones and speaker are already built-in  
✅ No wiring needed  
⚠️ Board comes EMPTY – this is normal (not plug & play)

---

## 🧰 What you need

- Waveshare ESP32-S3-AUDIO board
- USB cable (DATA cable)
- Computer
- Home Assistant installed

---

## ⚙️ Step 1: Install ESPHome

In Home Assistant:

Settings → Add-ons → ESPHome → Install → Start

---

## 🔌 Step 2: Connect the board

- Plug the ESP32 into your computer via USB
- Wait a few seconds

---

## ➕ Step 3: Create device in ESPHome

- Click "New Device"
- Name it (example: voice-esp)
- Select board: ESP32-S3

---

## 📄 Step 4: Upload config

- Open the YAML file ESPHome created
- DELETE everything inside
- Copy everything from:

👉 voice_assistant.yaml (this repo)

- Paste it there

---

## 📡 Step 5: Set WiFi

Find this section:

wifi:
  ssid: "YOUR_WIFI_SSID"
  password: "YOUR_WIFI_PASSWORD"

Replace with your WiFi credentials.

---

## 🔐 Step 6: API encryption key (IMPORTANT)

⚠️ This step is REQUIRED

In ESPHome:
- Click Install → Manual download
- ESPHome will generate an API key

Replace this line in YAML:

api:
  encryption:
    key: "YOUR_KEY"

---

## 🚀 Step 7: Flash firmware

Click:

Install → Plug into this computer

Wait until upload finishes.

---

## 🏠 Step 8: Add to Home Assistant

- Device will appear automatically
- Click "Add"

---

## 🎤 How to use

This config uses Push-To-Talk (PTT):

- Press the button → start speaking  
- Release / stop → assistant responds  

(No wake word enabled by default)

---

## 💡 Features included

- 🎤 Built-in microphones (ES7210)
- 🔊 Built-in speaker (ES8311)
- 🔘 Push-to-talk buttons
- 💡 LED ring with status effects:
  - Listening
  - Thinking
  - Speaking
  - Error
- 🔊 Volume control from Home Assistant

---

## ❗ Important

This is NOT a defective product.

ESP32 boards always come blank and must be programmed.

---

## 🛠 Troubleshooting

- Not detected → use a DATA USB cable
- No sound → check volume in Home Assistant
- No connection → check WiFi credentials
- No response → make sure Home Assistant Assist is configured

---

## 👍 If this helped

Leave a helpful Thanks, Bogdan!
