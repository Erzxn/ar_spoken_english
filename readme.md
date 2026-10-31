# 🌐 CyberSpoken AR - Next-Gen Pronunciation Lab

เว็บแอปพลิเคชันเกมฝึกออกเสียงคำศัพท์เทคโนโลยีและไอทีภาษาอังกฤษ (20 คำ) ในรูปแบบ **Cyberpunk / Holographic AR HUD** ด้วยระบบตรวจจับเสียงพูดจริงผ่านไมโครโฟน (Web Speech Recognition API) และกล้องเว็บแคมสำหรับแสดงเอฟเฟกต์ AR Biometric Scanner

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-Single--File-orange.svg)
![TailwindCSS](https://img.shields.io/badge/TailwindCSS-v3-38bdf8.svg)
![WebSpeechAPI](https://img.shields.io/badge/API-Web_Speech_Recognition-green.svg)

---

## ⚡ ฟีเจอร์เด่น (Key Features)

- **Cyberpunk Hologram HUD Design:** ส่วนติดต่อผู้ใช้ออกแบบในสไตล์ Sci-Fi Dark Mode ตกแต่งด้วยเส้น Neon Cyan, Matrix Emerald, Cyber Grid และ Radar Biometric Reticle
- **3-Second Preparation Buffer:** ระบบนับเวลาถอยหลังเตรียมตัว 3 วินาที (3... 2... 1...) ก่อนเปิดรับเสียงในทุกข้อ เพื่อให้ผู้เล่นได้สังเกตคำศัพท์และคำแปล
- **Live Voice Recognition & Levenshtein Matching:** ตรวจจับเสียงพูดภาษาอังกฤษเปรียบเทียบกับคำศัพท์เป้าหมาย คำนวณเปอร์เซ็นต์ความแม่นยำ (Accuracy %) แบบเรียลไทม์
- **Fail & Pass Auto Skip:** 
  - หากพูดถูกต้อง ($\ge 75\%$): ขึ้นสถานะ **"ผ่าน!"** และจุดพลุ Confetti ฉลอง พร้อมบันทึกคะแนน
  - หากพูดไม่ผ่านหรือหมดเวลา: ขึ้นแจ้งเตือน **"เสียงคุณไม่ได้"** ด้วยแถบสีแดงและเสียงแจ้งเตือน จากนั้นจะข้ามไปข้อถัดไปอัตโนมัติ
- **Text-to-Speech (TTS):** มีปุ่มลำโพงสำหรับกดฟังตัวอย่างสำเนียงที่ถูกต้องได้ทุกคำ
- **Single-File Architecture:** โค้ดทั้งหมดรวมอยู่ในไฟล์ `index.html` เพียงไฟล์เดียว ใช้งานได้ทันทีโดยไม่ต้อง Build หรือลง Package เสริม

---

## 🎮 กติกาการเล่น (Gameplay Rules)

1. เมื่อเริ่มข้อใหม่ ระบบจะนับถอยหลัง **3 วินาที** สำหรับเตรียมตัว (ไมโครโฟนยังปิดอยู่)
2. เมื่อครบ 3 วินาที สถานะจะเปลี่ยนเป็น `SPEAK NOW` ให้พูดออกเสียงตามคำศัพท์ที่ปรากฏ
3. หากออกเสียงถูกต้องและแม่นยำ จะได้คะแนนสะสมและผ่านไปข้อถัดไป
4. หากพูดไม่ชัด สำเนียงไม่ถูกต้อง หรือไม่พูดภายในเวลา ระบบจะเตือนว่า **"เสียงคุณไม่ได้"** และสลับข้อถัดไปให้อัตโนมัติ

---

## 🚀 วิธีการเปิดใช้งานบน GitHub Pages

โปรเจกต์นี้พร้อมเผยแพร่ผ่าน **GitHub Pages** ได้ทันทีโดยมีขั้นตอนดังนี้:

1. นำไฟล์ `index.html` และ `README.md` อัปโหลดขึ้น Repository บน GitHub
2. ไปที่แท็บ **Settings** ของ Repository
3. ในเมนูด้านซ้าย เลือกหัวข้อ **Pages**
4. ภายใต้หมวด **Build and deployment**:
   - **Source:** เลือก `Deploy from a branch`
   - **Branch:** เลือก `main` (หรือ `master`) และโฟลเดอร์เป็น `/(root)`
5. กด **Save** รอประมาณ 1-2 นาที คุณจะได้ URL สำหรับเล่นเกมทันที เช่น:
   ```
   https://<your-username>.github.io/<repository-name>/
   ```

> **หมายเหตุ:** เบราว์เซอร์จำเป็นต้องรันผ่านโปรโตคอล `https://` หรือ `localhost` เพื่อให้สิทธิ์การใช้งานกล้องเว็บแคมและ Web Speech API ทำงานได้อย่างสมบูรณ์ (แนะนำให้เปิดเล่นผ่าน Google Chrome หรือ Microsoft Edge)

---

## 🛠️ เทคโนโลยีที่ใช้ (Tech Stack)

- **Frontend:** HTML5, CSS3, JavaScript (ES6+)
- **Styling:** Tailwind CSS (CDN), Font Awesome Icons, Google Fonts (`Orbitron`, `Bai Jamjuree`)
- **Audio & Speech:** Web Speech API (`SpeechRecognition`), Web Speech Synthesis (`SpeechSynthesisUtterance`), Web Audio API (Synthesizer Beeps)
- **Effects:** Canvas Confetti

---

## 📄 ใบอนุญาต (License)

โปรเจกต์นี้เผยแพร่ภายใต้สัญญาอนุญาต [MIT License](LICENSE) สามารถนำไปพัฒนาต่อยอดเพื่อการศึกษาได้อิสระ