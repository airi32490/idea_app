# テーブル設計

## categories テーブル

| Column | Type   | Options                   |
| ------ | ------ | ------------------------- |
| id     | bigint | primary_key: true         |
| name   | string | null: false, unique: true |

### Association

- has_many :ideas

## ideas テーブル

| Column      | Type   | Options                        |
|------------ | ------ | ------------------------------ |
| id          | bigint | primary_key: true              |
| category_id | bigint | null: false, foreign_key: true |
| body        | text   | null: false                    |

### Association

- belongs_to :category