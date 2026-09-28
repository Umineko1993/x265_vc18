# x265_x86_64

Building x265_git ( https://github.com/Multicorewareinc/x265 ).

# Brief steps to build

Required items

> [Cmake](https://cmake.org/download/)</br>
> [git](https://git-scm.com/downloads/win)</br>
> [Visual Studio 2026](https://visualstudio.microsoft.com/downloads/)</br>
> [NASM](https://nasm.us/)

Register packages for CMake, git, and NASM

① Create an empty folder to save x265. Open Windows Terminal or Command Prompt inside this folder and run:

` git clone https://bitbucket.org/multicoreware/x265_git.git] ` to clone the repository. (Requires Git here)

If you want to build the x265 test version?, run `git clone https://bitbucket.org/multicoreware/x265_git_testing.git` instead. (A file named `x265_git_testing` will be created)

② A folder named `x265_git` will be created. Navigate to `x265_git\build\vc17-x86_64`. 

~~③ Open `make-solutions.bat` in the folder with Notepad. Replace `cmake -G “Visual Studio 17 2022” ..\..\source && cmake-gui ..\..\source` with `cmake -G “Visual Studio 18 2026” ..\..\source && cmake-gui ..\..\source`. (Skip this step if building with Visual Studio 2022)~~

④ Run `make-solutions.bat` in the folder. (CMake is required here)

⑤ When the CMake window opens, click `Configure`, then `Generate`, then `Open Project` to launch Visual Studio. (You can close the CMake window after Visual Studio launches)

⑥ After Visual Studio launches, click the `Build (B) tab` at the top of the window → `Build Solution (B)`.

⑦ When the output log displays `=========== Build completed at -:--:- and took --.--- seconds ==========`, close Visual Studio.

⑧`x265.exe` will be created in the `x265_git→build→vc17-x86_64→Debug` folder.

Translated with DeepL.com (free version)
