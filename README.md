# pywebview-gui-app
pywebview practice

# 
- python 3.8.10

# Tool list
- pyenv
- poetry

# reference
- pywebview
  - https://pywebview.flowrl.com/

# Trouble Shoot
- pyenvで3.X.Xを作成しているにもかかわらず、poetryでそのバージョンの環境が作成できない
  - よくわからないので、以下の方法で対応。`poetry shell`だと勝手にpython3.8.10が作られる...
    ```bash
    $python -V
    3.9.10
    $python -m venv .venv
    $poetry env use ./venv/Scripts/python.exe
    ```
- pywebview
  - `3.9.10`ではwebviewのインストール(poetry add)でエラーになる
    - 詳細にいうと、`pythonnet (2.5.2)`でエラーになる
    - 調べた感じだと、`python3.8`に対応しているため、それ以上のバージョンでエラーになるみたい