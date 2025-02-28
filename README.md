# Rush Hour Taxi Game

Rush Hour Taxi Game is a simple C++ console-based game that combines graphics drawn using the Windows GDI API with keyboard interactivity. In this game, you control a taxi that picks up and drops off passengers while avoiding obstacles and oncoming traffic. The game tracks your score, adds extra challenges as you progress, and saves high scores in a text file.

## Features

- **Interactive Gameplay:**  
  Control a taxi using the keyboard (W, A, S, D for movement and Spacebar to pick up/drop passengers).  
- **Dynamic Graphics:**  
  Uses Windows GDI functions to draw shapes (lines, rectangles, ellipses) and text. The drawing functions are implemented in [`mygraphics.cpp`](21i0438_B_project/mygraphics.cpp) and [`mygraphics.h`](21i0438_B_project/mygraphics.h).
- **Obstacles and Traffic:**  
  Randomly placed obstacles and other moving cars create a dynamic environment that the taxi must avoid.
- **Passenger Pickup and Destination:**  
  Picking up a passenger generates a random destination on the map while updating the score.
- **Highscore Management:**  
  High scores are stored in [`highscores.txt`](21i0438_B_project/highscores.txt) and updated when a new high score is reached.
- **Additional Console Features:**  
  Uses custom console utilities from [`myconsole.cpp`](21i0438_B_project/myconsole.cpp) and [`myconsole.h`](21i0438_B_project/myconsole.h) to control cursor position, clear the screen, and check key presses.

## Libraries and Technologies Used

- **Windows API (GDI):**  
  The game uses Windows API calls such as `GetConsoleWindow()`, `HDC`, and GDI drawing functions for rendering graphics.
- **Standard C++ Libraries:**  
  Input/output streams (`iostream`, `fstream`, `sstream`), time functions (`time.h`, `clock()`), and string manipulation.
- **Conio.h:**  
  For non-standard console input functions like `getch()` and `kbhit()`.
- **GDI32 Library:**  
  When compiling the project, ensure to link with the GDI32 library using `-lgdi32` as it is used for drawing and manipulating graphics in the console window.


## How to Build and Run

**Requirements:**
- Windows operating system.
- A C++ compiler that supports Windows API (e.g., MinGW or Visual Studio).

**Using Command Line (MinGW Example):**

1. Open a terminal in the root directory `21i0438_B_project/`.
2. Compile the project with the following command:

   ```sh
   g++ -o RushHour.exe Game.cpp mygraphics.cpp myconsole.cpp -lgdi32
   ./RushHour.exe
