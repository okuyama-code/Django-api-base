## 詳しい環境構築は以下のブログをご覧ください
TODO これを投稿したら更新する。そしてリモートのpush先を変更する
https://qiita.com/drafts/be58d39f277f1a7a9f63/edit

## .envファイルを以下に作成
1. .env (プロジェクト 配下)
```
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_DB=dev
```

2. backend/.env
```
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
POSTGRES_DB=dev
```

最終的なディレクトリ構成はこちら
```
.
├── .devcontainer
│   ├── Dockerfile
│   └── devcontainer.json
├── .env
├── .gitignore
├── backend
│   ├── .env
│   ├── db.sqlite3
│   ├── manage.py
│   ├── myapi
│   │   ├── __init__.py
│   │   ├── __pycache__
│   │   │   ├── __init__.cpython-313.pyc
│   │   │   ├── admin.cpython-313.pyc
│   │   │   ├── models.cpython-313.pyc
│   │   │   ├── settings.cpython-313.pyc
│   │   │   ├── urls.cpython-313.pyc
│   │   │   └── wsgi.cpython-313.pyc
│   │   ├── admin.py
│   │   ├── asgi.py
│   │   ├── migrations
│   │   │   ├── 0001_initial.py
│   │   │   ├── __init__.py
│   │   │   └── __pycache__
│   │   │       ├── 0001_initial.cpython-313.pyc
│   │   │       └── __init__.cpython-313.pyc
│   │   ├── models.py
│   │   ├── settings.py
│   │   ├── urls.py
│   │   └── wsgi.py
│   └── requirements.txt
└── docker-compose.yml
```