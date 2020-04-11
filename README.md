
Notes on how to compile a .asm file with .cpp using Visual Studio 2019:

#### Simplistic form (it will generate a smaller .exe with no dependencies) 

To generate smaller binaries I noticed I had to make few changes:

Step 1: (replace "myfunction" name  with your .asm file)

* `ml64.exe /c /nologo  /Fo"myfunction.obj" /Ta myfunction.asm `

Step 2: (replace "my_program" name with your .cpp file and also add or remove kernel32.lib and user32.lib)

* `cl.exe /nologo /EHsc /D UNICODE /MT /INCREMENTAL /Fo"my_program.obj" /TP my_program.cpp /link myfunction.obj myprogram.obj kernel32.lib user32.lib  /out:"my_program.exe"`


#### How to invoke "x64 Native Tools Command Prompt for VS 2019" variable inside powershell 

Check it out @majkinetor powershell script to invoke variables from a .bat file  

* `https://github.com/majkinetor/posh/blob/master/MM_Admin/Invoke-Environment.ps1`
* `Import-Module Invoke-Environment.ps1`
*  `$vs_x64_bitness = "C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Auxiliary\Build\vcvars64.bat"`
* `Invoke-Environment $vs_x64_bitness`

Enjoy! 


  



