# x265_x86_64
x265 ( https://github.com/Multicorewareinc/x265 ) ~~( https://bitbucket.org/multicoreware/workspace/projects/PROJ )~~ をビルドしてます。

# 簡単にビルドまでの手順を説明

必要な物
> [Cmake](https://cmake.org/download/)</br>
> [git](https://git-scm.com/downloads/win)</br>
> [Visual Studio 2026](https://visualstudio.microsoft.com/ja/downloads/)</br>
> [NASM](https://nasm.us/)

Cmake・git・NASMのPachを登録しておく

①x265を保存する空フォルダを用意して、空フォルダ内でWindowsターミナル又はコマンドプロンプトを開き、
` git clone https://github.com/Multicorewareinc/x265.git ` を実行してクローンを作成。(ここでgit必要)

~~x265 古いやつ ` git clone https://bitbucket.org/multicoreware/x265_git.git `~~

~~x265のテスト版?のビルドしたい場合は、` git clone https://bitbucket.org/multicoreware/x265_git_testing.git ` こっちを実行。(x265_git_testingってファイルが出来る)~~

②x265_gitってフォルダが作成されるので、`x265_git→build→vc17-x86_64`と移動。 

~~③フォルダ内の`make-solutions.bat`をメモ帳で開き、 cmake -G "Visual Studio 17 2022" ..\..\source && cmake-gui ..\..\source を cmake -G "Visual Studio 18 2026" ..\..\source && cmake-gui ..\..\source に書き換え。 (Visual Studio 2022でビルドする場合は飛ばす)~~

④フォルダ内の`make-solutions.bat`を実行。(ここでCmake必要)

⑤CMakeのウインドウが開いたら、`Configure`・`Generate`・`Open Project`の順にクリックするとVisual Studioが起動する。(Visual Studioが起動したらCmakeのウインドウは閉じてOK)

⑥Visual Studioが起動後ウインドウ上部の `ビルド(B)タブ`→`ソリューションのビルド(B)`をクリック。

⑦出力logに `=========== ビルド は -:--:- で完了し、--.--- 秒 掛かりました ==========`  が表示されたら、Visual Studioを終了させる。

⑧`x265→build→vc18→Debug`のフォルダ内に`x265.exe`が作成されている。

# Linux コマンド

作成順は、linux→arm-linux→aarch64-linux

① ~$ Desktop && sudo rm -r x265 && git clone https://github.com/Multicorewareinc/x265.git && cd x265 && build &&  linux && ./make-Makefiles.bash && make

② ~$ .. && arm-linux && sudo chmod o+x make-Makefiles.bash && sudo ./make-Makefiles.bash && sudo make

③ ~$ .. && aarch64-linux && ./make-Makefiles.bash && make
