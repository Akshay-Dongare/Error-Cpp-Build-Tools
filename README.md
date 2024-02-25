# Error-Cpp-Build-Tools
error: Microsoft Visual C++ 14.0 or greater is required. Get it with "Microsoft C++ Build Tools": https://visualstudio.microsoft.com/visual-cpp-build-tools/
## ERROR: Microsoft Visual C++ 14.0 or greater is required
If you are getting an error while building wheels for any package during pip installation, the following steps worked for me:
1. Download the Visual Studio Build Tools installer at https://visualstudio.microsoft.com/visual-cpp-build-tools/ 
2. Install the 'Desktop Development with C++' components using Visual Studio Build tool. (approx 6.84GB total)
3. Locate the directory where MSBuild is installed (typically "C:\Program Files (x86)\Microsoft Visual Studio\20xx\BuildTools\MSBuild\Current\Bin" where the xx in 20xx signifies the version of Microsoft Build Tools you have downloaded) and add it to the PATH variable (This is an extremely important step as it ensures that Build Tools can be found by other programs like pip). Add it to the System Environment PATH variable rather than User Environment PATH variable.
4. Install cmake (pip install cmake) if not already installed.
5. RESTART your computer.
* Source: https://learn.microsoft.com/en-us/answers/questions/136595/error-microsoft-visual-c-14-0-or-greater-is-requir 
