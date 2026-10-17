# How to Run the Project

This guide explains how to compile and run the RPG Game engine on Windows using Command Prompt (`cmd`).

---

## Quick Start (Already in the Folder)

If your Command Prompt is already opened in the project folder:
```cmd
C:\Users\diksh\OneDrive\Desktop\My_Project\OOPs Game\Game 2 - Copy>
```

### 1. Build and Run (Recommended)
This automatically closes any running instance, recompiles any changed source code, and launches the game:
```cmd
build.bat
```

### 2. Run Directly Without Recompiling
If the game has already been built:
```cmd
game.exe
```

---

## Full Step-by-Step Instructions

### Step 1: Open Command Prompt in the Project Folder
- **Method 1 (Fastest):** 
  Open File Explorer, go to the project folder, click inside the top address bar, type `cmd`, and press `Enter`.
- **Method 2:** 
  Press `Win + R`, type `cmd`, press `Enter`, and navigate to the directory:
  ```cmd
  cd /d "C:\Users\diksh\OneDrive\Desktop\My_Project\OOPs Game\Game 2 - Copy"
  ```

### Step 2: Compile and Launch
Run:
```cmd
build.bat
```

---

## Manual Compilation (Optional)

If you wish to compile manually with `g++` and SFML:
```cmd
g++ -std=c++17 src/*.cpp -Iinclude -IC:/SFML/include -LC:/SFML/lib -lsfml-graphics -lsfml-window -lsfml-system -lsfml-audio -o game.exe
game.exe
```

---

## Troubleshooting
- **Build fails with missing compiler?** Ensure MinGW / `g++` is added to your Windows system `PATH`.
- **Missing DLL error?** Ensure the SFML `.dll` files (`sfml-graphics-2.dll`, `sfml-window-2.dll`, `sfml-system-2.dll`, `sfml-audio-2.dll`, `openal32.dll`) are present in the same directory as `game.exe`.
- **Game window not showing?** Check `build_log.txt` in the project directory for any compilation warnings or errors.
