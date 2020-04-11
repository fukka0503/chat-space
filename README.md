# README

## users table

|Column|Type|Options|
|------|----|-------|
|nickname | stirng |:name, null: false|
|email| string |:email, unique: true|
|password| string|:user, foreign_key: true|

## Association
- has_many :groups,through::group_users
- has_many :messages
- has_many :group_users


## group table

|Column|Type|Options|
|------|----|-------|
|name| stirng |null: false|

## Association
- has_many :users,through::group_users
- has_many :group_users
- has_many :messages



## message table

|Column|Type|Options|
|------|----|-------|
|text|text||
|image|text||
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
## Association
- belongs_to :user
- belongs_to :group

## 
groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user