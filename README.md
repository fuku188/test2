## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null:false|
|image|string|null:false|
|group_id|integer|null:false, foreign_key: ture|
|user_id|integer|null:false, foreign_key: true|

###Association
- belongs_to :group
- belongs_to :user

## usersテーブル

- デフォルト + nameカラム + group_idカラム

###Association
- has_one :group
- has_many :messages


## groupテーブル

|Column|Type|Options|
|------|----|-------|
|group_id|integer|null:false, foreign_key: true|
|user_id|integer|null:false, foreign_key: true|
|date|integer|null:false|

###Association
- has_one :user
- has_many :group


