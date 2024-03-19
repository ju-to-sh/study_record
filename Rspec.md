## Rspecまとめ
### セットアップ
#### 【Gemのインストール】
Gemfileに以下の記載を追加し、bundle installをする
```
group :development, :test do
  gem 'rspec-rails'
  #factory botを使用してテストデータを作成する場合
  gem 'factory_bot_rails'
end
```
#### 【設定ファイルの作成】
gemインストール完了後、以下のコマンドを実行する
```
bundle exec rails g rspec:install
```
実行すると以下のファイル/ディレクトリが作成される
- create  .rspec (RSpec用の設定ファイル)
- create  spec (スペックファイルを格納するディレクトリ)
- create  spec/spec_helper.rb (RSpecの動きをカスタマイズするヘルパーファイル)
- create  spec/rails_helper.rb (RSpecの動きをカスタマイズするヘルパーファイル)

実行結果を読みやすくするために.rspecに以下を記述する
```
--format documentation
```
#### 【動作確認】
以下のコードを実行し、Rspecが起動することを確認する
```
bundle exec rspec
```
正常にインストールされている場合、以下のような表示となる
```
No examples found.

Finished in 0.00074 seconds (files took 0.14443 seconds to load)
0 examples, 0 failures
```
