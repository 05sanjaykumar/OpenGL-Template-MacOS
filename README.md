
# OpenGL Template

This repository provides a basic OpenGL setup using GLFW and GLAD for macOS. It includes a simple template to quickly start building OpenGL projects.

## Folder Structure

```
.
├── include                # Header files for GLFW and GLAD
│   ├── GLFW
│   │   ├── glfw3.h        # GLFW header
│   │   └── glfw3native.h  # GLFW native header
│   ├── KHR
│   │   └── khrplatform.h  # KHR platform header
│   └── glad
│       └── glad.h         # GLAD header
├── lib                    # External libraries
│   ├── libglfw.3.dylib    # GLFW shared library
│   └── libglfw3.a         # GLFW static library (optional)
├── src                    # Source files
│   ├── glad.c             # GLAD source file
│   └── main.cpp           # Main application source file
├── main.out               # Compiled binary
└── main.out.dSYM          # Debugging symbols (generated automatically)
```

## Dependencies (macOS)

### Install via Homebrew
1. **Install Homebrew** (if you don't have it yet):
   ```bash
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
   ```

2. **Install GLFW and GLAD**:
   - GLFW:
     ```bash
     brew install glfw
     ```
   - GLAD:
     - Clone the GLAD repository:
       ```bash
       git clone https://github.com/Dav1dde/glad.git
       ```
     - Follow the instructions from [GLAD's website](https://glad.dav1d.de/) to generate the loader for OpenGL 3.3 core profile.

### Additional Dependencies

You might need to install Xcode Command Line Tools if you haven't already:
```bash
xcode-select --install
```

## Build & Run the Project

1. **Open the project in VSCode**:
   - Open the terminal and navigate to the project directory.
   - Open VSCode:
     ```bash
     code .
     ```

2. **Build the project using VSCode**:
   - Press `Cmd+Shift+B` to build the project (this runs the task defined in `tasks.json`).

3. **Set the `DYLD_LIBRARY_PATH` and run the application**:
   - Open the terminal and set the `DYLD_LIBRARY_PATH` to include the `lib` folder:
     ```bash
     export DYLD_LIBRARY_PATH=./lib:$DYLD_LIBRARY_PATH
     ```
   - Run the compiled application:
     ```bash
     ./main.out
     ```

## Quick Reference for Running the Project

If you are running the application from the terminal, make sure to set the `DYLD_LIBRARY_PATH` variable so that the system can find the GLFW library:
```bash
export DYLD_LIBRARY_PATH=./lib:$DYLD_LIBRARY_PATH
./main.out
```

## Notes

- The folder structure is organized as follows:
  - **include**: Contains the header files for GLAD and GLFW.
  - **lib**: Contains the compiled GLFW libraries.
  - **src**: Contains the C++ source files (`main.cpp`) and the GLAD loader (`glad.c`).
  - **main.out**: The compiled output of the project.
  
- If you encounter any issues with linking GLFW or GLAD, make sure the paths are correctly set in `tasks.json` and that the environment variables are configured properly.

---

Feel free to modify this template as per your project's needs. If you face any issues or need more assistance, feel free to open an issue or create a pull request!
```

### How to Use This `README.md`
1. **Dependencies Installation**: It explains how to install GLFW and GLAD for macOS using Homebrew and manually (if needed).
2. **Build & Run**: Instructions on building the project using VSCode's `Cmd+Shift+B` shortcut and how to set the `DYLD_LIBRARY_PATH` to link GLFW properly when running the project.
3. **Folder Structure**: Describes the folder structure of the project so others can understand how the project is organized.

