# 2023年度スケジュール
実施日時：6/16-7/28の毎週金曜日，8月1日（火曜日）の5限（16:30-18:00）

  - 6/16：初回ガイダンス・準備
  - 6/23-7/28：コンペティションに参加
  - 7/7：中間報告
  - 7/28：コンペティション終了（23時59分）
  - 8/1：レポート作成日，レポート締切

# Pythonの利用方法・インストールに関するポインタ
本演習ではプログラミング言語[**Python**](https://www.python.org/)と，ブラウザ上で動作するインタラクティブなPython実行環境を提供する[**Jupyter Lab (Notebook)**](https://jupyter.org)（といくつかのライブラリ）を使用します．
そのため，以下ではPythonおよびPythonライブラリの利用方法・インストールのためのポインタ（詳細はリンク先を参照してください）と，Python開発環境におけるいくつかの事項を紹介します．
あくまで一例であり，別の方法でインストールして頂いても全く問題はありません．

最初に注意ですが，何らかのソフトウェアをインストールする際に，そのインストール方法については適当に検索すると様々情報が出てくると思いますが．基本的には**まず公式のインストレーションを見ましょう．**
公式のインストレーションを読むのがどうしてもつらい・公式のインストレーション通りに手順を踏んでもどうしてもできない場合に，Web上に存在する様々な日本語の非公式記事を参考にすると良いでしょう．

詳しく説明する前に，以下で紹介する方法を簡単にまとめておきます．
  - Google Colabを用いる（**推奨**）：Googleアカウント+インターネット環境があれば良い，インストール等不要で最も簡単．
  - WSLを用いる（Windows 10）：Microsoftが提供するWindows上でLinuxを動かす機能を使ってLinuxを動作させ，そのLinux上にPythonをインストールする．WSLをインストールした時点でPythonが使え，さらに他のライブラリ等も比較的簡単にインストールができる．
  - WinPythonを用いる（Windows）：ポータブルなPython環境を作る．ダウンロード後，そのディレクトリにあるコマンドプロンプトを起動するとPythonが使える．
  - 公式インストーラを用いる（Mac）：公式のインストーラを用いてPythonをインストールする．
  - Homebrewを用いる（Mac）：Macのパッケージ管理システムであるHomebrewを用いてPythonをインストールする．

## Google Colabを用いる（OS非依存，推奨）
[Google Colab](https://colab.research.google.com/notebooks/intro.ipynb)は，クラウド上のJupyter Notebook実行環境を提供するwebサービスです．
Google Colabを利用すれば，**インターネットにつながってさえいれば余計な環境構築・インストール作業無しにJupyter Notebookを動かすことができます**．
ColabはGoogleアカウントがあればすぐに使えます．
主要なほとんどのブラウザ上で動作するはずです．
演習で提供するノートブックは「ファイル」->「ノートブックをアップロード」でColab上で利用可能になります．
本演習で用いるデータをGoogleドライブに置くことでそれらをColab上で用いることができます．
詳しくは[ioに関する公式のurl](https://colab.research.google.com/notebooks/io.ipynb)を参考にしてください．
Colabを用いる場合はGoogleアカウントの作成以外特にすることはありません（上述の外部データの利用方法について調べておく，くらいです）．

## For Windows
### 方法1：Windows Subsystem for Linux（WSL）を用いる
WSLはWindowsの公式が提供するWindows 10上でLinuxを動かす機能です．
Windowsで直接開発環境を整えることはしんどい場合が多いですが，WSLでLinuxを動かせるようにし，そのLinux環境上に開発環境を整えることは比較的簡単であることが多いです．
[公式のURLの手順](https://docs.microsoft.com/ja-jp/learn/modules/get-started-with-windows-subsystem-for-linux/)の「Windows Subsystem for Linux を有効にし，ディストリビューションをインストールする」まで行えば，WSLがひとまず使用可能になります（2020/04/22）．

Pythonは標準で使えるようになっているはずなので，それでPythonのインストールについては終了です．


ライブラリのインストールについては，後述の「Pythonのライブラリのインストールに関するポインタ」をご覧ください．

Pythonに限らず，WSL上で開発環境を整える場合は基本的にLinuxのコマンドを用いて開発環境を整えることになります．
したがって，対応するLinuxディストリビューションにおける環境構築方法を参考にすると良いです（もちろん，WSL特有の事項も存在しますが）．
WSLは本演習に限らず今後の生活に役に立つと思うので，多少面倒かもしれませんがこの方法はおすすめです．

### 方法2：[WinPython](https://winpython.github.io/)を用いる
Windowsが10でなかったり，何らかの都合によりどうしてもWSLを使いたくない，今後のことはどうでもよいのでとにかく楽に演習を行えるようにしたいという場合，WinPythonを利用するのが便利です．

WinPythonはポータブルなPythonの実行環境を提供します．
WinpPythonインストール後，WinPythonのディレクトリにあるコマンドプロンプトを起動すると，そのコマンドプロンプト上でPythonが使えるようになります．
2022/06/06時点ですと，最新版は

    https://sourceforge.net/projects/winpython/files/WinPython_3.10/3.10.4.0/

にあります．
いくつかバリエーションがありますが`Winpython64-3.10.4.0.exe`を使ってインストールした場合，標準で本演習で用いるライブラリ群が全て入っていますので，以上で手順は完全に終了です（以下の作業は完全に不要です）．

## For Mac
macOSには`/usr/bin/python`としてpython2.7がプリインストールされており，また最新版のmacOS Catalina(10.15)には`/usr/bin/python3`としてpython3がプリインストールされています．これらのpythonはシステムやサードパーティソフトウェアが使用するものです．これらのpythonを今回の演習やこれからのプログラミング等に使用することもできますが，OSのアップグレードの際にインストールしたライブラリが消えてしまったり，設定を変更するうちにほかのシステムが正常に動かなくなったりすることがあるので新しくpythonをインストールするのがよいでしょう．

Macにpythonをインストールするには次のような方法があります．

### [公式サイト](https://www.python.org/downloads/mac-osx/)のインストーラを用いる  
インストールするとMacのシェルの設定ファイルにパスの設定が加えられます．これでデフォルトでプリインストールされているpythonではなく，新しくインストールされたpythonが使用できます．ライブラリのインストールは`pip3`を用います．

### Homebrewを使用する
HomebrewとはMacのパッケージ管理ツールです．Homebrewを使うことでpythonだけでなく様々なパッケージの管理を一元的に行うことができます．Homebrewのインストール要件は
- macOS High Sierra(10.13) 以上のバージョン
- Command Line Tools for Xcodeがインストールされている

です．Command Line Toolsは，https://developer.apple.com/download/more/ からインストーラをダウンロードするか，`xcode-select install`コマンドでインストールできます．

Homebrewをインストールします．[公式サイト](https://brew.sh/index_ja)にある通り，
```
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"`
```
Homebrewでpython3をインストールします．
```
$ brew install python
```
PATHの設定をします．シェルにbashを使用している場合，`~/.bash_profile`に以下の行を追加し，
```
export PATH=/usr/local/bin:$PATH
```
設定を反映させます．
```
$ source ~/.bash_profile
```
シェルにzshを使用している場合は対応した設定ファイルを編集してください．

# Pythonのライブラリのインストールに関するポインタ
本演習では主に以下のライブラリを利用します：
- [NumPy](https://numpy.org/)
- [SciPy](https://www.scipy.org/)
- [scikit-learn](https://scikit-learn.org/stable/)
- [jupyter](https://jupyter.org/)
- [pandas](https://pandas.pydata.org/)

以下に公式のインストレーションを列挙します：
- [NumPy/SciPy](https://www.scipy.org/install.html)
- [scikit-learn](https://scikit-learn.org/stable/install.html)
- [jupyter](https://jupyter.org/install)
- [pandas](https://pandas.pydata.org/getting_started.html)

ライブラリが豊富なプログラミング言語には，**パッケージ管理システム**が存在することがほとんどです．
これは，ライブラリを管理し，インストール・アンインストール・アップデート，依存関係の管理等を簡単に行うことを可能にするようなソフトウェアです．
Pythonにも[**pip**](https://pip.pypa.io/en/stable/)というパッケージ管理システムが存在します．
例えば，パッケージ`hoge`をインストールしたいとき，pipを用いると，
```
$ pip install hoge
```
でインストールが可能です（もしくは `pip3 install hoge`）．
上述のライブラリのインストレーションでもpipを用いたものが紹介されています．
pipはPython3.5以降であればインストール後から使えるはずです．
ライブラリによっては，Pythonライブラリとは別に様々なライブラリが必要になる場合はあります．
公式のインストレーションをよく読んで，必要なものは適宜インストールしてください．


# より綺麗なPython環境のために（オプション）
上の方法では，システムの標準のPythonに様々なライブラリをインストールします．
ライブラリというのは一旦公開されて終わりではなく，日々バグの修正や機能追加，機能変更等が行われ，進歩していきます．
研究・開発を進めていると，同じライブラリでも異なるバージョンのものを使いたい場合もあります（もしかすると，同じくPythonを使う他の実験・演習で，想定するバージョンが違うということもあるかもしれません）．
単純な方法はその都度ライブラリを特定のバージョンにインストールし直すことですが，これはあまりにも面倒です．
このような場合，**Pythonの仮想環境**を作成すると良いです（例えば，実験Aのための仮想環境，実験B・C用の仮想環境）．**各仮想環境はそれぞれ独立したPythonバイナリを持ち，独立したライブラリ群を持ちます**（つまり，同じライブラリであっても仮想環境ごとに異なるバージョンのものを入れることができます）．
Pythonの仮想環境構築方法・フレームワークは様々あります．以下にいくつか列挙しておきます．
 - [venv](https://docs.python.org/ja/3/library/venv.html)
 - [virtualenv](https://virtualenv.pypa.io/en/latest/)
 - [Pipenv](https://pipenv-ja.readthedocs.io/ja/translate-ja/)

`venv`は公式が提供しているものなので，利用するのは一番楽かもしれません．


また，Python自体にも様々なバージョンがあり，異なるものを使いたい場合があります．
Pythonのバージョン切り替えのツールとして，例えば[pyenv](https://qiita.com/KRiver1/items/c1788e616b77a9bad4dd)があります．
pyenvを上のPython仮想環境ツールと組み合わせることで良いPython開発環境を構築できます．
しかし，それなりに手間はかかると思いますので，ひとまず本演習を乗り切るだけで良いのであればやらなくともよいと思います．
