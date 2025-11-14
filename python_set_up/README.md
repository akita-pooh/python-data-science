# Python 環境構築のための手順書
以下の手順で Python のセットアップを行い, ローカル環境で使えるようにする.

## 1. エディタのダウンロード
推奨エディタは以下の2つ.

- [VSCode](https://code.visualstudio.com/download)
- [Cursor](https://cursor.com/ja/download)

ただし, Cursor は上長への許可が必要である.  
Slack の適切なチャンネルにて申請を行い, ダウンロードする.

## 2. Homebrew のインストール
ターミナル上で [Homebrew](https://brew.sh/ja/) をインストールする.  
以下のコマンドでインストールできる.

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

ターミナルに表示される `Next steps` の指示通りにコマンドを入力する([参考](https://qiita.com/wooooo/items/6d8a7de5ffafed1cc66c#%E6%89%8B%E9%A0%86)).  
Homebrew がインストールされたら, Python のバージョンを指定してダウンロードする.

```sh
brew install python@3.x
```

おそらくこれだけではパスが通っていないため, 以下のコマンドを打つ.

```sh
which -a python3
```

ここで,

```txt
/opt/homebrew/bin/python3
```

のようなものが出てくるので,

```sh
export PATH="/opt/homebrew/bin:$PATH"
source ~/.zshrc
```

と打ち, 正しくインストールされたかを以下のように確認する.

```sh
python3 -V
```

バージョンも合っていればインストール完了である.

## 3. 拡張機能の追加
VSCode や Cursor で, Python の補助機能を追加する.  
以下の機能を Marketplace で検索し, ダウンロードする.

- Jupyter
- Black Formatter
- Flake8
- isort
- Jupyter Cell Tags
- Jupyter Keymap
- Jupyter Notebook Renderers
- Jupyter Slide Show
- Mypy Type Checker
- Pylance
- Python
- Python Debugger
- Python Environments