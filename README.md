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