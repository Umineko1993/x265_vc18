# x265_x86_64

Building x265_git ( https://github.com/Multicorewareinc/x265 ).

# Brief steps to build

Required items

> [Cmake](https://cmake.org/download/)</br>
> [git](https://git-scm.com/downloads/win)</br>
> [Visual Studio 2026](https://visualstudio.microsoft.com/downloads/)</br>
> [NASM](https://nasm.us/)

Set the paths for CMake, Git, and NASM

① Create an empty folder to save x265. Open Windows Terminal or Command Prompt inside this folder and run:

` git clone https://github.com/Multicorewareinc/x265.git ` to clone the repository. (Requires Git here)

② A folder named `x265` will be created. Navigate to `x265\build\vc18`. 

③ Run `make-solutions.bat` in the folder. (CMake is required here)

④ When the CMake window opens, click `Configure`, then `Generate`, then `Open Project` to launch Visual Studio. (You can close the CMake window after Visual Studio launches)

⑤ After Visual Studio launches, click the `Build (B) tab` at the top of the window → `Build Solution (B)`.

⑥ When the output log displays `=========== Build completed at -:--:- and took --.--- seconds ==========`, close Visual Studio.

⑦`x265.exe` will be created in the `x265→build→vc18→Debug` folder.

# Linux Command

Preparation Commands

~$  sudo add-apt-repository ppa:git-core/ppa && sudo apt update && sudo apt install -y git cmake nasm cmake-curses-gui build-essential yasm git-all gcc-arm-linux-gnueabi g++-arm-linux-gnueabi gcc-aarch64-linux-gnu g++-aarch64-linux-gnu

The order of creation is: linux → arm-linux → aarch64-linux

① ~$ Desktop && sudo rm -r x265 && git clone https://github.com/Multicorewareinc/x265.git && cd x265 && build &&  linux && ./make-Makefiles.bash && make

② ~$ .. && arm-linux && sudo chmod o+x make-Makefiles.bash && sudo ./make-Makefiles.bash && sudo make

③ ~$ .. && aarch64-linux && ./make-Makefiles.bash && make

Translated with DeepL.com (free version)
