# ⏱️ JavaFX Presentation Timer

A simple and elegant **presentation timer** built with **JavaFX**.  
This project was developed as part of a software engineering assignment to help presenters manage and visualize their speaking time during a session.

---

## 🧩 Features

- ⏳ **Start / Pause / Reset** controls for flexible timing  
- 🎨 **Visual feedback** (color change or alert) when time is nearly up  
- 🖥️ **Clean JavaFX interface** defined in `view.fxml`  
- ⚙️ **MVC architecture** for structured code separation:
  - `Main.java` → launches the application  
  - `Controlleur.java` → handles UI logic and user events  
  - `Timer.java` → manages timing and countdown logic  

---

## 🛠️ Technologies

- Java 11 or higher  
- JavaFX SDK  

---

## 🚀 Getting Started

### 1. Clone the repository

bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

2. Compile the project
   
javac *.java

4. Run the application

java Main

Or, if you’re using an IDE like IntelliJ IDEA or Eclipse, simply open the project and run Main.java.

🧠 Architecture Overview
The application follows a simple Model–View–Controller (MVC) pattern:


┌────────────────────┐
│     Main.java      │  → Initializes the app and loads FXML
├────────────────────┤
│  Controlleur.java  │  → Handles UI events and state updates
├────────────────────┤
│     Timer.java     │  → Core timer logic and time tracking
├────────────────────┤
│     view.fxml      │  → Defines the graphical layout
└────────────────────┘
🖼️ Preview
(Optional — add a screenshot here)

+---------------------------+
|     Presentation Timer    |
|---------------------------|
| [ Start ]  [ Pause ]      |
| Remaining time: 05:00     |
+---------------------------+
👥 Authors
Developed by Loann Pottier and collaborators

Project for the Software Engineering module

📄 License
This project is released under the MIT License.
You are free to use, modify, and distribute it.

💡 Future Improvements
Add customizable presets (5, 10, 15 min, etc.)

Sound or vibration alerts

Save previous session durations


