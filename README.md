#GCC自動ビルドシェルスクリプト
##概要
GCCの最新版を取ってきて自動でビルドし、インストールまで行います。

##ターゲットOS(他のOSでも動くかもしれません)
CentOS 6～

##必要なもの
- GCCなどのC/C++コンパイラ
- Subversion
- tcsh
- porgもしくはpaco(ソースビルドしたソフトウェアの管理ソフト)
- その他GCCのビルドに必要なライブラリなど

##インストールする言語
C・C++のみです。他の言語は一切インストールしません。インストールしたい場合はスクリプトを直接いじってください。

##注意
- このスクリプトでインストールしたGCCのバイナリ名は「`gcc5`」「`g++5`」(5.xが最新版の場合)のようにメジャーバージョンが末尾につきます。単に「`gcc`」「`g++`」とするとパッケージ等でインストールした古いバージョンが起動します。
- このスクリプトは環境変数の設定を一切行いません。`PATH`・`LIBRARY_PATH`・`LD_RUN_PATH`・`LD_LIBRARY_PATH`・`CPATH`の設定は各自行ってください。

##使用方法
- `gcc_build`をダウンロードします。
```Bash
wget https://raw.githubusercontent.com/tats-u/gcc-autobuild/master/gcc_build
```
- ダウンロードした`gcc_build`を開いて、設定項目をいじります。
- `gcc_build`に実行権限を与えます。(`chmod +x gcc_build`)
- 最後に、端末から
```Bash
./gcc_build
```
を実行します。
