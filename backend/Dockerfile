FROM ruby:3.2.5
ARG RUBYGEMS_VERSION=3.3.20

# 作業ディレクトリを指定
WORKDIR /app

# ホストのGemfileをコンテナ内の作業ディレクトリにコピー
COPY ./backend/Gemfile* /app/

# bundle installを実行
RUN bundle install

# アプリケーションのソースコードをコピー
COPY . .

# Rails のポート
EXPOSE 3000

# デフォルトのコマンド
CMD ["rails", "server", "-b", "0.0.0.0"]