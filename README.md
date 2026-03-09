# config-program-languages
VS Code Programming Language Profiles
This repository contains pre-configured Visual Studio Code profiles and environment settings for a wide variety of programming languages, optimized for Windows, Linux, and macOS. These configurations are designed to provide a "plug-and-play" experience for students and developers using tools like Code Runner and the native F5 Debugger.

📝 Included Languages
This repository includes configurations for:

Assembly / AutoHotKey / Basic / C / C++ / C# / Cobol / Dart / F# / Fortran / Go / Java / JavaScript / Kotlin / Lua / Objective-C / Pascal / Perl / Python / R / Ruby / Rust / Scala / Simula / Smalltalk / Swift / TypeScript / Visual Basic.

🚀 Overview
The project aims to simplify the setup process for multiple languages by providing:

settings.json: Optimized for terminal execution and UTF-8 encoding.

tasks.json: Automated build systems (the "engine" for compilation).

launch.json: Ready-to-use debugging configurations.

VS Code Profiles: Exported environments containing all necessary extensions.

💻 Operating System Recommendations
While most languages are cross-platform, some environments are more stable in specific systems:

Linux / macOS: Highly recommended for Objective-C, Swift, and Ruby. These systems have native package managers and header files that make compilation seamless.

Windows: Best for Visual Basic (.NET) and C#. For C-based languages (C, C++, Objective-C), we use the MSYS2 (MinGW-w64) environment.

📂 How to Use These Profiles
Importing to VS Code
Open VS Code and click the Gear icon (bottom-left) > Profiles > Import Profile....

Select the .code-profile file corresponding to your OS (Windows, Linux, or macOS).

VS Code will automatically install the required extensions and apply the settings.

Running Code
Code Runner (Terminal): Press the Play button (top-right) or Ctrl+Alt+N to run a script directly in the terminal.

Debugging (F5): Press F5 to compile and debug. The tasks.json will automatically create a bin/ folder and generate the executable there.

🛠️ Complete Compiler Installation Guide
This guide covers the full stack found in your repository: C, C++, Objective-C, Pascal, Perl, Python, R, Ruby, Rust, Scala, Simula, Smalltalk, Swift, TypeScript, Visual Basic, Lua, Basic Classic, and COBOL.

🪟 Windows (MSYS2 & Official Toolkits)
For Windows, MSYS2 handles most of your heavy lifting, while specific installers handle the high-level languages.

MSYS2 Terminal (UCRT64 or MINGW64):

C / C++ / Objective-C: pacman -S mingw-w64-x86_64-gcc mingw-w64-x86_64-gcc-objc mingw-w64-x86_64-gnustep-base.

Pascal: pacman -S mingw-w64-x86_64-fpc.

Lua: pacman -S mingw-w64-x86_64-lua.

COBOL (GnuCOBOL): pacman -S mingw-w64-x86_64-gnucobol.

Smalltalk (GNU): pacman -S mingw-w64-x86_64-gnu-smalltalk.

Official Installers:

Python, Perl, R, Ruby: Use the official .exe installers from python.org, strawberryperl.com, r-project.org, and rubyinstaller.org.

Basic Classic (FreeBASIC): Download the Windows installer from freebasic.net.

Rust: Use rustup-init.exe from rustup.rs.

Swift: Download the toolchain from swift.org.

TypeScript: Install Node.js, then run npm install -g typescript.

Visual Basic / .NET: Download the .NET SDK from Microsoft.

Scala: Use cs setup via the Coursier installer.

🐧 Linux (Ubuntu / Debian)
Linux users can install almost everything through the apt package manager.

The "Essentials": sudo apt update && sudo apt install build-essential (Covers C/C++).

System Languages:

Objective-C: sudo apt install gobjc gnustep gnustep-devel.

Pascal: sudo apt install fpc.

Lua: sudo apt install lua5.4.

COBOL: sudo apt install gnucobol.

Basic Classic: sudo apt install freebasic.

Interpreted & High-Level:

Python / Perl / R / Ruby: sudo apt install python3 perl r-base ruby-full.

Scala: sudo apt install scala.

TypeScript: sudo apt install nodejs npm && sudo npm install -g typescript.

Simula: sudo apt install cim.

Smalltalk: sudo apt install gnu-smalltalk.

Modern Toolkits:

Rust: curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh.

Swift: Follow the specific repo instructions at swift.org.

🍎 macOS (Homebrew)
On macOS, your terminal will be powered by the Homebrew manager.

Pre-requisite: xcode-select --install (Required for C/C++/Objective-C/Swift headers).

Brew Commands:

Pascal: brew install fpc.

Lua: brew install lua.

COBOL: brew install gnu-cobol.

Basic Classic: brew install freebasic.

Ruby / R / Perl: brew install ruby r perl.

Smalltalk / Simula: brew install gnu-smalltalk cim.

TypeScript: brew install node && npm install -g typescript.

Scala: brew install scala.

Others:

Rust: curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh.

Visual Basic: Install the .NET SDK for Mac from Microsoft.

🌎 Environment Variables (The "Path" Rule)
For VS Code to "obey" your commands, it must find these programs in your system's memory.

Windows: Open "Edit the system environment variables" and add the following to your Path:

C:\msys64\mingw64\bin (For GCC, G++, Lua, COBOL, Pascal).

%USERPROFILE%\.cargo\bin (For Rust).

Specific paths for Python or Ruby if they weren't added during installation.

Linux/macOS: Most installers handle this, but for Rust, ensure you source the environment:

source $HOME/.cargo/env

Language            Folder in Repo          Best OS to run
Lua	                lua/            	    Universal
COBOL   	        cobol/  	            Linux / Windows (MSYS2)
Basic Classic	    basic-classic/  	    Windows
Objective-C 	    objective-c/    	    macOS / Linux
Rust            	rust/           	    Universal