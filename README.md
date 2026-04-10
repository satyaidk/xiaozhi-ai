##  ESP32 Xiao Zhi AI Desk Assitant
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

## Circuit daigram 
<img width="1138" height="947" alt="Screenshot 2026-04-08 170613" src="https://github.com/user-attachments/assets/9ed5ddbf-57d7-43fa-89fa-19a2511b06d0" />
