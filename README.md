#♟️ JavaFX Chess

A minimal two-player chess clock built with JavaFX. Each player has an independent countdown; turns are switched, styles update (white/black sides), and time choices are picked via a startup dialog.

Features

Time selection at launch: a ChoiceDialog lets you pick the base time (minutes) for both players.

Two synchronized timers: one runs while the other is paused; they swap on turn change.

Side switching: a Switch sides button flips left/right players (useful if you set up the board the other way around).

Clear visual cues: white vs. black panes with large, centered labels for remaining time.

Tech Stack

Java 11+ (or 8 if you bundle JavaFX)

JavaFX (FXML UI)

Simple MVC-style classes:

app.Main — bootstraps the JavaFX application and loads view.fxml.

app.Controlleur — UI controller: time selection dialog, start/stop, side switch, and style updates.

app.models.Timer — Runnable chess clock logic handling the two players and turn swapping.

app.models.Player — holds per-player state (remaining time, color, active/inactive).

Getting Started
1) Clone
git clone <your-repo-url>
cd <repo>

2) Run (IDE way)

Open the project in IntelliJ IDEA or VS Code with Java and JavaFX support, then run app.Main.

3) Run (CLI way, with standalone JavaFX)

If you have JavaFX SDK installed, adjust the path below and run:

# Compile
javac --module-path <PATH_TO_FX>/lib --add-modules javafx.controls,javafx.fxml \
  -d out $(find . -name "*.java")

# Run
java --module-path <PATH_TO_FX>/lib --add-modules javafx.controls,javafx.fxml \
  -cp out app.Main

How to Use

Start the app → a dialog appears to choose the base time (e.g., “5 minutes”).

Clock starts → one side is active and counts down; the other is paused.

Switch turns → use the on-screen control (Switch sides) to flip left/right players if needed.
(Turn progression and style updates are handled by the controller and model.)

Tip: The large time labels (time1, time2) and white/black pane backgrounds make it easy to see who’s on move.

Project Structure
src/
 └─ app/
     ├─ Main.java                # Launches JavaFX and loads FXML
     ├─ Controlleur.java         # UI logic (dialog, styles, switching)
     └─ models/
         ├─ Timer.java           # Runnable chess-clock engine
         └─ Player.java          # Player state (time, color, active)
resources/
 └─ view.fxml                    # Layout (two panes, labels, switch button)

Roadmap

Time increments (Fischer/bronstein)

Pause/Resume and Reset controls

Sound/vibration alerts near time-out

Keyboard shortcuts (e.g., space to switch)

Packaging a self-contained build (jlink/jpackage)
