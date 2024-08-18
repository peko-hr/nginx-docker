# Nginx Docker Project

このプロジェクトは、Dockerを使用してNginxウェブサーバーを簡単に設定し、実行するためのものです。

## 前提条件

このプロジェクトを実行するには、以下のソフトウェアがインストールされている必要があります：

- Docker
- Docker Compose

## プロジェクト構造
project/  
├── compose.yaml  
├── nginx/  
│   ├── Dockerfile  
│   └── nginx.conf  
└── html/  
└── index.html  

- `compose.yaml`: Docker Composeの設定ファイル
- `nginx/Dockerfile`: Nginxコンテナのビルド指示
- `nginx/nginx.conf`: Nginxの設定ファイル
- `html/index.html`: サンプルのHTMLファイル

## セットアップと実行

1. このリポジトリをクローンまたはダウンロードします。
2. プロジェクトのルートディレクトリに移動します：
```sh
cd path/to/project
```

3. Docker Composeを使用してコンテナをビルドし、起動します：
```sh
docker-compose up -d
```

4. ブラウザで `http://localhost` にアクセスして、Nginxサーバーが正常に動作していることを確認します。

## カスタマイズ

- HTMLコンテンツを変更するには、`html/` ディレクトリ内のファイルを編集または追加します。
- Nginxの設定を変更するには、`nginx/nginx.conf` ファイルを編集し、コンテナを再ビルドします。

## コンテナの停止

コンテナを停止するには、以下のコマンドを実行します：
```sh
docker-compose down
```

## トラブルシューティング

問題が発生した場合は、以下を確認してください：

1. Dockerデーモンが実行されていることを確認します。
2. ポート80が他のプロセスで使用されていないことを確認します。
3. ログを確認するには、`docker-compose logs nginx` コマンドを使用します。
