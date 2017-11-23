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
