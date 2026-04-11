##  ESP32 Xiao Zhi AI Desktop Gadget

## **How it works**

<img width="1402" height="1121" alt="How Xiaozhi works" src="https://github.com/user-attachments/assets/3e38e701-fd90-414d-84be-a43e6bda5d56" />


---
This project doesn't run AI directly on the ESP32. Instead, it uses cloud-based processing, which is why even a small board can act like a smart assistant.

**The working flow:**

1. You speak into the microphone
2. The ESP32 records your voice using I2S audio input
3. It sends that audio over WiFi to the Xiaozhi cloud
4. On the cloud side:
   - Your voice is converted into text (Speech-to-Text)
   - The AI model understands it and generates a reply
   - That reply is converted back into voice (Text-to-Speech)
5. The audio response is sent back to the ESP32
6. The ESP32 plays it through the speaker

**The ESP32 handles:**
- Recording and playing audio
- Connecting to WiFi
- Managing the device

**The actual AI thinking happens in the cloud.**

---
## Breadboard Version (for prototyping)

| Component | Description |
|-----------|-------------|
| ESP32 DevKit Module | Main development board |
| INMP441 | Digital I2S microphone |
| MAX98357A | I2S audio amplifier |
| Speaker | 4Ω–8Ω, 2–3W |
| OLED Display | SSD1306, 0.91" or 0.96" |
| Push button | For interaction |
| Breadboard + jumper wires | For prototyping |

---
## Understanding the Hardware

Both the microphone and speaker use the **I2S interface**, making this a clean, all-digital audio system.

## ESP32 DevKit V1 Pinout

![esp32-devkit-v1-pinout](https://github.com/user-attachments/assets/6cfe4b95-652d-44ec-a14e-292e0571fd55)



---
## Circuit daigram 
<img width="1138" height="947" alt="Screenshot 2026-04-08 170613" src="https://github.com/user-attachments/assets/9ed5ddbf-57d7-43fa-89fa-19a2511b06d0" />
