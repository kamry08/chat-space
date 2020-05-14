
## usersテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
|mail|text|null: false|
|password|string|null: false|

## Associationテーブル
- has many :tweets
- has many :groups through groups_users
- has many :groups_users

## tweetsテーブル
|Column|Type|Options|
|------|----|-------|
|text|text|
|image|text|
|user_id|reference|null: false, foreign_key: true|
|group_id|reference|null: false, foreign_key: true|

## Associationテーブル
- belongs_to :user
- belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|

## Associationテーブル
- has many :users through groups_users
- has many :groups_users
- has many :tweets 

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|reference|null: false, foreign_key: true|
|group_id|reference|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user


