# ベースイメージを指定
# FROM node
FROM node:19-alpine

# アプリケーションファイルをコンテナ内にコピー
COPY . /home/node/webapp

# ローカルのpackage.jsonとpackage-lock.jsonをコンテナ内にコピー
COPY package*.json /home/node/webapp

# Node.jsパッケージをインストール
RUN cd /home/node/webapp && npm install -y

# 作業ディレクトリを指定
WORKDIR /home/node/webapp

# コンテナを起動する際に実行するコマンドを指定
CMD [ "npm", "start" ]
