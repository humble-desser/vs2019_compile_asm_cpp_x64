# vs2019_compile_asm_cpp_x64
Notes on how to use Visual Studio 2019  command line in order to compile a .asm file with .cpp using:
ml64.exe
cl.exe
link.exe

# Install Visual Studio 2019

Open "x64 Native Tools Command Prompt for VS 2019"

# Recipe
ml64.exe /c /nologo  /Fo"myfunction.obj" /Ta myfunction.asm 

cl /c /nologo /EHsc /D UNICODE /MDd /Fo"mycode.obj" /TP  mycode.cpp 

link.exe  /OUT:"mydemo.exe" /INCREMENTAL /NOLOGO  /SUBSYSTEM:CONSOLE mycode.obj myfunction.obj

Enjoy your binary! 


