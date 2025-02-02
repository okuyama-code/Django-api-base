# ベースとなるDockerイメージを指定
# ここではPythonのバージョン3.11.1を使用
FROM python:3.11.1

# コンテナ内で作業するディレクトリを指定
# ここでは `/usr/src/app` を作業ディレクトリとして設定
WORKDIR /usr/src/app

# 必要なシステムパッケージをインストール
# - `apt-get update`: パッケージリストを更新
# - `libpq-dev`: PostgreSQLとの接続に必要なライブラリをインストール
# - `rm -rf /var/lib/apt/lists/*`: 不要なキャッシュを削除してコンテナのサイズを削減
RUN apt-get update \
    && apt-get install -y libpq-dev
# Pythonパッケージの依存関係をインストール
# - `COPY backend/requirements.txt .` : `requirements.txt` をコンテナ内にコピー
# - `pip install --upgrade pip`: `pip` を最新バージョンに更新
# - `pip install -r requirements.txt`: `requirements.txt` に記載されたパッケージをインストール
COPY backend/requirements.txt .
RUN pip install --upgrade pip \
    && pip install -r requirements.txt

# コンテナのポート8000番を開放
# Djangoの開発サーバーはデフォルトで8000番ポートを使用するため
EXPOSE 8000