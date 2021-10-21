# README

## users テーブル

| Column             | Type   | Options                   |
| ------------------ | ------ | -----------               |
| nickname           | string | null: false               |
| email              | string | null: false, unique: true |
| encrypted_password | string | null: false               |
| first_name         | string | null: false               |
| last_name          | string | null: false               |

has_many :tweets

## tweets テーブル

| Column             | Type       | Options                         |
| ------------------ | ------     | -----------                     |
| place              | string     | null: false                     |
| text               | string     |                                 |
| genre_id           | int        | null: false                     |Active hush
| with_id            | int        | null: false                     |Active hush
| transport_id       | int        | null: false                     |Active hush
| user               | references | null: false, foreign_key: true  |

belongs_to :user
has_one :like

## like 

| Column             | Type   | Options                  |
| ------------------ | ------ | -----------              |
| like               | button |                          |

belongs_to :tweet

## like 

| Column             | Type   | Options                  |
| ------------------ | ------ | -----------              |
| map                |        |                          |

