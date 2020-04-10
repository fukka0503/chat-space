# README

## users table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|nickname | stirng |:name, null: false
|email| string |:email, unique: true
|password| string|:user, foreign_key: true

## Association
- belongs_to :user
- has_many groups



## group table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
## Association
- has_many users
- has_many groups



## message table

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
## Association
- belongs_to :user
- has_many groups

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|

### Association
- belongs_to :group
- belongs_to :user