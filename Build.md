# To BUILD or not to BUILD

# Windows

1. Install Visual Studio 2019 or newer.
2. Install Git for Windows
3. Install Vcpkg
	-	Open a PowerShell / CMD / Git Bash in the folder where you wish to install vcpkg, (e.g. `C:/`)
	-	Vcpkg is a package management software that download and build the required software dependencies.
	-	`git clone https://github.com/microsoft/vcpkg`
	-	`.\bootstrap-vcpkg.bat`
	-	After vcpkg is installed, install the dependency of this project
		-	On 64-bit system (most system today) `.\vcpkg.exe install freetype:x64-windows`
		-	On 32-bit system (may not work well) `.\vcpkg.exe install freetype`
4. Open Visual Studio, use "Clone or Check out Code"
	-	Use the GitHub Classroom repository link
5. After the project is opened and the files are listed, right click on `CMakeLists.txt`, and then click "CMake Settings for Assignment1"
	-	On the left, press the add button and add a configuration with "x64-Release" (or "x86-Release" on a 32-bit machine). You will still be able to debug the project, but the optimizations of release code will be applied.
	-	Then, find field "CMake toolchain file", enter `[location of vcpkg]/scripts/buildsystems/vcpkg.cmake`. (e.g. `C:/vcpkg/scripts/buildsystems/vcpkg.cmake`)
6. "Build" -> "Build All"
7. Then you can run your project

You only need to do step 1 to 3 once for this class. You may need to install additional libraries with later assignments with vcpkg. You can repeat steps 4-7 with any of the assignments later.