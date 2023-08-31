# Bookers2_JE

JE研修を実施するbookers2です。

# 実施内容 


- devise
https://github.com/heartcombo/devise
	- パスワードの変更機能・日本語化をする
	- ユーザー認証機能実装Gem

- acts-as-taggable-on(Gem)
https://github.com/mbleigh/acts-as-taggable-on
	- タグ機能追加

- ransack(Gem)
https://github.com/activerecord-hackery/ransack
	- 複数条件を用いた検索機能の実装
	- 実装参考記事↓
	- https://qiita.com/nishina555/items/2c1f8bae980e426519bc

- slick(JS Library)
http://kenwheeler.github.io/slick/
	- Bookers2にslickを導入し、画像スライドショーを組み込む
		- 読み込みはCDN
		- JSの記述は`app/assets/javascript/application.js`に記述
		- 組み込む場所はどこでもいい

- Google Maps Platform(API)
https://developers.google.com/maps/documentation?hl=ja
	- マイページに自分の住所の地図を導入
		- userモデルに、郵便番号、住所を格納するカラムを追加
		- 新規登録画面に郵便番号を入力するフォームを追加
		- 郵便番号入力後、郵便番号に対応する住所を住所フォームに自動入力(jpostal.jp, Gem: jp_prefectureを使用)
		- 他人の詳細画面では住所を表示しない
		- Google Map APIを使用する
		- APIトークンはGem dotenv-railsを使用し、環境変数として扱う
