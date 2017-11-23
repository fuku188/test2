## messagesテーブル

|Column|Type|Options|
|------|----|-------|
|body|text|null:false|
|image|string|null:false|
|group_id|integer|null:false, foreign_key: ture|
|user_id|integer|null:false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user

## usersテーブル

|Column|Type|Option|
|------|----|------|
|name|stirng|null:false|
|group_id|null:false, foreign_key:  true|

### Association
- has_one :group
- has_many :messages
- has_and_belongs_to_many :group


## groupテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null:false, foreign_key: true|
|date|integer|null:false|

### Association
- has_and_belongs_to_many :user
- has_many_messages

