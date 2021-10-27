# テーブル設計



| Column             | Type   | 0ptions     |
| ------------------ | ------ | ----------  |
| name               | string | null: false |
| email
| encrypted_password | string | null: false |



- has_many :room_users
- has_many :rooms,through: :room_users
- has_many :messages




| Column | Type   | Options     |
| ------ | ------ | ----------- |
| name   | string | null: false |


- has_many :room_users
- has_many :users, through: :room_users
- has_many :messages



| Column | Type       | Options                        |
| ------ | ---------- | ------------------------------ |
| user   | references | null: false, foreign_key: true |
| room   | references | unll: false, foreign_key: true |



- belongs_to :room
- belongs_to :user



| Column  | Type       | Options                        |
| ------- | ---------- | ------------------------------ |
| content | string     |                                |
| user    | references | null: false, foreign_key: true |
| roon    | references | null: false, foreign_key: true |



- belongs_to :room
- belongs_to :user
