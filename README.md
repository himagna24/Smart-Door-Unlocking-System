# 🔐 Smart Door Unlocking System

### 🧠 Project Overview  
This project demonstrates a **Smart Door Unlocking System** built using **Arduino** and **Java**.  
It provides a secure and automated way to control door access in restricted environments like **banks** and **corporate offices**.  
The system integrates hardware-based authentication (via sensors) with a Java-based software layer for real-time access verification.

---

## ⚙️ Tools & Technologies
- **Arduino UNO Board**
- **Java (JDK 17+)**
- **jSerialComm Library** for serial communication
- **Servo Motor** (for door lock)
- **RFID / Keypad Sensor**

---

## 🧩 System Working

1. The **Arduino** continuously monitors input from a **sensor** (RFID or keypad).
2. When a user requests access, Arduino sends a signal (`REQUEST_UNLOCK`) to the **Java application** through serial communication.
3. The **Java program** prompts the user for authentication (e.g., passcode).
4. If the credentials match, Java sends an `ACCESS_GRANTED` message to Arduino.
5. Arduino activates the **servo motor** to unlock the door.
6. If authentication fails, it remains locked and displays “Access Denied”.

---

## 🖥️ Project Architecture
Smart-Door-Unlocking-System/
├── Arduino/
│   └── SmartDoor.ino
│
├── JavaApp/
│   ├── src/
│   │   └── SmartDoorApp.java
│   ├── lib/
│   │   └── jSerialComm.jar

## 🚀 How to Run  

### 🧩 1️⃣ Hardware Setup  
- Connect the **sensor** to pin **7** and the **servo motor** to pin **9** on the **Arduino UNO**.  
- Connect the **Arduino board** to your PC via a **USB cable**.  

---

### ⚙️ 2️⃣ Arduino Code Upload  
- Open the `SmartDoor.ino` file in the **Arduino IDE**.  
- Select the correct **board** and **port** from the **Tools** menu.  
- Click on **Upload** to flash the code to your Arduino.  

---

### ☕ 3️⃣ Run Java Application  
- Add the `jSerialComm.jar` file to your **classpath**.  
- Open and run the `SmartDoorApp.java` file in your Java IDE or terminal.  
- When prompted, enter your **passcode** (default: `12345`).  

---

### 🔍 4️⃣ Observe  
- If authentication **succeeds**, the **servo motor unlocks** the door and the **LED turns ON**.  
- If authentication **fails**, the **door remains locked** and the LED indicates **Access Denied**.  
