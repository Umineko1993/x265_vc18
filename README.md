# x265
x265 ( https://github.com/Multicorewareinc/x265 ) をビルドしています。

# 簡単にビルドまでの手順を説明

必要な物
> [Cmake](https://cmake.org/download/)</br>
> [git](https://git-scm.com/downloads/win)</br>
> [Visual Studio 2026](https://visualstudio.microsoft.com/ja/downloads/)</br>
> [NASM](https://nasm.us/)

Cmake・git・NASMのPathを登録しておく

①x265を保存する空フォルダを用意して、空フォルダ内でWindowsターミナル又はコマンドプロンプトを開き、
` git clone https://github.com/Multicorewareinc/x265.git ` を実行してクローンを作成。(ここでgit必要)

②x265ってフォルダが作成されるので、`x265→build→vc18`と移動。 

③フォルダ内の`make-solutions.bat`を実行。(ここでCmake必要)

④CMakeのウインドウが開いたら、`Configure`・`Generate`・`Open Project`の順にクリックするとVisual Studioが起動する。(Visual Studioが起動したらCmakeのウインドウは閉じてOK)

⑤Visual Studioが起動後ウインドウ上部の `ビルド(B)タブ`→`ソリューションのビルド(B)`をクリック。

⑥出力logに `=========== ビルド は -:--:- で完了し、--.--- 秒 掛かりました ==========`  が表示されたら、Visual Studioを終了させる。

⑦`x265→build→vc18→Debug`のフォルダ内に`x265.exe`が作成されている。

# Linux コマンド

準備コマンド

~$  sudo add-apt-repository ppa:git-core/ppa && sudo apt update && sudo apt install -y git cmake nasm cmake-curses-gui build-essential yasm git-all gcc-arm-linux-gnueabi g++-arm-linux-gnueabi gcc-aarch64-linux-gnu g++-aarch64-linux-gnu

作成順は、linux→arm-linux→aarch64-linux

① ~$ Desktop && sudo rm -r x265 && git clone https://github.com/Multicorewareinc/x265.git && cd x265 && build &&  linux && ./make-Makefiles.bash && make

② ~$ .. && arm-linux && sudo chmod o+x make-Makefiles.bash && sudo ./make-Makefiles.bash && sudo make

③ ~$ .. && aarch64-linux && ./make-Makefiles.bash && make
