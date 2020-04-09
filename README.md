# vs2019_compile_asm_cpp_x64

Notes on how to compile a .asm file with .cpp using Visual Studio 2019:

Step 1: Generate an .obj file from your .asm 

ml64.exe

Step 2: Generate an .obj file from your .cpp

cl.exe

Step 3: Link your object files and generate an .exe 

link.exe


# Install Visual Studio 2019

Open "x64 Native Tools Command Prompt for VS 2019"

Follow the raw_notes.txt

