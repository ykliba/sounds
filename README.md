##DB

###usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|email|string|null: false|
|password|string|null: false|
### Association
- has_many :reviews
- has_many :comments
- has_many :likes

###reviewsテーブル
|column|Type|Options|
|------|----|-------|
|title|string|null: false|
|artist|string|null: false|
|desc|text|null: false|
|image|text|  |
|link|text|  |
### Association
- has_many :comments
- has_many :likes
- belongs_to :user

###commentsテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|  |
|review_id|integer|  |
|message|text|  |
### Association
- belongs_to :user
- belongs_to :review

###likesテーブル
|Column|Type|Options|
|------|----|-------|
|reply_id|integer|  |
|user_id|integer|  |
### Association
- belongs_to :user
- belongs_to :review




