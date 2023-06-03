# アプリケーション名
DREAM

# アプリケーション概要
キャンドルのお店のwebサイト。お客様の閲覧サイドと、店主の編集サイドを作っていく。
後々はECサイトに出来るようにがんばりたい。

# URL
なし

# テスト用アカウント
認証ID okinawa
認証PS 12345

# アプリケーションを作成した背景
姉がキャンドルのお店を経営しており、もっと多くの方に知ってもらいたい想いからWEBサイトを作成したいと思いました。来年今のお店を手放すことになったので、イベント出店のみの活動になります。
WEBサイトで少しでも多くの方にイベントに来てもらい、後々はWEBサイトで収益が出るように活動を広げていければな。と考えております。

# 洗い出した要件
？？？？？

# データベース設計
[![Image from Gyazo](https://i.gyazo.com/c80a69d1a8b0f7b038de0d52b89be4e3.png)](https://gyazo.com/c80a69d1a8b0f7b038de0d52b89be4e3)

# 画面遷移図
[![Image from Gyazo](https://i.gyazo.com/4199b7382bca8254764500be8d62ad87.png)](https://gyazo.com/4199b7382bca8254764500be8d62ad87)
# テーブル設計

## Me テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| profile            | text    | null: false |

## Candles テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| name               | string  | null: false |
| explain            | text    | null: false |
| price              | integer |             |

### Association
- has_many :Aromas


## Aromas テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| name               | string  | null: false |
| explain            | text    | null: false |

### Association
- has_many :Candles


## Events テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| name               | string  | null: false |
| place              | string  | null: false |
| description        | text    | null: false |

### Association
- has_many :Workshops


## Workshops テーブル

| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| name               | string  | null: false |
| explain            | text    | null: false |

### Association
- has_many :Events


## Others
| Column             | Type    | Options     |
| ------------------ | ------- | ----------- |
| name               | string  | null: false |
| explain            | text    | null: false |
| price              | integer |             |